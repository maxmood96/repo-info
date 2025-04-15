## `julia:1-bookworm`

```console
$ docker pull julia@sha256:268c49be0b370c1e1e00b015933307e50c147e96f7a84021ff4092f7bda0fdef
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
$ docker pull julia@sha256:ae01d1ba2d289cd3efd61a7b3faaa789c5ce5c1c3603565fffc33bea2d0d10b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322352874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43a3d26fb0d1777c9ff579a5ba430c57852f0985195ed88c59d07f30bdf577c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 14 Apr 2025 23:59:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_VERSION=1.11.5
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.5-linux-x86_64.tar.gz'; 			sha256='723e878c642220cc0251a0e13758c059a389cadc7f01376feaf1ea7388fe8f9c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.5-linux-aarch64.tar.gz'; 			sha256='f63203574fba25c9bda5e98b2f87f985d4672109855633a46bae32bfba3cbc0d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.5-linux-i686.tar.gz'; 			sha256='c2b6f5763edd994cb01407b8e71797bd25901cc513132d155953742f54b3a294'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.5-linux-ppc64le.tar.gz'; 			sha256='11ae7f0b83663de35d9a30e916373378f7985424c030a4a5af96aecc9b6eaa66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f63205a5a7f7b2f1f0b6a47a254f243c8dbc38cc9fa13904179d175ec7859`  
		Last Modified: Tue, 15 Apr 2025 21:52:46 GMT  
		Size: 5.7 MB (5713481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5685a54748b415b3afdf253f94fe008c15c6466721971d9f221d0cc30552f8`  
		Last Modified: Tue, 15 Apr 2025 21:52:50 GMT  
		Size: 288.4 MB (288411760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed7548008135ad9643ffe52d37506a86bedec5573d84035ea42489a373957fb`  
		Last Modified: Tue, 15 Apr 2025 21:52:46 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0392c0d4df27fac7af024a4d5be52463c499a708e5da38e9991cdf7297c5908e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c4d19f0d4db1459053e6ab17a4cc273d8d579180061f84f303b4d60fbf1629`

```dockerfile
```

-	Layers:
	-	`sha256:bca3410611e906dcf717ef4b5ad71bb956318fc3abe580bc2535defad6f11c31`  
		Last Modified: Tue, 15 Apr 2025 21:52:46 GMT  
		Size: 2.4 MB (2446804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0d4e5ee29705e38e68bef49684687fda880b8368be46d235f9084bd0ece2158`  
		Last Modified: Tue, 15 Apr 2025 21:52:46 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:afce91a38f28884dc5c8a3dbc46bbe095eec77fecd9779780281a00491bdcf46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337599579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e7b1455307e51bb35daf06581d7f41ef1b7c8713cb31f47aa668c7301eb2e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 14 Apr 2025 23:59:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_VERSION=1.11.5
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.5-linux-x86_64.tar.gz'; 			sha256='723e878c642220cc0251a0e13758c059a389cadc7f01376feaf1ea7388fe8f9c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.5-linux-aarch64.tar.gz'; 			sha256='f63203574fba25c9bda5e98b2f87f985d4672109855633a46bae32bfba3cbc0d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.5-linux-i686.tar.gz'; 			sha256='c2b6f5763edd994cb01407b8e71797bd25901cc513132d155953742f54b3a294'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.5-linux-ppc64le.tar.gz'; 			sha256='11ae7f0b83663de35d9a30e916373378f7985424c030a4a5af96aecc9b6eaa66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07b4f8f3342cdcbe71b46ef8121c7cb575c806d77f376239c5686c08f063b06`  
		Last Modified: Tue, 15 Apr 2025 21:54:09 GMT  
		Size: 5.5 MB (5538329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b6bf3d12f000b47d6e2e157599548dd1f7aeb552b9f2791a3f25077edd9035`  
		Last Modified: Tue, 15 Apr 2025 21:54:16 GMT  
		Size: 304.0 MB (303994557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0c358d92ae7a073bae7b89aed639ecc9dcdc1b0f776e13b85c9a8f8f29e2ff`  
		Last Modified: Tue, 15 Apr 2025 21:54:09 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e8f1cd86a9507f4245e62465bbd2450a684018a25543ad5dbd12d097272e842f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdefd13701f4c969e11f7307b1cc4c3ee122d77e584b76526e5a1c66173999d`

```dockerfile
```

-	Layers:
	-	`sha256:447ea621b2adcd938f14c0a3f2010ab1f2a72274cdba318be39276ee23dc8007`  
		Last Modified: Tue, 15 Apr 2025 21:54:09 GMT  
		Size: 2.4 MB (2447127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd56072c7e895efe8ab5268b1fbf2407a9e07dfabbd95174500bef2b8cd600c`  
		Last Modified: Tue, 15 Apr 2025 21:54:09 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:bfedacc83399c70b7b2eb61d2305aa78f35deeb5943c141beea243544ef7675f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272345386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381249d7685d624bef67e2184671375210b68ada7f6cd92c2904fca3464e1689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 14 Apr 2025 23:59:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_VERSION=1.11.5
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.5-linux-x86_64.tar.gz'; 			sha256='723e878c642220cc0251a0e13758c059a389cadc7f01376feaf1ea7388fe8f9c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.5-linux-aarch64.tar.gz'; 			sha256='f63203574fba25c9bda5e98b2f87f985d4672109855633a46bae32bfba3cbc0d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.5-linux-i686.tar.gz'; 			sha256='c2b6f5763edd994cb01407b8e71797bd25901cc513132d155953742f54b3a294'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.5-linux-ppc64le.tar.gz'; 			sha256='11ae7f0b83663de35d9a30e916373378f7985424c030a4a5af96aecc9b6eaa66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed1e42241413ec0478b46ef32c4d37d8bdc0ccd8ab79b2ab020d514b61c2f82`  
		Last Modified: Tue, 15 Apr 2025 21:52:46 GMT  
		Size: 5.9 MB (5872232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41362f1e3df90a3eac50cdb38d72da426c0aa03d2c7748f8aea6cd80b3195a6`  
		Last Modified: Tue, 15 Apr 2025 21:52:52 GMT  
		Size: 237.3 MB (237262052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f92092b5ca77d23c1fe3cbabc6a3f4a3bcf3b6f273e818a724556dcf8dd40e6`  
		Last Modified: Tue, 15 Apr 2025 21:52:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:2a56009626ec49ca9f10e6f9196f1d148d24739d99abff6daf4802f6bbe5b705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c36d8cf6c9e517ea5df79774d7f892464564c1c5582d2fd8275f7593d40c7fe`

```dockerfile
```

-	Layers:
	-	`sha256:356778e19475d0a5262f4c2d1e2d270b8da7654abe8bb5e52e7228ce5296cedb`  
		Last Modified: Tue, 15 Apr 2025 21:52:46 GMT  
		Size: 2.4 MB (2443877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bac87f6d5d8ff7b2e8d19999514aac00c9d7b7e3edfad0df16f191855a6018d`  
		Last Modified: Tue, 15 Apr 2025 21:52:46 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:9872c71bc4187b0f5cebf4aaaea85b87a8cc92eb12e4768018427d18a83bed99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286604313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0396c072c23e0a1459dcde5170d0cf5c7ce9efe201eb136c3a705d0a3597c5aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 14 Apr 2025 23:59:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_VERSION=1.11.5
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.5-linux-x86_64.tar.gz'; 			sha256='723e878c642220cc0251a0e13758c059a389cadc7f01376feaf1ea7388fe8f9c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.5-linux-aarch64.tar.gz'; 			sha256='f63203574fba25c9bda5e98b2f87f985d4672109855633a46bae32bfba3cbc0d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.5-linux-i686.tar.gz'; 			sha256='c2b6f5763edd994cb01407b8e71797bd25901cc513132d155953742f54b3a294'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.5-linux-ppc64le.tar.gz'; 			sha256='11ae7f0b83663de35d9a30e916373378f7985424c030a4a5af96aecc9b6eaa66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7819ee1da072436e9699315e84aa318074d22424232760df37b294dcc7602ead`  
		Last Modified: Tue, 15 Apr 2025 21:53:47 GMT  
		Size: 6.2 MB (6249560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af44edf2164c4b57c5cf640e81d30a2539736edb3bc64abcc94e8560b45467ce`  
		Last Modified: Tue, 15 Apr 2025 21:53:53 GMT  
		Size: 248.3 MB (248286150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2856ad96f1608b885a014a8dc704f48de1a53c6ac2c61bfb26ffe7badb094f`  
		Last Modified: Tue, 15 Apr 2025 21:53:47 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1723ec330a690962a841d1763016770464a53b063d7b2d7cdda2945fc026a9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68e7a0f91129a79b24ea01aba2908bb08651778de5ba922a9c578ad28d30fdf`

```dockerfile
```

-	Layers:
	-	`sha256:5eb767f66b02c34a78e55cd002f4d57925217c5fcc460e933f3b70d3301658d2`  
		Last Modified: Tue, 15 Apr 2025 21:53:47 GMT  
		Size: 2.5 MB (2451236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7fe7e33db6fd9379b55b4a03e126c0efde8599be8bd2e959f496b14b0f17b0`  
		Last Modified: Tue, 15 Apr 2025 21:53:47 GMT  
		Size: 18.5 KB (18469 bytes)  
		MIME: application/vnd.in-toto+json
