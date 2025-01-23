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
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-bullseye`](#julia110-bullseye)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-1809`](#julia110-windowsservercore-1809)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10-windowsservercore-ltsc2025`](#julia110-windowsservercore-ltsc2025)
-	[`julia:1.10.7`](#julia1107)
-	[`julia:1.10.7-bookworm`](#julia1107-bookworm)
-	[`julia:1.10.7-bullseye`](#julia1107-bullseye)
-	[`julia:1.10.7-windowsservercore`](#julia1107-windowsservercore)
-	[`julia:1.10.7-windowsservercore-1809`](#julia1107-windowsservercore-1809)
-	[`julia:1.10.7-windowsservercore-ltsc2022`](#julia1107-windowsservercore-ltsc2022)
-	[`julia:1.10.7-windowsservercore-ltsc2025`](#julia1107-windowsservercore-ltsc2025)
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
$ docker pull julia@sha256:b939e747dd91e2b63293854ed8d239dab9858aa33c8c0f6b3c0f23db11ffde4d
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
$ docker pull julia@sha256:edd8de6510b41380651a0cfce22b95b35c4da74184b445c72403d79a61128e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209820793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4b22e31d70c27cdbc9b37d5cb06473a0aa44220fa11776bbbe8ed773f5500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f28404f369a710bab9a7c8388f492515011cc9095e9c3e12e849397abb5f4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 5.7 MB (5713137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d950c86f350d07745d0403dfd6e7416bf0d520f5bb22e57a8127ee78f3689884`  
		Last Modified: Tue, 14 Jan 2025 02:20:47 GMT  
		Size: 175.9 MB (175894869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6dc88d3be5f4199dc8c192ce0db757a06af315119d62918deb33b1b735cd84`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:83649d9658dc29386ea551f5b6a26e4a4f881e72b84af153c9de225516dce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cceb6560d44190fbd71209922e92d21aa460129b81be0851c3eddba013f46db3`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd313d1adc26214152571b6a8361b2f047de3fbaca2fdd643fa596075ac75d`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687f2e415413015322e2ae1220790502438bbf0a4b55874f0913fd2d7e4960a4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f6af94e92c3d6347eab43aadb000bb521875ef99e5ec82de1aaf5521b1016144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211231308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d97223e860c940f4d8d1a4a061e40dd6985221472e191b52817510ea2cbdde3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c08dd08bd17849cf22675ca0243c698c6fe4b01fabf6a3c3d073ef52292bc`  
		Last Modified: Tue, 14 Jan 2025 03:06:10 GMT  
		Size: 177.7 MB (177651878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add6f4e4175dd49db2bde47c474a365f589850c500efe8b17e48ed1535cd756`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:98dc2724dd034ffa94dd1f0f51581ac92581d5494d620beedfd99159873e59cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5079d2214bbd30e0b479a0e06e399a978371ce527844283919e1810d5821f`

```dockerfile
```

-	Layers:
	-	`sha256:584938e17917b487f9f2c8b8c1c4698fd5a185b74a5efd7396891594cdeddb5e`  
		Last Modified: Tue, 14 Jan 2025 03:06:06 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58528a32f89e6930ab0f01a38d3579676a8c42a3c1de8037d4691f810c72e23d`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:a225d5ce3452efef8a6a3c7b3128752f37432714f470939463dd9bfd85025b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192844952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9966ac739b39d1a45e05398b35cfbdf47a58d4b97757c26b4c312ab20ba21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacadf125ebfe614f9d429c8b5bdf6d0d903c4df91e2da95d4132ce3c3a82e2`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 5.9 MB (5872050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dba39a827ee7f55656de9c241021310212ca40705cd8f8c9bec6c14d9880c7`  
		Last Modified: Tue, 14 Jan 2025 02:32:01 GMT  
		Size: 157.8 MB (157784935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388237bea775ed66dc6f643bb7d0c724ec9defae5550008ac32ad5e0d2e7ca22`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:b0b3fbabded9d034923cc5379cb00d41b9b80829dba5100bcb7524115879ea3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274e9ccf1d8fb36d5d92f737c19bff89fdcba539fa03dd899174db0d5039333`

```dockerfile
```

-	Layers:
	-	`sha256:cde977fe1eb34823bbb2bb31c87ddd7596095cdc36d134a6fc3f862b1eee9aef`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea311a8209b26d03597c5b41d6fda1ee44775d18c496c8acdad213c081e776a`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:417e5fc281dfa44fc541d6df19d69af1c650dc06aaa978e25360cfb85f3351b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3f23264d7289f18ce257bee838033b1a6a2a4b70f0f5311791be9606346526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5a111a086bbf1d30ef24a905695854d18360157ff9692f11169c90ccc428e`  
		Last Modified: Tue, 14 Jan 2025 02:59:02 GMT  
		Size: 155.5 MB (155493289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4d0b667db150b41b9760574e56cdd03830247e5c902dcfc7a95b1cf9e8c0c`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:9858b4a4e5491fda48000243dcbe4017e8e5456af0147070065871ee8e1dddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2e3bd039358880b6e19c014c81ccb9785636c895bcfc85489dcb6189d0bc2f`

```dockerfile
```

-	Layers:
	-	`sha256:85ff17fb46e315f1e821f7e0f86f3c00a6f80fb0320db89cb4eb6402f5b194de`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13be94c786bf7ce3dbe980dc608d497c828bda708eb0849cb3ef08c0ca18eabe`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:a49c2e75d3b371cf365addacc687c8f71f48dadcf03c9417bb8ee67229e7ca0d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2689440632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63cd7f4c35b1688492bda75f3f774ab8070e64021a57fba4b03c3c8a5a5f4ed`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 22 Jan 2025 20:35:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:32 GMT
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
	-	`sha256:3007cf6a11b7dd6200c77c3ba581f7d0bcb2142d09555d188e0d4b408a775062`  
		Last Modified: Wed, 22 Jan 2025 20:35:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b05fc45dd54af8121cf0f84844135533e77d53ce2d81d53da183218518d1cb0`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856feb4ecc2fd57104f241da3561d75b3b62e02f35ed98599c4b3be6b997d3a`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd68166947a4f28cff1eb750cbd1065d824a4e0b70ff0955961806b2cd840457`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79733bd4f2a9afdf53927a7f517bad453db219dd8722463858c9d327958637`  
		Last Modified: Wed, 22 Jan 2025 20:36:01 GMT  
		Size: 189.2 MB (189156558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5953b7295844933e2b861a3a55daf37c8e95b376af626f43d8b9f136b8778`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:9725e412b84cb38042b4013e7a056b2daf6d880b037fcd14965bed67b3f9fca8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451487149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9581f75e8ebcb81fb80ca69f19fae9a9d3cba24297811fbf6605bb3051e4e5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:35:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:35:36 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:35:37 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:35:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:36:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:36:23 GMT
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
	-	`sha256:4376861050dccc91b670adcf4ea779d0ac5942bc0e40e981bfa60102ed4b6066`  
		Last Modified: Tue, 14 Jan 2025 23:36:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49b5b2742734144c11e2b0183f6e93aecef6c6f8f302af11cbfbcfa73d2ba2`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0058a655cba8bb06901b06673ec5728cdd68a4cbc91dc4cf6643de0da477389`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b05eb59373c24387e468f02f222ae3c6f8ea335bacf5df1ebf8103da13f385`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6f7eeaccdd2f57b8ca7feecc04669f8cfe027ea01838b781d05ac162fb72e`  
		Last Modified: Tue, 14 Jan 2025 23:36:50 GMT  
		Size: 189.1 MB (189095478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd82d3d1bccdc4e95a36020c73253edf3b58397496e676cb4ee1f478f5a4f0c`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:39c597e14765afb9afaad442cf37f84facf986848a8c3f9fd6dc8fb5dfe921c9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa61517f629e100c2ce136d7f909fe623ab16fd582cce12a390a2b44ec8b0b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:32:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:07 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:33:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:30 GMT
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
	-	`sha256:e9179ebee2d8b696550cd1af0779cb6936a65338055936b0ae6bfbd1d47346ea`  
		Last Modified: Tue, 14 Jan 2025 23:33:36 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff628f0c6f11e0896cdd9dbd1c81bc68e167ebd51da0faeeaeac535cdcbc8a8b`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adce5640202f2c8ed4b8e27252b3f03eaf562e21c7f7ddf6130c527c9d780e2`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb00945cf018f301a8fa7c8cd45077acb611bace824b24a2259fae3b79c28dd`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b617a719f9f109e838d31694141d200694e7923e96dc770aaa48c62e3954dad`  
		Last Modified: Tue, 14 Jan 2025 23:33:58 GMT  
		Size: 189.0 MB (189040375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b31d408143407e3080adcd8ab9297540ecdefe8335946f3eae8d5588b59fcd`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:ead6152a885d859cf83d3ba7194be4e4f07bbe63b83a140d28e42e1ff6b5e656
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
$ docker pull julia@sha256:edd8de6510b41380651a0cfce22b95b35c4da74184b445c72403d79a61128e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209820793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4b22e31d70c27cdbc9b37d5cb06473a0aa44220fa11776bbbe8ed773f5500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f28404f369a710bab9a7c8388f492515011cc9095e9c3e12e849397abb5f4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 5.7 MB (5713137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d950c86f350d07745d0403dfd6e7416bf0d520f5bb22e57a8127ee78f3689884`  
		Last Modified: Tue, 14 Jan 2025 02:20:47 GMT  
		Size: 175.9 MB (175894869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6dc88d3be5f4199dc8c192ce0db757a06af315119d62918deb33b1b735cd84`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:83649d9658dc29386ea551f5b6a26e4a4f881e72b84af153c9de225516dce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cceb6560d44190fbd71209922e92d21aa460129b81be0851c3eddba013f46db3`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd313d1adc26214152571b6a8361b2f047de3fbaca2fdd643fa596075ac75d`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687f2e415413015322e2ae1220790502438bbf0a4b55874f0913fd2d7e4960a4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f6af94e92c3d6347eab43aadb000bb521875ef99e5ec82de1aaf5521b1016144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211231308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d97223e860c940f4d8d1a4a061e40dd6985221472e191b52817510ea2cbdde3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c08dd08bd17849cf22675ca0243c698c6fe4b01fabf6a3c3d073ef52292bc`  
		Last Modified: Tue, 14 Jan 2025 03:06:10 GMT  
		Size: 177.7 MB (177651878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add6f4e4175dd49db2bde47c474a365f589850c500efe8b17e48ed1535cd756`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:98dc2724dd034ffa94dd1f0f51581ac92581d5494d620beedfd99159873e59cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5079d2214bbd30e0b479a0e06e399a978371ce527844283919e1810d5821f`

```dockerfile
```

-	Layers:
	-	`sha256:584938e17917b487f9f2c8b8c1c4698fd5a185b74a5efd7396891594cdeddb5e`  
		Last Modified: Tue, 14 Jan 2025 03:06:06 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58528a32f89e6930ab0f01a38d3579676a8c42a3c1de8037d4691f810c72e23d`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:a225d5ce3452efef8a6a3c7b3128752f37432714f470939463dd9bfd85025b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192844952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9966ac739b39d1a45e05398b35cfbdf47a58d4b97757c26b4c312ab20ba21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacadf125ebfe614f9d429c8b5bdf6d0d903c4df91e2da95d4132ce3c3a82e2`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 5.9 MB (5872050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dba39a827ee7f55656de9c241021310212ca40705cd8f8c9bec6c14d9880c7`  
		Last Modified: Tue, 14 Jan 2025 02:32:01 GMT  
		Size: 157.8 MB (157784935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388237bea775ed66dc6f643bb7d0c724ec9defae5550008ac32ad5e0d2e7ca22`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b0b3fbabded9d034923cc5379cb00d41b9b80829dba5100bcb7524115879ea3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274e9ccf1d8fb36d5d92f737c19bff89fdcba539fa03dd899174db0d5039333`

```dockerfile
```

-	Layers:
	-	`sha256:cde977fe1eb34823bbb2bb31c87ddd7596095cdc36d134a6fc3f862b1eee9aef`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea311a8209b26d03597c5b41d6fda1ee44775d18c496c8acdad213c081e776a`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:417e5fc281dfa44fc541d6df19d69af1c650dc06aaa978e25360cfb85f3351b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3f23264d7289f18ce257bee838033b1a6a2a4b70f0f5311791be9606346526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5a111a086bbf1d30ef24a905695854d18360157ff9692f11169c90ccc428e`  
		Last Modified: Tue, 14 Jan 2025 02:59:02 GMT  
		Size: 155.5 MB (155493289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4d0b667db150b41b9760574e56cdd03830247e5c902dcfc7a95b1cf9e8c0c`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9858b4a4e5491fda48000243dcbe4017e8e5456af0147070065871ee8e1dddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2e3bd039358880b6e19c014c81ccb9785636c895bcfc85489dcb6189d0bc2f`

```dockerfile
```

-	Layers:
	-	`sha256:85ff17fb46e315f1e821f7e0f86f3c00a6f80fb0320db89cb4eb6402f5b194de`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13be94c786bf7ce3dbe980dc608d497c828bda708eb0849cb3ef08c0ca18eabe`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:a643b586fe3237aa1e3b85b8498eb71780a62dd93e802f026325162f3053fbbc
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
$ docker pull julia@sha256:aac9a837df906922a4340a6c00a7b79df61544569823530b35ce1e5f097559e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3037480c5ee98533eb0b15669864b9e843a8acc2ebc67c9ca4f204ac0198968f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d55b5df03cc04376fb0a788be2fb725f972110e022d592477a1ccad2788538b`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 2.2 MB (2222645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b9988d5edf1d2e245b240c8fe1c9ec8fecd839e593d09e1508db59e8ce950`  
		Last Modified: Tue, 14 Jan 2025 02:20:51 GMT  
		Size: 175.9 MB (175895657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb0a37975db8025f32e81a3e717b83a2405bcfce346ab98530668b7c85ebabb`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:294c6b5db1c4d27b0997b89aa867b06eb6964c2456b7401a1c923ca4b0c9b80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b88bf9d073694ea233e45e582239affd9f857b529c405b553be16b46ba8751`

```dockerfile
```

-	Layers:
	-	`sha256:74a7be86fe063c42ab0f5b1ecc059825edd73dcd2bb029add233636087ae5e29`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb04cca202779d02693c8339cec1cfea3c49817dcea8b88143d2b2c3e8fce28`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8c730d262ba8e00edc305a153b344806c0d8cb625df5af427aac0cef4b179391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208607436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0673c51f1f055362811b1b709c816c4c8fd481f983dc3c16f6395b8e52af9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ba9e296c53b7e882a6fba6d9ff8c72398e380d38de500e5effd7f2fb92285`  
		Last Modified: Tue, 14 Jan 2025 03:04:51 GMT  
		Size: 2.2 MB (2210283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd0a2d27d92a61bc9a4ead6261c01be9335fe3104de9ffb57614fa832f2ccc1`  
		Last Modified: Tue, 14 Jan 2025 03:07:06 GMT  
		Size: 177.7 MB (177651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f07fffbea1c39ed3847dbd063891bbe6e87b7f6bfc71269a488d73d5adc93d`  
		Last Modified: Tue, 14 Jan 2025 03:07:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:49afea0e98166811c93be8a8e28c44f8d3849e9bc65080c98d0f85bf6e2faa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685f782e1c3ae70ab6f35994ac0437e77772d0bd357524ebdf0a3eee07d58fb3`

```dockerfile
```

-	Layers:
	-	`sha256:1ec5482662762f70d5b53a0c5639dd9b6d8e3363d3e68876b460a5689d00a429`  
		Last Modified: Tue, 14 Jan 2025 03:07:02 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d6f3d22d160c355da4ce15c196eb2df5baf6707b314e07d1c4cc6c07480e15`  
		Last Modified: Tue, 14 Jan 2025 03:07:01 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:170c925a9da9a0b982fc2c4d9aaaa503624e5562f0aead115f347320f411eac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191292320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0beebdd84b2fc10ea9226ce9826470f3f72a62023bc87a3d64abe5bb9db52011`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e879f31fb96b43e23c3e054f0820123765b412dc66530af4ad3588c9b5bf44e1`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 2.3 MB (2328064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec88cc224c3977de0a32d85d327e7840466c5b64ab35971ff90e47ae28d715b`  
		Last Modified: Tue, 14 Jan 2025 02:16:32 GMT  
		Size: 157.8 MB (157784860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47442c6195b93bb9d7b49a40f8c450fc0900ff87d96030a583287dec9607b031`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:adec2665c7cf2c7300b1ea7fc3405d27c93287d1673b4ca039fe10abb2ce402f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8112c94bd75b90229d93506219da7ca4c57d6cb71bec263d46f0eaa04a98e25c`

```dockerfile
```

-	Layers:
	-	`sha256:c216fd2acccb7d7dbf197f9e689c2a26613942aff7862c8e2030ae22caa15bd4`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3819793522831161986b2a33da4bbce69a029175059ca1ca5691cb9ed760462f`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:43c4b3f7abe069b59b950c7608d707c86b2b7dc49d41eba988edcaec35dcfaf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:a49c2e75d3b371cf365addacc687c8f71f48dadcf03c9417bb8ee67229e7ca0d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2689440632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63cd7f4c35b1688492bda75f3f774ab8070e64021a57fba4b03c3c8a5a5f4ed`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 22 Jan 2025 20:35:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:32 GMT
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
	-	`sha256:3007cf6a11b7dd6200c77c3ba581f7d0bcb2142d09555d188e0d4b408a775062`  
		Last Modified: Wed, 22 Jan 2025 20:35:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b05fc45dd54af8121cf0f84844135533e77d53ce2d81d53da183218518d1cb0`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856feb4ecc2fd57104f241da3561d75b3b62e02f35ed98599c4b3be6b997d3a`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd68166947a4f28cff1eb750cbd1065d824a4e0b70ff0955961806b2cd840457`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79733bd4f2a9afdf53927a7f517bad453db219dd8722463858c9d327958637`  
		Last Modified: Wed, 22 Jan 2025 20:36:01 GMT  
		Size: 189.2 MB (189156558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5953b7295844933e2b861a3a55daf37c8e95b376af626f43d8b9f136b8778`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:9725e412b84cb38042b4013e7a056b2daf6d880b037fcd14965bed67b3f9fca8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451487149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9581f75e8ebcb81fb80ca69f19fae9a9d3cba24297811fbf6605bb3051e4e5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:35:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:35:36 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:35:37 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:35:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:36:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:36:23 GMT
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
	-	`sha256:4376861050dccc91b670adcf4ea779d0ac5942bc0e40e981bfa60102ed4b6066`  
		Last Modified: Tue, 14 Jan 2025 23:36:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49b5b2742734144c11e2b0183f6e93aecef6c6f8f302af11cbfbcfa73d2ba2`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0058a655cba8bb06901b06673ec5728cdd68a4cbc91dc4cf6643de0da477389`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b05eb59373c24387e468f02f222ae3c6f8ea335bacf5df1ebf8103da13f385`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6f7eeaccdd2f57b8ca7feecc04669f8cfe027ea01838b781d05ac162fb72e`  
		Last Modified: Tue, 14 Jan 2025 23:36:50 GMT  
		Size: 189.1 MB (189095478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd82d3d1bccdc4e95a36020c73253edf3b58397496e676cb4ee1f478f5a4f0c`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:39c597e14765afb9afaad442cf37f84facf986848a8c3f9fd6dc8fb5dfe921c9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa61517f629e100c2ce136d7f909fe623ab16fd582cce12a390a2b44ec8b0b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:32:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:07 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:33:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:30 GMT
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
	-	`sha256:e9179ebee2d8b696550cd1af0779cb6936a65338055936b0ae6bfbd1d47346ea`  
		Last Modified: Tue, 14 Jan 2025 23:33:36 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff628f0c6f11e0896cdd9dbd1c81bc68e167ebd51da0faeeaeac535cdcbc8a8b`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adce5640202f2c8ed4b8e27252b3f03eaf562e21c7f7ddf6130c527c9d780e2`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb00945cf018f301a8fa7c8cd45077acb611bace824b24a2259fae3b79c28dd`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b617a719f9f109e838d31694141d200694e7923e96dc770aaa48c62e3954dad`  
		Last Modified: Tue, 14 Jan 2025 23:33:58 GMT  
		Size: 189.0 MB (189040375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b31d408143407e3080adcd8ab9297540ecdefe8335946f3eae8d5588b59fcd`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:0f92c7ddbed506140a9175ad5f84b94a1bdd8fce024dac2486cf494c3d798c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:39c597e14765afb9afaad442cf37f84facf986848a8c3f9fd6dc8fb5dfe921c9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa61517f629e100c2ce136d7f909fe623ab16fd582cce12a390a2b44ec8b0b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:32:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:07 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:33:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:30 GMT
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
	-	`sha256:e9179ebee2d8b696550cd1af0779cb6936a65338055936b0ae6bfbd1d47346ea`  
		Last Modified: Tue, 14 Jan 2025 23:33:36 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff628f0c6f11e0896cdd9dbd1c81bc68e167ebd51da0faeeaeac535cdcbc8a8b`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adce5640202f2c8ed4b8e27252b3f03eaf562e21c7f7ddf6130c527c9d780e2`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb00945cf018f301a8fa7c8cd45077acb611bace824b24a2259fae3b79c28dd`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b617a719f9f109e838d31694141d200694e7923e96dc770aaa48c62e3954dad`  
		Last Modified: Tue, 14 Jan 2025 23:33:58 GMT  
		Size: 189.0 MB (189040375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b31d408143407e3080adcd8ab9297540ecdefe8335946f3eae8d5588b59fcd`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:89fd65f5d44cf58047eef192f5799c49a959f4080ff139a7a465a53563e5c2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:9725e412b84cb38042b4013e7a056b2daf6d880b037fcd14965bed67b3f9fca8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451487149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9581f75e8ebcb81fb80ca69f19fae9a9d3cba24297811fbf6605bb3051e4e5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:35:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:35:36 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:35:37 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:35:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:36:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:36:23 GMT
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
	-	`sha256:4376861050dccc91b670adcf4ea779d0ac5942bc0e40e981bfa60102ed4b6066`  
		Last Modified: Tue, 14 Jan 2025 23:36:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49b5b2742734144c11e2b0183f6e93aecef6c6f8f302af11cbfbcfa73d2ba2`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0058a655cba8bb06901b06673ec5728cdd68a4cbc91dc4cf6643de0da477389`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b05eb59373c24387e468f02f222ae3c6f8ea335bacf5df1ebf8103da13f385`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6f7eeaccdd2f57b8ca7feecc04669f8cfe027ea01838b781d05ac162fb72e`  
		Last Modified: Tue, 14 Jan 2025 23:36:50 GMT  
		Size: 189.1 MB (189095478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd82d3d1bccdc4e95a36020c73253edf3b58397496e676cb4ee1f478f5a4f0c`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:04b41d1b15ace47526fb384f03b13ded0d1733384d1c9d4abb0c60445a5dbacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:a49c2e75d3b371cf365addacc687c8f71f48dadcf03c9417bb8ee67229e7ca0d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2689440632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63cd7f4c35b1688492bda75f3f774ab8070e64021a57fba4b03c3c8a5a5f4ed`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 22 Jan 2025 20:35:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:32 GMT
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
	-	`sha256:3007cf6a11b7dd6200c77c3ba581f7d0bcb2142d09555d188e0d4b408a775062`  
		Last Modified: Wed, 22 Jan 2025 20:35:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b05fc45dd54af8121cf0f84844135533e77d53ce2d81d53da183218518d1cb0`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856feb4ecc2fd57104f241da3561d75b3b62e02f35ed98599c4b3be6b997d3a`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd68166947a4f28cff1eb750cbd1065d824a4e0b70ff0955961806b2cd840457`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79733bd4f2a9afdf53927a7f517bad453db219dd8722463858c9d327958637`  
		Last Modified: Wed, 22 Jan 2025 20:36:01 GMT  
		Size: 189.2 MB (189156558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5953b7295844933e2b861a3a55daf37c8e95b376af626f43d8b9f136b8778`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7`

```console
$ docker pull julia@sha256:b939e747dd91e2b63293854ed8d239dab9858aa33c8c0f6b3c0f23db11ffde4d
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

### `julia:1.10.7` - linux; amd64

```console
$ docker pull julia@sha256:edd8de6510b41380651a0cfce22b95b35c4da74184b445c72403d79a61128e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209820793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4b22e31d70c27cdbc9b37d5cb06473a0aa44220fa11776bbbe8ed773f5500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f28404f369a710bab9a7c8388f492515011cc9095e9c3e12e849397abb5f4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 5.7 MB (5713137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d950c86f350d07745d0403dfd6e7416bf0d520f5bb22e57a8127ee78f3689884`  
		Last Modified: Tue, 14 Jan 2025 02:20:47 GMT  
		Size: 175.9 MB (175894869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6dc88d3be5f4199dc8c192ce0db757a06af315119d62918deb33b1b735cd84`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:83649d9658dc29386ea551f5b6a26e4a4f881e72b84af153c9de225516dce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cceb6560d44190fbd71209922e92d21aa460129b81be0851c3eddba013f46db3`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd313d1adc26214152571b6a8361b2f047de3fbaca2fdd643fa596075ac75d`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687f2e415413015322e2ae1220790502438bbf0a4b55874f0913fd2d7e4960a4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f6af94e92c3d6347eab43aadb000bb521875ef99e5ec82de1aaf5521b1016144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211231308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d97223e860c940f4d8d1a4a061e40dd6985221472e191b52817510ea2cbdde3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c08dd08bd17849cf22675ca0243c698c6fe4b01fabf6a3c3d073ef52292bc`  
		Last Modified: Tue, 14 Jan 2025 03:06:10 GMT  
		Size: 177.7 MB (177651878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add6f4e4175dd49db2bde47c474a365f589850c500efe8b17e48ed1535cd756`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:98dc2724dd034ffa94dd1f0f51581ac92581d5494d620beedfd99159873e59cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5079d2214bbd30e0b479a0e06e399a978371ce527844283919e1810d5821f`

```dockerfile
```

-	Layers:
	-	`sha256:584938e17917b487f9f2c8b8c1c4698fd5a185b74a5efd7396891594cdeddb5e`  
		Last Modified: Tue, 14 Jan 2025 03:06:06 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58528a32f89e6930ab0f01a38d3579676a8c42a3c1de8037d4691f810c72e23d`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; 386

```console
$ docker pull julia@sha256:a225d5ce3452efef8a6a3c7b3128752f37432714f470939463dd9bfd85025b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192844952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9966ac739b39d1a45e05398b35cfbdf47a58d4b97757c26b4c312ab20ba21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacadf125ebfe614f9d429c8b5bdf6d0d903c4df91e2da95d4132ce3c3a82e2`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 5.9 MB (5872050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dba39a827ee7f55656de9c241021310212ca40705cd8f8c9bec6c14d9880c7`  
		Last Modified: Tue, 14 Jan 2025 02:32:01 GMT  
		Size: 157.8 MB (157784935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388237bea775ed66dc6f643bb7d0c724ec9defae5550008ac32ad5e0d2e7ca22`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:b0b3fbabded9d034923cc5379cb00d41b9b80829dba5100bcb7524115879ea3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274e9ccf1d8fb36d5d92f737c19bff89fdcba539fa03dd899174db0d5039333`

```dockerfile
```

-	Layers:
	-	`sha256:cde977fe1eb34823bbb2bb31c87ddd7596095cdc36d134a6fc3f862b1eee9aef`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea311a8209b26d03597c5b41d6fda1ee44775d18c496c8acdad213c081e776a`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; ppc64le

```console
$ docker pull julia@sha256:417e5fc281dfa44fc541d6df19d69af1c650dc06aaa978e25360cfb85f3351b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3f23264d7289f18ce257bee838033b1a6a2a4b70f0f5311791be9606346526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5a111a086bbf1d30ef24a905695854d18360157ff9692f11169c90ccc428e`  
		Last Modified: Tue, 14 Jan 2025 02:59:02 GMT  
		Size: 155.5 MB (155493289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4d0b667db150b41b9760574e56cdd03830247e5c902dcfc7a95b1cf9e8c0c`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:9858b4a4e5491fda48000243dcbe4017e8e5456af0147070065871ee8e1dddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2e3bd039358880b6e19c014c81ccb9785636c895bcfc85489dcb6189d0bc2f`

```dockerfile
```

-	Layers:
	-	`sha256:85ff17fb46e315f1e821f7e0f86f3c00a6f80fb0320db89cb4eb6402f5b194de`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13be94c786bf7ce3dbe980dc608d497c828bda708eb0849cb3ef08c0ca18eabe`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:a49c2e75d3b371cf365addacc687c8f71f48dadcf03c9417bb8ee67229e7ca0d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2689440632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63cd7f4c35b1688492bda75f3f774ab8070e64021a57fba4b03c3c8a5a5f4ed`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 22 Jan 2025 20:35:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:32 GMT
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
	-	`sha256:3007cf6a11b7dd6200c77c3ba581f7d0bcb2142d09555d188e0d4b408a775062`  
		Last Modified: Wed, 22 Jan 2025 20:35:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b05fc45dd54af8121cf0f84844135533e77d53ce2d81d53da183218518d1cb0`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856feb4ecc2fd57104f241da3561d75b3b62e02f35ed98599c4b3be6b997d3a`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd68166947a4f28cff1eb750cbd1065d824a4e0b70ff0955961806b2cd840457`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79733bd4f2a9afdf53927a7f517bad453db219dd8722463858c9d327958637`  
		Last Modified: Wed, 22 Jan 2025 20:36:01 GMT  
		Size: 189.2 MB (189156558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5953b7295844933e2b861a3a55daf37c8e95b376af626f43d8b9f136b8778`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:9725e412b84cb38042b4013e7a056b2daf6d880b037fcd14965bed67b3f9fca8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451487149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9581f75e8ebcb81fb80ca69f19fae9a9d3cba24297811fbf6605bb3051e4e5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:35:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:35:36 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:35:37 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:35:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:36:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:36:23 GMT
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
	-	`sha256:4376861050dccc91b670adcf4ea779d0ac5942bc0e40e981bfa60102ed4b6066`  
		Last Modified: Tue, 14 Jan 2025 23:36:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49b5b2742734144c11e2b0183f6e93aecef6c6f8f302af11cbfbcfa73d2ba2`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0058a655cba8bb06901b06673ec5728cdd68a4cbc91dc4cf6643de0da477389`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b05eb59373c24387e468f02f222ae3c6f8ea335bacf5df1ebf8103da13f385`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6f7eeaccdd2f57b8ca7feecc04669f8cfe027ea01838b781d05ac162fb72e`  
		Last Modified: Tue, 14 Jan 2025 23:36:50 GMT  
		Size: 189.1 MB (189095478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd82d3d1bccdc4e95a36020c73253edf3b58397496e676cb4ee1f478f5a4f0c`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:39c597e14765afb9afaad442cf37f84facf986848a8c3f9fd6dc8fb5dfe921c9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa61517f629e100c2ce136d7f909fe623ab16fd582cce12a390a2b44ec8b0b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:32:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:07 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:33:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:30 GMT
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
	-	`sha256:e9179ebee2d8b696550cd1af0779cb6936a65338055936b0ae6bfbd1d47346ea`  
		Last Modified: Tue, 14 Jan 2025 23:33:36 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff628f0c6f11e0896cdd9dbd1c81bc68e167ebd51da0faeeaeac535cdcbc8a8b`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adce5640202f2c8ed4b8e27252b3f03eaf562e21c7f7ddf6130c527c9d780e2`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb00945cf018f301a8fa7c8cd45077acb611bace824b24a2259fae3b79c28dd`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b617a719f9f109e838d31694141d200694e7923e96dc770aaa48c62e3954dad`  
		Last Modified: Tue, 14 Jan 2025 23:33:58 GMT  
		Size: 189.0 MB (189040375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b31d408143407e3080adcd8ab9297540ecdefe8335946f3eae8d5588b59fcd`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-bookworm`

```console
$ docker pull julia@sha256:ead6152a885d859cf83d3ba7194be4e4f07bbe63b83a140d28e42e1ff6b5e656
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

### `julia:1.10.7-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:edd8de6510b41380651a0cfce22b95b35c4da74184b445c72403d79a61128e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209820793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4b22e31d70c27cdbc9b37d5cb06473a0aa44220fa11776bbbe8ed773f5500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f28404f369a710bab9a7c8388f492515011cc9095e9c3e12e849397abb5f4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 5.7 MB (5713137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d950c86f350d07745d0403dfd6e7416bf0d520f5bb22e57a8127ee78f3689884`  
		Last Modified: Tue, 14 Jan 2025 02:20:47 GMT  
		Size: 175.9 MB (175894869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6dc88d3be5f4199dc8c192ce0db757a06af315119d62918deb33b1b735cd84`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:83649d9658dc29386ea551f5b6a26e4a4f881e72b84af153c9de225516dce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cceb6560d44190fbd71209922e92d21aa460129b81be0851c3eddba013f46db3`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd313d1adc26214152571b6a8361b2f047de3fbaca2fdd643fa596075ac75d`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687f2e415413015322e2ae1220790502438bbf0a4b55874f0913fd2d7e4960a4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f6af94e92c3d6347eab43aadb000bb521875ef99e5ec82de1aaf5521b1016144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211231308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d97223e860c940f4d8d1a4a061e40dd6985221472e191b52817510ea2cbdde3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c08dd08bd17849cf22675ca0243c698c6fe4b01fabf6a3c3d073ef52292bc`  
		Last Modified: Tue, 14 Jan 2025 03:06:10 GMT  
		Size: 177.7 MB (177651878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add6f4e4175dd49db2bde47c474a365f589850c500efe8b17e48ed1535cd756`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:98dc2724dd034ffa94dd1f0f51581ac92581d5494d620beedfd99159873e59cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5079d2214bbd30e0b479a0e06e399a978371ce527844283919e1810d5821f`

```dockerfile
```

-	Layers:
	-	`sha256:584938e17917b487f9f2c8b8c1c4698fd5a185b74a5efd7396891594cdeddb5e`  
		Last Modified: Tue, 14 Jan 2025 03:06:06 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58528a32f89e6930ab0f01a38d3579676a8c42a3c1de8037d4691f810c72e23d`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:a225d5ce3452efef8a6a3c7b3128752f37432714f470939463dd9bfd85025b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192844952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9966ac739b39d1a45e05398b35cfbdf47a58d4b97757c26b4c312ab20ba21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacadf125ebfe614f9d429c8b5bdf6d0d903c4df91e2da95d4132ce3c3a82e2`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 5.9 MB (5872050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dba39a827ee7f55656de9c241021310212ca40705cd8f8c9bec6c14d9880c7`  
		Last Modified: Tue, 14 Jan 2025 02:32:01 GMT  
		Size: 157.8 MB (157784935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388237bea775ed66dc6f643bb7d0c724ec9defae5550008ac32ad5e0d2e7ca22`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b0b3fbabded9d034923cc5379cb00d41b9b80829dba5100bcb7524115879ea3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274e9ccf1d8fb36d5d92f737c19bff89fdcba539fa03dd899174db0d5039333`

```dockerfile
```

-	Layers:
	-	`sha256:cde977fe1eb34823bbb2bb31c87ddd7596095cdc36d134a6fc3f862b1eee9aef`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea311a8209b26d03597c5b41d6fda1ee44775d18c496c8acdad213c081e776a`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:417e5fc281dfa44fc541d6df19d69af1c650dc06aaa978e25360cfb85f3351b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3f23264d7289f18ce257bee838033b1a6a2a4b70f0f5311791be9606346526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5a111a086bbf1d30ef24a905695854d18360157ff9692f11169c90ccc428e`  
		Last Modified: Tue, 14 Jan 2025 02:59:02 GMT  
		Size: 155.5 MB (155493289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4d0b667db150b41b9760574e56cdd03830247e5c902dcfc7a95b1cf9e8c0c`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9858b4a4e5491fda48000243dcbe4017e8e5456af0147070065871ee8e1dddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2e3bd039358880b6e19c014c81ccb9785636c895bcfc85489dcb6189d0bc2f`

```dockerfile
```

-	Layers:
	-	`sha256:85ff17fb46e315f1e821f7e0f86f3c00a6f80fb0320db89cb4eb6402f5b194de`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13be94c786bf7ce3dbe980dc608d497c828bda708eb0849cb3ef08c0ca18eabe`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.7-bullseye`

```console
$ docker pull julia@sha256:a643b586fe3237aa1e3b85b8498eb71780a62dd93e802f026325162f3053fbbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.7-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:aac9a837df906922a4340a6c00a7b79df61544569823530b35ce1e5f097559e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3037480c5ee98533eb0b15669864b9e843a8acc2ebc67c9ca4f204ac0198968f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d55b5df03cc04376fb0a788be2fb725f972110e022d592477a1ccad2788538b`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 2.2 MB (2222645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b9988d5edf1d2e245b240c8fe1c9ec8fecd839e593d09e1508db59e8ce950`  
		Last Modified: Tue, 14 Jan 2025 02:20:51 GMT  
		Size: 175.9 MB (175895657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb0a37975db8025f32e81a3e717b83a2405bcfce346ab98530668b7c85ebabb`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:294c6b5db1c4d27b0997b89aa867b06eb6964c2456b7401a1c923ca4b0c9b80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b88bf9d073694ea233e45e582239affd9f857b529c405b553be16b46ba8751`

```dockerfile
```

-	Layers:
	-	`sha256:74a7be86fe063c42ab0f5b1ecc059825edd73dcd2bb029add233636087ae5e29`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb04cca202779d02693c8339cec1cfea3c49817dcea8b88143d2b2c3e8fce28`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8c730d262ba8e00edc305a153b344806c0d8cb625df5af427aac0cef4b179391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208607436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0673c51f1f055362811b1b709c816c4c8fd481f983dc3c16f6395b8e52af9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ba9e296c53b7e882a6fba6d9ff8c72398e380d38de500e5effd7f2fb92285`  
		Last Modified: Tue, 14 Jan 2025 03:04:51 GMT  
		Size: 2.2 MB (2210283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd0a2d27d92a61bc9a4ead6261c01be9335fe3104de9ffb57614fa832f2ccc1`  
		Last Modified: Tue, 14 Jan 2025 03:07:06 GMT  
		Size: 177.7 MB (177651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f07fffbea1c39ed3847dbd063891bbe6e87b7f6bfc71269a488d73d5adc93d`  
		Last Modified: Tue, 14 Jan 2025 03:07:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:49afea0e98166811c93be8a8e28c44f8d3849e9bc65080c98d0f85bf6e2faa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685f782e1c3ae70ab6f35994ac0437e77772d0bd357524ebdf0a3eee07d58fb3`

```dockerfile
```

-	Layers:
	-	`sha256:1ec5482662762f70d5b53a0c5639dd9b6d8e3363d3e68876b460a5689d00a429`  
		Last Modified: Tue, 14 Jan 2025 03:07:02 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d6f3d22d160c355da4ce15c196eb2df5baf6707b314e07d1c4cc6c07480e15`  
		Last Modified: Tue, 14 Jan 2025 03:07:01 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bullseye` - linux; 386

```console
$ docker pull julia@sha256:170c925a9da9a0b982fc2c4d9aaaa503624e5562f0aead115f347320f411eac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191292320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0beebdd84b2fc10ea9226ce9826470f3f72a62023bc87a3d64abe5bb9db52011`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e879f31fb96b43e23c3e054f0820123765b412dc66530af4ad3588c9b5bf44e1`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 2.3 MB (2328064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec88cc224c3977de0a32d85d327e7840466c5b64ab35971ff90e47ae28d715b`  
		Last Modified: Tue, 14 Jan 2025 02:16:32 GMT  
		Size: 157.8 MB (157784860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47442c6195b93bb9d7b49a40f8c450fc0900ff87d96030a583287dec9607b031`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:adec2665c7cf2c7300b1ea7fc3405d27c93287d1673b4ca039fe10abb2ce402f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8112c94bd75b90229d93506219da7ca4c57d6cb71bec263d46f0eaa04a98e25c`

```dockerfile
```

-	Layers:
	-	`sha256:c216fd2acccb7d7dbf197f9e689c2a26613942aff7862c8e2030ae22caa15bd4`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3819793522831161986b2a33da4bbce69a029175059ca1ca5691cb9ed760462f`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.7-windowsservercore`

```console
$ docker pull julia@sha256:43c4b3f7abe069b59b950c7608d707c86b2b7dc49d41eba988edcaec35dcfaf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10.7-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:a49c2e75d3b371cf365addacc687c8f71f48dadcf03c9417bb8ee67229e7ca0d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2689440632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63cd7f4c35b1688492bda75f3f774ab8070e64021a57fba4b03c3c8a5a5f4ed`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 22 Jan 2025 20:35:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:32 GMT
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
	-	`sha256:3007cf6a11b7dd6200c77c3ba581f7d0bcb2142d09555d188e0d4b408a775062`  
		Last Modified: Wed, 22 Jan 2025 20:35:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b05fc45dd54af8121cf0f84844135533e77d53ce2d81d53da183218518d1cb0`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856feb4ecc2fd57104f241da3561d75b3b62e02f35ed98599c4b3be6b997d3a`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd68166947a4f28cff1eb750cbd1065d824a4e0b70ff0955961806b2cd840457`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79733bd4f2a9afdf53927a7f517bad453db219dd8722463858c9d327958637`  
		Last Modified: Wed, 22 Jan 2025 20:36:01 GMT  
		Size: 189.2 MB (189156558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5953b7295844933e2b861a3a55daf37c8e95b376af626f43d8b9f136b8778`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:9725e412b84cb38042b4013e7a056b2daf6d880b037fcd14965bed67b3f9fca8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451487149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9581f75e8ebcb81fb80ca69f19fae9a9d3cba24297811fbf6605bb3051e4e5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:35:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:35:36 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:35:37 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:35:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:36:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:36:23 GMT
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
	-	`sha256:4376861050dccc91b670adcf4ea779d0ac5942bc0e40e981bfa60102ed4b6066`  
		Last Modified: Tue, 14 Jan 2025 23:36:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49b5b2742734144c11e2b0183f6e93aecef6c6f8f302af11cbfbcfa73d2ba2`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0058a655cba8bb06901b06673ec5728cdd68a4cbc91dc4cf6643de0da477389`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b05eb59373c24387e468f02f222ae3c6f8ea335bacf5df1ebf8103da13f385`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6f7eeaccdd2f57b8ca7feecc04669f8cfe027ea01838b781d05ac162fb72e`  
		Last Modified: Tue, 14 Jan 2025 23:36:50 GMT  
		Size: 189.1 MB (189095478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd82d3d1bccdc4e95a36020c73253edf3b58397496e676cb4ee1f478f5a4f0c`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:39c597e14765afb9afaad442cf37f84facf986848a8c3f9fd6dc8fb5dfe921c9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa61517f629e100c2ce136d7f909fe623ab16fd582cce12a390a2b44ec8b0b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:32:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:07 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:33:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:30 GMT
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
	-	`sha256:e9179ebee2d8b696550cd1af0779cb6936a65338055936b0ae6bfbd1d47346ea`  
		Last Modified: Tue, 14 Jan 2025 23:33:36 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff628f0c6f11e0896cdd9dbd1c81bc68e167ebd51da0faeeaeac535cdcbc8a8b`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adce5640202f2c8ed4b8e27252b3f03eaf562e21c7f7ddf6130c527c9d780e2`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb00945cf018f301a8fa7c8cd45077acb611bace824b24a2259fae3b79c28dd`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b617a719f9f109e838d31694141d200694e7923e96dc770aaa48c62e3954dad`  
		Last Modified: Tue, 14 Jan 2025 23:33:58 GMT  
		Size: 189.0 MB (189040375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b31d408143407e3080adcd8ab9297540ecdefe8335946f3eae8d5588b59fcd`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-windowsservercore-1809`

```console
$ docker pull julia@sha256:0f92c7ddbed506140a9175ad5f84b94a1bdd8fce024dac2486cf494c3d798c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `julia:1.10.7-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull julia@sha256:39c597e14765afb9afaad442cf37f84facf986848a8c3f9fd6dc8fb5dfe921c9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa61517f629e100c2ce136d7f909fe623ab16fd582cce12a390a2b44ec8b0b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:32:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:07 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:32:08 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:33:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:30 GMT
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
	-	`sha256:e9179ebee2d8b696550cd1af0779cb6936a65338055936b0ae6bfbd1d47346ea`  
		Last Modified: Tue, 14 Jan 2025 23:33:36 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff628f0c6f11e0896cdd9dbd1c81bc68e167ebd51da0faeeaeac535cdcbc8a8b`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adce5640202f2c8ed4b8e27252b3f03eaf562e21c7f7ddf6130c527c9d780e2`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb00945cf018f301a8fa7c8cd45077acb611bace824b24a2259fae3b79c28dd`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b617a719f9f109e838d31694141d200694e7923e96dc770aaa48c62e3954dad`  
		Last Modified: Tue, 14 Jan 2025 23:33:58 GMT  
		Size: 189.0 MB (189040375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b31d408143407e3080adcd8ab9297540ecdefe8335946f3eae8d5588b59fcd`  
		Last Modified: Tue, 14 Jan 2025 23:33:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:89fd65f5d44cf58047eef192f5799c49a959f4080ff139a7a465a53563e5c2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:1.10.7-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:9725e412b84cb38042b4013e7a056b2daf6d880b037fcd14965bed67b3f9fca8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451487149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9581f75e8ebcb81fb80ca69f19fae9a9d3cba24297811fbf6605bb3051e4e5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:35:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:35:36 GMT
ENV JULIA_VERSION=1.10.7
# Tue, 14 Jan 2025 23:35:37 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Tue, 14 Jan 2025 23:35:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Tue, 14 Jan 2025 23:36:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:36:23 GMT
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
	-	`sha256:4376861050dccc91b670adcf4ea779d0ac5942bc0e40e981bfa60102ed4b6066`  
		Last Modified: Tue, 14 Jan 2025 23:36:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49b5b2742734144c11e2b0183f6e93aecef6c6f8f302af11cbfbcfa73d2ba2`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0058a655cba8bb06901b06673ec5728cdd68a4cbc91dc4cf6643de0da477389`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b05eb59373c24387e468f02f222ae3c6f8ea335bacf5df1ebf8103da13f385`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6f7eeaccdd2f57b8ca7feecc04669f8cfe027ea01838b781d05ac162fb72e`  
		Last Modified: Tue, 14 Jan 2025 23:36:50 GMT  
		Size: 189.1 MB (189095478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd82d3d1bccdc4e95a36020c73253edf3b58397496e676cb4ee1f478f5a4f0c`  
		Last Modified: Tue, 14 Jan 2025 23:36:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:04b41d1b15ace47526fb384f03b13ded0d1733384d1c9d4abb0c60445a5dbacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `julia:1.10.7-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull julia@sha256:a49c2e75d3b371cf365addacc687c8f71f48dadcf03c9417bb8ee67229e7ca0d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2689440632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63cd7f4c35b1688492bda75f3f774ab8070e64021a57fba4b03c3c8a5a5f4ed`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:34:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 22 Jan 2025 20:34:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 22 Jan 2025 20:34:51 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 22 Jan 2025 20:35:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:32 GMT
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
	-	`sha256:3007cf6a11b7dd6200c77c3ba581f7d0bcb2142d09555d188e0d4b408a775062`  
		Last Modified: Wed, 22 Jan 2025 20:35:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b05fc45dd54af8121cf0f84844135533e77d53ce2d81d53da183218518d1cb0`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856feb4ecc2fd57104f241da3561d75b3b62e02f35ed98599c4b3be6b997d3a`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd68166947a4f28cff1eb750cbd1065d824a4e0b70ff0955961806b2cd840457`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79733bd4f2a9afdf53927a7f517bad453db219dd8722463858c9d327958637`  
		Last Modified: Wed, 22 Jan 2025 20:36:01 GMT  
		Size: 189.2 MB (189156558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5953b7295844933e2b861a3a55daf37c8e95b376af626f43d8b9f136b8778`  
		Last Modified: Wed, 22 Jan 2025 20:35:34 GMT  
		Size: 1.3 KB (1288 bytes)  
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
