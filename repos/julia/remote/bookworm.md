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
