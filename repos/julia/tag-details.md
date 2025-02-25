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
$ docker pull julia@sha256:2cedc072424d2e6795c432f1c921cedf720f8895a898fe9284f408edd5daf096
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
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:21a2f31eb0afbc61cf00e8832cf9878fde336806c09d6037e369c449e41adb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302237946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667dd69b841cc680d1fd298e989ee1f12ecfb8bc58765ff2c7762470f452a8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ad764b6536afc32f7f6c07197f1524fe7d510ac76409bb60db3f450e08be6`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 5.7 MB (5713132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784588307487c202b864f398d3d71a71d26dcbdac4e31de50e99316494360644`  
		Last Modified: Tue, 25 Feb 2025 02:16:53 GMT  
		Size: 268.3 MB (268305141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f9e2b0fd2ceac4ac0c0f47405cef6bfa98f1ffde76e9b7b3d07973c3e6cdb`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:627eba988065767ad312f4f0627101b8223db458658d2be445f01ca95493cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f2f07b04a978ddfaf53f31aeaf3b5d81ba78ba106a2f94bca9dbfb04d3ee5a`

```dockerfile
```

-	Layers:
	-	`sha256:6138b3281398d6e38371d01eddb44415b8a78272a30a180cdfa4fbb0be3ce544`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.4 MB (2445456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0463451a38f357fc3ef05f31df155094dc72292b62c28fd5e43fa52ae679be6c`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:aba40bb6b6c686ca62e6a4bdc597818e26a2b3529bbd1fa95f737dda7b8527d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317521098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f8f8f99d3b28dfcd057d40f3316092eb744bf6891ab7a48a657878bd3ac65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f4963ec0f4ec9a964e744c494d8c0524ff01b292fd232727fb76b699ff0c0`  
		Last Modified: Tue, 25 Feb 2025 02:53:17 GMT  
		Size: 283.9 MB (283934209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dbedf45b8961bfd5c3753b651c3ae061b06d4f133b8f886a78fd9dd79b5c`  
		Last Modified: Tue, 25 Feb 2025 02:53:10 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:becf6fa65f281f5d60ae19863c5ace12f2e6d888441eb8817ddbbcb427f6cdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7846b68e7aadd64609368e927baaf73fa83d821d6dbcdbb5a420954805762a6`

```dockerfile
```

-	Layers:
	-	`sha256:868cc353399b91966b6a4f6e2df3c47a99a77c2864ababbcaf298ebb960c7990`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 2.4 MB (2445779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3988a1ba379532da23400b9280a68fdb69fbccf28d299778b159d09c49a6190`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:acd6e3dc9e639a6fafff6353a7298ffbca88ac410169dccf8699ca161cf29581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252982209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c4041fd0170c99549d59fa33bbf28dda58589890fed8f50ce88a8140bae95d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213e1b09c8d081c075b1cbe4f6add0244567064c4ba15857e80f28318f989a0`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 5.9 MB (5872055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff72f08d516ff6915525f10dad0fdbec7a7a81d5c94baae581e8056e7ce68ff`  
		Last Modified: Tue, 25 Feb 2025 02:12:38 GMT  
		Size: 217.9 MB (217915195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70511d5c6ee7fb9b97489e07f00ead0a1e758360f4c850a3e22aefa13ac0b99f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:8705454a0ddce89dd8f3e87b1572e377290f0561de1c05f05dbbcd98221ccc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc8d8d55e0e44f92e2bcc1340e62bf647dd44fb0826f6fbf46fb8d5b72e81d`

```dockerfile
```

-	Layers:
	-	`sha256:7b06096cc360b390c1325226d4c138b5d3c994f0c87aabcf0ba95feb3ebd0030`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 2.4 MB (2442529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fed0d72a11007583f709d303cf78d3f5b894522f2aaf2d946fd1e130fa7e8f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; ppc64le

```console
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
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

### `julia:1` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:7e62d80dc9847456c44e7c7205e79d4eff5d807417ca391390b5d21eca40a485
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
$ docker pull julia@sha256:21a2f31eb0afbc61cf00e8832cf9878fde336806c09d6037e369c449e41adb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302237946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667dd69b841cc680d1fd298e989ee1f12ecfb8bc58765ff2c7762470f452a8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ad764b6536afc32f7f6c07197f1524fe7d510ac76409bb60db3f450e08be6`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 5.7 MB (5713132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784588307487c202b864f398d3d71a71d26dcbdac4e31de50e99316494360644`  
		Last Modified: Tue, 25 Feb 2025 02:16:53 GMT  
		Size: 268.3 MB (268305141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f9e2b0fd2ceac4ac0c0f47405cef6bfa98f1ffde76e9b7b3d07973c3e6cdb`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:627eba988065767ad312f4f0627101b8223db458658d2be445f01ca95493cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f2f07b04a978ddfaf53f31aeaf3b5d81ba78ba106a2f94bca9dbfb04d3ee5a`

```dockerfile
```

-	Layers:
	-	`sha256:6138b3281398d6e38371d01eddb44415b8a78272a30a180cdfa4fbb0be3ce544`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.4 MB (2445456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0463451a38f357fc3ef05f31df155094dc72292b62c28fd5e43fa52ae679be6c`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:aba40bb6b6c686ca62e6a4bdc597818e26a2b3529bbd1fa95f737dda7b8527d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317521098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f8f8f99d3b28dfcd057d40f3316092eb744bf6891ab7a48a657878bd3ac65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f4963ec0f4ec9a964e744c494d8c0524ff01b292fd232727fb76b699ff0c0`  
		Last Modified: Tue, 25 Feb 2025 02:53:17 GMT  
		Size: 283.9 MB (283934209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dbedf45b8961bfd5c3753b651c3ae061b06d4f133b8f886a78fd9dd79b5c`  
		Last Modified: Tue, 25 Feb 2025 02:53:10 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:becf6fa65f281f5d60ae19863c5ace12f2e6d888441eb8817ddbbcb427f6cdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7846b68e7aadd64609368e927baaf73fa83d821d6dbcdbb5a420954805762a6`

```dockerfile
```

-	Layers:
	-	`sha256:868cc353399b91966b6a4f6e2df3c47a99a77c2864ababbcaf298ebb960c7990`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 2.4 MB (2445779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3988a1ba379532da23400b9280a68fdb69fbccf28d299778b159d09c49a6190`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:acd6e3dc9e639a6fafff6353a7298ffbca88ac410169dccf8699ca161cf29581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252982209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c4041fd0170c99549d59fa33bbf28dda58589890fed8f50ce88a8140bae95d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213e1b09c8d081c075b1cbe4f6add0244567064c4ba15857e80f28318f989a0`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 5.9 MB (5872055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff72f08d516ff6915525f10dad0fdbec7a7a81d5c94baae581e8056e7ce68ff`  
		Last Modified: Tue, 25 Feb 2025 02:12:38 GMT  
		Size: 217.9 MB (217915195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70511d5c6ee7fb9b97489e07f00ead0a1e758360f4c850a3e22aefa13ac0b99f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8705454a0ddce89dd8f3e87b1572e377290f0561de1c05f05dbbcd98221ccc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc8d8d55e0e44f92e2bcc1340e62bf647dd44fb0826f6fbf46fb8d5b72e81d`

```dockerfile
```

-	Layers:
	-	`sha256:7b06096cc360b390c1325226d4c138b5d3c994f0c87aabcf0ba95feb3ebd0030`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 2.4 MB (2442529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fed0d72a11007583f709d303cf78d3f5b894522f2aaf2d946fd1e130fa7e8f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:11d4d97486a98c0125980155216f5fdc457742b0d0134dee9bab3823c7e52143
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
$ docker pull julia@sha256:e64d13743fef5bee538747ac3ca5a753da245fab00666b43738a2140f182a804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300782132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b1e593902167844e0f8c6ad5487957aa3b121e642611ed59b8840b765362fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcafc09016b343666a8d68e276afa1cd649c2dcf4eec976831223671bf3f7e8`  
		Last Modified: Tue, 25 Feb 2025 02:16:45 GMT  
		Size: 2.2 MB (2222692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86f9ade150a6fd38f241687982dc0eaba6f0951421a079c9c42a134fbb83e5`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 268.3 MB (268305139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5427fcc0a2762fab1cb70aadcb7bf1e60a558695210a462de23cf98636c08bf6`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b1bc4430f3d8b56636729de4d562ea52fdc12c800bc0e28a5b395cad99541146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c60387f29f351dcfab4553ddbec1fbd49b3245a25fb77033a62be4d118387a`

```dockerfile
```

-	Layers:
	-	`sha256:ce2fde94b0f58e3b94d7978ef308c3c07130e9683bf69c105ca8c94cb9c431d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60c79f7ca801535cc5684531dd06ac4573d5398783929fbd30ac201028e12d5`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a4069520380136d9cdb2e7ecd5c66e80c69232e3868afcfca5fb5e964670dd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314892835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60765db82c102b930c3f02dcfc17102c77ff65ffe2a3187cf192b4fb0159f461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb70ac9c266fdb923eb0632b4f22d215191a2b807529efbaabd3012f5356c8f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.2 MB (2210296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bc6a668f27d84fc2ed9afcb7d5782d481f80c6866cbe938c00dfbb1bca7fb2`  
		Last Modified: Tue, 25 Feb 2025 02:54:39 GMT  
		Size: 283.9 MB (283936179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc55ee2b8200aa8c9e0df3088c6c573e2fd6b3ef73768158109da258f628f41f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8f132cd176ca26509524467c3048ab38033a7a2de40221fb97e1c6fd9cb0f233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26036101f475014f6b6687df3d6c5ab2dae8eca5a06093dd7c09e902ac79f844`

```dockerfile
```

-	Layers:
	-	`sha256:84be007fb550007647934941a06746976588afb4943c80420be20472c08c741a`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b21c55600dffaffa1b55e309eca82ac9ab44fbd7abe1c5d094a40bad6f8934f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:dd4b0775d7c3247adb5bd871c9283fd36afb17020f625c24cb605762b516c3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251423827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc774e6584b17557fc9db131bfe1340e5f28930c27c1fcbbb30b4ef6c4a1265`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1102477f498de586c7b0314598e024085d6b13f13a854c5878aa6f00bd98e9`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 2.3 MB (2328115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaa08382b40474ae5bbf8503cc0f9c0411967be2c581ffdb8a4ef81ab8e905d`  
		Last Modified: Tue, 25 Feb 2025 02:12:40 GMT  
		Size: 217.9 MB (217914915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b54104f3c6f7da984c2739dc0725a5fa9a7cda0415c2db447575b9ba62a3334`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e47cea5e39712bc87d5fef445c4966cccf8bd3e008e4475b39796fb78dc5676c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389305f43e31f8582345649842365969d4dbf5ee09f564ec99d27afe0a00fea4`

```dockerfile
```

-	Layers:
	-	`sha256:c968cf7e25787cf4f4ef6904f81afe1f5d55b29dfb92b8b9e06b0aa923199898`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3998d18c45834b1a24b7cfdc5709065142630b19ba6cf69e3a777c1c38de6600`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:0a9215fb8bff2ddae3ae14be87d1702eb1337bc3b744117af7de2d033161d716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

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

### `julia:1-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:2e7bd23cb87b2b1bd0cdcc013c54c0b618044b9750fe0527be5e012363a73f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:67a9470180bfe119828cda80614b5c765934f592f08dd030ae237136aff79352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull julia@sha256:33ec8ff98baa156ee5cc5cf80bd9eee6bea41ef249c80812bd6e0c644e03c4cc
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
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:16861b30aa44ba3014024b04d8a2d19f7d4714afc5603766247615408554cc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209692973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419d8852aabd187a4ca302441b40822ed038f26132124c51ebd6280cf1b97a96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122c4f07cddf958472ebcfefdef6e04b8ec05ab084bc17a174d2322f7f6d4dbb`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 5.7 MB (5713123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c11064192e1e6dd1a385540dec0ddf4a32495ef567fefa9946a246bd55fd22`  
		Last Modified: Tue, 25 Feb 2025 03:22:14 GMT  
		Size: 175.8 MB (175760175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596281411f81f3ae58170786cad06c187e3c33206cce78af5fb20f484c1266fd`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:91837517f7ae752dc92b578339254f5d3df7103c0ed1074282314cbd6227dc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206a90d860b87f476330b3e2df57e4eea143236e3db530d0e2846f0cc184b6`

```dockerfile
```

-	Layers:
	-	`sha256:bfd4c0287847f6e0cf0f820e520acff430a0c8dfd178aa3da7f79d326436bce9`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 2.4 MB (2445501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311413abb4d5612100c3a8f20126ac12799989b6af9eea7533138331e8b2bb92`  
		Last Modified: Tue, 25 Feb 2025 03:22:08 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:17882851585204b254730a9aa1db15b2a5683f61ebcc8a43580c2e70eb838e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210727082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f831015f384e2af9848b80098b94f9b54d97dd3e0452f7105eed561881a9b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d144f1ce3cd4d7a2c095e6ffcbe18e0b43cc306302c98af58fd0366ad441b8`  
		Last Modified: Tue, 25 Feb 2025 11:26:30 GMT  
		Size: 177.1 MB (177140194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4679683f406ac5df6a8b6ef50af68d26f2cc3dd292f4ea7f6dcf5d03d910e6`  
		Last Modified: Tue, 25 Feb 2025 11:26:24 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:584f1ec86e7e2e26c0fe9ba0640946ececb65920ff463e37328129a6aa2793d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb12d5782efdd7d0aca89c3a931f531adbf60bf0cf8a0843c4201fdd20cce10`

```dockerfile
```

-	Layers:
	-	`sha256:8bf1c62b2798a091a3fab2d7d92b25cb09f39c949b82ca6ef6ee065143500804`  
		Last Modified: Tue, 25 Feb 2025 11:26:25 GMT  
		Size: 2.4 MB (2444545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b6a59f11a6afc9e319cb5f37c24783db716ec3744f45609b3e815e67b830cf`  
		Last Modified: Tue, 25 Feb 2025 11:26:25 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:b0e1e114a631996919bf0ac8a33af67ac1c268ea1d208c7bfcf9c13cc9795bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b9531ef3d714de609e16e1d268fb99bfebd8e2604b5e31053bff704ce3715e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026ffb89d7f74c36830ec9de84b40e4d25886dfc8fbedb6fd0cd6d6d29f007d`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 5.9 MB (5872073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6684adda4e8db08dde58ecb6edcf9b83fc0893d2662d4d72da1fd0b1840165`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 157.8 MB (157801936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517f1f728c76a2ab7c2017ccbe16c5280d39563b142f511b2a27f3082da2dff4`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:cd7e3ce301f96d2c226e04f85df771fe41e4dac8ab475e2f25f4873d1bf5d709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cdd62bdd0b2173d4eb4759a98a4a029c1f12738adbac374b89acd643b4b2c1`

```dockerfile
```

-	Layers:
	-	`sha256:ac9634187f26163526cf2c7f9dca5b95bb6979c4b2a657b14f4fc1a0e98d39f5`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 2.4 MB (2442594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93388392b4150bfdbe25a2cded73353f22a6818a196480e5501c2df623e48a6`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:e2098f0ec371c8d9544d0785b5b84647f8dab8b3f6cb50dd0631a0b39c83ff0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193459312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79611a383285f249aaee725495ccb56c1ec506f6cce28c08298f315b8d22c931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a01e2350cb6f03b0da6d34b7ea67118dc4f0ee789279e0106e3e129ec4f2a1f`  
		Last Modified: Tue, 25 Feb 2025 02:36:23 GMT  
		Size: 155.2 MB (155157257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b90912e0605bcf3e5f1145012ba57e524d67ca2b53566f38bcd071077b3b7`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:193328fad219591f1ebe48951e320b0d0ef8a074417ac72447204422a27409eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353333249b3cc3ccbf35310a0be7f9799c32b0a00de6b77197647599cb085a65`

```dockerfile
```

-	Layers:
	-	`sha256:bc375cc77ef1b96e128f67a0cc769ef1ffd2fe5fd98feb3390a049962a51b3a0`  
		Last Modified: Tue, 25 Feb 2025 02:36:20 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc454e075d0910fe622f24e0c3520fb73938b551685986a865d74f5d13356a33`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 17.3 KB (17260 bytes)  
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

### `julia:1.10` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:ac79fdbb729145cb1bffbdcdac5c90f0659420b2c32a042db8e09ef5046c12ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452517945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a427a05613dcbebc39e69375a7a22c6de08dca1a906ce33785a88edddae738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:37:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:37:49 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:38:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ed8e7202322ceebbde66bd5c17e8cb63f0a63deeba0dce25ca0165af4cd94`  
		Last Modified: Thu, 13 Feb 2025 00:38:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d463e8f59a011a182e6b4e5c59ca3b24501c020944150165d7923668fff5`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691753fae6105922bbdc47180303ef3e79f0262b36268f73c2ee704321a43dc1`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cedad76f34702d30642f568d3467dc6f1f420c3fc61ac77dfe77b68af40e468`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb673a4bf380f9c6a5308a15b2a2a57b82a2d923bc93c5afab400e3c1c1b838`  
		Last Modified: Thu, 13 Feb 2025 00:39:10 GMT  
		Size: 188.7 MB (188653406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d63bac5eabd3f54a59db28184d9bad8be6ad92dd626462ad51bc06e3f662db`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:9e3801b456c24260294efa77599c44818954fa48ec8a4a6f54bb5bbf57fc538a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325517602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5322a337b2455c2f0d0235881437dfa635e05f9a936c4cb27dff5df3bbb53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:08 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:35:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8581044a74ef698a3ae34bab811faa129529027c7eb77a6b0c0754748f6055`  
		Last Modified: Thu, 13 Feb 2025 00:35:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79abe04602eb193952fd20451edc2e0c3edec25b5140860576ab8dd43434ccb`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45face97a75a56bdc0329ba85ac9adf2164e9692773043bba1e330df0a7701`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f5bde34f5706ee15891362936963912b7c2e41b557cf665abe48182cdd775b`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58967fcbfa6fea8b02512fa1441f7ec6bd92d7623897ec3c826b7185d98f15`  
		Last Modified: Thu, 13 Feb 2025 00:35:47 GMT  
		Size: 188.6 MB (188602321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ba356d441b938ba068b455cc2d082fac429a473b9dffa6f0f3eda32523be4`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:fde3a2f343281404e65e75f6e1dba2b52b43e982947599462c7942a9dada5e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:0c5a7cb3a53fddbfc5f5858565c26e687e2b7ca0955eb423fcb5eed325858a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182654555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5eed16e3a5cdd9a2d0a0616d9d07473136d56634021e44288850a3d06ba6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bc633fb744540a8186183a70c5f87975154b6482ab9c2eabcbb37325ae108d`  
		Last Modified: Fri, 14 Feb 2025 19:15:59 GMT  
		Size: 179.0 MB (179011941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c989ce9e32627332370f11e298b17b0ba8828e9d2b55f5e05848ef795dbc99`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:51b30c9c61ec38432645c4b2682a4cd0614d3b92de18bb215e109b1f2c7d20cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f38a89a779409744eadb880fd458ada92e3242a07d5244f7b3b633db07410e9`

```dockerfile
```

-	Layers:
	-	`sha256:b258d9aef98d4d8be8f1093ef84a93da1385098e6be38cdb67a2232b1a5abb1a`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 79.9 KB (79887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2231f8800e0744dad35c200ea21ea2b4fdaf2710bad565cb3f200cc92291f7`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.20`

```console
$ docker pull julia@sha256:cb3e18af01c393f335c67c206c1c03e5fc0a00fc09ea5eaa1aa717ca949f7490
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:ddd0c1ce44e345efc275a36319f0eb0e5891c9c3db58ff98ae08abfbdb78d8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182638245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d53181291492847160d2291d858cb5dd21d64dedd3f9f45d6ab0d7ac9fc946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adf9f8ee73736ece7799870a876adb5fa6e8cb7fb89586038818492e0309651`  
		Last Modified: Fri, 14 Feb 2025 19:16:42 GMT  
		Size: 179.0 MB (179010980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0db0f345ecba4900ec3b86881cd225812958cdbebb85c593ff779c1a82ba9e7`  
		Last Modified: Fri, 14 Feb 2025 19:16:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:06ae6e2e3886a47f010bd0e55e18db672fcef53e0e429da710877ca372027dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a90ef83d1183d2f8c4fc7b2960f40f8044566347689e6c7bbbb60f5634f6d9e`

```dockerfile
```

-	Layers:
	-	`sha256:e0234bb02d29a858408cb1f537668a1b6fd6a240d9c3dd7790430374b821d93c`  
		Last Modified: Fri, 14 Feb 2025 19:16:37 GMT  
		Size: 73.5 KB (73545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945797eb1de64e8c5053ba25ffe9b170fbaf889b7c3677d456b2533ca0ab8825`  
		Last Modified: Fri, 14 Feb 2025 19:16:37 GMT  
		Size: 12.0 KB (11964 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.21`

```console
$ docker pull julia@sha256:fde3a2f343281404e65e75f6e1dba2b52b43e982947599462c7942a9dada5e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:0c5a7cb3a53fddbfc5f5858565c26e687e2b7ca0955eb423fcb5eed325858a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182654555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5eed16e3a5cdd9a2d0a0616d9d07473136d56634021e44288850a3d06ba6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bc633fb744540a8186183a70c5f87975154b6482ab9c2eabcbb37325ae108d`  
		Last Modified: Fri, 14 Feb 2025 19:15:59 GMT  
		Size: 179.0 MB (179011941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c989ce9e32627332370f11e298b17b0ba8828e9d2b55f5e05848ef795dbc99`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:51b30c9c61ec38432645c4b2682a4cd0614d3b92de18bb215e109b1f2c7d20cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f38a89a779409744eadb880fd458ada92e3242a07d5244f7b3b633db07410e9`

```dockerfile
```

-	Layers:
	-	`sha256:b258d9aef98d4d8be8f1093ef84a93da1385098e6be38cdb67a2232b1a5abb1a`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 79.9 KB (79887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2231f8800e0744dad35c200ea21ea2b4fdaf2710bad565cb3f200cc92291f7`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:b550ca97387e84559a24ed9ded4006051479eae9781f53beecd2b18def37de23
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
$ docker pull julia@sha256:16861b30aa44ba3014024b04d8a2d19f7d4714afc5603766247615408554cc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209692973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419d8852aabd187a4ca302441b40822ed038f26132124c51ebd6280cf1b97a96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122c4f07cddf958472ebcfefdef6e04b8ec05ab084bc17a174d2322f7f6d4dbb`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 5.7 MB (5713123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c11064192e1e6dd1a385540dec0ddf4a32495ef567fefa9946a246bd55fd22`  
		Last Modified: Tue, 25 Feb 2025 03:22:14 GMT  
		Size: 175.8 MB (175760175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596281411f81f3ae58170786cad06c187e3c33206cce78af5fb20f484c1266fd`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:91837517f7ae752dc92b578339254f5d3df7103c0ed1074282314cbd6227dc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206a90d860b87f476330b3e2df57e4eea143236e3db530d0e2846f0cc184b6`

```dockerfile
```

-	Layers:
	-	`sha256:bfd4c0287847f6e0cf0f820e520acff430a0c8dfd178aa3da7f79d326436bce9`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 2.4 MB (2445501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311413abb4d5612100c3a8f20126ac12799989b6af9eea7533138331e8b2bb92`  
		Last Modified: Tue, 25 Feb 2025 03:22:08 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:17882851585204b254730a9aa1db15b2a5683f61ebcc8a43580c2e70eb838e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210727082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f831015f384e2af9848b80098b94f9b54d97dd3e0452f7105eed561881a9b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d144f1ce3cd4d7a2c095e6ffcbe18e0b43cc306302c98af58fd0366ad441b8`  
		Last Modified: Tue, 25 Feb 2025 11:26:30 GMT  
		Size: 177.1 MB (177140194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4679683f406ac5df6a8b6ef50af68d26f2cc3dd292f4ea7f6dcf5d03d910e6`  
		Last Modified: Tue, 25 Feb 2025 11:26:24 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:584f1ec86e7e2e26c0fe9ba0640946ececb65920ff463e37328129a6aa2793d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb12d5782efdd7d0aca89c3a931f531adbf60bf0cf8a0843c4201fdd20cce10`

```dockerfile
```

-	Layers:
	-	`sha256:8bf1c62b2798a091a3fab2d7d92b25cb09f39c949b82ca6ef6ee065143500804`  
		Last Modified: Tue, 25 Feb 2025 11:26:25 GMT  
		Size: 2.4 MB (2444545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b6a59f11a6afc9e319cb5f37c24783db716ec3744f45609b3e815e67b830cf`  
		Last Modified: Tue, 25 Feb 2025 11:26:25 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:b0e1e114a631996919bf0ac8a33af67ac1c268ea1d208c7bfcf9c13cc9795bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b9531ef3d714de609e16e1d268fb99bfebd8e2604b5e31053bff704ce3715e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026ffb89d7f74c36830ec9de84b40e4d25886dfc8fbedb6fd0cd6d6d29f007d`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 5.9 MB (5872073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6684adda4e8db08dde58ecb6edcf9b83fc0893d2662d4d72da1fd0b1840165`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 157.8 MB (157801936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517f1f728c76a2ab7c2017ccbe16c5280d39563b142f511b2a27f3082da2dff4`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:cd7e3ce301f96d2c226e04f85df771fe41e4dac8ab475e2f25f4873d1bf5d709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cdd62bdd0b2173d4eb4759a98a4a029c1f12738adbac374b89acd643b4b2c1`

```dockerfile
```

-	Layers:
	-	`sha256:ac9634187f26163526cf2c7f9dca5b95bb6979c4b2a657b14f4fc1a0e98d39f5`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 2.4 MB (2442594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93388392b4150bfdbe25a2cded73353f22a6818a196480e5501c2df623e48a6`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:e2098f0ec371c8d9544d0785b5b84647f8dab8b3f6cb50dd0631a0b39c83ff0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193459312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79611a383285f249aaee725495ccb56c1ec506f6cce28c08298f315b8d22c931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a01e2350cb6f03b0da6d34b7ea67118dc4f0ee789279e0106e3e129ec4f2a1f`  
		Last Modified: Tue, 25 Feb 2025 02:36:23 GMT  
		Size: 155.2 MB (155157257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b90912e0605bcf3e5f1145012ba57e524d67ca2b53566f38bcd071077b3b7`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:193328fad219591f1ebe48951e320b0d0ef8a074417ac72447204422a27409eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353333249b3cc3ccbf35310a0be7f9799c32b0a00de6b77197647599cb085a65`

```dockerfile
```

-	Layers:
	-	`sha256:bc375cc77ef1b96e128f67a0cc769ef1ffd2fe5fd98feb3390a049962a51b3a0`  
		Last Modified: Tue, 25 Feb 2025 02:36:20 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc454e075d0910fe622f24e0c3520fb73938b551685986a865d74f5d13356a33`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:829de4107352553a2de12ea722a39898d18351af25bab5b3caaea738c4bedc7d
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
$ docker pull julia@sha256:276b6794004a535dd48163a8dc1933831e664441b28ba05107067236f8f4eb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208237330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db77ca1b7ec38568315c3b0146aa832ffff765a03e4c01009a44b40c71254bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537cacb47ed4409781d1199ed9a486feab9b36ba9dbeec99b1799618e1d10942`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.2 MB (2222624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbbe690acbffc4d19431e54d00c0568c51820d4b04d2ba8c81a33d818b999f3`  
		Last Modified: Tue, 25 Feb 2025 02:16:50 GMT  
		Size: 175.8 MB (175760407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0432e741400db75afba85576f7b607b213c646a57b317b5642afb46e38d6712`  
		Last Modified: Tue, 25 Feb 2025 02:16:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:683fec5907071fcf53560cbb425f5881b4d6051d6c3717c8a6b96c18237eaf4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc8dd76e5b71450d263ee0fcc986d8c1c26e0dd4fe6a1f92bbe9ed02c28dfb3`

```dockerfile
```

-	Layers:
	-	`sha256:9b62610382c69b145d8503466a1175ba882dd5d572e8ac31fe510eed60728eea`  
		Last Modified: Tue, 25 Feb 2025 02:16:47 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda4f139e0afc726bf69bf32420471035a27f35f961919ad37c25ae0d0060e08`  
		Last Modified: Tue, 25 Feb 2025 02:16:47 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:712086ced6e853c1c1237571fd709c0d61a24f3db1e1c0b0db19d8bfbd96d522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208097263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faa8a68052cb6f66374c91a9e3383ee29c94430465885e9acaa343a0d434c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb70ac9c266fdb923eb0632b4f22d215191a2b807529efbaabd3012f5356c8f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.2 MB (2210296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7591cbfbfafc8b32059c36e34d09bb32473d7a4cb3d83ab5658937ee63cddb7`  
		Last Modified: Tue, 25 Feb 2025 02:55:43 GMT  
		Size: 177.1 MB (177140609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4ac6f869de3615b13054f13e26efbaa1894227d24300a85e6ead532b3e1427`  
		Last Modified: Tue, 25 Feb 2025 02:55:38 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:9573e2c7eae53de0c624cedb615c65fbfa9f79f1dc195e1079797d5440d74c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d66b48d28bdbcdf97c5609757d527ea0ef01af0a9f2d2f6ee5f9670efcfb4c1`

```dockerfile
```

-	Layers:
	-	`sha256:a3676567423bf5822fefddd02df867abdc26c0da704627cd4a9922c65ed84d44`  
		Last Modified: Tue, 25 Feb 2025 02:55:38 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bb5e265de1e0ebe13d1ce1d06404470d24164596a05c15b8166be3da0ee61b`  
		Last Modified: Tue, 25 Feb 2025 02:55:38 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:2dc670805d439e691abb7f5e843979cffd9f4f171f75a56f735a6b86d1aeefb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191310872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3d7a0bd4d350b5bd9ee20592f11c0316d67febbb19eb6f817d37f96b44ec9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54415e0560708d03cde1351310902ba116685db651be9f8648fb8269c8ac9750`  
		Last Modified: Tue, 25 Feb 2025 02:12:25 GMT  
		Size: 2.3 MB (2328129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0f7f50bfc8dafda6641dead3c5c5ece290d547e97f111d627ec33c4c2d8373`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 157.8 MB (157801945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef06be5a3288a740c1eac59f8de63ea0dc568c07d261cefeb681856063950f00`  
		Last Modified: Tue, 25 Feb 2025 02:12:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:ace80bafa2c33ef8f49a15d416312fd68ea1f58627cbe948200f3d30fc9c7a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52e24068a9e8ada4180d882e6d723d8496307d27c9f73f9deda4c249a4f7afd`

```dockerfile
```

-	Layers:
	-	`sha256:4e3f88279f03e8dceb4431ded41237ebd7a6db853184babf7653217f9f7e299b`  
		Last Modified: Tue, 25 Feb 2025 02:12:25 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87088a5b696817f43d1d80674f6bb6d75193a02def23ccfbb93f8c5bdbee66ed`  
		Last Modified: Tue, 25 Feb 2025 02:12:25 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:e10d0d02a66fe615e86959d560acbd0a87159fe6a7c4866135ac7c3c6b8846a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

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

### `julia:1.10-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:ac79fdbb729145cb1bffbdcdac5c90f0659420b2c32a042db8e09ef5046c12ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452517945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a427a05613dcbebc39e69375a7a22c6de08dca1a906ce33785a88edddae738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:37:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:37:49 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:38:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ed8e7202322ceebbde66bd5c17e8cb63f0a63deeba0dce25ca0165af4cd94`  
		Last Modified: Thu, 13 Feb 2025 00:38:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d463e8f59a011a182e6b4e5c59ca3b24501c020944150165d7923668fff5`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691753fae6105922bbdc47180303ef3e79f0262b36268f73c2ee704321a43dc1`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cedad76f34702d30642f568d3467dc6f1f420c3fc61ac77dfe77b68af40e468`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb673a4bf380f9c6a5308a15b2a2a57b82a2d923bc93c5afab400e3c1c1b838`  
		Last Modified: Thu, 13 Feb 2025 00:39:10 GMT  
		Size: 188.7 MB (188653406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d63bac5eabd3f54a59db28184d9bad8be6ad92dd626462ad51bc06e3f662db`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:9e3801b456c24260294efa77599c44818954fa48ec8a4a6f54bb5bbf57fc538a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325517602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5322a337b2455c2f0d0235881437dfa635e05f9a936c4cb27dff5df3bbb53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:08 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:35:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8581044a74ef698a3ae34bab811faa129529027c7eb77a6b0c0754748f6055`  
		Last Modified: Thu, 13 Feb 2025 00:35:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79abe04602eb193952fd20451edc2e0c3edec25b5140860576ab8dd43434ccb`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45face97a75a56bdc0329ba85ac9adf2164e9692773043bba1e330df0a7701`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f5bde34f5706ee15891362936963912b7c2e41b557cf665abe48182cdd775b`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58967fcbfa6fea8b02512fa1441f7ec6bd92d7623897ec3c826b7185d98f15`  
		Last Modified: Thu, 13 Feb 2025 00:35:47 GMT  
		Size: 188.6 MB (188602321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ba356d441b938ba068b455cc2d082fac429a473b9dffa6f0f3eda32523be4`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:507c37ca88e0d966becafe997ce6dc105fa3cfa7c09182b23bf1f2ff3898c1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:9e3801b456c24260294efa77599c44818954fa48ec8a4a6f54bb5bbf57fc538a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325517602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5322a337b2455c2f0d0235881437dfa635e05f9a936c4cb27dff5df3bbb53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:08 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:35:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8581044a74ef698a3ae34bab811faa129529027c7eb77a6b0c0754748f6055`  
		Last Modified: Thu, 13 Feb 2025 00:35:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79abe04602eb193952fd20451edc2e0c3edec25b5140860576ab8dd43434ccb`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45face97a75a56bdc0329ba85ac9adf2164e9692773043bba1e330df0a7701`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f5bde34f5706ee15891362936963912b7c2e41b557cf665abe48182cdd775b`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58967fcbfa6fea8b02512fa1441f7ec6bd92d7623897ec3c826b7185d98f15`  
		Last Modified: Thu, 13 Feb 2025 00:35:47 GMT  
		Size: 188.6 MB (188602321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ba356d441b938ba068b455cc2d082fac429a473b9dffa6f0f3eda32523be4`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:6ea0f734de4588ffd1d83678be1e21a39d6af7576cf876e5426c51c900b2c72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:ac79fdbb729145cb1bffbdcdac5c90f0659420b2c32a042db8e09ef5046c12ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452517945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a427a05613dcbebc39e69375a7a22c6de08dca1a906ce33785a88edddae738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:37:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:37:49 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:38:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ed8e7202322ceebbde66bd5c17e8cb63f0a63deeba0dce25ca0165af4cd94`  
		Last Modified: Thu, 13 Feb 2025 00:38:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d463e8f59a011a182e6b4e5c59ca3b24501c020944150165d7923668fff5`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691753fae6105922bbdc47180303ef3e79f0262b36268f73c2ee704321a43dc1`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cedad76f34702d30642f568d3467dc6f1f420c3fc61ac77dfe77b68af40e468`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb673a4bf380f9c6a5308a15b2a2a57b82a2d923bc93c5afab400e3c1c1b838`  
		Last Modified: Thu, 13 Feb 2025 00:39:10 GMT  
		Size: 188.7 MB (188653406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d63bac5eabd3f54a59db28184d9bad8be6ad92dd626462ad51bc06e3f662db`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1288 bytes)  
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
$ docker pull julia@sha256:33ec8ff98baa156ee5cc5cf80bd9eee6bea41ef249c80812bd6e0c644e03c4cc
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
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10.8` - linux; amd64

```console
$ docker pull julia@sha256:16861b30aa44ba3014024b04d8a2d19f7d4714afc5603766247615408554cc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209692973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419d8852aabd187a4ca302441b40822ed038f26132124c51ebd6280cf1b97a96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122c4f07cddf958472ebcfefdef6e04b8ec05ab084bc17a174d2322f7f6d4dbb`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 5.7 MB (5713123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c11064192e1e6dd1a385540dec0ddf4a32495ef567fefa9946a246bd55fd22`  
		Last Modified: Tue, 25 Feb 2025 03:22:14 GMT  
		Size: 175.8 MB (175760175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596281411f81f3ae58170786cad06c187e3c33206cce78af5fb20f484c1266fd`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8` - unknown; unknown

```console
$ docker pull julia@sha256:91837517f7ae752dc92b578339254f5d3df7103c0ed1074282314cbd6227dc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206a90d860b87f476330b3e2df57e4eea143236e3db530d0e2846f0cc184b6`

```dockerfile
```

-	Layers:
	-	`sha256:bfd4c0287847f6e0cf0f820e520acff430a0c8dfd178aa3da7f79d326436bce9`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 2.4 MB (2445501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311413abb4d5612100c3a8f20126ac12799989b6af9eea7533138331e8b2bb92`  
		Last Modified: Tue, 25 Feb 2025 03:22:08 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:17882851585204b254730a9aa1db15b2a5683f61ebcc8a43580c2e70eb838e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210727082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f831015f384e2af9848b80098b94f9b54d97dd3e0452f7105eed561881a9b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d144f1ce3cd4d7a2c095e6ffcbe18e0b43cc306302c98af58fd0366ad441b8`  
		Last Modified: Tue, 25 Feb 2025 11:26:30 GMT  
		Size: 177.1 MB (177140194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4679683f406ac5df6a8b6ef50af68d26f2cc3dd292f4ea7f6dcf5d03d910e6`  
		Last Modified: Tue, 25 Feb 2025 11:26:24 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8` - unknown; unknown

```console
$ docker pull julia@sha256:584f1ec86e7e2e26c0fe9ba0640946ececb65920ff463e37328129a6aa2793d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb12d5782efdd7d0aca89c3a931f531adbf60bf0cf8a0843c4201fdd20cce10`

```dockerfile
```

-	Layers:
	-	`sha256:8bf1c62b2798a091a3fab2d7d92b25cb09f39c949b82ca6ef6ee065143500804`  
		Last Modified: Tue, 25 Feb 2025 11:26:25 GMT  
		Size: 2.4 MB (2444545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b6a59f11a6afc9e319cb5f37c24783db716ec3744f45609b3e815e67b830cf`  
		Last Modified: Tue, 25 Feb 2025 11:26:25 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8` - linux; 386

```console
$ docker pull julia@sha256:b0e1e114a631996919bf0ac8a33af67ac1c268ea1d208c7bfcf9c13cc9795bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b9531ef3d714de609e16e1d268fb99bfebd8e2604b5e31053bff704ce3715e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026ffb89d7f74c36830ec9de84b40e4d25886dfc8fbedb6fd0cd6d6d29f007d`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 5.9 MB (5872073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6684adda4e8db08dde58ecb6edcf9b83fc0893d2662d4d72da1fd0b1840165`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 157.8 MB (157801936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517f1f728c76a2ab7c2017ccbe16c5280d39563b142f511b2a27f3082da2dff4`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8` - unknown; unknown

```console
$ docker pull julia@sha256:cd7e3ce301f96d2c226e04f85df771fe41e4dac8ab475e2f25f4873d1bf5d709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cdd62bdd0b2173d4eb4759a98a4a029c1f12738adbac374b89acd643b4b2c1`

```dockerfile
```

-	Layers:
	-	`sha256:ac9634187f26163526cf2c7f9dca5b95bb6979c4b2a657b14f4fc1a0e98d39f5`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 2.4 MB (2442594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93388392b4150bfdbe25a2cded73353f22a6818a196480e5501c2df623e48a6`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8` - linux; ppc64le

```console
$ docker pull julia@sha256:e2098f0ec371c8d9544d0785b5b84647f8dab8b3f6cb50dd0631a0b39c83ff0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193459312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79611a383285f249aaee725495ccb56c1ec506f6cce28c08298f315b8d22c931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a01e2350cb6f03b0da6d34b7ea67118dc4f0ee789279e0106e3e129ec4f2a1f`  
		Last Modified: Tue, 25 Feb 2025 02:36:23 GMT  
		Size: 155.2 MB (155157257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b90912e0605bcf3e5f1145012ba57e524d67ca2b53566f38bcd071077b3b7`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8` - unknown; unknown

```console
$ docker pull julia@sha256:193328fad219591f1ebe48951e320b0d0ef8a074417ac72447204422a27409eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353333249b3cc3ccbf35310a0be7f9799c32b0a00de6b77197647599cb085a65`

```dockerfile
```

-	Layers:
	-	`sha256:bc375cc77ef1b96e128f67a0cc769ef1ffd2fe5fd98feb3390a049962a51b3a0`  
		Last Modified: Tue, 25 Feb 2025 02:36:20 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc454e075d0910fe622f24e0c3520fb73938b551685986a865d74f5d13356a33`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 17.3 KB (17260 bytes)  
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

### `julia:1.10.8` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:ac79fdbb729145cb1bffbdcdac5c90f0659420b2c32a042db8e09ef5046c12ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452517945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a427a05613dcbebc39e69375a7a22c6de08dca1a906ce33785a88edddae738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:37:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:37:49 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:38:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ed8e7202322ceebbde66bd5c17e8cb63f0a63deeba0dce25ca0165af4cd94`  
		Last Modified: Thu, 13 Feb 2025 00:38:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d463e8f59a011a182e6b4e5c59ca3b24501c020944150165d7923668fff5`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691753fae6105922bbdc47180303ef3e79f0262b36268f73c2ee704321a43dc1`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cedad76f34702d30642f568d3467dc6f1f420c3fc61ac77dfe77b68af40e468`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb673a4bf380f9c6a5308a15b2a2a57b82a2d923bc93c5afab400e3c1c1b838`  
		Last Modified: Thu, 13 Feb 2025 00:39:10 GMT  
		Size: 188.7 MB (188653406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d63bac5eabd3f54a59db28184d9bad8be6ad92dd626462ad51bc06e3f662db`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.8` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:9e3801b456c24260294efa77599c44818954fa48ec8a4a6f54bb5bbf57fc538a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325517602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5322a337b2455c2f0d0235881437dfa635e05f9a936c4cb27dff5df3bbb53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:08 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:35:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8581044a74ef698a3ae34bab811faa129529027c7eb77a6b0c0754748f6055`  
		Last Modified: Thu, 13 Feb 2025 00:35:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79abe04602eb193952fd20451edc2e0c3edec25b5140860576ab8dd43434ccb`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45face97a75a56bdc0329ba85ac9adf2164e9692773043bba1e330df0a7701`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f5bde34f5706ee15891362936963912b7c2e41b557cf665abe48182cdd775b`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58967fcbfa6fea8b02512fa1441f7ec6bd92d7623897ec3c826b7185d98f15`  
		Last Modified: Thu, 13 Feb 2025 00:35:47 GMT  
		Size: 188.6 MB (188602321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ba356d441b938ba068b455cc2d082fac429a473b9dffa6f0f3eda32523be4`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.8-alpine`

```console
$ docker pull julia@sha256:fde3a2f343281404e65e75f6e1dba2b52b43e982947599462c7942a9dada5e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.8-alpine` - linux; amd64

```console
$ docker pull julia@sha256:0c5a7cb3a53fddbfc5f5858565c26e687e2b7ca0955eb423fcb5eed325858a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182654555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5eed16e3a5cdd9a2d0a0616d9d07473136d56634021e44288850a3d06ba6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bc633fb744540a8186183a70c5f87975154b6482ab9c2eabcbb37325ae108d`  
		Last Modified: Fri, 14 Feb 2025 19:15:59 GMT  
		Size: 179.0 MB (179011941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c989ce9e32627332370f11e298b17b0ba8828e9d2b55f5e05848ef795dbc99`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:51b30c9c61ec38432645c4b2682a4cd0614d3b92de18bb215e109b1f2c7d20cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f38a89a779409744eadb880fd458ada92e3242a07d5244f7b3b633db07410e9`

```dockerfile
```

-	Layers:
	-	`sha256:b258d9aef98d4d8be8f1093ef84a93da1385098e6be38cdb67a2232b1a5abb1a`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 79.9 KB (79887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2231f8800e0744dad35c200ea21ea2b4fdaf2710bad565cb3f200cc92291f7`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-alpine3.20`

```console
$ docker pull julia@sha256:cb3e18af01c393f335c67c206c1c03e5fc0a00fc09ea5eaa1aa717ca949f7490
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.8-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:ddd0c1ce44e345efc275a36319f0eb0e5891c9c3db58ff98ae08abfbdb78d8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182638245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d53181291492847160d2291d858cb5dd21d64dedd3f9f45d6ab0d7ac9fc946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adf9f8ee73736ece7799870a876adb5fa6e8cb7fb89586038818492e0309651`  
		Last Modified: Fri, 14 Feb 2025 19:16:42 GMT  
		Size: 179.0 MB (179010980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0db0f345ecba4900ec3b86881cd225812958cdbebb85c593ff779c1a82ba9e7`  
		Last Modified: Fri, 14 Feb 2025 19:16:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:06ae6e2e3886a47f010bd0e55e18db672fcef53e0e429da710877ca372027dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a90ef83d1183d2f8c4fc7b2960f40f8044566347689e6c7bbbb60f5634f6d9e`

```dockerfile
```

-	Layers:
	-	`sha256:e0234bb02d29a858408cb1f537668a1b6fd6a240d9c3dd7790430374b821d93c`  
		Last Modified: Fri, 14 Feb 2025 19:16:37 GMT  
		Size: 73.5 KB (73545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945797eb1de64e8c5053ba25ffe9b170fbaf889b7c3677d456b2533ca0ab8825`  
		Last Modified: Fri, 14 Feb 2025 19:16:37 GMT  
		Size: 12.0 KB (11964 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-alpine3.21`

```console
$ docker pull julia@sha256:fde3a2f343281404e65e75f6e1dba2b52b43e982947599462c7942a9dada5e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.8-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:0c5a7cb3a53fddbfc5f5858565c26e687e2b7ca0955eb423fcb5eed325858a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182654555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5eed16e3a5cdd9a2d0a0616d9d07473136d56634021e44288850a3d06ba6e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bc633fb744540a8186183a70c5f87975154b6482ab9c2eabcbb37325ae108d`  
		Last Modified: Fri, 14 Feb 2025 19:15:59 GMT  
		Size: 179.0 MB (179011941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c989ce9e32627332370f11e298b17b0ba8828e9d2b55f5e05848ef795dbc99`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:51b30c9c61ec38432645c4b2682a4cd0614d3b92de18bb215e109b1f2c7d20cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f38a89a779409744eadb880fd458ada92e3242a07d5244f7b3b633db07410e9`

```dockerfile
```

-	Layers:
	-	`sha256:b258d9aef98d4d8be8f1093ef84a93da1385098e6be38cdb67a2232b1a5abb1a`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 79.9 KB (79887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2231f8800e0744dad35c200ea21ea2b4fdaf2710bad565cb3f200cc92291f7`  
		Last Modified: Fri, 14 Feb 2025 19:15:56 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-bookworm`

```console
$ docker pull julia@sha256:b550ca97387e84559a24ed9ded4006051479eae9781f53beecd2b18def37de23
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
$ docker pull julia@sha256:16861b30aa44ba3014024b04d8a2d19f7d4714afc5603766247615408554cc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209692973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419d8852aabd187a4ca302441b40822ed038f26132124c51ebd6280cf1b97a96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122c4f07cddf958472ebcfefdef6e04b8ec05ab084bc17a174d2322f7f6d4dbb`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 5.7 MB (5713123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c11064192e1e6dd1a385540dec0ddf4a32495ef567fefa9946a246bd55fd22`  
		Last Modified: Tue, 25 Feb 2025 03:22:14 GMT  
		Size: 175.8 MB (175760175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596281411f81f3ae58170786cad06c187e3c33206cce78af5fb20f484c1266fd`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:91837517f7ae752dc92b578339254f5d3df7103c0ed1074282314cbd6227dc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206a90d860b87f476330b3e2df57e4eea143236e3db530d0e2846f0cc184b6`

```dockerfile
```

-	Layers:
	-	`sha256:bfd4c0287847f6e0cf0f820e520acff430a0c8dfd178aa3da7f79d326436bce9`  
		Last Modified: Tue, 25 Feb 2025 03:22:09 GMT  
		Size: 2.4 MB (2445501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311413abb4d5612100c3a8f20126ac12799989b6af9eea7533138331e8b2bb92`  
		Last Modified: Tue, 25 Feb 2025 03:22:08 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:17882851585204b254730a9aa1db15b2a5683f61ebcc8a43580c2e70eb838e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210727082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f831015f384e2af9848b80098b94f9b54d97dd3e0452f7105eed561881a9b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d144f1ce3cd4d7a2c095e6ffcbe18e0b43cc306302c98af58fd0366ad441b8`  
		Last Modified: Tue, 25 Feb 2025 11:26:30 GMT  
		Size: 177.1 MB (177140194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4679683f406ac5df6a8b6ef50af68d26f2cc3dd292f4ea7f6dcf5d03d910e6`  
		Last Modified: Tue, 25 Feb 2025 11:26:24 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:584f1ec86e7e2e26c0fe9ba0640946ececb65920ff463e37328129a6aa2793d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb12d5782efdd7d0aca89c3a931f531adbf60bf0cf8a0843c4201fdd20cce10`

```dockerfile
```

-	Layers:
	-	`sha256:8bf1c62b2798a091a3fab2d7d92b25cb09f39c949b82ca6ef6ee065143500804`  
		Last Modified: Tue, 25 Feb 2025 11:26:25 GMT  
		Size: 2.4 MB (2444545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b6a59f11a6afc9e319cb5f37c24783db716ec3744f45609b3e815e67b830cf`  
		Last Modified: Tue, 25 Feb 2025 11:26:25 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bookworm` - linux; 386

```console
$ docker pull julia@sha256:b0e1e114a631996919bf0ac8a33af67ac1c268ea1d208c7bfcf9c13cc9795bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b9531ef3d714de609e16e1d268fb99bfebd8e2604b5e31053bff704ce3715e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026ffb89d7f74c36830ec9de84b40e4d25886dfc8fbedb6fd0cd6d6d29f007d`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 5.9 MB (5872073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6684adda4e8db08dde58ecb6edcf9b83fc0893d2662d4d72da1fd0b1840165`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 157.8 MB (157801936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517f1f728c76a2ab7c2017ccbe16c5280d39563b142f511b2a27f3082da2dff4`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:cd7e3ce301f96d2c226e04f85df771fe41e4dac8ab475e2f25f4873d1bf5d709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cdd62bdd0b2173d4eb4759a98a4a029c1f12738adbac374b89acd643b4b2c1`

```dockerfile
```

-	Layers:
	-	`sha256:ac9634187f26163526cf2c7f9dca5b95bb6979c4b2a657b14f4fc1a0e98d39f5`  
		Last Modified: Tue, 25 Feb 2025 02:12:32 GMT  
		Size: 2.4 MB (2442594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93388392b4150bfdbe25a2cded73353f22a6818a196480e5501c2df623e48a6`  
		Last Modified: Tue, 25 Feb 2025 02:12:31 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:e2098f0ec371c8d9544d0785b5b84647f8dab8b3f6cb50dd0631a0b39c83ff0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193459312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79611a383285f249aaee725495ccb56c1ec506f6cce28c08298f315b8d22c931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a01e2350cb6f03b0da6d34b7ea67118dc4f0ee789279e0106e3e129ec4f2a1f`  
		Last Modified: Tue, 25 Feb 2025 02:36:23 GMT  
		Size: 155.2 MB (155157257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b90912e0605bcf3e5f1145012ba57e524d67ca2b53566f38bcd071077b3b7`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:193328fad219591f1ebe48951e320b0d0ef8a074417ac72447204422a27409eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353333249b3cc3ccbf35310a0be7f9799c32b0a00de6b77197647599cb085a65`

```dockerfile
```

-	Layers:
	-	`sha256:bc375cc77ef1b96e128f67a0cc769ef1ffd2fe5fd98feb3390a049962a51b3a0`  
		Last Modified: Tue, 25 Feb 2025 02:36:20 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc454e075d0910fe622f24e0c3520fb73938b551685986a865d74f5d13356a33`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-bullseye`

```console
$ docker pull julia@sha256:829de4107352553a2de12ea722a39898d18351af25bab5b3caaea738c4bedc7d
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
$ docker pull julia@sha256:276b6794004a535dd48163a8dc1933831e664441b28ba05107067236f8f4eb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208237330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db77ca1b7ec38568315c3b0146aa832ffff765a03e4c01009a44b40c71254bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537cacb47ed4409781d1199ed9a486feab9b36ba9dbeec99b1799618e1d10942`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.2 MB (2222624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbbe690acbffc4d19431e54d00c0568c51820d4b04d2ba8c81a33d818b999f3`  
		Last Modified: Tue, 25 Feb 2025 02:16:50 GMT  
		Size: 175.8 MB (175760407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0432e741400db75afba85576f7b607b213c646a57b317b5642afb46e38d6712`  
		Last Modified: Tue, 25 Feb 2025 02:16:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:683fec5907071fcf53560cbb425f5881b4d6051d6c3717c8a6b96c18237eaf4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc8dd76e5b71450d263ee0fcc986d8c1c26e0dd4fe6a1f92bbe9ed02c28dfb3`

```dockerfile
```

-	Layers:
	-	`sha256:9b62610382c69b145d8503466a1175ba882dd5d572e8ac31fe510eed60728eea`  
		Last Modified: Tue, 25 Feb 2025 02:16:47 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda4f139e0afc726bf69bf32420471035a27f35f961919ad37c25ae0d0060e08`  
		Last Modified: Tue, 25 Feb 2025 02:16:47 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:712086ced6e853c1c1237571fd709c0d61a24f3db1e1c0b0db19d8bfbd96d522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208097263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faa8a68052cb6f66374c91a9e3383ee29c94430465885e9acaa343a0d434c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb70ac9c266fdb923eb0632b4f22d215191a2b807529efbaabd3012f5356c8f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.2 MB (2210296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7591cbfbfafc8b32059c36e34d09bb32473d7a4cb3d83ab5658937ee63cddb7`  
		Last Modified: Tue, 25 Feb 2025 02:55:43 GMT  
		Size: 177.1 MB (177140609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4ac6f869de3615b13054f13e26efbaa1894227d24300a85e6ead532b3e1427`  
		Last Modified: Tue, 25 Feb 2025 02:55:38 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:9573e2c7eae53de0c624cedb615c65fbfa9f79f1dc195e1079797d5440d74c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d66b48d28bdbcdf97c5609757d527ea0ef01af0a9f2d2f6ee5f9670efcfb4c1`

```dockerfile
```

-	Layers:
	-	`sha256:a3676567423bf5822fefddd02df867abdc26c0da704627cd4a9922c65ed84d44`  
		Last Modified: Tue, 25 Feb 2025 02:55:38 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bb5e265de1e0ebe13d1ce1d06404470d24164596a05c15b8166be3da0ee61b`  
		Last Modified: Tue, 25 Feb 2025 02:55:38 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.8-bullseye` - linux; 386

```console
$ docker pull julia@sha256:2dc670805d439e691abb7f5e843979cffd9f4f171f75a56f735a6b86d1aeefb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191310872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3d7a0bd4d350b5bd9ee20592f11c0316d67febbb19eb6f817d37f96b44ec9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54415e0560708d03cde1351310902ba116685db651be9f8648fb8269c8ac9750`  
		Last Modified: Tue, 25 Feb 2025 02:12:25 GMT  
		Size: 2.3 MB (2328129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0f7f50bfc8dafda6641dead3c5c5ece290d547e97f111d627ec33c4c2d8373`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 157.8 MB (157801945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef06be5a3288a740c1eac59f8de63ea0dc568c07d261cefeb681856063950f00`  
		Last Modified: Tue, 25 Feb 2025 02:12:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.8-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:ace80bafa2c33ef8f49a15d416312fd68ea1f58627cbe948200f3d30fc9c7a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52e24068a9e8ada4180d882e6d723d8496307d27c9f73f9deda4c249a4f7afd`

```dockerfile
```

-	Layers:
	-	`sha256:4e3f88279f03e8dceb4431ded41237ebd7a6db853184babf7653217f9f7e299b`  
		Last Modified: Tue, 25 Feb 2025 02:12:25 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87088a5b696817f43d1d80674f6bb6d75193a02def23ccfbb93f8c5bdbee66ed`  
		Last Modified: Tue, 25 Feb 2025 02:12:25 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.8-windowsservercore`

```console
$ docker pull julia@sha256:e10d0d02a66fe615e86959d560acbd0a87159fe6a7c4866135ac7c3c6b8846a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

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

### `julia:1.10.8-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:ac79fdbb729145cb1bffbdcdac5c90f0659420b2c32a042db8e09ef5046c12ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452517945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a427a05613dcbebc39e69375a7a22c6de08dca1a906ce33785a88edddae738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:37:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:37:49 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:38:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ed8e7202322ceebbde66bd5c17e8cb63f0a63deeba0dce25ca0165af4cd94`  
		Last Modified: Thu, 13 Feb 2025 00:38:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d463e8f59a011a182e6b4e5c59ca3b24501c020944150165d7923668fff5`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691753fae6105922bbdc47180303ef3e79f0262b36268f73c2ee704321a43dc1`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cedad76f34702d30642f568d3467dc6f1f420c3fc61ac77dfe77b68af40e468`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb673a4bf380f9c6a5308a15b2a2a57b82a2d923bc93c5afab400e3c1c1b838`  
		Last Modified: Thu, 13 Feb 2025 00:39:10 GMT  
		Size: 188.7 MB (188653406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d63bac5eabd3f54a59db28184d9bad8be6ad92dd626462ad51bc06e3f662db`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.8-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:9e3801b456c24260294efa77599c44818954fa48ec8a4a6f54bb5bbf57fc538a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325517602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5322a337b2455c2f0d0235881437dfa635e05f9a936c4cb27dff5df3bbb53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:08 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:35:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8581044a74ef698a3ae34bab811faa129529027c7eb77a6b0c0754748f6055`  
		Last Modified: Thu, 13 Feb 2025 00:35:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79abe04602eb193952fd20451edc2e0c3edec25b5140860576ab8dd43434ccb`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45face97a75a56bdc0329ba85ac9adf2164e9692773043bba1e330df0a7701`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f5bde34f5706ee15891362936963912b7c2e41b557cf665abe48182cdd775b`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58967fcbfa6fea8b02512fa1441f7ec6bd92d7623897ec3c826b7185d98f15`  
		Last Modified: Thu, 13 Feb 2025 00:35:47 GMT  
		Size: 188.6 MB (188602321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ba356d441b938ba068b455cc2d082fac429a473b9dffa6f0f3eda32523be4`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.8-windowsservercore-1809`

```console
$ docker pull julia@sha256:507c37ca88e0d966becafe997ce6dc105fa3cfa7c09182b23bf1f2ff3898c1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10.8-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:9e3801b456c24260294efa77599c44818954fa48ec8a4a6f54bb5bbf57fc538a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325517602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5322a337b2455c2f0d0235881437dfa635e05f9a936c4cb27dff5df3bbb53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:08 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:35:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8581044a74ef698a3ae34bab811faa129529027c7eb77a6b0c0754748f6055`  
		Last Modified: Thu, 13 Feb 2025 00:35:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79abe04602eb193952fd20451edc2e0c3edec25b5140860576ab8dd43434ccb`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45face97a75a56bdc0329ba85ac9adf2164e9692773043bba1e330df0a7701`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f5bde34f5706ee15891362936963912b7c2e41b557cf665abe48182cdd775b`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58967fcbfa6fea8b02512fa1441f7ec6bd92d7623897ec3c826b7185d98f15`  
		Last Modified: Thu, 13 Feb 2025 00:35:47 GMT  
		Size: 188.6 MB (188602321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ba356d441b938ba068b455cc2d082fac429a473b9dffa6f0f3eda32523be4`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.8-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:6ea0f734de4588ffd1d83678be1e21a39d6af7576cf876e5426c51c900b2c72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.10.8-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:ac79fdbb729145cb1bffbdcdac5c90f0659420b2c32a042db8e09ef5046c12ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452517945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a427a05613dcbebc39e69375a7a22c6de08dca1a906ce33785a88edddae738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:37:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:37:49 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:38:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ed8e7202322ceebbde66bd5c17e8cb63f0a63deeba0dce25ca0165af4cd94`  
		Last Modified: Thu, 13 Feb 2025 00:38:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d463e8f59a011a182e6b4e5c59ca3b24501c020944150165d7923668fff5`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691753fae6105922bbdc47180303ef3e79f0262b36268f73c2ee704321a43dc1`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cedad76f34702d30642f568d3467dc6f1f420c3fc61ac77dfe77b68af40e468`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb673a4bf380f9c6a5308a15b2a2a57b82a2d923bc93c5afab400e3c1c1b838`  
		Last Modified: Thu, 13 Feb 2025 00:39:10 GMT  
		Size: 188.7 MB (188653406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d63bac5eabd3f54a59db28184d9bad8be6ad92dd626462ad51bc06e3f662db`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1288 bytes)  
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
$ docker pull julia@sha256:2cedc072424d2e6795c432f1c921cedf720f8895a898fe9284f408edd5daf096
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
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:21a2f31eb0afbc61cf00e8832cf9878fde336806c09d6037e369c449e41adb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302237946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667dd69b841cc680d1fd298e989ee1f12ecfb8bc58765ff2c7762470f452a8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ad764b6536afc32f7f6c07197f1524fe7d510ac76409bb60db3f450e08be6`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 5.7 MB (5713132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784588307487c202b864f398d3d71a71d26dcbdac4e31de50e99316494360644`  
		Last Modified: Tue, 25 Feb 2025 02:16:53 GMT  
		Size: 268.3 MB (268305141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f9e2b0fd2ceac4ac0c0f47405cef6bfa98f1ffde76e9b7b3d07973c3e6cdb`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:627eba988065767ad312f4f0627101b8223db458658d2be445f01ca95493cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f2f07b04a978ddfaf53f31aeaf3b5d81ba78ba106a2f94bca9dbfb04d3ee5a`

```dockerfile
```

-	Layers:
	-	`sha256:6138b3281398d6e38371d01eddb44415b8a78272a30a180cdfa4fbb0be3ce544`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.4 MB (2445456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0463451a38f357fc3ef05f31df155094dc72292b62c28fd5e43fa52ae679be6c`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:aba40bb6b6c686ca62e6a4bdc597818e26a2b3529bbd1fa95f737dda7b8527d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317521098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f8f8f99d3b28dfcd057d40f3316092eb744bf6891ab7a48a657878bd3ac65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f4963ec0f4ec9a964e744c494d8c0524ff01b292fd232727fb76b699ff0c0`  
		Last Modified: Tue, 25 Feb 2025 02:53:17 GMT  
		Size: 283.9 MB (283934209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dbedf45b8961bfd5c3753b651c3ae061b06d4f133b8f886a78fd9dd79b5c`  
		Last Modified: Tue, 25 Feb 2025 02:53:10 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:becf6fa65f281f5d60ae19863c5ace12f2e6d888441eb8817ddbbcb427f6cdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7846b68e7aadd64609368e927baaf73fa83d821d6dbcdbb5a420954805762a6`

```dockerfile
```

-	Layers:
	-	`sha256:868cc353399b91966b6a4f6e2df3c47a99a77c2864ababbcaf298ebb960c7990`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 2.4 MB (2445779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3988a1ba379532da23400b9280a68fdb69fbccf28d299778b159d09c49a6190`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:acd6e3dc9e639a6fafff6353a7298ffbca88ac410169dccf8699ca161cf29581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252982209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c4041fd0170c99549d59fa33bbf28dda58589890fed8f50ce88a8140bae95d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213e1b09c8d081c075b1cbe4f6add0244567064c4ba15857e80f28318f989a0`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 5.9 MB (5872055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff72f08d516ff6915525f10dad0fdbec7a7a81d5c94baae581e8056e7ce68ff`  
		Last Modified: Tue, 25 Feb 2025 02:12:38 GMT  
		Size: 217.9 MB (217915195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70511d5c6ee7fb9b97489e07f00ead0a1e758360f4c850a3e22aefa13ac0b99f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:8705454a0ddce89dd8f3e87b1572e377290f0561de1c05f05dbbcd98221ccc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc8d8d55e0e44f92e2bcc1340e62bf647dd44fb0826f6fbf46fb8d5b72e81d`

```dockerfile
```

-	Layers:
	-	`sha256:7b06096cc360b390c1325226d4c138b5d3c994f0c87aabcf0ba95feb3ebd0030`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 2.4 MB (2442529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fed0d72a11007583f709d303cf78d3f5b894522f2aaf2d946fd1e130fa7e8f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
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

### `julia:1.11` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:7e62d80dc9847456c44e7c7205e79d4eff5d807417ca391390b5d21eca40a485
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
$ docker pull julia@sha256:21a2f31eb0afbc61cf00e8832cf9878fde336806c09d6037e369c449e41adb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302237946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667dd69b841cc680d1fd298e989ee1f12ecfb8bc58765ff2c7762470f452a8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ad764b6536afc32f7f6c07197f1524fe7d510ac76409bb60db3f450e08be6`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 5.7 MB (5713132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784588307487c202b864f398d3d71a71d26dcbdac4e31de50e99316494360644`  
		Last Modified: Tue, 25 Feb 2025 02:16:53 GMT  
		Size: 268.3 MB (268305141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f9e2b0fd2ceac4ac0c0f47405cef6bfa98f1ffde76e9b7b3d07973c3e6cdb`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:627eba988065767ad312f4f0627101b8223db458658d2be445f01ca95493cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f2f07b04a978ddfaf53f31aeaf3b5d81ba78ba106a2f94bca9dbfb04d3ee5a`

```dockerfile
```

-	Layers:
	-	`sha256:6138b3281398d6e38371d01eddb44415b8a78272a30a180cdfa4fbb0be3ce544`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.4 MB (2445456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0463451a38f357fc3ef05f31df155094dc72292b62c28fd5e43fa52ae679be6c`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:aba40bb6b6c686ca62e6a4bdc597818e26a2b3529bbd1fa95f737dda7b8527d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317521098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f8f8f99d3b28dfcd057d40f3316092eb744bf6891ab7a48a657878bd3ac65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f4963ec0f4ec9a964e744c494d8c0524ff01b292fd232727fb76b699ff0c0`  
		Last Modified: Tue, 25 Feb 2025 02:53:17 GMT  
		Size: 283.9 MB (283934209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dbedf45b8961bfd5c3753b651c3ae061b06d4f133b8f886a78fd9dd79b5c`  
		Last Modified: Tue, 25 Feb 2025 02:53:10 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:becf6fa65f281f5d60ae19863c5ace12f2e6d888441eb8817ddbbcb427f6cdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7846b68e7aadd64609368e927baaf73fa83d821d6dbcdbb5a420954805762a6`

```dockerfile
```

-	Layers:
	-	`sha256:868cc353399b91966b6a4f6e2df3c47a99a77c2864ababbcaf298ebb960c7990`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 2.4 MB (2445779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3988a1ba379532da23400b9280a68fdb69fbccf28d299778b159d09c49a6190`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:acd6e3dc9e639a6fafff6353a7298ffbca88ac410169dccf8699ca161cf29581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252982209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c4041fd0170c99549d59fa33bbf28dda58589890fed8f50ce88a8140bae95d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213e1b09c8d081c075b1cbe4f6add0244567064c4ba15857e80f28318f989a0`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 5.9 MB (5872055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff72f08d516ff6915525f10dad0fdbec7a7a81d5c94baae581e8056e7ce68ff`  
		Last Modified: Tue, 25 Feb 2025 02:12:38 GMT  
		Size: 217.9 MB (217915195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70511d5c6ee7fb9b97489e07f00ead0a1e758360f4c850a3e22aefa13ac0b99f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8705454a0ddce89dd8f3e87b1572e377290f0561de1c05f05dbbcd98221ccc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc8d8d55e0e44f92e2bcc1340e62bf647dd44fb0826f6fbf46fb8d5b72e81d`

```dockerfile
```

-	Layers:
	-	`sha256:7b06096cc360b390c1325226d4c138b5d3c994f0c87aabcf0ba95feb3ebd0030`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 2.4 MB (2442529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fed0d72a11007583f709d303cf78d3f5b894522f2aaf2d946fd1e130fa7e8f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bullseye`

```console
$ docker pull julia@sha256:11d4d97486a98c0125980155216f5fdc457742b0d0134dee9bab3823c7e52143
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
$ docker pull julia@sha256:e64d13743fef5bee538747ac3ca5a753da245fab00666b43738a2140f182a804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300782132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b1e593902167844e0f8c6ad5487957aa3b121e642611ed59b8840b765362fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcafc09016b343666a8d68e276afa1cd649c2dcf4eec976831223671bf3f7e8`  
		Last Modified: Tue, 25 Feb 2025 02:16:45 GMT  
		Size: 2.2 MB (2222692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86f9ade150a6fd38f241687982dc0eaba6f0951421a079c9c42a134fbb83e5`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 268.3 MB (268305139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5427fcc0a2762fab1cb70aadcb7bf1e60a558695210a462de23cf98636c08bf6`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b1bc4430f3d8b56636729de4d562ea52fdc12c800bc0e28a5b395cad99541146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c60387f29f351dcfab4553ddbec1fbd49b3245a25fb77033a62be4d118387a`

```dockerfile
```

-	Layers:
	-	`sha256:ce2fde94b0f58e3b94d7978ef308c3c07130e9683bf69c105ca8c94cb9c431d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60c79f7ca801535cc5684531dd06ac4573d5398783929fbd30ac201028e12d5`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a4069520380136d9cdb2e7ecd5c66e80c69232e3868afcfca5fb5e964670dd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314892835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60765db82c102b930c3f02dcfc17102c77ff65ffe2a3187cf192b4fb0159f461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb70ac9c266fdb923eb0632b4f22d215191a2b807529efbaabd3012f5356c8f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.2 MB (2210296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bc6a668f27d84fc2ed9afcb7d5782d481f80c6866cbe938c00dfbb1bca7fb2`  
		Last Modified: Tue, 25 Feb 2025 02:54:39 GMT  
		Size: 283.9 MB (283936179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc55ee2b8200aa8c9e0df3088c6c573e2fd6b3ef73768158109da258f628f41f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8f132cd176ca26509524467c3048ab38033a7a2de40221fb97e1c6fd9cb0f233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26036101f475014f6b6687df3d6c5ab2dae8eca5a06093dd7c09e902ac79f844`

```dockerfile
```

-	Layers:
	-	`sha256:84be007fb550007647934941a06746976588afb4943c80420be20472c08c741a`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b21c55600dffaffa1b55e309eca82ac9ab44fbd7abe1c5d094a40bad6f8934f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; 386

```console
$ docker pull julia@sha256:dd4b0775d7c3247adb5bd871c9283fd36afb17020f625c24cb605762b516c3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251423827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc774e6584b17557fc9db131bfe1340e5f28930c27c1fcbbb30b4ef6c4a1265`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1102477f498de586c7b0314598e024085d6b13f13a854c5878aa6f00bd98e9`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 2.3 MB (2328115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaa08382b40474ae5bbf8503cc0f9c0411967be2c581ffdb8a4ef81ab8e905d`  
		Last Modified: Tue, 25 Feb 2025 02:12:40 GMT  
		Size: 217.9 MB (217914915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b54104f3c6f7da984c2739dc0725a5fa9a7cda0415c2db447575b9ba62a3334`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e47cea5e39712bc87d5fef445c4966cccf8bd3e008e4475b39796fb78dc5676c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389305f43e31f8582345649842365969d4dbf5ee09f564ec99d27afe0a00fea4`

```dockerfile
```

-	Layers:
	-	`sha256:c968cf7e25787cf4f4ef6904f81afe1f5d55b29dfb92b8b9e06b0aa923199898`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3998d18c45834b1a24b7cfdc5709065142630b19ba6cf69e3a777c1c38de6600`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:0a9215fb8bff2ddae3ae14be87d1702eb1337bc3b744117af7de2d033161d716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

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

### `julia:1.11-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:2e7bd23cb87b2b1bd0cdcc013c54c0b618044b9750fe0527be5e012363a73f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:67a9470180bfe119828cda80614b5c765934f592f08dd030ae237136aff79352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull julia@sha256:2cedc072424d2e6795c432f1c921cedf720f8895a898fe9284f408edd5daf096
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
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11.3` - linux; amd64

```console
$ docker pull julia@sha256:21a2f31eb0afbc61cf00e8832cf9878fde336806c09d6037e369c449e41adb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302237946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667dd69b841cc680d1fd298e989ee1f12ecfb8bc58765ff2c7762470f452a8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ad764b6536afc32f7f6c07197f1524fe7d510ac76409bb60db3f450e08be6`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 5.7 MB (5713132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784588307487c202b864f398d3d71a71d26dcbdac4e31de50e99316494360644`  
		Last Modified: Tue, 25 Feb 2025 02:16:53 GMT  
		Size: 268.3 MB (268305141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f9e2b0fd2ceac4ac0c0f47405cef6bfa98f1ffde76e9b7b3d07973c3e6cdb`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3` - unknown; unknown

```console
$ docker pull julia@sha256:627eba988065767ad312f4f0627101b8223db458658d2be445f01ca95493cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f2f07b04a978ddfaf53f31aeaf3b5d81ba78ba106a2f94bca9dbfb04d3ee5a`

```dockerfile
```

-	Layers:
	-	`sha256:6138b3281398d6e38371d01eddb44415b8a78272a30a180cdfa4fbb0be3ce544`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.4 MB (2445456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0463451a38f357fc3ef05f31df155094dc72292b62c28fd5e43fa52ae679be6c`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:aba40bb6b6c686ca62e6a4bdc597818e26a2b3529bbd1fa95f737dda7b8527d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317521098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f8f8f99d3b28dfcd057d40f3316092eb744bf6891ab7a48a657878bd3ac65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f4963ec0f4ec9a964e744c494d8c0524ff01b292fd232727fb76b699ff0c0`  
		Last Modified: Tue, 25 Feb 2025 02:53:17 GMT  
		Size: 283.9 MB (283934209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dbedf45b8961bfd5c3753b651c3ae061b06d4f133b8f886a78fd9dd79b5c`  
		Last Modified: Tue, 25 Feb 2025 02:53:10 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3` - unknown; unknown

```console
$ docker pull julia@sha256:becf6fa65f281f5d60ae19863c5ace12f2e6d888441eb8817ddbbcb427f6cdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7846b68e7aadd64609368e927baaf73fa83d821d6dbcdbb5a420954805762a6`

```dockerfile
```

-	Layers:
	-	`sha256:868cc353399b91966b6a4f6e2df3c47a99a77c2864ababbcaf298ebb960c7990`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 2.4 MB (2445779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3988a1ba379532da23400b9280a68fdb69fbccf28d299778b159d09c49a6190`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3` - linux; 386

```console
$ docker pull julia@sha256:acd6e3dc9e639a6fafff6353a7298ffbca88ac410169dccf8699ca161cf29581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252982209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c4041fd0170c99549d59fa33bbf28dda58589890fed8f50ce88a8140bae95d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213e1b09c8d081c075b1cbe4f6add0244567064c4ba15857e80f28318f989a0`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 5.9 MB (5872055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff72f08d516ff6915525f10dad0fdbec7a7a81d5c94baae581e8056e7ce68ff`  
		Last Modified: Tue, 25 Feb 2025 02:12:38 GMT  
		Size: 217.9 MB (217915195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70511d5c6ee7fb9b97489e07f00ead0a1e758360f4c850a3e22aefa13ac0b99f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3` - unknown; unknown

```console
$ docker pull julia@sha256:8705454a0ddce89dd8f3e87b1572e377290f0561de1c05f05dbbcd98221ccc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc8d8d55e0e44f92e2bcc1340e62bf647dd44fb0826f6fbf46fb8d5b72e81d`

```dockerfile
```

-	Layers:
	-	`sha256:7b06096cc360b390c1325226d4c138b5d3c994f0c87aabcf0ba95feb3ebd0030`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 2.4 MB (2442529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fed0d72a11007583f709d303cf78d3f5b894522f2aaf2d946fd1e130fa7e8f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3` - linux; ppc64le

```console
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
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

### `julia:1.11.3` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.3` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.3-bookworm`

```console
$ docker pull julia@sha256:7e62d80dc9847456c44e7c7205e79d4eff5d807417ca391390b5d21eca40a485
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
$ docker pull julia@sha256:21a2f31eb0afbc61cf00e8832cf9878fde336806c09d6037e369c449e41adb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302237946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667dd69b841cc680d1fd298e989ee1f12ecfb8bc58765ff2c7762470f452a8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ad764b6536afc32f7f6c07197f1524fe7d510ac76409bb60db3f450e08be6`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 5.7 MB (5713132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784588307487c202b864f398d3d71a71d26dcbdac4e31de50e99316494360644`  
		Last Modified: Tue, 25 Feb 2025 02:16:53 GMT  
		Size: 268.3 MB (268305141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f9e2b0fd2ceac4ac0c0f47405cef6bfa98f1ffde76e9b7b3d07973c3e6cdb`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:627eba988065767ad312f4f0627101b8223db458658d2be445f01ca95493cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f2f07b04a978ddfaf53f31aeaf3b5d81ba78ba106a2f94bca9dbfb04d3ee5a`

```dockerfile
```

-	Layers:
	-	`sha256:6138b3281398d6e38371d01eddb44415b8a78272a30a180cdfa4fbb0be3ce544`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.4 MB (2445456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0463451a38f357fc3ef05f31df155094dc72292b62c28fd5e43fa52ae679be6c`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:aba40bb6b6c686ca62e6a4bdc597818e26a2b3529bbd1fa95f737dda7b8527d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317521098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f8f8f99d3b28dfcd057d40f3316092eb744bf6891ab7a48a657878bd3ac65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f4963ec0f4ec9a964e744c494d8c0524ff01b292fd232727fb76b699ff0c0`  
		Last Modified: Tue, 25 Feb 2025 02:53:17 GMT  
		Size: 283.9 MB (283934209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dbedf45b8961bfd5c3753b651c3ae061b06d4f133b8f886a78fd9dd79b5c`  
		Last Modified: Tue, 25 Feb 2025 02:53:10 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:becf6fa65f281f5d60ae19863c5ace12f2e6d888441eb8817ddbbcb427f6cdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7846b68e7aadd64609368e927baaf73fa83d821d6dbcdbb5a420954805762a6`

```dockerfile
```

-	Layers:
	-	`sha256:868cc353399b91966b6a4f6e2df3c47a99a77c2864ababbcaf298ebb960c7990`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 2.4 MB (2445779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3988a1ba379532da23400b9280a68fdb69fbccf28d299778b159d09c49a6190`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bookworm` - linux; 386

```console
$ docker pull julia@sha256:acd6e3dc9e639a6fafff6353a7298ffbca88ac410169dccf8699ca161cf29581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252982209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c4041fd0170c99549d59fa33bbf28dda58589890fed8f50ce88a8140bae95d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213e1b09c8d081c075b1cbe4f6add0244567064c4ba15857e80f28318f989a0`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 5.9 MB (5872055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff72f08d516ff6915525f10dad0fdbec7a7a81d5c94baae581e8056e7ce68ff`  
		Last Modified: Tue, 25 Feb 2025 02:12:38 GMT  
		Size: 217.9 MB (217915195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70511d5c6ee7fb9b97489e07f00ead0a1e758360f4c850a3e22aefa13ac0b99f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8705454a0ddce89dd8f3e87b1572e377290f0561de1c05f05dbbcd98221ccc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc8d8d55e0e44f92e2bcc1340e62bf647dd44fb0826f6fbf46fb8d5b72e81d`

```dockerfile
```

-	Layers:
	-	`sha256:7b06096cc360b390c1325226d4c138b5d3c994f0c87aabcf0ba95feb3ebd0030`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 2.4 MB (2442529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fed0d72a11007583f709d303cf78d3f5b894522f2aaf2d946fd1e130fa7e8f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.3-bullseye`

```console
$ docker pull julia@sha256:11d4d97486a98c0125980155216f5fdc457742b0d0134dee9bab3823c7e52143
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
$ docker pull julia@sha256:e64d13743fef5bee538747ac3ca5a753da245fab00666b43738a2140f182a804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300782132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b1e593902167844e0f8c6ad5487957aa3b121e642611ed59b8840b765362fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcafc09016b343666a8d68e276afa1cd649c2dcf4eec976831223671bf3f7e8`  
		Last Modified: Tue, 25 Feb 2025 02:16:45 GMT  
		Size: 2.2 MB (2222692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86f9ade150a6fd38f241687982dc0eaba6f0951421a079c9c42a134fbb83e5`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 268.3 MB (268305139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5427fcc0a2762fab1cb70aadcb7bf1e60a558695210a462de23cf98636c08bf6`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b1bc4430f3d8b56636729de4d562ea52fdc12c800bc0e28a5b395cad99541146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c60387f29f351dcfab4553ddbec1fbd49b3245a25fb77033a62be4d118387a`

```dockerfile
```

-	Layers:
	-	`sha256:ce2fde94b0f58e3b94d7978ef308c3c07130e9683bf69c105ca8c94cb9c431d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60c79f7ca801535cc5684531dd06ac4573d5398783929fbd30ac201028e12d5`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a4069520380136d9cdb2e7ecd5c66e80c69232e3868afcfca5fb5e964670dd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314892835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60765db82c102b930c3f02dcfc17102c77ff65ffe2a3187cf192b4fb0159f461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb70ac9c266fdb923eb0632b4f22d215191a2b807529efbaabd3012f5356c8f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.2 MB (2210296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bc6a668f27d84fc2ed9afcb7d5782d481f80c6866cbe938c00dfbb1bca7fb2`  
		Last Modified: Tue, 25 Feb 2025 02:54:39 GMT  
		Size: 283.9 MB (283936179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc55ee2b8200aa8c9e0df3088c6c573e2fd6b3ef73768158109da258f628f41f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8f132cd176ca26509524467c3048ab38033a7a2de40221fb97e1c6fd9cb0f233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26036101f475014f6b6687df3d6c5ab2dae8eca5a06093dd7c09e902ac79f844`

```dockerfile
```

-	Layers:
	-	`sha256:84be007fb550007647934941a06746976588afb4943c80420be20472c08c741a`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b21c55600dffaffa1b55e309eca82ac9ab44fbd7abe1c5d094a40bad6f8934f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.3-bullseye` - linux; 386

```console
$ docker pull julia@sha256:dd4b0775d7c3247adb5bd871c9283fd36afb17020f625c24cb605762b516c3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251423827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc774e6584b17557fc9db131bfe1340e5f28930c27c1fcbbb30b4ef6c4a1265`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1102477f498de586c7b0314598e024085d6b13f13a854c5878aa6f00bd98e9`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 2.3 MB (2328115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaa08382b40474ae5bbf8503cc0f9c0411967be2c581ffdb8a4ef81ab8e905d`  
		Last Modified: Tue, 25 Feb 2025 02:12:40 GMT  
		Size: 217.9 MB (217914915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b54104f3c6f7da984c2739dc0725a5fa9a7cda0415c2db447575b9ba62a3334`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.3-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e47cea5e39712bc87d5fef445c4966cccf8bd3e008e4475b39796fb78dc5676c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389305f43e31f8582345649842365969d4dbf5ee09f564ec99d27afe0a00fea4`

```dockerfile
```

-	Layers:
	-	`sha256:c968cf7e25787cf4f4ef6904f81afe1f5d55b29dfb92b8b9e06b0aa923199898`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3998d18c45834b1a24b7cfdc5709065142630b19ba6cf69e3a777c1c38de6600`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.3-windowsservercore`

```console
$ docker pull julia@sha256:0a9215fb8bff2ddae3ae14be87d1702eb1337bc3b744117af7de2d033161d716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

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

### `julia:1.11.3-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.3-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.3-windowsservercore-1809`

```console
$ docker pull julia@sha256:2e7bd23cb87b2b1bd0cdcc013c54c0b618044b9750fe0527be5e012363a73f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11.3-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.3-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:67a9470180bfe119828cda80614b5c765934f592f08dd030ae237136aff79352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.11.3-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull julia@sha256:7e62d80dc9847456c44e7c7205e79d4eff5d807417ca391390b5d21eca40a485
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
$ docker pull julia@sha256:21a2f31eb0afbc61cf00e8832cf9878fde336806c09d6037e369c449e41adb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302237946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667dd69b841cc680d1fd298e989ee1f12ecfb8bc58765ff2c7762470f452a8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ad764b6536afc32f7f6c07197f1524fe7d510ac76409bb60db3f450e08be6`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 5.7 MB (5713132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784588307487c202b864f398d3d71a71d26dcbdac4e31de50e99316494360644`  
		Last Modified: Tue, 25 Feb 2025 02:16:53 GMT  
		Size: 268.3 MB (268305141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f9e2b0fd2ceac4ac0c0f47405cef6bfa98f1ffde76e9b7b3d07973c3e6cdb`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:627eba988065767ad312f4f0627101b8223db458658d2be445f01ca95493cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f2f07b04a978ddfaf53f31aeaf3b5d81ba78ba106a2f94bca9dbfb04d3ee5a`

```dockerfile
```

-	Layers:
	-	`sha256:6138b3281398d6e38371d01eddb44415b8a78272a30a180cdfa4fbb0be3ce544`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.4 MB (2445456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0463451a38f357fc3ef05f31df155094dc72292b62c28fd5e43fa52ae679be6c`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:aba40bb6b6c686ca62e6a4bdc597818e26a2b3529bbd1fa95f737dda7b8527d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317521098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f8f8f99d3b28dfcd057d40f3316092eb744bf6891ab7a48a657878bd3ac65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f4963ec0f4ec9a964e744c494d8c0524ff01b292fd232727fb76b699ff0c0`  
		Last Modified: Tue, 25 Feb 2025 02:53:17 GMT  
		Size: 283.9 MB (283934209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dbedf45b8961bfd5c3753b651c3ae061b06d4f133b8f886a78fd9dd79b5c`  
		Last Modified: Tue, 25 Feb 2025 02:53:10 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:becf6fa65f281f5d60ae19863c5ace12f2e6d888441eb8817ddbbcb427f6cdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7846b68e7aadd64609368e927baaf73fa83d821d6dbcdbb5a420954805762a6`

```dockerfile
```

-	Layers:
	-	`sha256:868cc353399b91966b6a4f6e2df3c47a99a77c2864ababbcaf298ebb960c7990`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 2.4 MB (2445779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3988a1ba379532da23400b9280a68fdb69fbccf28d299778b159d09c49a6190`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:acd6e3dc9e639a6fafff6353a7298ffbca88ac410169dccf8699ca161cf29581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252982209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c4041fd0170c99549d59fa33bbf28dda58589890fed8f50ce88a8140bae95d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213e1b09c8d081c075b1cbe4f6add0244567064c4ba15857e80f28318f989a0`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 5.9 MB (5872055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff72f08d516ff6915525f10dad0fdbec7a7a81d5c94baae581e8056e7ce68ff`  
		Last Modified: Tue, 25 Feb 2025 02:12:38 GMT  
		Size: 217.9 MB (217915195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70511d5c6ee7fb9b97489e07f00ead0a1e758360f4c850a3e22aefa13ac0b99f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8705454a0ddce89dd8f3e87b1572e377290f0561de1c05f05dbbcd98221ccc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc8d8d55e0e44f92e2bcc1340e62bf647dd44fb0826f6fbf46fb8d5b72e81d`

```dockerfile
```

-	Layers:
	-	`sha256:7b06096cc360b390c1325226d4c138b5d3c994f0c87aabcf0ba95feb3ebd0030`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 2.4 MB (2442529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fed0d72a11007583f709d303cf78d3f5b894522f2aaf2d946fd1e130fa7e8f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:11d4d97486a98c0125980155216f5fdc457742b0d0134dee9bab3823c7e52143
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
$ docker pull julia@sha256:e64d13743fef5bee538747ac3ca5a753da245fab00666b43738a2140f182a804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300782132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b1e593902167844e0f8c6ad5487957aa3b121e642611ed59b8840b765362fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcafc09016b343666a8d68e276afa1cd649c2dcf4eec976831223671bf3f7e8`  
		Last Modified: Tue, 25 Feb 2025 02:16:45 GMT  
		Size: 2.2 MB (2222692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86f9ade150a6fd38f241687982dc0eaba6f0951421a079c9c42a134fbb83e5`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 268.3 MB (268305139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5427fcc0a2762fab1cb70aadcb7bf1e60a558695210a462de23cf98636c08bf6`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b1bc4430f3d8b56636729de4d562ea52fdc12c800bc0e28a5b395cad99541146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c60387f29f351dcfab4553ddbec1fbd49b3245a25fb77033a62be4d118387a`

```dockerfile
```

-	Layers:
	-	`sha256:ce2fde94b0f58e3b94d7978ef308c3c07130e9683bf69c105ca8c94cb9c431d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60c79f7ca801535cc5684531dd06ac4573d5398783929fbd30ac201028e12d5`  
		Last Modified: Tue, 25 Feb 2025 02:16:44 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a4069520380136d9cdb2e7ecd5c66e80c69232e3868afcfca5fb5e964670dd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314892835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60765db82c102b930c3f02dcfc17102c77ff65ffe2a3187cf192b4fb0159f461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb70ac9c266fdb923eb0632b4f22d215191a2b807529efbaabd3012f5356c8f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.2 MB (2210296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bc6a668f27d84fc2ed9afcb7d5782d481f80c6866cbe938c00dfbb1bca7fb2`  
		Last Modified: Tue, 25 Feb 2025 02:54:39 GMT  
		Size: 283.9 MB (283936179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc55ee2b8200aa8c9e0df3088c6c573e2fd6b3ef73768158109da258f628f41f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8f132cd176ca26509524467c3048ab38033a7a2de40221fb97e1c6fd9cb0f233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26036101f475014f6b6687df3d6c5ab2dae8eca5a06093dd7c09e902ac79f844`

```dockerfile
```

-	Layers:
	-	`sha256:84be007fb550007647934941a06746976588afb4943c80420be20472c08c741a`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b21c55600dffaffa1b55e309eca82ac9ab44fbd7abe1c5d094a40bad6f8934f`  
		Last Modified: Tue, 25 Feb 2025 02:54:33 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:dd4b0775d7c3247adb5bd871c9283fd36afb17020f625c24cb605762b516c3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251423827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc774e6584b17557fc9db131bfe1340e5f28930c27c1fcbbb30b4ef6c4a1265`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1102477f498de586c7b0314598e024085d6b13f13a854c5878aa6f00bd98e9`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 2.3 MB (2328115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaa08382b40474ae5bbf8503cc0f9c0411967be2c581ffdb8a4ef81ab8e905d`  
		Last Modified: Tue, 25 Feb 2025 02:12:40 GMT  
		Size: 217.9 MB (217914915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b54104f3c6f7da984c2739dc0725a5fa9a7cda0415c2db447575b9ba62a3334`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e47cea5e39712bc87d5fef445c4966cccf8bd3e008e4475b39796fb78dc5676c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389305f43e31f8582345649842365969d4dbf5ee09f564ec99d27afe0a00fea4`

```dockerfile
```

-	Layers:
	-	`sha256:c968cf7e25787cf4f4ef6904f81afe1f5d55b29dfb92b8b9e06b0aa923199898`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3998d18c45834b1a24b7cfdc5709065142630b19ba6cf69e3a777c1c38de6600`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:2cedc072424d2e6795c432f1c921cedf720f8895a898fe9284f408edd5daf096
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
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:21a2f31eb0afbc61cf00e8832cf9878fde336806c09d6037e369c449e41adb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302237946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667dd69b841cc680d1fd298e989ee1f12ecfb8bc58765ff2c7762470f452a8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ad764b6536afc32f7f6c07197f1524fe7d510ac76409bb60db3f450e08be6`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 5.7 MB (5713132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784588307487c202b864f398d3d71a71d26dcbdac4e31de50e99316494360644`  
		Last Modified: Tue, 25 Feb 2025 02:16:53 GMT  
		Size: 268.3 MB (268305141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9f9e2b0fd2ceac4ac0c0f47405cef6bfa98f1ffde76e9b7b3d07973c3e6cdb`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:627eba988065767ad312f4f0627101b8223db458658d2be445f01ca95493cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f2f07b04a978ddfaf53f31aeaf3b5d81ba78ba106a2f94bca9dbfb04d3ee5a`

```dockerfile
```

-	Layers:
	-	`sha256:6138b3281398d6e38371d01eddb44415b8a78272a30a180cdfa4fbb0be3ce544`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 2.4 MB (2445456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0463451a38f357fc3ef05f31df155094dc72292b62c28fd5e43fa52ae679be6c`  
		Last Modified: Tue, 25 Feb 2025 02:16:48 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:aba40bb6b6c686ca62e6a4bdc597818e26a2b3529bbd1fa95f737dda7b8527d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317521098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f8f8f99d3b28dfcd057d40f3316092eb744bf6891ab7a48a657878bd3ac65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24a0c3ef7da0c92521592c021e3512cbeed8248657a431802b58737bde25f`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f4963ec0f4ec9a964e744c494d8c0524ff01b292fd232727fb76b699ff0c0`  
		Last Modified: Tue, 25 Feb 2025 02:53:17 GMT  
		Size: 283.9 MB (283934209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dbedf45b8961bfd5c3753b651c3ae061b06d4f133b8f886a78fd9dd79b5c`  
		Last Modified: Tue, 25 Feb 2025 02:53:10 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:becf6fa65f281f5d60ae19863c5ace12f2e6d888441eb8817ddbbcb427f6cdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7846b68e7aadd64609368e927baaf73fa83d821d6dbcdbb5a420954805762a6`

```dockerfile
```

-	Layers:
	-	`sha256:868cc353399b91966b6a4f6e2df3c47a99a77c2864ababbcaf298ebb960c7990`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 2.4 MB (2445779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3988a1ba379532da23400b9280a68fdb69fbccf28d299778b159d09c49a6190`  
		Last Modified: Tue, 25 Feb 2025 02:53:11 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:acd6e3dc9e639a6fafff6353a7298ffbca88ac410169dccf8699ca161cf29581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252982209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c4041fd0170c99549d59fa33bbf28dda58589890fed8f50ce88a8140bae95d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213e1b09c8d081c075b1cbe4f6add0244567064c4ba15857e80f28318f989a0`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 5.9 MB (5872055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff72f08d516ff6915525f10dad0fdbec7a7a81d5c94baae581e8056e7ce68ff`  
		Last Modified: Tue, 25 Feb 2025 02:12:38 GMT  
		Size: 217.9 MB (217915195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70511d5c6ee7fb9b97489e07f00ead0a1e758360f4c850a3e22aefa13ac0b99f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:8705454a0ddce89dd8f3e87b1572e377290f0561de1c05f05dbbcd98221ccc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc8d8d55e0e44f92e2bcc1340e62bf647dd44fb0826f6fbf46fb8d5b72e81d`

```dockerfile
```

-	Layers:
	-	`sha256:7b06096cc360b390c1325226d4c138b5d3c994f0c87aabcf0ba95feb3ebd0030`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 2.4 MB (2442529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fed0d72a11007583f709d303cf78d3f5b894522f2aaf2d946fd1e130fa7e8f`  
		Last Modified: Tue, 25 Feb 2025 02:12:33 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
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

### `julia:latest` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:0a9215fb8bff2ddae3ae14be87d1702eb1337bc3b744117af7de2d033161d716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

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

### `julia:windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:2e7bd23cb87b2b1bd0cdcc013c54c0b618044b9750fe0527be5e012363a73f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:67a9470180bfe119828cda80614b5c765934f592f08dd030ae237136aff79352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
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
