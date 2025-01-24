<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1-windowsservercore-ltsc2025`](#julia1-windowsservercore-ltsc2025)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-alpine`](#julia110-alpine)
-	[`julia:1.10-alpine3.20`](#julia110-alpine320)
-	[`julia:1.10-alpine3.21`](#julia110-alpine321)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-bullseye`](#julia110-bullseye)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-1809`](#julia110-windowsservercore-1809)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10-windowsservercore-ltsc2025`](#julia110-windowsservercore-ltsc2025)
-	[`julia:1.10.8`](#julia1108)
-	[`julia:1.10.8-alpine`](#julia1108-alpine)
-	[`julia:1.10.8-alpine3.20`](#julia1108-alpine320)
-	[`julia:1.10.8-alpine3.21`](#julia1108-alpine321)
-	[`julia:1.10.8-bookworm`](#julia1108-bookworm)
-	[`julia:1.10.8-bullseye`](#julia1108-bullseye)
-	[`julia:1.10.8-windowsservercore`](#julia1108-windowsservercore)
-	[`julia:1.10.8-windowsservercore-1809`](#julia1108-windowsservercore-1809)
-	[`julia:1.10.8-windowsservercore-ltsc2022`](#julia1108-windowsservercore-ltsc2022)
-	[`julia:1.10.8-windowsservercore-ltsc2025`](#julia1108-windowsservercore-ltsc2025)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-bullseye`](#julia111-bullseye)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-1809`](#julia111-windowsservercore-1809)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11-windowsservercore-ltsc2025`](#julia111-windowsservercore-ltsc2025)
-	[`julia:1.11.3`](#julia1113)
-	[`julia:1.11.3-bookworm`](#julia1113-bookworm)
-	[`julia:1.11.3-bullseye`](#julia1113-bullseye)
-	[`julia:1.11.3-windowsservercore`](#julia1113-windowsservercore)
-	[`julia:1.11.3-windowsservercore-1809`](#julia1113-windowsservercore-1809)
-	[`julia:1.11.3-windowsservercore-ltsc2022`](#julia1113-windowsservercore-ltsc2022)
-	[`julia:1.11.3-windowsservercore-ltsc2025`](#julia1113-windowsservercore-ltsc2025)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)
-	[`julia:windowsservercore-ltsc2025`](#juliawindowsservercore-ltsc2025)

## `julia:1`

```console
$ docker pull julia@sha256:19123e4338d8ad2fc3d719eafb9611b8f8dcfa02861089c038d37aab26388371
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:dfd9e0c4c633f254a308c1916578ce6710fe9d83369d49c5041ac31c92514403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302230971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15da0b07dfa5794bba53fc0b720a07076c26b6b3137fa1c4a0901b1b7b6b203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11860dad45048203d204a51474f3925e9683760498bf50f92df3cca666dd458b`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 5.7 MB (5713140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac9baef82d2d108ad6edf1a74295af617edc712cd5c8ab23e8ff2374ac77ed`  
		Last Modified: Wed, 22 Jan 2025 20:32:10 GMT  
		Size: 268.3 MB (268305043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472e8b8bc35a5891e935d49aa58655018aedd4e7fd1385a16d6a309bd25da9b9`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:b0e563c0d521de7b2a427bbf46438b2f1f6c5e10674a3b5c5917a25155aea078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824872dea940f11b8ff617822decf8d0c116bb8f1405dcd8500490f1634a60c0`

```dockerfile
```

-	Layers:
	-	`sha256:70a9556a7e1795501be1e9027bb1e59d86d0319c09f9f17dab00e4c12edae264`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7af1b6e5c9662831f11bd0d9b9f3c7a7778283a77fa77047476a8d7b3211b6`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b6b57a30ff9c52f062fe0d438029cdd84acf063ac25abea70927491f48647e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ff4826fb6b79ca9e2f60429606e6750bf387340f9ddd220c8c8e0d616ab8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2508a326b870e86f138cfd69d3040b99b4c69da739a433a76f0d42e2d7295`  
		Last Modified: Wed, 22 Jan 2025 20:47:55 GMT  
		Size: 283.9 MB (283934039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811908adbde892f0dc087de51d194a44302234dd8db1e1edd0a23b28b6590`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:be7b3b6d64bd30778c516836cba5d3319f5b6a93f0356a89b904b1f50606caf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edb88069991bac9ce6470a081597ddd1244fbb437808f645fb86d92527ebcd2`

```dockerfile
```

-	Layers:
	-	`sha256:4880a0936365197181a4c4fd61b3de79bd9c1a6fec18f7b100bd342204f2e9b6`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eac05a8fe45fb0942ac43f011c50367ca5c9238aff408712b8f3eb77b55591`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:814b7fec42d571633907dc2cef4faa25d6398d9b56d85ee4d1c46c48431d8db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252975156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366aa7705fa4ebea2a897877c696d91f3e63433b84350c783bd0c2924ffca7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4c578b793469a79623c080953da1703a24154efcd4d115d0bd6f6861e91ed`  
		Last Modified: Wed, 22 Jan 2025 20:31:56 GMT  
		Size: 5.9 MB (5872033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2d23153d25f71daec926fb2601f508915eb86ae59b035f26da7984e60b60d`  
		Last Modified: Wed, 22 Jan 2025 20:32:00 GMT  
		Size: 217.9 MB (217915156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a4c16e5d74edd13537edd7983b1cd6f51d8d1564968f8dfe1b43ef30f3ce4`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:3dc4e34abd257a0c7de8ba7913e600994574286aed92ea308628d25a465cda1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e503f41d3f52790f1be988dadefdee94f7efc64a36dfba30c9de3c005590d5d`

```dockerfile
```

-	Layers:
	-	`sha256:0990cc379cdc9c889f2638e77546ce33d5d756db6da2de1c7588beb6becf84e5`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410284fbd0a09ef4fde53132a1df54dad2e8931ad3a218f4fec9ad984ee2598b`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; ppc64le

```console
$ docker pull julia@sha256:3e27a466b4db0fcd6951fba88bbd792201e36f66a0f3c8ff29316cf33d536197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909eb8fce329f21bb6f910d0f97efce27330dcdd686d89f2e8828968fffa10d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88deb77bfd22b73b5868698e1252ff274e03e929f8078b18558dff903688ebb`  
		Last Modified: Wed, 22 Jan 2025 22:10:26 GMT  
		Size: 228.6 MB (228554518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420be3a0625df33882f4115a70e7cbab62892bcf6537408403cb373a1d89005b`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:bcd8d8618f705417c25783d30ea72b25e7de656f94697752316dbb67b2990c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6720277dd6a7fb7f038fd659f97c800a83c412651af7a82c34d22378666eb32`

```dockerfile
```

-	Layers:
	-	`sha256:cc01de99746f8e67a67aeda29c1fe24ba526e7041ce370c2a6c49d3a085e5f68`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e137bcd587be4a60bda3ad46a6d0562f3d1261afd55cb1bc77a4e82ea4a2dd6`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:0dec0ffb23a93fb5a4f415ea2967d2d95d9dcf714c91cfb9bd7f9fbf7b5d853d
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

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:dfd9e0c4c633f254a308c1916578ce6710fe9d83369d49c5041ac31c92514403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302230971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15da0b07dfa5794bba53fc0b720a07076c26b6b3137fa1c4a0901b1b7b6b203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11860dad45048203d204a51474f3925e9683760498bf50f92df3cca666dd458b`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 5.7 MB (5713140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac9baef82d2d108ad6edf1a74295af617edc712cd5c8ab23e8ff2374ac77ed`  
		Last Modified: Wed, 22 Jan 2025 20:32:10 GMT  
		Size: 268.3 MB (268305043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472e8b8bc35a5891e935d49aa58655018aedd4e7fd1385a16d6a309bd25da9b9`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b0e563c0d521de7b2a427bbf46438b2f1f6c5e10674a3b5c5917a25155aea078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824872dea940f11b8ff617822decf8d0c116bb8f1405dcd8500490f1634a60c0`

```dockerfile
```

-	Layers:
	-	`sha256:70a9556a7e1795501be1e9027bb1e59d86d0319c09f9f17dab00e4c12edae264`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7af1b6e5c9662831f11bd0d9b9f3c7a7778283a77fa77047476a8d7b3211b6`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b6b57a30ff9c52f062fe0d438029cdd84acf063ac25abea70927491f48647e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ff4826fb6b79ca9e2f60429606e6750bf387340f9ddd220c8c8e0d616ab8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2508a326b870e86f138cfd69d3040b99b4c69da739a433a76f0d42e2d7295`  
		Last Modified: Wed, 22 Jan 2025 20:47:55 GMT  
		Size: 283.9 MB (283934039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811908adbde892f0dc087de51d194a44302234dd8db1e1edd0a23b28b6590`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:be7b3b6d64bd30778c516836cba5d3319f5b6a93f0356a89b904b1f50606caf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edb88069991bac9ce6470a081597ddd1244fbb437808f645fb86d92527ebcd2`

```dockerfile
```

-	Layers:
	-	`sha256:4880a0936365197181a4c4fd61b3de79bd9c1a6fec18f7b100bd342204f2e9b6`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eac05a8fe45fb0942ac43f011c50367ca5c9238aff408712b8f3eb77b55591`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:814b7fec42d571633907dc2cef4faa25d6398d9b56d85ee4d1c46c48431d8db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252975156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366aa7705fa4ebea2a897877c696d91f3e63433b84350c783bd0c2924ffca7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4c578b793469a79623c080953da1703a24154efcd4d115d0bd6f6861e91ed`  
		Last Modified: Wed, 22 Jan 2025 20:31:56 GMT  
		Size: 5.9 MB (5872033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2d23153d25f71daec926fb2601f508915eb86ae59b035f26da7984e60b60d`  
		Last Modified: Wed, 22 Jan 2025 20:32:00 GMT  
		Size: 217.9 MB (217915156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a4c16e5d74edd13537edd7983b1cd6f51d8d1564968f8dfe1b43ef30f3ce4`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3dc4e34abd257a0c7de8ba7913e600994574286aed92ea308628d25a465cda1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e503f41d3f52790f1be988dadefdee94f7efc64a36dfba30c9de3c005590d5d`

```dockerfile
```

-	Layers:
	-	`sha256:0990cc379cdc9c889f2638e77546ce33d5d756db6da2de1c7588beb6becf84e5`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410284fbd0a09ef4fde53132a1df54dad2e8931ad3a218f4fec9ad984ee2598b`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:3e27a466b4db0fcd6951fba88bbd792201e36f66a0f3c8ff29316cf33d536197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909eb8fce329f21bb6f910d0f97efce27330dcdd686d89f2e8828968fffa10d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88deb77bfd22b73b5868698e1252ff274e03e929f8078b18558dff903688ebb`  
		Last Modified: Wed, 22 Jan 2025 22:10:26 GMT  
		Size: 228.6 MB (228554518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420be3a0625df33882f4115a70e7cbab62892bcf6537408403cb373a1d89005b`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bcd8d8618f705417c25783d30ea72b25e7de656f94697752316dbb67b2990c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6720277dd6a7fb7f038fd659f97c800a83c412651af7a82c34d22378666eb32`

```dockerfile
```

-	Layers:
	-	`sha256:cc01de99746f8e67a67aeda29c1fe24ba526e7041ce370c2a6c49d3a085e5f68`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e137bcd587be4a60bda3ad46a6d0562f3d1261afd55cb1bc77a4e82ea4a2dd6`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:e9ee3bb81f4ac27dfe4b0265461288134ceda8675734267eb1d8f94d32d4bf0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:781b30fe7f616a0f2e856db2c849abfe7046fc742d6bb0f57f60842a7fd742d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300780897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6ede12ef81315a7b438b0146b5f231f7f61cc2a2cec1cc2b5e3e7e8af53513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315057799844e342367e62797410ef3f354df191a3eddfff67174f8280aa2574`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706e1632f981a535ef3b384530c7a992532b9d1711a6419e5a6e3b56b61140a4`  
		Last Modified: Wed, 22 Jan 2025 20:32:27 GMT  
		Size: 268.3 MB (268305170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d8cd2b8533d98a0906bc9959647aa9b42f1fef5b5515d7ed6b5e96ac469e1`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:ce9df326374bc88c2fd965d6bbda05332eb976fffba0b87dc92a24ab921350ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047f824041ea2bfe680f42c783898976041b40f20b3336d15bc91bc494a92546`

```dockerfile
```

-	Layers:
	-	`sha256:2a206d07edd1ca3327674f132466b77256cc4e51cf25a4aa54d010eb8936afa6`  
		Last Modified: Wed, 22 Jan 2025 20:32:22 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e8a5c92f79371895b1676de8c14a76f0c4cb4f467d753fef88e007cbd34ff1`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d8be078c91e946b763ad4eb8bc64d41d7b5979cc56981d79d84f149060487e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314891613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3a0bb9b65de1d8a7581fff3f9887e2197036d68b8b800ef54d1bec7f5ac678`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1835e135f44f85a0bb5c2c3a94070c34d2c3edbcad74d7c221aa15bf1e174c8`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.2 MB (2210265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e277e65273fc46fa6e750c0e3bd08d3df1e24543ded9eb1070dbea35ce672ca`  
		Last Modified: Wed, 22 Jan 2025 20:49:26 GMT  
		Size: 283.9 MB (283936065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32efa8f69db69aea668db9ffa5e5138a4ef44a0ef4c6b1fa8fcb9fe86df22f55`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0522c45ced18a4a568f2884b10827a2051aef7c30d731dcb56caac1f1688d556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5791640cd2d006fdf4ecd31e70e5d4029ead71ce99ee238936074dc4e33eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ecdf93b8b928b31de96a6216f658d90220c50a9b77c3978dcf5113e514e223fb`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fda29c8f157db9624e9f5926ec8093b4066888a17d9570d7fe89816e1615c69`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:ec5e4205e52a62b49a78332b1a22592adaeeffe3830b0db7297378441fb3832c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251422332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af1eb265cfada65b5b4799579e755c84c8aa07242febde2ed4351a89e9df0f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b412cbf4071893ed1b94e858a9b759748e886686516f5d75aa03a1fbe5234f79`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 2.3 MB (2328090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cbb1693b6baa5b8a9bcc1be3b299e68e6c96c60b1edb2e12b8ec9e4383c092`  
		Last Modified: Wed, 22 Jan 2025 20:32:19 GMT  
		Size: 217.9 MB (217914846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3a3068160a28ce84408f0e1baa3b0d54560eadfeb855b9bcc1acbfd5da3c83`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:961fd255152fb9f195fbd909625d951117b9bb1b326b18dc21a3073dde1ecb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c6127c8c489d9790921190cb0f102547b84cc7c0f293ae95774cb42517f1c1`

```dockerfile
```

-	Layers:
	-	`sha256:a6de4ca2fba28dbc08fafad965f9bd085ae56f92159b60c850be65be3308fd43`  
		Last Modified: Wed, 22 Jan 2025 20:32:14 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915d105ffd540dab571a864c9b9de7d5db098a2096b6b9e3056809e8a0c917e9`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:05f492a8b62ea4e989705f5f2a6d24f3b3f1a4025f4299a7396302a19717c7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:d15ed40b5dd0f815972c8d1ce60a9d900f3f279aaa3ecf63fa9b56587f4f567a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1eb9a74451306dd33a9bc7fa579743f12f360f011137705318dc2581ef72d41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:67fda6c48eda4e0f77740f4573ef5dc220572ab87ca07290a699cad567522bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:6600d54e5a855dcf7f0f1ed04f348f775ad930f7168ca9f7538d3467e77431ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:28436c66a05871bbf899572c1c3a82ee1747779ff354b6ac59d72b1fc278e0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209686117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa47198934943bc7076f73b3265130466dda364f32f892c9c58a82a5f08b961`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b6ab97b16e056f5a321255a4e1f5179de80c759153d351136e2585bea6d2c`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 5.7 MB (5713128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea11abd24a9b767f6bb8b3821425d4bd9a969064c8bf7574174fc241ba5b4d`  
		Last Modified: Thu, 23 Jan 2025 22:26:53 GMT  
		Size: 175.8 MB (175760202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec122af0696b5535f9b28763ced10330c1de7baccec9325d1d45c4ac535db22`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:cd1ffd6f2e0bbdbc335f5d2b13c5b0ac7fb6e7514ff1a3a7d9f2c1b0db2735e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7781bea1cd52621d384c4b58b4b42c6db82f57ca3ed8cb78390d6b24f14772e8`

```dockerfile
```

-	Layers:
	-	`sha256:464bab9db9677b4e33ee2f1db8fe35d15cabf42c97c3f1f1958ee21ed0cfbfb2`  
		Last Modified: Thu, 23 Jan 2025 22:26:49 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2438f3ab538da93b3c1bf721e9a21405475214e73b4bf06fbefde48dd2485e`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4574ba2dec556d708ebcab68d52a7432c9a935519ee2fba723d12aa52e113358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210719667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778d696b38e9044182a9d078a7b952fc5b39527a81cc3c0cf9041a44b71071e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaebaaec883bb0d408d44dfe9fe655264f98c965523af9ccfd4d2f284e65f`  
		Last Modified: Thu, 23 Jan 2025 22:27:45 GMT  
		Size: 177.1 MB (177140224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce03a8824f25406bf2f0b5ba1c2668e89ec8bd0b9b2106d02c5f41d0df72861`  
		Last Modified: Thu, 23 Jan 2025 22:27:40 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:c6af2185e838da80a2fcf66e31324aba6fe5122d6b24c730ba528fc4ddb75f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df19670a503eab60afd8a7a90ba858cc8df3f5f2ce44e1e193f95c336b1df8`

```dockerfile
```

-	Layers:
	-	`sha256:d9ba2ae57517165460478eac1ef2cd1c145d9dd311ed3d50a45e4e5cbb4966a0`  
		Last Modified: Thu, 23 Jan 2025 22:27:41 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc77c84d352b96a9b9ff7f668c363bcf062daf2ba313764d92d2933deace079`  
		Last Modified: Thu, 23 Jan 2025 22:27:40 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:9866141646e334620aa4c662cf04dfa079d3c30e95aa59e0e844afaf488589b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192861935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ef1263b2ea234148ecdbc0433e64cf3ec70b3f225dbf90611d28e20a27e2bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fd5f5a561c987a285556ad1d86dc4c5b3458100245cc0378f2789e4bb1e7b9`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 5.9 MB (5872009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86384ba08a0862dfffd851bc268a6f2f06be1a3256b1bae6294a504dda6438f`  
		Last Modified: Thu, 23 Jan 2025 22:26:45 GMT  
		Size: 157.8 MB (157801960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f1151e37cac805de1f9e76ace0f3bdb60af8369433d55a67553dded26e9035`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:89c83f8f256b0eb75e3cd6e2378ac829bb3867265aaefd319954ae8499b8378a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5425f3427d1f1acce0d548921041dccf366d381ad71497388eb3ebf3c9ffe6e0`

```dockerfile
```

-	Layers:
	-	`sha256:8bd18c6faa7b646ca966a66e0b3e038c673b11e44c05ad244767a58a0ee1a905`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68791ad3e30ba41066ee5dddbf5f9f9ed14159cc8a00f17804681cb4aeac9388`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:f56bc6c2be5398da1b9c37e6ac8b39ce599c57d8f07436ff3da3555d11745524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193451800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e786a229f1503d1ee665ff3b12b671e86e09b8da17e3802dc708ee7d441423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e4efbced4fc8c5378f9eeaef5325b9a3772daa1de8c88c78c5ca10ef3431ab`  
		Last Modified: Thu, 23 Jan 2025 22:27:18 GMT  
		Size: 155.2 MB (155157283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da33c6c1c49ce20ae77586e7cae169835285288d207aed8f3a5f8d18eede24df`  
		Last Modified: Thu, 23 Jan 2025 22:27:13 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:82ccdd03e72eb992b905a7285a4b838a0ed42a2a71c0b05e28f487ea92841446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5809c3bd5bf871dcef5c146c01d108d291bcc5f80dff7dc2d53f042be906f4`

```dockerfile
```

-	Layers:
	-	`sha256:90e7a5e8a11ebeed1ca226c90904bb5b31d270801f12cdab9c91b9db4562a2e4`  
		Last Modified: Thu, 23 Jan 2025 22:27:14 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ec2f7d3b159c8172c8c04f55c7269da04fb33d847e542c1f0bacdc50e7ea8a`  
		Last Modified: Thu, 23 Jan 2025 22:27:13 GMT  
		Size: 17.3 KB (17258 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:7d2b9a6c3fa28dcd28d65427c88e7d379503acb88b508d7b983cf0d55046ca1d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2688969059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b221656547fd936d19281af7c828c5199cd0f73e63f4c1f784165b2246e652d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 22:29:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:29:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:30:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c5302aa7bbe98d12864a76d1af7a5184aa438b7697b7b5b1b9471a4b10d5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758924ec3eb9afedb56332ca25760819f815634bc287ace59d70a9511debd8ab`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cf9b43ec1e778c763a162f521798fa1e0bf745c69242b33f7e3cd24d6278e7`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592cd9a88a0b5ca750c8ecc16f4ff2364fb758f7b22ac2ed22ec72fa12e7fb62`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86633cc37ee5bd328743417b01a85b3d76fce28439d5b9ba357b537988ff95`  
		Last Modified: Thu, 23 Jan 2025 22:31:03 GMT  
		Size: 188.7 MB (188684999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0146c4ebe9975a16078c961377a65aa938570da795ab8dc81e3e757b42cda5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:1d16c3f0485cd1f94ee5274275b3f39595b2795ef808f9503dc663c7107b9f27
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451010480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c70f55c2ac0775592f1bb6728b284abdc4dece11612e910adb896fec3ddb82a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 22:26:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:21 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:23 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:28:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4c90ee13d429da08cd963a7e0eafca2c47c68adf32c51710368a76b5fe6ebe`  
		Last Modified: Thu, 23 Jan 2025 22:28:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb0cb206b0751f05379acabc31ec8499eaf5ada517967bfb8f8f6f53d94f1f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e7fdfad8844eba72c2f010575b51d1853acfa6f5d4178eda779e5e3248f665`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda37e286727615d00d3bea8d09e794f44239a009d5cdcb233c8770ccce5617f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d08118e95deb42f13d3aad50343087c81fd82c5fd1249711238860e5b5dbe6`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 188.6 MB (188618802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe6ee26314619eb9565ac44c5ed9096091ca9ad82699df195fe0ed570c0075`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:4eccb96fa80116fb7bfdb2016202d031acab310aff1fbe1a31ed3458c7925d6e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310847455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf17d5f9ce3a5ba7a1710b20b3702fe11610173c4f498a9a2cc84b7b3038c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 22:25:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:01 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:27:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559775808be333a0da9ac865f922637f6d96964d8a49b01dc7a539e30da53541`  
		Last Modified: Thu, 23 Jan 2025 22:27:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbb06df7a13245a54deeb8da4ca94d4fbcbb1e8d833632999811496c4a6646`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e856345c30f26ba775fe0c97a987d19316ab76023e6a52c1b908e8dacffb13`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c729ee0ff0aea816ca3ae7688827dfe9e53ccaacc6d4bc77e871ba9f67fb172c`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245fa98868b43a67c87aaefa5b9cf1018d8e5ad2b556a7b372ea3e34a71ff8be`  
		Last Modified: Thu, 23 Jan 2025 22:27:49 GMT  
		Size: 188.6 MB (188628804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dd8b372a3fd21947c8ca5292b8b02e40d9c0384441598589ee0967262a8878`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:369b351b7d190d052c91017897962a57a4cd3d3e194e18d2785bdb4ec1a1898a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:03b393416ff577fbbb8756ac775efd9641a78bbd59153ea59b290570da58cb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182653366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8867740affab2dd3e90d4e2b10b6f945d4ede1847730de657c92490273154`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.8-musl-x86_64.tar.gz'; 			sha256='db86a8e62084f5131acec57f2b83a774a2864bb74b0cd4aa890d91b355521f66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d0bfaec32c6a95944cc0d8d65114cdfe73adcb2b9be18ccff77237fdb45cdf`  
		Last Modified: Thu, 23 Jan 2025 22:26:51 GMT  
		Size: 179.0 MB (179011286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ccec73be86e109eb77dcb294160650f5cff80405d9701f3641a1acd1736b2c`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:4c5598eb38ca9d08f29ef02d975c70a5ef18ea89df0f78f6c33645f6a1ce831b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfbdfb9641648c97fde168beb4709606e9eb8f6f4a2e07985aad6361b59babf`

```dockerfile
```

-	Layers:
	-	`sha256:0c63e29d0d4a59b5076d597b3b168dbca25a05633afa1e9470e34ab8795db523`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 79.9 KB (79881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb09901da9dd4747aef83a8e71bdb3c371b88e82a26e418525f446d9178c20ce`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.20`

```console
$ docker pull julia@sha256:9ec4f5c7de80faff56955279e3d5262ee5eda3110720f1b96b53c0e156454b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:ab544964e48dca5777b4acdb0c47f58904b241746b3a398b875d28ff030eabb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182636897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e634b8acbb090e3061daee729efa57f125da061b73c6c94f7ec2051d1ad51c1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.8-musl-x86_64.tar.gz'; 			sha256='db86a8e62084f5131acec57f2b83a774a2864bb74b0cd4aa890d91b355521f66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb48fa4c3deae8211e602594ff713ed33d71b5e57e21b466f8d7ea0b4a4fa89`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 179.0 MB (179010268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a869c5410324e61154fe821757b53c4a0939cccdb58220151ae6a79d3664bb47`  
		Last Modified: Thu, 23 Jan 2025 22:26:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:a129de9c28f7fd4b53f2c485437e267b44442530e59b91360a331451e39d5e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b507495049b3cad39218f57615f92d998c50f4271ab13b55b847dc1a579204`

```dockerfile
```

-	Layers:
	-	`sha256:1bf28ba86bb2b4a0ebac8fcfbaea8375d6b5557b4e348297c62c4825399ed014`  
		Last Modified: Thu, 23 Jan 2025 22:26:37 GMT  
		Size: 73.5 KB (73545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48d243381e24a468f6e3ed864ad9e308ba4421bd32e669e996691cbaf70a1cb`  
		Last Modified: Thu, 23 Jan 2025 22:26:37 GMT  
		Size: 12.0 KB (11964 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.21`

```console
$ docker pull julia@sha256:369b351b7d190d052c91017897962a57a4cd3d3e194e18d2785bdb4ec1a1898a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:03b393416ff577fbbb8756ac775efd9641a78bbd59153ea59b290570da58cb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182653366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8867740affab2dd3e90d4e2b10b6f945d4ede1847730de657c92490273154`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.8-musl-x86_64.tar.gz'; 			sha256='db86a8e62084f5131acec57f2b83a774a2864bb74b0cd4aa890d91b355521f66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d0bfaec32c6a95944cc0d8d65114cdfe73adcb2b9be18ccff77237fdb45cdf`  
		Last Modified: Thu, 23 Jan 2025 22:26:51 GMT  
		Size: 179.0 MB (179011286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ccec73be86e109eb77dcb294160650f5cff80405d9701f3641a1acd1736b2c`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:4c5598eb38ca9d08f29ef02d975c70a5ef18ea89df0f78f6c33645f6a1ce831b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfbdfb9641648c97fde168beb4709606e9eb8f6f4a2e07985aad6361b59babf`

```dockerfile
```

-	Layers:
	-	`sha256:0c63e29d0d4a59b5076d597b3b168dbca25a05633afa1e9470e34ab8795db523`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 79.9 KB (79881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb09901da9dd4747aef83a8e71bdb3c371b88e82a26e418525f446d9178c20ce`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:f2f50113e343141448ba3f04f21eb08f61f1e26e32f2b93ab32a86af3bead43c
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
$ docker pull julia@sha256:28436c66a05871bbf899572c1c3a82ee1747779ff354b6ac59d72b1fc278e0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209686117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa47198934943bc7076f73b3265130466dda364f32f892c9c58a82a5f08b961`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b6ab97b16e056f5a321255a4e1f5179de80c759153d351136e2585bea6d2c`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 5.7 MB (5713128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea11abd24a9b767f6bb8b3821425d4bd9a969064c8bf7574174fc241ba5b4d`  
		Last Modified: Thu, 23 Jan 2025 22:26:53 GMT  
		Size: 175.8 MB (175760202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec122af0696b5535f9b28763ced10330c1de7baccec9325d1d45c4ac535db22`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:cd1ffd6f2e0bbdbc335f5d2b13c5b0ac7fb6e7514ff1a3a7d9f2c1b0db2735e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7781bea1cd52621d384c4b58b4b42c6db82f57ca3ed8cb78390d6b24f14772e8`

```dockerfile
```

-	Layers:
	-	`sha256:464bab9db9677b4e33ee2f1db8fe35d15cabf42c97c3f1f1958ee21ed0cfbfb2`  
		Last Modified: Thu, 23 Jan 2025 22:26:49 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2438f3ab538da93b3c1bf721e9a21405475214e73b4bf06fbefde48dd2485e`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4574ba2dec556d708ebcab68d52a7432c9a935519ee2fba723d12aa52e113358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210719667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778d696b38e9044182a9d078a7b952fc5b39527a81cc3c0cf9041a44b71071e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaebaaec883bb0d408d44dfe9fe655264f98c965523af9ccfd4d2f284e65f`  
		Last Modified: Thu, 23 Jan 2025 22:27:45 GMT  
		Size: 177.1 MB (177140224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce03a8824f25406bf2f0b5ba1c2668e89ec8bd0b9b2106d02c5f41d0df72861`  
		Last Modified: Thu, 23 Jan 2025 22:27:40 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c6af2185e838da80a2fcf66e31324aba6fe5122d6b24c730ba528fc4ddb75f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df19670a503eab60afd8a7a90ba858cc8df3f5f2ce44e1e193f95c336b1df8`

```dockerfile
```

-	Layers:
	-	`sha256:d9ba2ae57517165460478eac1ef2cd1c145d9dd311ed3d50a45e4e5cbb4966a0`  
		Last Modified: Thu, 23 Jan 2025 22:27:41 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc77c84d352b96a9b9ff7f668c363bcf062daf2ba313764d92d2933deace079`  
		Last Modified: Thu, 23 Jan 2025 22:27:40 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:9866141646e334620aa4c662cf04dfa079d3c30e95aa59e0e844afaf488589b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192861935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ef1263b2ea234148ecdbc0433e64cf3ec70b3f225dbf90611d28e20a27e2bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fd5f5a561c987a285556ad1d86dc4c5b3458100245cc0378f2789e4bb1e7b9`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 5.9 MB (5872009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86384ba08a0862dfffd851bc268a6f2f06be1a3256b1bae6294a504dda6438f`  
		Last Modified: Thu, 23 Jan 2025 22:26:45 GMT  
		Size: 157.8 MB (157801960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f1151e37cac805de1f9e76ace0f3bdb60af8369433d55a67553dded26e9035`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:89c83f8f256b0eb75e3cd6e2378ac829bb3867265aaefd319954ae8499b8378a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5425f3427d1f1acce0d548921041dccf366d381ad71497388eb3ebf3c9ffe6e0`

```dockerfile
```

-	Layers:
	-	`sha256:8bd18c6faa7b646ca966a66e0b3e038c673b11e44c05ad244767a58a0ee1a905`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68791ad3e30ba41066ee5dddbf5f9f9ed14159cc8a00f17804681cb4aeac9388`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:f56bc6c2be5398da1b9c37e6ac8b39ce599c57d8f07436ff3da3555d11745524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193451800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e786a229f1503d1ee665ff3b12b671e86e09b8da17e3802dc708ee7d441423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e4efbced4fc8c5378f9eeaef5325b9a3772daa1de8c88c78c5ca10ef3431ab`  
		Last Modified: Thu, 23 Jan 2025 22:27:18 GMT  
		Size: 155.2 MB (155157283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da33c6c1c49ce20ae77586e7cae169835285288d207aed8f3a5f8d18eede24df`  
		Last Modified: Thu, 23 Jan 2025 22:27:13 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:82ccdd03e72eb992b905a7285a4b838a0ed42a2a71c0b05e28f487ea92841446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5809c3bd5bf871dcef5c146c01d108d291bcc5f80dff7dc2d53f042be906f4`

```dockerfile
```

-	Layers:
	-	`sha256:90e7a5e8a11ebeed1ca226c90904bb5b31d270801f12cdab9c91b9db4562a2e4`  
		Last Modified: Thu, 23 Jan 2025 22:27:14 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ec2f7d3b159c8172c8c04f55c7269da04fb33d847e542c1f0bacdc50e7ea8a`  
		Last Modified: Thu, 23 Jan 2025 22:27:13 GMT  
		Size: 17.3 KB (17258 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:06222907b683ec38998e7c3eda5d9560b74ee0211cfb7f8e9280d6f027aec377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:45d401ac9f80924d6c9e6b066c2ad9e646c741591dc4cb0887d212238e713cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208236155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbb36a380b348eefda5d2a9197a4973b6ee806b5a408f2d3b9fad25f051f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f64a555a7910d5b7d05b24a815082fd0c77ca699f23d1ce18b021b48f5471db`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa2b6a7e5f4105c5170192c5351d71759718eec814f6d17ec2cdd170fe751f`  
		Last Modified: Thu, 23 Jan 2025 22:26:42 GMT  
		Size: 175.8 MB (175760431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937821286df5cb49e4d136dc1cd7383e6fd933e369a26944a7708fc41539791`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:3e04a6588ee7cf187ac05cd4cd73c62100c733de17f07d467910d763f2b0b590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428859650e27e4faf81eebac17a35f37f3c26f774df81d247a73c43dea3a1633`

```dockerfile
```

-	Layers:
	-	`sha256:668f9c8a767bab0a90b9cccafbca643c0e37d0641c49c9484ba50fd478fa5cd1`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0928cba69fe357d7bff75b3ccd226126f3f38fe5a68094f41ded015feed4cc1`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4410a60b7c45f45e2ed5bde215d431925f0b28d251307c1ae9a2d4af6b7c3f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208096103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b0ba3311fe7a70b3388bc79c7f4722d0812a0e2e8c88ef6520f5c711b41f4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1835e135f44f85a0bb5c2c3a94070c34d2c3edbcad74d7c221aa15bf1e174c8`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.2 MB (2210265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2783cf4efe73257fb9b81dd152a1c62ac4d47c3589b654fbc431250acad0b72c`  
		Last Modified: Thu, 23 Jan 2025 22:28:51 GMT  
		Size: 177.1 MB (177140553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af3a9ed1fdf83eb772353c63e429cb867e5697004b1002e34ce9e92404205ca`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0c3727b56ef2f1068dd2af69dcf1ccf4a1c4f79f3309004a1a2a18d4bcc3a0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93b9a77053fac0d17ee1ef1f6774a639189ddb0802ea9254201899c675096de`

```dockerfile
```

-	Layers:
	-	`sha256:25cced3e18cf4a02da250ff3334c75eb86bf647cce27e3d25cfffbf1c5d46227`  
		Last Modified: Thu, 23 Jan 2025 22:28:47 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3344f742d41e5c4458c940f2a50b81df95df5d1ff11cacded230cc912bee0d47`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:8ab785bd9ad0faeb613e0667080e85a76800f939b5adb3f734e698ea3b841526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191309340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83a05bdebe2da16c7aa1653b5608fb839d2b582d32ef96a0b298f1280485500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9f16c63408f231fb65c48018657b31b5c5eafdf798975d354ffcdedd4668ec`  
		Last Modified: Thu, 23 Jan 2025 22:26:44 GMT  
		Size: 2.3 MB (2328090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967e5db2cdcc01a8012b937856fd4742a503272eda6f984263af5537d878c137`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 157.8 MB (157801851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e357a27391f1706f185a2f5e3a43b40194625920794bb9f118d16cc7f54082a`  
		Last Modified: Thu, 23 Jan 2025 22:26:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:7358c48135bf7642a604cb265bea41fbcd7af230def4358af3ee87cbf56fc5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0d4d432c5362ca6a4ba2d2dd3e9a629eeff325ca40c4fbb4a6db6005a2f2bc`

```dockerfile
```

-	Layers:
	-	`sha256:98e5246574e714566cf3d165d7b5d83a24164d0f1d2240e8818b48571b13e487`  
		Last Modified: Thu, 23 Jan 2025 22:26:44 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4de4126886745c4183443d663939f1a68e1d59b694d471420e16f4339d46c95`  
		Last Modified: Thu, 23 Jan 2025 22:26:44 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:0d94e6602a7f27123870b6e9947da76a92c533743cf8f3b65c0e2793daac75c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:7d2b9a6c3fa28dcd28d65427c88e7d379503acb88b508d7b983cf0d55046ca1d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2688969059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b221656547fd936d19281af7c828c5199cd0f73e63f4c1f784165b2246e652d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 22:29:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:29:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:30:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c5302aa7bbe98d12864a76d1af7a5184aa438b7697b7b5b1b9471a4b10d5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758924ec3eb9afedb56332ca25760819f815634bc287ace59d70a9511debd8ab`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cf9b43ec1e778c763a162f521798fa1e0bf745c69242b33f7e3cd24d6278e7`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592cd9a88a0b5ca750c8ecc16f4ff2364fb758f7b22ac2ed22ec72fa12e7fb62`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86633cc37ee5bd328743417b01a85b3d76fce28439d5b9ba357b537988ff95`  
		Last Modified: Thu, 23 Jan 2025 22:31:03 GMT  
		Size: 188.7 MB (188684999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0146c4ebe9975a16078c961377a65aa938570da795ab8dc81e3e757b42cda5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:1d16c3f0485cd1f94ee5274275b3f39595b2795ef808f9503dc663c7107b9f27
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451010480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c70f55c2ac0775592f1bb6728b284abdc4dece11612e910adb896fec3ddb82a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 22:26:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:21 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:23 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:28:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4c90ee13d429da08cd963a7e0eafca2c47c68adf32c51710368a76b5fe6ebe`  
		Last Modified: Thu, 23 Jan 2025 22:28:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb0cb206b0751f05379acabc31ec8499eaf5ada517967bfb8f8f6f53d94f1f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e7fdfad8844eba72c2f010575b51d1853acfa6f5d4178eda779e5e3248f665`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda37e286727615d00d3bea8d09e794f44239a009d5cdcb233c8770ccce5617f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d08118e95deb42f13d3aad50343087c81fd82c5fd1249711238860e5b5dbe6`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 188.6 MB (188618802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe6ee26314619eb9565ac44c5ed9096091ca9ad82699df195fe0ed570c0075`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:4eccb96fa80116fb7bfdb2016202d031acab310aff1fbe1a31ed3458c7925d6e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310847455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf17d5f9ce3a5ba7a1710b20b3702fe11610173c4f498a9a2cc84b7b3038c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 22:25:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:01 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:27:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559775808be333a0da9ac865f922637f6d96964d8a49b01dc7a539e30da53541`  
		Last Modified: Thu, 23 Jan 2025 22:27:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbb06df7a13245a54deeb8da4ca94d4fbcbb1e8d833632999811496c4a6646`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e856345c30f26ba775fe0c97a987d19316ab76023e6a52c1b908e8dacffb13`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c729ee0ff0aea816ca3ae7688827dfe9e53ccaacc6d4bc77e871ba9f67fb172c`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245fa98868b43a67c87aaefa5b9cf1018d8e5ad2b556a7b372ea3e34a71ff8be`  
		Last Modified: Thu, 23 Jan 2025 22:27:49 GMT  
		Size: 188.6 MB (188628804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dd8b372a3fd21947c8ca5292b8b02e40d9c0384441598589ee0967262a8878`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:2acf0e798ebcbe2f2c6c2cb19e94537035accf6202e32c51ac6e24e6d334b6b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:4eccb96fa80116fb7bfdb2016202d031acab310aff1fbe1a31ed3458c7925d6e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310847455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf17d5f9ce3a5ba7a1710b20b3702fe11610173c4f498a9a2cc84b7b3038c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 22:25:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:01 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:27:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559775808be333a0da9ac865f922637f6d96964d8a49b01dc7a539e30da53541`  
		Last Modified: Thu, 23 Jan 2025 22:27:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbb06df7a13245a54deeb8da4ca94d4fbcbb1e8d833632999811496c4a6646`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e856345c30f26ba775fe0c97a987d19316ab76023e6a52c1b908e8dacffb13`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c729ee0ff0aea816ca3ae7688827dfe9e53ccaacc6d4bc77e871ba9f67fb172c`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245fa98868b43a67c87aaefa5b9cf1018d8e5ad2b556a7b372ea3e34a71ff8be`  
		Last Modified: Thu, 23 Jan 2025 22:27:49 GMT  
		Size: 188.6 MB (188628804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dd8b372a3fd21947c8ca5292b8b02e40d9c0384441598589ee0967262a8878`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:9b46af7c5c71d4ed466b812d132b603c6a3d150a967a6650f561901733c5bc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:1d16c3f0485cd1f94ee5274275b3f39595b2795ef808f9503dc663c7107b9f27
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451010480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c70f55c2ac0775592f1bb6728b284abdc4dece11612e910adb896fec3ddb82a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 22:26:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:21 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:23 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:28:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4c90ee13d429da08cd963a7e0eafca2c47c68adf32c51710368a76b5fe6ebe`  
		Last Modified: Thu, 23 Jan 2025 22:28:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb0cb206b0751f05379acabc31ec8499eaf5ada517967bfb8f8f6f53d94f1f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e7fdfad8844eba72c2f010575b51d1853acfa6f5d4178eda779e5e3248f665`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda37e286727615d00d3bea8d09e794f44239a009d5cdcb233c8770ccce5617f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d08118e95deb42f13d3aad50343087c81fd82c5fd1249711238860e5b5dbe6`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 188.6 MB (188618802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe6ee26314619eb9565ac44c5ed9096091ca9ad82699df195fe0ed570c0075`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:06554fe34ef76ee712595115b73448f250812bac37df94dbd9ec6cb907e87650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:7d2b9a6c3fa28dcd28d65427c88e7d379503acb88b508d7b983cf0d55046ca1d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2688969059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b221656547fd936d19281af7c828c5199cd0f73e63f4c1f784165b2246e652d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 22:29:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:29:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:30:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c5302aa7bbe98d12864a76d1af7a5184aa438b7697b7b5b1b9471a4b10d5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758924ec3eb9afedb56332ca25760819f815634bc287ace59d70a9511debd8ab`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cf9b43ec1e778c763a162f521798fa1e0bf745c69242b33f7e3cd24d6278e7`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592cd9a88a0b5ca750c8ecc16f4ff2364fb758f7b22ac2ed22ec72fa12e7fb62`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86633cc37ee5bd328743417b01a85b3d76fce28439d5b9ba357b537988ff95`  
		Last Modified: Thu, 23 Jan 2025 22:31:03 GMT  
		Size: 188.7 MB (188684999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0146c4ebe9975a16078c961377a65aa938570da795ab8dc81e3e757b42cda5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.8`

```console
$ docker pull julia@sha256:6600d54e5a855dcf7f0f1ed04f348f775ad930f7168ca9f7538d3467e77431ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10.8` - linux; amd64

```console
$ docker pull julia@sha256:28436c66a05871bbf899572c1c3a82ee1747779ff354b6ac59d72b1fc278e0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209686117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa47198934943bc7076f73b3265130466dda364f32f892c9c58a82a5f08b961`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b6ab97b16e056f5a321255a4e1f5179de80c759153d351136e2585bea6d2c`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 5.7 MB (5713128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea11abd24a9b767f6bb8b3821425d4bd9a969064c8bf7574174fc241ba5b4d`  
		Last Modified: Thu, 23 Jan 2025 22:26:53 GMT  
		Size: 175.8 MB (175760202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec122af0696b5535f9b28763ced10330c1de7baccec9325d1d45c4ac535db22`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8` - unknown; unknown

```console
$ docker pull julia@sha256:cd1ffd6f2e0bbdbc335f5d2b13c5b0ac7fb6e7514ff1a3a7d9f2c1b0db2735e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7781bea1cd52621d384c4b58b4b42c6db82f57ca3ed8cb78390d6b24f14772e8`

```dockerfile
```

-	Layers:
	-	`sha256:464bab9db9677b4e33ee2f1db8fe35d15cabf42c97c3f1f1958ee21ed0cfbfb2`  
		Last Modified: Thu, 23 Jan 2025 22:26:49 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2438f3ab538da93b3c1bf721e9a21405475214e73b4bf06fbefde48dd2485e`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4574ba2dec556d708ebcab68d52a7432c9a935519ee2fba723d12aa52e113358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210719667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778d696b38e9044182a9d078a7b952fc5b39527a81cc3c0cf9041a44b71071e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaebaaec883bb0d408d44dfe9fe655264f98c965523af9ccfd4d2f284e65f`  
		Last Modified: Thu, 23 Jan 2025 22:27:45 GMT  
		Size: 177.1 MB (177140224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce03a8824f25406bf2f0b5ba1c2668e89ec8bd0b9b2106d02c5f41d0df72861`  
		Last Modified: Thu, 23 Jan 2025 22:27:40 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8` - unknown; unknown

```console
$ docker pull julia@sha256:c6af2185e838da80a2fcf66e31324aba6fe5122d6b24c730ba528fc4ddb75f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df19670a503eab60afd8a7a90ba858cc8df3f5f2ce44e1e193f95c336b1df8`

```dockerfile
```

-	Layers:
	-	`sha256:d9ba2ae57517165460478eac1ef2cd1c145d9dd311ed3d50a45e4e5cbb4966a0`  
		Last Modified: Thu, 23 Jan 2025 22:27:41 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc77c84d352b96a9b9ff7f668c363bcf062daf2ba313764d92d2933deace079`  
		Last Modified: Thu, 23 Jan 2025 22:27:40 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8` - linux; 386

```console
$ docker pull julia@sha256:9866141646e334620aa4c662cf04dfa079d3c30e95aa59e0e844afaf488589b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192861935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ef1263b2ea234148ecdbc0433e64cf3ec70b3f225dbf90611d28e20a27e2bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fd5f5a561c987a285556ad1d86dc4c5b3458100245cc0378f2789e4bb1e7b9`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 5.9 MB (5872009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86384ba08a0862dfffd851bc268a6f2f06be1a3256b1bae6294a504dda6438f`  
		Last Modified: Thu, 23 Jan 2025 22:26:45 GMT  
		Size: 157.8 MB (157801960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f1151e37cac805de1f9e76ace0f3bdb60af8369433d55a67553dded26e9035`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8` - unknown; unknown

```console
$ docker pull julia@sha256:89c83f8f256b0eb75e3cd6e2378ac829bb3867265aaefd319954ae8499b8378a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5425f3427d1f1acce0d548921041dccf366d381ad71497388eb3ebf3c9ffe6e0`

```dockerfile
```

-	Layers:
	-	`sha256:8bd18c6faa7b646ca966a66e0b3e038c673b11e44c05ad244767a58a0ee1a905`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68791ad3e30ba41066ee5dddbf5f9f9ed14159cc8a00f17804681cb4aeac9388`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8` - linux; ppc64le

```console
$ docker pull julia@sha256:f56bc6c2be5398da1b9c37e6ac8b39ce599c57d8f07436ff3da3555d11745524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193451800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e786a229f1503d1ee665ff3b12b671e86e09b8da17e3802dc708ee7d441423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e4efbced4fc8c5378f9eeaef5325b9a3772daa1de8c88c78c5ca10ef3431ab`  
		Last Modified: Thu, 23 Jan 2025 22:27:18 GMT  
		Size: 155.2 MB (155157283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da33c6c1c49ce20ae77586e7cae169835285288d207aed8f3a5f8d18eede24df`  
		Last Modified: Thu, 23 Jan 2025 22:27:13 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8` - unknown; unknown

```console
$ docker pull julia@sha256:82ccdd03e72eb992b905a7285a4b838a0ed42a2a71c0b05e28f487ea92841446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5809c3bd5bf871dcef5c146c01d108d291bcc5f80dff7dc2d53f042be906f4`

```dockerfile
```

-	Layers:
	-	`sha256:90e7a5e8a11ebeed1ca226c90904bb5b31d270801f12cdab9c91b9db4562a2e4`  
		Last Modified: Thu, 23 Jan 2025 22:27:14 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ec2f7d3b159c8172c8c04f55c7269da04fb33d847e542c1f0bacdc50e7ea8a`  
		Last Modified: Thu, 23 Jan 2025 22:27:13 GMT  
		Size: 17.3 KB (17258 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:7d2b9a6c3fa28dcd28d65427c88e7d379503acb88b508d7b983cf0d55046ca1d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2688969059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b221656547fd936d19281af7c828c5199cd0f73e63f4c1f784165b2246e652d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 22:29:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:29:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:30:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c5302aa7bbe98d12864a76d1af7a5184aa438b7697b7b5b1b9471a4b10d5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758924ec3eb9afedb56332ca25760819f815634bc287ace59d70a9511debd8ab`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cf9b43ec1e778c763a162f521798fa1e0bf745c69242b33f7e3cd24d6278e7`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592cd9a88a0b5ca750c8ecc16f4ff2364fb758f7b22ac2ed22ec72fa12e7fb62`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86633cc37ee5bd328743417b01a85b3d76fce28439d5b9ba357b537988ff95`  
		Last Modified: Thu, 23 Jan 2025 22:31:03 GMT  
		Size: 188.7 MB (188684999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0146c4ebe9975a16078c961377a65aa938570da795ab8dc81e3e757b42cda5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.8` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:1d16c3f0485cd1f94ee5274275b3f39595b2795ef808f9503dc663c7107b9f27
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451010480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c70f55c2ac0775592f1bb6728b284abdc4dece11612e910adb896fec3ddb82a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 22:26:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:21 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:23 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:28:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4c90ee13d429da08cd963a7e0eafca2c47c68adf32c51710368a76b5fe6ebe`  
		Last Modified: Thu, 23 Jan 2025 22:28:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb0cb206b0751f05379acabc31ec8499eaf5ada517967bfb8f8f6f53d94f1f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e7fdfad8844eba72c2f010575b51d1853acfa6f5d4178eda779e5e3248f665`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda37e286727615d00d3bea8d09e794f44239a009d5cdcb233c8770ccce5617f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d08118e95deb42f13d3aad50343087c81fd82c5fd1249711238860e5b5dbe6`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 188.6 MB (188618802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe6ee26314619eb9565ac44c5ed9096091ca9ad82699df195fe0ed570c0075`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.8` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:4eccb96fa80116fb7bfdb2016202d031acab310aff1fbe1a31ed3458c7925d6e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310847455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf17d5f9ce3a5ba7a1710b20b3702fe11610173c4f498a9a2cc84b7b3038c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 22:25:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:01 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:27:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559775808be333a0da9ac865f922637f6d96964d8a49b01dc7a539e30da53541`  
		Last Modified: Thu, 23 Jan 2025 22:27:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbb06df7a13245a54deeb8da4ca94d4fbcbb1e8d833632999811496c4a6646`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e856345c30f26ba775fe0c97a987d19316ab76023e6a52c1b908e8dacffb13`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c729ee0ff0aea816ca3ae7688827dfe9e53ccaacc6d4bc77e871ba9f67fb172c`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245fa98868b43a67c87aaefa5b9cf1018d8e5ad2b556a7b372ea3e34a71ff8be`  
		Last Modified: Thu, 23 Jan 2025 22:27:49 GMT  
		Size: 188.6 MB (188628804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dd8b372a3fd21947c8ca5292b8b02e40d9c0384441598589ee0967262a8878`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.8-alpine`

```console
$ docker pull julia@sha256:369b351b7d190d052c91017897962a57a4cd3d3e194e18d2785bdb4ec1a1898a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.8-alpine` - linux; amd64

```console
$ docker pull julia@sha256:03b393416ff577fbbb8756ac775efd9641a78bbd59153ea59b290570da58cb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182653366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8867740affab2dd3e90d4e2b10b6f945d4ede1847730de657c92490273154`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.8-musl-x86_64.tar.gz'; 			sha256='db86a8e62084f5131acec57f2b83a774a2864bb74b0cd4aa890d91b355521f66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d0bfaec32c6a95944cc0d8d65114cdfe73adcb2b9be18ccff77237fdb45cdf`  
		Last Modified: Thu, 23 Jan 2025 22:26:51 GMT  
		Size: 179.0 MB (179011286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ccec73be86e109eb77dcb294160650f5cff80405d9701f3641a1acd1736b2c`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:4c5598eb38ca9d08f29ef02d975c70a5ef18ea89df0f78f6c33645f6a1ce831b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfbdfb9641648c97fde168beb4709606e9eb8f6f4a2e07985aad6361b59babf`

```dockerfile
```

-	Layers:
	-	`sha256:0c63e29d0d4a59b5076d597b3b168dbca25a05633afa1e9470e34ab8795db523`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 79.9 KB (79881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb09901da9dd4747aef83a8e71bdb3c371b88e82a26e418525f446d9178c20ce`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-alpine3.20`

```console
$ docker pull julia@sha256:9ec4f5c7de80faff56955279e3d5262ee5eda3110720f1b96b53c0e156454b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.8-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:ab544964e48dca5777b4acdb0c47f58904b241746b3a398b875d28ff030eabb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182636897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e634b8acbb090e3061daee729efa57f125da061b73c6c94f7ec2051d1ad51c1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.8-musl-x86_64.tar.gz'; 			sha256='db86a8e62084f5131acec57f2b83a774a2864bb74b0cd4aa890d91b355521f66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb48fa4c3deae8211e602594ff713ed33d71b5e57e21b466f8d7ea0b4a4fa89`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 179.0 MB (179010268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a869c5410324e61154fe821757b53c4a0939cccdb58220151ae6a79d3664bb47`  
		Last Modified: Thu, 23 Jan 2025 22:26:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:a129de9c28f7fd4b53f2c485437e267b44442530e59b91360a331451e39d5e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b507495049b3cad39218f57615f92d998c50f4271ab13b55b847dc1a579204`

```dockerfile
```

-	Layers:
	-	`sha256:1bf28ba86bb2b4a0ebac8fcfbaea8375d6b5557b4e348297c62c4825399ed014`  
		Last Modified: Thu, 23 Jan 2025 22:26:37 GMT  
		Size: 73.5 KB (73545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48d243381e24a468f6e3ed864ad9e308ba4421bd32e669e996691cbaf70a1cb`  
		Last Modified: Thu, 23 Jan 2025 22:26:37 GMT  
		Size: 12.0 KB (11964 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-alpine3.21`

```console
$ docker pull julia@sha256:369b351b7d190d052c91017897962a57a4cd3d3e194e18d2785bdb4ec1a1898a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.8-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:03b393416ff577fbbb8756ac775efd9641a78bbd59153ea59b290570da58cb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182653366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8867740affab2dd3e90d4e2b10b6f945d4ede1847730de657c92490273154`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.8-musl-x86_64.tar.gz'; 			sha256='db86a8e62084f5131acec57f2b83a774a2864bb74b0cd4aa890d91b355521f66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d0bfaec32c6a95944cc0d8d65114cdfe73adcb2b9be18ccff77237fdb45cdf`  
		Last Modified: Thu, 23 Jan 2025 22:26:51 GMT  
		Size: 179.0 MB (179011286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ccec73be86e109eb77dcb294160650f5cff80405d9701f3641a1acd1736b2c`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:4c5598eb38ca9d08f29ef02d975c70a5ef18ea89df0f78f6c33645f6a1ce831b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfbdfb9641648c97fde168beb4709606e9eb8f6f4a2e07985aad6361b59babf`

```dockerfile
```

-	Layers:
	-	`sha256:0c63e29d0d4a59b5076d597b3b168dbca25a05633afa1e9470e34ab8795db523`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 79.9 KB (79881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb09901da9dd4747aef83a8e71bdb3c371b88e82a26e418525f446d9178c20ce`  
		Last Modified: Thu, 23 Jan 2025 22:26:46 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-bookworm`

```console
$ docker pull julia@sha256:f2f50113e343141448ba3f04f21eb08f61f1e26e32f2b93ab32a86af3bead43c
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

### `julia:1.10.8-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:28436c66a05871bbf899572c1c3a82ee1747779ff354b6ac59d72b1fc278e0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209686117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa47198934943bc7076f73b3265130466dda364f32f892c9c58a82a5f08b961`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b6ab97b16e056f5a321255a4e1f5179de80c759153d351136e2585bea6d2c`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 5.7 MB (5713128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea11abd24a9b767f6bb8b3821425d4bd9a969064c8bf7574174fc241ba5b4d`  
		Last Modified: Thu, 23 Jan 2025 22:26:53 GMT  
		Size: 175.8 MB (175760202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec122af0696b5535f9b28763ced10330c1de7baccec9325d1d45c4ac535db22`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:cd1ffd6f2e0bbdbc335f5d2b13c5b0ac7fb6e7514ff1a3a7d9f2c1b0db2735e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7781bea1cd52621d384c4b58b4b42c6db82f57ca3ed8cb78390d6b24f14772e8`

```dockerfile
```

-	Layers:
	-	`sha256:464bab9db9677b4e33ee2f1db8fe35d15cabf42c97c3f1f1958ee21ed0cfbfb2`  
		Last Modified: Thu, 23 Jan 2025 22:26:49 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2438f3ab538da93b3c1bf721e9a21405475214e73b4bf06fbefde48dd2485e`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4574ba2dec556d708ebcab68d52a7432c9a935519ee2fba723d12aa52e113358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210719667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778d696b38e9044182a9d078a7b952fc5b39527a81cc3c0cf9041a44b71071e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300aaebaaec883bb0d408d44dfe9fe655264f98c965523af9ccfd4d2f284e65f`  
		Last Modified: Thu, 23 Jan 2025 22:27:45 GMT  
		Size: 177.1 MB (177140224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce03a8824f25406bf2f0b5ba1c2668e89ec8bd0b9b2106d02c5f41d0df72861`  
		Last Modified: Thu, 23 Jan 2025 22:27:40 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c6af2185e838da80a2fcf66e31324aba6fe5122d6b24c730ba528fc4ddb75f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df19670a503eab60afd8a7a90ba858cc8df3f5f2ce44e1e193f95c336b1df8`

```dockerfile
```

-	Layers:
	-	`sha256:d9ba2ae57517165460478eac1ef2cd1c145d9dd311ed3d50a45e4e5cbb4966a0`  
		Last Modified: Thu, 23 Jan 2025 22:27:41 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc77c84d352b96a9b9ff7f668c363bcf062daf2ba313764d92d2933deace079`  
		Last Modified: Thu, 23 Jan 2025 22:27:40 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bookworm` - linux; 386

```console
$ docker pull julia@sha256:9866141646e334620aa4c662cf04dfa079d3c30e95aa59e0e844afaf488589b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192861935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ef1263b2ea234148ecdbc0433e64cf3ec70b3f225dbf90611d28e20a27e2bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fd5f5a561c987a285556ad1d86dc4c5b3458100245cc0378f2789e4bb1e7b9`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 5.9 MB (5872009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86384ba08a0862dfffd851bc268a6f2f06be1a3256b1bae6294a504dda6438f`  
		Last Modified: Thu, 23 Jan 2025 22:26:45 GMT  
		Size: 157.8 MB (157801960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f1151e37cac805de1f9e76ace0f3bdb60af8369433d55a67553dded26e9035`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:89c83f8f256b0eb75e3cd6e2378ac829bb3867265aaefd319954ae8499b8378a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5425f3427d1f1acce0d548921041dccf366d381ad71497388eb3ebf3c9ffe6e0`

```dockerfile
```

-	Layers:
	-	`sha256:8bd18c6faa7b646ca966a66e0b3e038c673b11e44c05ad244767a58a0ee1a905`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68791ad3e30ba41066ee5dddbf5f9f9ed14159cc8a00f17804681cb4aeac9388`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:f56bc6c2be5398da1b9c37e6ac8b39ce599c57d8f07436ff3da3555d11745524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193451800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e786a229f1503d1ee665ff3b12b671e86e09b8da17e3802dc708ee7d441423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e4efbced4fc8c5378f9eeaef5325b9a3772daa1de8c88c78c5ca10ef3431ab`  
		Last Modified: Thu, 23 Jan 2025 22:27:18 GMT  
		Size: 155.2 MB (155157283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da33c6c1c49ce20ae77586e7cae169835285288d207aed8f3a5f8d18eede24df`  
		Last Modified: Thu, 23 Jan 2025 22:27:13 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:82ccdd03e72eb992b905a7285a4b838a0ed42a2a71c0b05e28f487ea92841446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5809c3bd5bf871dcef5c146c01d108d291bcc5f80dff7dc2d53f042be906f4`

```dockerfile
```

-	Layers:
	-	`sha256:90e7a5e8a11ebeed1ca226c90904bb5b31d270801f12cdab9c91b9db4562a2e4`  
		Last Modified: Thu, 23 Jan 2025 22:27:14 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ec2f7d3b159c8172c8c04f55c7269da04fb33d847e542c1f0bacdc50e7ea8a`  
		Last Modified: Thu, 23 Jan 2025 22:27:13 GMT  
		Size: 17.3 KB (17258 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-bullseye`

```console
$ docker pull julia@sha256:06222907b683ec38998e7c3eda5d9560b74ee0211cfb7f8e9280d6f027aec377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.8-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:45d401ac9f80924d6c9e6b066c2ad9e646c741591dc4cb0887d212238e713cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208236155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cbb36a380b348eefda5d2a9197a4973b6ee806b5a408f2d3b9fad25f051f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f64a555a7910d5b7d05b24a815082fd0c77ca699f23d1ce18b021b48f5471db`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa2b6a7e5f4105c5170192c5351d71759718eec814f6d17ec2cdd170fe751f`  
		Last Modified: Thu, 23 Jan 2025 22:26:42 GMT  
		Size: 175.8 MB (175760431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937821286df5cb49e4d136dc1cd7383e6fd933e369a26944a7708fc41539791`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:3e04a6588ee7cf187ac05cd4cd73c62100c733de17f07d467910d763f2b0b590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428859650e27e4faf81eebac17a35f37f3c26f774df81d247a73c43dea3a1633`

```dockerfile
```

-	Layers:
	-	`sha256:668f9c8a767bab0a90b9cccafbca643c0e37d0641c49c9484ba50fd478fa5cd1`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0928cba69fe357d7bff75b3ccd226126f3f38fe5a68094f41ded015feed4cc1`  
		Last Modified: Thu, 23 Jan 2025 22:26:39 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4410a60b7c45f45e2ed5bde215d431925f0b28d251307c1ae9a2d4af6b7c3f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208096103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b0ba3311fe7a70b3388bc79c7f4722d0812a0e2e8c88ef6520f5c711b41f4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1835e135f44f85a0bb5c2c3a94070c34d2c3edbcad74d7c221aa15bf1e174c8`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.2 MB (2210265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2783cf4efe73257fb9b81dd152a1c62ac4d47c3589b654fbc431250acad0b72c`  
		Last Modified: Thu, 23 Jan 2025 22:28:51 GMT  
		Size: 177.1 MB (177140553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af3a9ed1fdf83eb772353c63e429cb867e5697004b1002e34ce9e92404205ca`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0c3727b56ef2f1068dd2af69dcf1ccf4a1c4f79f3309004a1a2a18d4bcc3a0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93b9a77053fac0d17ee1ef1f6774a639189ddb0802ea9254201899c675096de`

```dockerfile
```

-	Layers:
	-	`sha256:25cced3e18cf4a02da250ff3334c75eb86bf647cce27e3d25cfffbf1c5d46227`  
		Last Modified: Thu, 23 Jan 2025 22:28:47 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3344f742d41e5c4458c940f2a50b81df95df5d1ff11cacded230cc912bee0d47`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bullseye` - linux; 386

```console
$ docker pull julia@sha256:8ab785bd9ad0faeb613e0667080e85a76800f939b5adb3f734e698ea3b841526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191309340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83a05bdebe2da16c7aa1653b5608fb839d2b582d32ef96a0b298f1280485500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9f16c63408f231fb65c48018657b31b5c5eafdf798975d354ffcdedd4668ec`  
		Last Modified: Thu, 23 Jan 2025 22:26:44 GMT  
		Size: 2.3 MB (2328090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967e5db2cdcc01a8012b937856fd4742a503272eda6f984263af5537d878c137`  
		Last Modified: Thu, 23 Jan 2025 22:26:48 GMT  
		Size: 157.8 MB (157801851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e357a27391f1706f185a2f5e3a43b40194625920794bb9f118d16cc7f54082a`  
		Last Modified: Thu, 23 Jan 2025 22:26:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:7358c48135bf7642a604cb265bea41fbcd7af230def4358af3ee87cbf56fc5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0d4d432c5362ca6a4ba2d2dd3e9a629eeff325ca40c4fbb4a6db6005a2f2bc`

```dockerfile
```

-	Layers:
	-	`sha256:98e5246574e714566cf3d165d7b5d83a24164d0f1d2240e8818b48571b13e487`  
		Last Modified: Thu, 23 Jan 2025 22:26:44 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4de4126886745c4183443d663939f1a68e1d59b694d471420e16f4339d46c95`  
		Last Modified: Thu, 23 Jan 2025 22:26:44 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-windowsservercore`

```console
$ docker pull julia@sha256:0d94e6602a7f27123870b6e9947da76a92c533743cf8f3b65c0e2793daac75c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10.8-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:7d2b9a6c3fa28dcd28d65427c88e7d379503acb88b508d7b983cf0d55046ca1d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2688969059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b221656547fd936d19281af7c828c5199cd0f73e63f4c1f784165b2246e652d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 22:29:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:29:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:30:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c5302aa7bbe98d12864a76d1af7a5184aa438b7697b7b5b1b9471a4b10d5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758924ec3eb9afedb56332ca25760819f815634bc287ace59d70a9511debd8ab`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cf9b43ec1e778c763a162f521798fa1e0bf745c69242b33f7e3cd24d6278e7`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592cd9a88a0b5ca750c8ecc16f4ff2364fb758f7b22ac2ed22ec72fa12e7fb62`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86633cc37ee5bd328743417b01a85b3d76fce28439d5b9ba357b537988ff95`  
		Last Modified: Thu, 23 Jan 2025 22:31:03 GMT  
		Size: 188.7 MB (188684999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0146c4ebe9975a16078c961377a65aa938570da795ab8dc81e3e757b42cda5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.8-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:1d16c3f0485cd1f94ee5274275b3f39595b2795ef808f9503dc663c7107b9f27
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451010480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c70f55c2ac0775592f1bb6728b284abdc4dece11612e910adb896fec3ddb82a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 22:26:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:21 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:23 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:28:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4c90ee13d429da08cd963a7e0eafca2c47c68adf32c51710368a76b5fe6ebe`  
		Last Modified: Thu, 23 Jan 2025 22:28:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb0cb206b0751f05379acabc31ec8499eaf5ada517967bfb8f8f6f53d94f1f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e7fdfad8844eba72c2f010575b51d1853acfa6f5d4178eda779e5e3248f665`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda37e286727615d00d3bea8d09e794f44239a009d5cdcb233c8770ccce5617f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d08118e95deb42f13d3aad50343087c81fd82c5fd1249711238860e5b5dbe6`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 188.6 MB (188618802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe6ee26314619eb9565ac44c5ed9096091ca9ad82699df195fe0ed570c0075`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.8-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:4eccb96fa80116fb7bfdb2016202d031acab310aff1fbe1a31ed3458c7925d6e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310847455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf17d5f9ce3a5ba7a1710b20b3702fe11610173c4f498a9a2cc84b7b3038c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 22:25:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:01 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:27:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559775808be333a0da9ac865f922637f6d96964d8a49b01dc7a539e30da53541`  
		Last Modified: Thu, 23 Jan 2025 22:27:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbb06df7a13245a54deeb8da4ca94d4fbcbb1e8d833632999811496c4a6646`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e856345c30f26ba775fe0c97a987d19316ab76023e6a52c1b908e8dacffb13`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c729ee0ff0aea816ca3ae7688827dfe9e53ccaacc6d4bc77e871ba9f67fb172c`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245fa98868b43a67c87aaefa5b9cf1018d8e5ad2b556a7b372ea3e34a71ff8be`  
		Last Modified: Thu, 23 Jan 2025 22:27:49 GMT  
		Size: 188.6 MB (188628804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dd8b372a3fd21947c8ca5292b8b02e40d9c0384441598589ee0967262a8878`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.8-windowsservercore-1809`

```console
$ docker pull julia@sha256:2acf0e798ebcbe2f2c6c2cb19e94537035accf6202e32c51ac6e24e6d334b6b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10.8-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:4eccb96fa80116fb7bfdb2016202d031acab310aff1fbe1a31ed3458c7925d6e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310847455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf17d5f9ce3a5ba7a1710b20b3702fe11610173c4f498a9a2cc84b7b3038c6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 22:25:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:01 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:27:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559775808be333a0da9ac865f922637f6d96964d8a49b01dc7a539e30da53541`  
		Last Modified: Thu, 23 Jan 2025 22:27:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cbb06df7a13245a54deeb8da4ca94d4fbcbb1e8d833632999811496c4a6646`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e856345c30f26ba775fe0c97a987d19316ab76023e6a52c1b908e8dacffb13`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c729ee0ff0aea816ca3ae7688827dfe9e53ccaacc6d4bc77e871ba9f67fb172c`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245fa98868b43a67c87aaefa5b9cf1018d8e5ad2b556a7b372ea3e34a71ff8be`  
		Last Modified: Thu, 23 Jan 2025 22:27:49 GMT  
		Size: 188.6 MB (188628804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dd8b372a3fd21947c8ca5292b8b02e40d9c0384441598589ee0967262a8878`  
		Last Modified: Thu, 23 Jan 2025 22:27:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.8-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:9b46af7c5c71d4ed466b812d132b603c6a3d150a967a6650f561901733c5bc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:1.10.8-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:1d16c3f0485cd1f94ee5274275b3f39595b2795ef808f9503dc663c7107b9f27
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451010480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c70f55c2ac0775592f1bb6728b284abdc4dece11612e910adb896fec3ddb82a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 22:26:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:26:21 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:26:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:26:23 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:28:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4c90ee13d429da08cd963a7e0eafca2c47c68adf32c51710368a76b5fe6ebe`  
		Last Modified: Thu, 23 Jan 2025 22:28:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcb0cb206b0751f05379acabc31ec8499eaf5ada517967bfb8f8f6f53d94f1f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e7fdfad8844eba72c2f010575b51d1853acfa6f5d4178eda779e5e3248f665`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda37e286727615d00d3bea8d09e794f44239a009d5cdcb233c8770ccce5617f`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d08118e95deb42f13d3aad50343087c81fd82c5fd1249711238860e5b5dbe6`  
		Last Modified: Thu, 23 Jan 2025 22:28:46 GMT  
		Size: 188.6 MB (188618802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe6ee26314619eb9565ac44c5ed9096091ca9ad82699df195fe0ed570c0075`  
		Last Modified: Thu, 23 Jan 2025 22:28:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.8-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:06554fe34ef76ee712595115b73448f250812bac37df94dbd9ec6cb907e87650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `julia:1.10.8-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:7d2b9a6c3fa28dcd28d65427c88e7d379503acb88b508d7b983cf0d55046ca1d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2688969059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b221656547fd936d19281af7c828c5199cd0f73e63f4c1f784165b2246e652d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 22:29:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:29:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 23 Jan 2025 22:29:48 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 23 Jan 2025 22:30:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c5302aa7bbe98d12864a76d1af7a5184aa438b7697b7b5b1b9471a4b10d5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758924ec3eb9afedb56332ca25760819f815634bc287ace59d70a9511debd8ab`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cf9b43ec1e778c763a162f521798fa1e0bf745c69242b33f7e3cd24d6278e7`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592cd9a88a0b5ca750c8ecc16f4ff2364fb758f7b22ac2ed22ec72fa12e7fb62`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86633cc37ee5bd328743417b01a85b3d76fce28439d5b9ba357b537988ff95`  
		Last Modified: Thu, 23 Jan 2025 22:31:03 GMT  
		Size: 188.7 MB (188684999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0146c4ebe9975a16078c961377a65aa938570da795ab8dc81e3e757b42cda5fa`  
		Last Modified: Thu, 23 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:19123e4338d8ad2fc3d719eafb9611b8f8dcfa02861089c038d37aab26388371
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:dfd9e0c4c633f254a308c1916578ce6710fe9d83369d49c5041ac31c92514403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302230971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15da0b07dfa5794bba53fc0b720a07076c26b6b3137fa1c4a0901b1b7b6b203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11860dad45048203d204a51474f3925e9683760498bf50f92df3cca666dd458b`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 5.7 MB (5713140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac9baef82d2d108ad6edf1a74295af617edc712cd5c8ab23e8ff2374ac77ed`  
		Last Modified: Wed, 22 Jan 2025 20:32:10 GMT  
		Size: 268.3 MB (268305043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472e8b8bc35a5891e935d49aa58655018aedd4e7fd1385a16d6a309bd25da9b9`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:b0e563c0d521de7b2a427bbf46438b2f1f6c5e10674a3b5c5917a25155aea078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824872dea940f11b8ff617822decf8d0c116bb8f1405dcd8500490f1634a60c0`

```dockerfile
```

-	Layers:
	-	`sha256:70a9556a7e1795501be1e9027bb1e59d86d0319c09f9f17dab00e4c12edae264`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7af1b6e5c9662831f11bd0d9b9f3c7a7778283a77fa77047476a8d7b3211b6`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b6b57a30ff9c52f062fe0d438029cdd84acf063ac25abea70927491f48647e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ff4826fb6b79ca9e2f60429606e6750bf387340f9ddd220c8c8e0d616ab8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2508a326b870e86f138cfd69d3040b99b4c69da739a433a76f0d42e2d7295`  
		Last Modified: Wed, 22 Jan 2025 20:47:55 GMT  
		Size: 283.9 MB (283934039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811908adbde892f0dc087de51d194a44302234dd8db1e1edd0a23b28b6590`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:be7b3b6d64bd30778c516836cba5d3319f5b6a93f0356a89b904b1f50606caf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edb88069991bac9ce6470a081597ddd1244fbb437808f645fb86d92527ebcd2`

```dockerfile
```

-	Layers:
	-	`sha256:4880a0936365197181a4c4fd61b3de79bd9c1a6fec18f7b100bd342204f2e9b6`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eac05a8fe45fb0942ac43f011c50367ca5c9238aff408712b8f3eb77b55591`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:814b7fec42d571633907dc2cef4faa25d6398d9b56d85ee4d1c46c48431d8db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252975156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366aa7705fa4ebea2a897877c696d91f3e63433b84350c783bd0c2924ffca7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4c578b793469a79623c080953da1703a24154efcd4d115d0bd6f6861e91ed`  
		Last Modified: Wed, 22 Jan 2025 20:31:56 GMT  
		Size: 5.9 MB (5872033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2d23153d25f71daec926fb2601f508915eb86ae59b035f26da7984e60b60d`  
		Last Modified: Wed, 22 Jan 2025 20:32:00 GMT  
		Size: 217.9 MB (217915156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a4c16e5d74edd13537edd7983b1cd6f51d8d1564968f8dfe1b43ef30f3ce4`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:3dc4e34abd257a0c7de8ba7913e600994574286aed92ea308628d25a465cda1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e503f41d3f52790f1be988dadefdee94f7efc64a36dfba30c9de3c005590d5d`

```dockerfile
```

-	Layers:
	-	`sha256:0990cc379cdc9c889f2638e77546ce33d5d756db6da2de1c7588beb6becf84e5`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410284fbd0a09ef4fde53132a1df54dad2e8931ad3a218f4fec9ad984ee2598b`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:3e27a466b4db0fcd6951fba88bbd792201e36f66a0f3c8ff29316cf33d536197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909eb8fce329f21bb6f910d0f97efce27330dcdd686d89f2e8828968fffa10d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88deb77bfd22b73b5868698e1252ff274e03e929f8078b18558dff903688ebb`  
		Last Modified: Wed, 22 Jan 2025 22:10:26 GMT  
		Size: 228.6 MB (228554518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420be3a0625df33882f4115a70e7cbab62892bcf6537408403cb373a1d89005b`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:bcd8d8618f705417c25783d30ea72b25e7de656f94697752316dbb67b2990c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6720277dd6a7fb7f038fd659f97c800a83c412651af7a82c34d22378666eb32`

```dockerfile
```

-	Layers:
	-	`sha256:cc01de99746f8e67a67aeda29c1fe24ba526e7041ce370c2a6c49d3a085e5f68`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e137bcd587be4a60bda3ad46a6d0562f3d1261afd55cb1bc77a4e82ea4a2dd6`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:0dec0ffb23a93fb5a4f415ea2967d2d95d9dcf714c91cfb9bd7f9fbf7b5d853d
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
$ docker pull julia@sha256:dfd9e0c4c633f254a308c1916578ce6710fe9d83369d49c5041ac31c92514403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302230971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15da0b07dfa5794bba53fc0b720a07076c26b6b3137fa1c4a0901b1b7b6b203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11860dad45048203d204a51474f3925e9683760498bf50f92df3cca666dd458b`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 5.7 MB (5713140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac9baef82d2d108ad6edf1a74295af617edc712cd5c8ab23e8ff2374ac77ed`  
		Last Modified: Wed, 22 Jan 2025 20:32:10 GMT  
		Size: 268.3 MB (268305043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472e8b8bc35a5891e935d49aa58655018aedd4e7fd1385a16d6a309bd25da9b9`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b0e563c0d521de7b2a427bbf46438b2f1f6c5e10674a3b5c5917a25155aea078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824872dea940f11b8ff617822decf8d0c116bb8f1405dcd8500490f1634a60c0`

```dockerfile
```

-	Layers:
	-	`sha256:70a9556a7e1795501be1e9027bb1e59d86d0319c09f9f17dab00e4c12edae264`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7af1b6e5c9662831f11bd0d9b9f3c7a7778283a77fa77047476a8d7b3211b6`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b6b57a30ff9c52f062fe0d438029cdd84acf063ac25abea70927491f48647e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ff4826fb6b79ca9e2f60429606e6750bf387340f9ddd220c8c8e0d616ab8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2508a326b870e86f138cfd69d3040b99b4c69da739a433a76f0d42e2d7295`  
		Last Modified: Wed, 22 Jan 2025 20:47:55 GMT  
		Size: 283.9 MB (283934039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811908adbde892f0dc087de51d194a44302234dd8db1e1edd0a23b28b6590`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:be7b3b6d64bd30778c516836cba5d3319f5b6a93f0356a89b904b1f50606caf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edb88069991bac9ce6470a081597ddd1244fbb437808f645fb86d92527ebcd2`

```dockerfile
```

-	Layers:
	-	`sha256:4880a0936365197181a4c4fd61b3de79bd9c1a6fec18f7b100bd342204f2e9b6`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eac05a8fe45fb0942ac43f011c50367ca5c9238aff408712b8f3eb77b55591`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:814b7fec42d571633907dc2cef4faa25d6398d9b56d85ee4d1c46c48431d8db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252975156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366aa7705fa4ebea2a897877c696d91f3e63433b84350c783bd0c2924ffca7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4c578b793469a79623c080953da1703a24154efcd4d115d0bd6f6861e91ed`  
		Last Modified: Wed, 22 Jan 2025 20:31:56 GMT  
		Size: 5.9 MB (5872033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2d23153d25f71daec926fb2601f508915eb86ae59b035f26da7984e60b60d`  
		Last Modified: Wed, 22 Jan 2025 20:32:00 GMT  
		Size: 217.9 MB (217915156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a4c16e5d74edd13537edd7983b1cd6f51d8d1564968f8dfe1b43ef30f3ce4`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3dc4e34abd257a0c7de8ba7913e600994574286aed92ea308628d25a465cda1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e503f41d3f52790f1be988dadefdee94f7efc64a36dfba30c9de3c005590d5d`

```dockerfile
```

-	Layers:
	-	`sha256:0990cc379cdc9c889f2638e77546ce33d5d756db6da2de1c7588beb6becf84e5`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410284fbd0a09ef4fde53132a1df54dad2e8931ad3a218f4fec9ad984ee2598b`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:3e27a466b4db0fcd6951fba88bbd792201e36f66a0f3c8ff29316cf33d536197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909eb8fce329f21bb6f910d0f97efce27330dcdd686d89f2e8828968fffa10d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88deb77bfd22b73b5868698e1252ff274e03e929f8078b18558dff903688ebb`  
		Last Modified: Wed, 22 Jan 2025 22:10:26 GMT  
		Size: 228.6 MB (228554518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420be3a0625df33882f4115a70e7cbab62892bcf6537408403cb373a1d89005b`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bcd8d8618f705417c25783d30ea72b25e7de656f94697752316dbb67b2990c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6720277dd6a7fb7f038fd659f97c800a83c412651af7a82c34d22378666eb32`

```dockerfile
```

-	Layers:
	-	`sha256:cc01de99746f8e67a67aeda29c1fe24ba526e7041ce370c2a6c49d3a085e5f68`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e137bcd587be4a60bda3ad46a6d0562f3d1261afd55cb1bc77a4e82ea4a2dd6`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bullseye`

```console
$ docker pull julia@sha256:e9ee3bb81f4ac27dfe4b0265461288134ceda8675734267eb1d8f94d32d4bf0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:781b30fe7f616a0f2e856db2c849abfe7046fc742d6bb0f57f60842a7fd742d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300780897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6ede12ef81315a7b438b0146b5f231f7f61cc2a2cec1cc2b5e3e7e8af53513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315057799844e342367e62797410ef3f354df191a3eddfff67174f8280aa2574`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706e1632f981a535ef3b384530c7a992532b9d1711a6419e5a6e3b56b61140a4`  
		Last Modified: Wed, 22 Jan 2025 20:32:27 GMT  
		Size: 268.3 MB (268305170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d8cd2b8533d98a0906bc9959647aa9b42f1fef5b5515d7ed6b5e96ac469e1`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:ce9df326374bc88c2fd965d6bbda05332eb976fffba0b87dc92a24ab921350ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047f824041ea2bfe680f42c783898976041b40f20b3336d15bc91bc494a92546`

```dockerfile
```

-	Layers:
	-	`sha256:2a206d07edd1ca3327674f132466b77256cc4e51cf25a4aa54d010eb8936afa6`  
		Last Modified: Wed, 22 Jan 2025 20:32:22 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e8a5c92f79371895b1676de8c14a76f0c4cb4f467d753fef88e007cbd34ff1`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d8be078c91e946b763ad4eb8bc64d41d7b5979cc56981d79d84f149060487e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314891613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3a0bb9b65de1d8a7581fff3f9887e2197036d68b8b800ef54d1bec7f5ac678`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1835e135f44f85a0bb5c2c3a94070c34d2c3edbcad74d7c221aa15bf1e174c8`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.2 MB (2210265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e277e65273fc46fa6e750c0e3bd08d3df1e24543ded9eb1070dbea35ce672ca`  
		Last Modified: Wed, 22 Jan 2025 20:49:26 GMT  
		Size: 283.9 MB (283936065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32efa8f69db69aea668db9ffa5e5138a4ef44a0ef4c6b1fa8fcb9fe86df22f55`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0522c45ced18a4a568f2884b10827a2051aef7c30d731dcb56caac1f1688d556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5791640cd2d006fdf4ecd31e70e5d4029ead71ce99ee238936074dc4e33eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ecdf93b8b928b31de96a6216f658d90220c50a9b77c3978dcf5113e514e223fb`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fda29c8f157db9624e9f5926ec8093b4066888a17d9570d7fe89816e1615c69`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; 386

```console
$ docker pull julia@sha256:ec5e4205e52a62b49a78332b1a22592adaeeffe3830b0db7297378441fb3832c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251422332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af1eb265cfada65b5b4799579e755c84c8aa07242febde2ed4351a89e9df0f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b412cbf4071893ed1b94e858a9b759748e886686516f5d75aa03a1fbe5234f79`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 2.3 MB (2328090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cbb1693b6baa5b8a9bcc1be3b299e68e6c96c60b1edb2e12b8ec9e4383c092`  
		Last Modified: Wed, 22 Jan 2025 20:32:19 GMT  
		Size: 217.9 MB (217914846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3a3068160a28ce84408f0e1baa3b0d54560eadfeb855b9bcc1acbfd5da3c83`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:961fd255152fb9f195fbd909625d951117b9bb1b326b18dc21a3073dde1ecb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c6127c8c489d9790921190cb0f102547b84cc7c0f293ae95774cb42517f1c1`

```dockerfile
```

-	Layers:
	-	`sha256:a6de4ca2fba28dbc08fafad965f9bd085ae56f92159b60c850be65be3308fd43`  
		Last Modified: Wed, 22 Jan 2025 20:32:14 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915d105ffd540dab571a864c9b9de7d5db098a2096b6b9e3056809e8a0c917e9`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:05f492a8b62ea4e989705f5f2a6d24f3b3f1a4025f4299a7396302a19717c7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:d15ed40b5dd0f815972c8d1ce60a9d900f3f279aaa3ecf63fa9b56587f4f567a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1eb9a74451306dd33a9bc7fa579743f12f360f011137705318dc2581ef72d41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:67fda6c48eda4e0f77740f4573ef5dc220572ab87ca07290a699cad567522bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `julia:1.11-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.3`

```console
$ docker pull julia@sha256:19123e4338d8ad2fc3d719eafb9611b8f8dcfa02861089c038d37aab26388371
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.11.3` - linux; amd64

```console
$ docker pull julia@sha256:dfd9e0c4c633f254a308c1916578ce6710fe9d83369d49c5041ac31c92514403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302230971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15da0b07dfa5794bba53fc0b720a07076c26b6b3137fa1c4a0901b1b7b6b203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11860dad45048203d204a51474f3925e9683760498bf50f92df3cca666dd458b`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 5.7 MB (5713140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac9baef82d2d108ad6edf1a74295af617edc712cd5c8ab23e8ff2374ac77ed`  
		Last Modified: Wed, 22 Jan 2025 20:32:10 GMT  
		Size: 268.3 MB (268305043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472e8b8bc35a5891e935d49aa58655018aedd4e7fd1385a16d6a309bd25da9b9`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3` - unknown; unknown

```console
$ docker pull julia@sha256:b0e563c0d521de7b2a427bbf46438b2f1f6c5e10674a3b5c5917a25155aea078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824872dea940f11b8ff617822decf8d0c116bb8f1405dcd8500490f1634a60c0`

```dockerfile
```

-	Layers:
	-	`sha256:70a9556a7e1795501be1e9027bb1e59d86d0319c09f9f17dab00e4c12edae264`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7af1b6e5c9662831f11bd0d9b9f3c7a7778283a77fa77047476a8d7b3211b6`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b6b57a30ff9c52f062fe0d438029cdd84acf063ac25abea70927491f48647e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ff4826fb6b79ca9e2f60429606e6750bf387340f9ddd220c8c8e0d616ab8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2508a326b870e86f138cfd69d3040b99b4c69da739a433a76f0d42e2d7295`  
		Last Modified: Wed, 22 Jan 2025 20:47:55 GMT  
		Size: 283.9 MB (283934039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811908adbde892f0dc087de51d194a44302234dd8db1e1edd0a23b28b6590`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3` - unknown; unknown

```console
$ docker pull julia@sha256:be7b3b6d64bd30778c516836cba5d3319f5b6a93f0356a89b904b1f50606caf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edb88069991bac9ce6470a081597ddd1244fbb437808f645fb86d92527ebcd2`

```dockerfile
```

-	Layers:
	-	`sha256:4880a0936365197181a4c4fd61b3de79bd9c1a6fec18f7b100bd342204f2e9b6`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eac05a8fe45fb0942ac43f011c50367ca5c9238aff408712b8f3eb77b55591`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3` - linux; 386

```console
$ docker pull julia@sha256:814b7fec42d571633907dc2cef4faa25d6398d9b56d85ee4d1c46c48431d8db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252975156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366aa7705fa4ebea2a897877c696d91f3e63433b84350c783bd0c2924ffca7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4c578b793469a79623c080953da1703a24154efcd4d115d0bd6f6861e91ed`  
		Last Modified: Wed, 22 Jan 2025 20:31:56 GMT  
		Size: 5.9 MB (5872033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2d23153d25f71daec926fb2601f508915eb86ae59b035f26da7984e60b60d`  
		Last Modified: Wed, 22 Jan 2025 20:32:00 GMT  
		Size: 217.9 MB (217915156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a4c16e5d74edd13537edd7983b1cd6f51d8d1564968f8dfe1b43ef30f3ce4`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3` - unknown; unknown

```console
$ docker pull julia@sha256:3dc4e34abd257a0c7de8ba7913e600994574286aed92ea308628d25a465cda1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e503f41d3f52790f1be988dadefdee94f7efc64a36dfba30c9de3c005590d5d`

```dockerfile
```

-	Layers:
	-	`sha256:0990cc379cdc9c889f2638e77546ce33d5d756db6da2de1c7588beb6becf84e5`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410284fbd0a09ef4fde53132a1df54dad2e8931ad3a218f4fec9ad984ee2598b`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3` - linux; ppc64le

```console
$ docker pull julia@sha256:3e27a466b4db0fcd6951fba88bbd792201e36f66a0f3c8ff29316cf33d536197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909eb8fce329f21bb6f910d0f97efce27330dcdd686d89f2e8828968fffa10d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88deb77bfd22b73b5868698e1252ff274e03e929f8078b18558dff903688ebb`  
		Last Modified: Wed, 22 Jan 2025 22:10:26 GMT  
		Size: 228.6 MB (228554518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420be3a0625df33882f4115a70e7cbab62892bcf6537408403cb373a1d89005b`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3` - unknown; unknown

```console
$ docker pull julia@sha256:bcd8d8618f705417c25783d30ea72b25e7de656f94697752316dbb67b2990c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6720277dd6a7fb7f038fd659f97c800a83c412651af7a82c34d22378666eb32`

```dockerfile
```

-	Layers:
	-	`sha256:cc01de99746f8e67a67aeda29c1fe24ba526e7041ce370c2a6c49d3a085e5f68`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e137bcd587be4a60bda3ad46a6d0562f3d1261afd55cb1bc77a4e82ea4a2dd6`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.3` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.3` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.3-bookworm`

```console
$ docker pull julia@sha256:0dec0ffb23a93fb5a4f415ea2967d2d95d9dcf714c91cfb9bd7f9fbf7b5d853d
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

### `julia:1.11.3-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:dfd9e0c4c633f254a308c1916578ce6710fe9d83369d49c5041ac31c92514403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302230971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15da0b07dfa5794bba53fc0b720a07076c26b6b3137fa1c4a0901b1b7b6b203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11860dad45048203d204a51474f3925e9683760498bf50f92df3cca666dd458b`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 5.7 MB (5713140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac9baef82d2d108ad6edf1a74295af617edc712cd5c8ab23e8ff2374ac77ed`  
		Last Modified: Wed, 22 Jan 2025 20:32:10 GMT  
		Size: 268.3 MB (268305043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472e8b8bc35a5891e935d49aa58655018aedd4e7fd1385a16d6a309bd25da9b9`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b0e563c0d521de7b2a427bbf46438b2f1f6c5e10674a3b5c5917a25155aea078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824872dea940f11b8ff617822decf8d0c116bb8f1405dcd8500490f1634a60c0`

```dockerfile
```

-	Layers:
	-	`sha256:70a9556a7e1795501be1e9027bb1e59d86d0319c09f9f17dab00e4c12edae264`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7af1b6e5c9662831f11bd0d9b9f3c7a7778283a77fa77047476a8d7b3211b6`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b6b57a30ff9c52f062fe0d438029cdd84acf063ac25abea70927491f48647e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ff4826fb6b79ca9e2f60429606e6750bf387340f9ddd220c8c8e0d616ab8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2508a326b870e86f138cfd69d3040b99b4c69da739a433a76f0d42e2d7295`  
		Last Modified: Wed, 22 Jan 2025 20:47:55 GMT  
		Size: 283.9 MB (283934039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811908adbde892f0dc087de51d194a44302234dd8db1e1edd0a23b28b6590`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:be7b3b6d64bd30778c516836cba5d3319f5b6a93f0356a89b904b1f50606caf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edb88069991bac9ce6470a081597ddd1244fbb437808f645fb86d92527ebcd2`

```dockerfile
```

-	Layers:
	-	`sha256:4880a0936365197181a4c4fd61b3de79bd9c1a6fec18f7b100bd342204f2e9b6`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eac05a8fe45fb0942ac43f011c50367ca5c9238aff408712b8f3eb77b55591`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bookworm` - linux; 386

```console
$ docker pull julia@sha256:814b7fec42d571633907dc2cef4faa25d6398d9b56d85ee4d1c46c48431d8db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252975156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366aa7705fa4ebea2a897877c696d91f3e63433b84350c783bd0c2924ffca7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4c578b793469a79623c080953da1703a24154efcd4d115d0bd6f6861e91ed`  
		Last Modified: Wed, 22 Jan 2025 20:31:56 GMT  
		Size: 5.9 MB (5872033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2d23153d25f71daec926fb2601f508915eb86ae59b035f26da7984e60b60d`  
		Last Modified: Wed, 22 Jan 2025 20:32:00 GMT  
		Size: 217.9 MB (217915156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a4c16e5d74edd13537edd7983b1cd6f51d8d1564968f8dfe1b43ef30f3ce4`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3dc4e34abd257a0c7de8ba7913e600994574286aed92ea308628d25a465cda1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e503f41d3f52790f1be988dadefdee94f7efc64a36dfba30c9de3c005590d5d`

```dockerfile
```

-	Layers:
	-	`sha256:0990cc379cdc9c889f2638e77546ce33d5d756db6da2de1c7588beb6becf84e5`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410284fbd0a09ef4fde53132a1df54dad2e8931ad3a218f4fec9ad984ee2598b`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:3e27a466b4db0fcd6951fba88bbd792201e36f66a0f3c8ff29316cf33d536197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909eb8fce329f21bb6f910d0f97efce27330dcdd686d89f2e8828968fffa10d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88deb77bfd22b73b5868698e1252ff274e03e929f8078b18558dff903688ebb`  
		Last Modified: Wed, 22 Jan 2025 22:10:26 GMT  
		Size: 228.6 MB (228554518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420be3a0625df33882f4115a70e7cbab62892bcf6537408403cb373a1d89005b`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bcd8d8618f705417c25783d30ea72b25e7de656f94697752316dbb67b2990c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6720277dd6a7fb7f038fd659f97c800a83c412651af7a82c34d22378666eb32`

```dockerfile
```

-	Layers:
	-	`sha256:cc01de99746f8e67a67aeda29c1fe24ba526e7041ce370c2a6c49d3a085e5f68`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e137bcd587be4a60bda3ad46a6d0562f3d1261afd55cb1bc77a4e82ea4a2dd6`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.3-bullseye`

```console
$ docker pull julia@sha256:e9ee3bb81f4ac27dfe4b0265461288134ceda8675734267eb1d8f94d32d4bf0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11.3-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:781b30fe7f616a0f2e856db2c849abfe7046fc742d6bb0f57f60842a7fd742d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300780897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6ede12ef81315a7b438b0146b5f231f7f61cc2a2cec1cc2b5e3e7e8af53513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315057799844e342367e62797410ef3f354df191a3eddfff67174f8280aa2574`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706e1632f981a535ef3b384530c7a992532b9d1711a6419e5a6e3b56b61140a4`  
		Last Modified: Wed, 22 Jan 2025 20:32:27 GMT  
		Size: 268.3 MB (268305170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d8cd2b8533d98a0906bc9959647aa9b42f1fef5b5515d7ed6b5e96ac469e1`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:ce9df326374bc88c2fd965d6bbda05332eb976fffba0b87dc92a24ab921350ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047f824041ea2bfe680f42c783898976041b40f20b3336d15bc91bc494a92546`

```dockerfile
```

-	Layers:
	-	`sha256:2a206d07edd1ca3327674f132466b77256cc4e51cf25a4aa54d010eb8936afa6`  
		Last Modified: Wed, 22 Jan 2025 20:32:22 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e8a5c92f79371895b1676de8c14a76f0c4cb4f467d753fef88e007cbd34ff1`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d8be078c91e946b763ad4eb8bc64d41d7b5979cc56981d79d84f149060487e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314891613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3a0bb9b65de1d8a7581fff3f9887e2197036d68b8b800ef54d1bec7f5ac678`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1835e135f44f85a0bb5c2c3a94070c34d2c3edbcad74d7c221aa15bf1e174c8`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.2 MB (2210265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e277e65273fc46fa6e750c0e3bd08d3df1e24543ded9eb1070dbea35ce672ca`  
		Last Modified: Wed, 22 Jan 2025 20:49:26 GMT  
		Size: 283.9 MB (283936065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32efa8f69db69aea668db9ffa5e5138a4ef44a0ef4c6b1fa8fcb9fe86df22f55`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0522c45ced18a4a568f2884b10827a2051aef7c30d731dcb56caac1f1688d556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5791640cd2d006fdf4ecd31e70e5d4029ead71ce99ee238936074dc4e33eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ecdf93b8b928b31de96a6216f658d90220c50a9b77c3978dcf5113e514e223fb`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fda29c8f157db9624e9f5926ec8093b4066888a17d9570d7fe89816e1615c69`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bullseye` - linux; 386

```console
$ docker pull julia@sha256:ec5e4205e52a62b49a78332b1a22592adaeeffe3830b0db7297378441fb3832c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251422332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af1eb265cfada65b5b4799579e755c84c8aa07242febde2ed4351a89e9df0f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b412cbf4071893ed1b94e858a9b759748e886686516f5d75aa03a1fbe5234f79`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 2.3 MB (2328090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cbb1693b6baa5b8a9bcc1be3b299e68e6c96c60b1edb2e12b8ec9e4383c092`  
		Last Modified: Wed, 22 Jan 2025 20:32:19 GMT  
		Size: 217.9 MB (217914846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3a3068160a28ce84408f0e1baa3b0d54560eadfeb855b9bcc1acbfd5da3c83`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:961fd255152fb9f195fbd909625d951117b9bb1b326b18dc21a3073dde1ecb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c6127c8c489d9790921190cb0f102547b84cc7c0f293ae95774cb42517f1c1`

```dockerfile
```

-	Layers:
	-	`sha256:a6de4ca2fba28dbc08fafad965f9bd085ae56f92159b60c850be65be3308fd43`  
		Last Modified: Wed, 22 Jan 2025 20:32:14 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915d105ffd540dab571a864c9b9de7d5db098a2096b6b9e3056809e8a0c917e9`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.3-windowsservercore`

```console
$ docker pull julia@sha256:05f492a8b62ea4e989705f5f2a6d24f3b3f1a4025f4299a7396302a19717c7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.11.3-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.3-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.3-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.3-windowsservercore-1809`

```console
$ docker pull julia@sha256:d15ed40b5dd0f815972c8d1ce60a9d900f3f279aaa3ecf63fa9b56587f4f567a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `julia:1.11.3-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.3-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1eb9a74451306dd33a9bc7fa579743f12f360f011137705318dc2581ef72d41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:1.11.3-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.3-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:67fda6c48eda4e0f77740f4573ef5dc220572ab87ca07290a699cad567522bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `julia:1.11.3-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:0dec0ffb23a93fb5a4f415ea2967d2d95d9dcf714c91cfb9bd7f9fbf7b5d853d
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

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:dfd9e0c4c633f254a308c1916578ce6710fe9d83369d49c5041ac31c92514403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302230971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15da0b07dfa5794bba53fc0b720a07076c26b6b3137fa1c4a0901b1b7b6b203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11860dad45048203d204a51474f3925e9683760498bf50f92df3cca666dd458b`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 5.7 MB (5713140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac9baef82d2d108ad6edf1a74295af617edc712cd5c8ab23e8ff2374ac77ed`  
		Last Modified: Wed, 22 Jan 2025 20:32:10 GMT  
		Size: 268.3 MB (268305043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472e8b8bc35a5891e935d49aa58655018aedd4e7fd1385a16d6a309bd25da9b9`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b0e563c0d521de7b2a427bbf46438b2f1f6c5e10674a3b5c5917a25155aea078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824872dea940f11b8ff617822decf8d0c116bb8f1405dcd8500490f1634a60c0`

```dockerfile
```

-	Layers:
	-	`sha256:70a9556a7e1795501be1e9027bb1e59d86d0319c09f9f17dab00e4c12edae264`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7af1b6e5c9662831f11bd0d9b9f3c7a7778283a77fa77047476a8d7b3211b6`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b6b57a30ff9c52f062fe0d438029cdd84acf063ac25abea70927491f48647e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ff4826fb6b79ca9e2f60429606e6750bf387340f9ddd220c8c8e0d616ab8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2508a326b870e86f138cfd69d3040b99b4c69da739a433a76f0d42e2d7295`  
		Last Modified: Wed, 22 Jan 2025 20:47:55 GMT  
		Size: 283.9 MB (283934039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811908adbde892f0dc087de51d194a44302234dd8db1e1edd0a23b28b6590`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:be7b3b6d64bd30778c516836cba5d3319f5b6a93f0356a89b904b1f50606caf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edb88069991bac9ce6470a081597ddd1244fbb437808f645fb86d92527ebcd2`

```dockerfile
```

-	Layers:
	-	`sha256:4880a0936365197181a4c4fd61b3de79bd9c1a6fec18f7b100bd342204f2e9b6`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eac05a8fe45fb0942ac43f011c50367ca5c9238aff408712b8f3eb77b55591`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:814b7fec42d571633907dc2cef4faa25d6398d9b56d85ee4d1c46c48431d8db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252975156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366aa7705fa4ebea2a897877c696d91f3e63433b84350c783bd0c2924ffca7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4c578b793469a79623c080953da1703a24154efcd4d115d0bd6f6861e91ed`  
		Last Modified: Wed, 22 Jan 2025 20:31:56 GMT  
		Size: 5.9 MB (5872033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2d23153d25f71daec926fb2601f508915eb86ae59b035f26da7984e60b60d`  
		Last Modified: Wed, 22 Jan 2025 20:32:00 GMT  
		Size: 217.9 MB (217915156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a4c16e5d74edd13537edd7983b1cd6f51d8d1564968f8dfe1b43ef30f3ce4`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3dc4e34abd257a0c7de8ba7913e600994574286aed92ea308628d25a465cda1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e503f41d3f52790f1be988dadefdee94f7efc64a36dfba30c9de3c005590d5d`

```dockerfile
```

-	Layers:
	-	`sha256:0990cc379cdc9c889f2638e77546ce33d5d756db6da2de1c7588beb6becf84e5`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410284fbd0a09ef4fde53132a1df54dad2e8931ad3a218f4fec9ad984ee2598b`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:3e27a466b4db0fcd6951fba88bbd792201e36f66a0f3c8ff29316cf33d536197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909eb8fce329f21bb6f910d0f97efce27330dcdd686d89f2e8828968fffa10d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88deb77bfd22b73b5868698e1252ff274e03e929f8078b18558dff903688ebb`  
		Last Modified: Wed, 22 Jan 2025 22:10:26 GMT  
		Size: 228.6 MB (228554518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420be3a0625df33882f4115a70e7cbab62892bcf6537408403cb373a1d89005b`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bcd8d8618f705417c25783d30ea72b25e7de656f94697752316dbb67b2990c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6720277dd6a7fb7f038fd659f97c800a83c412651af7a82c34d22378666eb32`

```dockerfile
```

-	Layers:
	-	`sha256:cc01de99746f8e67a67aeda29c1fe24ba526e7041ce370c2a6c49d3a085e5f68`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e137bcd587be4a60bda3ad46a6d0562f3d1261afd55cb1bc77a4e82ea4a2dd6`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:e9ee3bb81f4ac27dfe4b0265461288134ceda8675734267eb1d8f94d32d4bf0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:781b30fe7f616a0f2e856db2c849abfe7046fc742d6bb0f57f60842a7fd742d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300780897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6ede12ef81315a7b438b0146b5f231f7f61cc2a2cec1cc2b5e3e7e8af53513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315057799844e342367e62797410ef3f354df191a3eddfff67174f8280aa2574`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706e1632f981a535ef3b384530c7a992532b9d1711a6419e5a6e3b56b61140a4`  
		Last Modified: Wed, 22 Jan 2025 20:32:27 GMT  
		Size: 268.3 MB (268305170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d8cd2b8533d98a0906bc9959647aa9b42f1fef5b5515d7ed6b5e96ac469e1`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:ce9df326374bc88c2fd965d6bbda05332eb976fffba0b87dc92a24ab921350ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047f824041ea2bfe680f42c783898976041b40f20b3336d15bc91bc494a92546`

```dockerfile
```

-	Layers:
	-	`sha256:2a206d07edd1ca3327674f132466b77256cc4e51cf25a4aa54d010eb8936afa6`  
		Last Modified: Wed, 22 Jan 2025 20:32:22 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e8a5c92f79371895b1676de8c14a76f0c4cb4f467d753fef88e007cbd34ff1`  
		Last Modified: Wed, 22 Jan 2025 20:32:21 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d8be078c91e946b763ad4eb8bc64d41d7b5979cc56981d79d84f149060487e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314891613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3a0bb9b65de1d8a7581fff3f9887e2197036d68b8b800ef54d1bec7f5ac678`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1835e135f44f85a0bb5c2c3a94070c34d2c3edbcad74d7c221aa15bf1e174c8`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.2 MB (2210265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e277e65273fc46fa6e750c0e3bd08d3df1e24543ded9eb1070dbea35ce672ca`  
		Last Modified: Wed, 22 Jan 2025 20:49:26 GMT  
		Size: 283.9 MB (283936065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32efa8f69db69aea668db9ffa5e5138a4ef44a0ef4c6b1fa8fcb9fe86df22f55`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0522c45ced18a4a568f2884b10827a2051aef7c30d731dcb56caac1f1688d556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5791640cd2d006fdf4ecd31e70e5d4029ead71ce99ee238936074dc4e33eb5`

```dockerfile
```

-	Layers:
	-	`sha256:ecdf93b8b928b31de96a6216f658d90220c50a9b77c3978dcf5113e514e223fb`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fda29c8f157db9624e9f5926ec8093b4066888a17d9570d7fe89816e1615c69`  
		Last Modified: Wed, 22 Jan 2025 20:49:18 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:ec5e4205e52a62b49a78332b1a22592adaeeffe3830b0db7297378441fb3832c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251422332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af1eb265cfada65b5b4799579e755c84c8aa07242febde2ed4351a89e9df0f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b412cbf4071893ed1b94e858a9b759748e886686516f5d75aa03a1fbe5234f79`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 2.3 MB (2328090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cbb1693b6baa5b8a9bcc1be3b299e68e6c96c60b1edb2e12b8ec9e4383c092`  
		Last Modified: Wed, 22 Jan 2025 20:32:19 GMT  
		Size: 217.9 MB (217914846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3a3068160a28ce84408f0e1baa3b0d54560eadfeb855b9bcc1acbfd5da3c83`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:961fd255152fb9f195fbd909625d951117b9bb1b326b18dc21a3073dde1ecb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c6127c8c489d9790921190cb0f102547b84cc7c0f293ae95774cb42517f1c1`

```dockerfile
```

-	Layers:
	-	`sha256:a6de4ca2fba28dbc08fafad965f9bd085ae56f92159b60c850be65be3308fd43`  
		Last Modified: Wed, 22 Jan 2025 20:32:14 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915d105ffd540dab571a864c9b9de7d5db098a2096b6b9e3056809e8a0c917e9`  
		Last Modified: Wed, 22 Jan 2025 20:32:13 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:19123e4338d8ad2fc3d719eafb9611b8f8dcfa02861089c038d37aab26388371
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:dfd9e0c4c633f254a308c1916578ce6710fe9d83369d49c5041ac31c92514403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302230971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15da0b07dfa5794bba53fc0b720a07076c26b6b3137fa1c4a0901b1b7b6b203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11860dad45048203d204a51474f3925e9683760498bf50f92df3cca666dd458b`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 5.7 MB (5713140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac9baef82d2d108ad6edf1a74295af617edc712cd5c8ab23e8ff2374ac77ed`  
		Last Modified: Wed, 22 Jan 2025 20:32:10 GMT  
		Size: 268.3 MB (268305043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472e8b8bc35a5891e935d49aa58655018aedd4e7fd1385a16d6a309bd25da9b9`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:b0e563c0d521de7b2a427bbf46438b2f1f6c5e10674a3b5c5917a25155aea078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824872dea940f11b8ff617822decf8d0c116bb8f1405dcd8500490f1634a60c0`

```dockerfile
```

-	Layers:
	-	`sha256:70a9556a7e1795501be1e9027bb1e59d86d0319c09f9f17dab00e4c12edae264`  
		Last Modified: Wed, 22 Jan 2025 20:32:06 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7af1b6e5c9662831f11bd0d9b9f3c7a7778283a77fa77047476a8d7b3211b6`  
		Last Modified: Wed, 22 Jan 2025 20:32:07 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b6b57a30ff9c52f062fe0d438029cdd84acf063ac25abea70927491f48647e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ff4826fb6b79ca9e2f60429606e6750bf387340f9ddd220c8c8e0d616ab8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786cdd393aaf45a4351a11e42b9a053701c1949ab94463c4246991a12c95218`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 5.5 MB (5538041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2508a326b870e86f138cfd69d3040b99b4c69da739a433a76f0d42e2d7295`  
		Last Modified: Wed, 22 Jan 2025 20:47:55 GMT  
		Size: 283.9 MB (283934039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1811908adbde892f0dc087de51d194a44302234dd8db1e1edd0a23b28b6590`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:be7b3b6d64bd30778c516836cba5d3319f5b6a93f0356a89b904b1f50606caf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edb88069991bac9ce6470a081597ddd1244fbb437808f645fb86d92527ebcd2`

```dockerfile
```

-	Layers:
	-	`sha256:4880a0936365197181a4c4fd61b3de79bd9c1a6fec18f7b100bd342204f2e9b6`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eac05a8fe45fb0942ac43f011c50367ca5c9238aff408712b8f3eb77b55591`  
		Last Modified: Wed, 22 Jan 2025 20:47:44 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:814b7fec42d571633907dc2cef4faa25d6398d9b56d85ee4d1c46c48431d8db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252975156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366aa7705fa4ebea2a897877c696d91f3e63433b84350c783bd0c2924ffca7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4c578b793469a79623c080953da1703a24154efcd4d115d0bd6f6861e91ed`  
		Last Modified: Wed, 22 Jan 2025 20:31:56 GMT  
		Size: 5.9 MB (5872033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2d23153d25f71daec926fb2601f508915eb86ae59b035f26da7984e60b60d`  
		Last Modified: Wed, 22 Jan 2025 20:32:00 GMT  
		Size: 217.9 MB (217915156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a4c16e5d74edd13537edd7983b1cd6f51d8d1564968f8dfe1b43ef30f3ce4`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:3dc4e34abd257a0c7de8ba7913e600994574286aed92ea308628d25a465cda1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e503f41d3f52790f1be988dadefdee94f7efc64a36dfba30c9de3c005590d5d`

```dockerfile
```

-	Layers:
	-	`sha256:0990cc379cdc9c889f2638e77546ce33d5d756db6da2de1c7588beb6becf84e5`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410284fbd0a09ef4fde53132a1df54dad2e8931ad3a218f4fec9ad984ee2598b`  
		Last Modified: Wed, 22 Jan 2025 20:31:55 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:3e27a466b4db0fcd6951fba88bbd792201e36f66a0f3c8ff29316cf33d536197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909eb8fce329f21bb6f910d0f97efce27330dcdd686d89f2e8828968fffa10d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd56e15100449d9b7004cd986df2de44f70f44cab84a96b0cde19b1e440f29`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 6.2 MB (6249297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88deb77bfd22b73b5868698e1252ff274e03e929f8078b18558dff903688ebb`  
		Last Modified: Wed, 22 Jan 2025 22:10:26 GMT  
		Size: 228.6 MB (228554518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420be3a0625df33882f4115a70e7cbab62892bcf6537408403cb373a1d89005b`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:bcd8d8618f705417c25783d30ea72b25e7de656f94697752316dbb67b2990c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6720277dd6a7fb7f038fd659f97c800a83c412651af7a82c34d22378666eb32`

```dockerfile
```

-	Layers:
	-	`sha256:cc01de99746f8e67a67aeda29c1fe24ba526e7041ce370c2a6c49d3a085e5f68`  
		Last Modified: Wed, 22 Jan 2025 22:10:20 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e137bcd587be4a60bda3ad46a6d0562f3d1261afd55cb1bc77a4e82ea4a2dd6`  
		Last Modified: Wed, 22 Jan 2025 22:10:19 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:05f492a8b62ea4e989705f5f2a6d24f3b3f1a4025f4299a7396302a19717c7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:d15ed40b5dd0f815972c8d1ce60a9d900f3f279aaa3ecf63fa9b56587f4f567a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:6ce7bfde794ab93821f6790b9df12f0c7e97b45233e54934951549c9a11762ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2387051824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5833be32a6ebf8709d9adce3078d7dacfc268226e63e441ed74612eeae00b36`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 22 Jan 2025 20:31:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:31:22 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:31:23 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe688b84e36179b70cfed3165df17a8e97c4b92cd9e21c59a5c07ee2e69bce`  
		Last Modified: Wed, 22 Jan 2025 20:35:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab706aeec31ba62c56e07f3acfa2cbd97be4acdd82c07b5ef299c5ef8ff4d1`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e57876679b602d7b48986bee1d568ecdb828acc57e4898a9607bf860711816`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942badd8aa11801eb2f1aba4d6f2e5c2bb51ea4d4acc8bd52ebc3ae2b138e81f`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1be7ace7f1d0f17a1c3def8640d83e7ca924a0711aed1bcf40a4371765684a`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 264.8 MB (264832921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194c0dfee7dbcdb138ec867ade869961d81043cdb4bc543c340d05e74f87575`  
		Last Modified: Wed, 22 Jan 2025 20:35:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1eb9a74451306dd33a9bc7fa579743f12f360f011137705318dc2581ef72d41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:67fda6c48eda4e0f77740f4573ef5dc220572ab87ca07290a699cad567522bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:aece3fe5f7aa16ea11478c724f75089140faf3ac244b1a4dd163daeb87e039a4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2765132416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df128f2784c955c9565d187552eac2bd40edd9c2a16fda8ad38290b27413508c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:34:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:34:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:35:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf4ef7cd9010f866edd616bd5b746a297d22d9dd1c2cdce55c3294e79c85a0`  
		Last Modified: Wed, 22 Jan 2025 20:35:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e02cdf482d7669c769f5019952229e05a9c2644551f290cfda4c67a653e62a`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc590d81c0bfd216c06dd17b375af61e49934611fdfe3d9f7fdd066ff84e819`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36260560c2e76fa7f10775ed9157fd9c129a95438d3ecc60631c53eddbcbbefd`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bac3e7c4635a924918bfc47479c83d468048cff125741fc4d6c6f3035f1578`  
		Last Modified: Wed, 22 Jan 2025 20:36:37 GMT  
		Size: 264.8 MB (264848425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf297cae685b78b748386c6a5d84ed1b26f9543118db76f3a1f38b2af8c29a36`  
		Last Modified: Wed, 22 Jan 2025 20:35:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
