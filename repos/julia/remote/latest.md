## `julia:latest`

```console
$ docker pull julia@sha256:940e828a6123fa63a8ed1ed29f3d818c4ce9683dbbd499154630a4da34460f69
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
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `julia:latest` - linux; amd64

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

### `julia:latest` - unknown; unknown

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

### `julia:latest` - linux; arm64 variant v8

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

### `julia:latest` - unknown; unknown

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

### `julia:latest` - linux; 386

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

### `julia:latest` - unknown; unknown

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

### `julia:latest` - linux; ppc64le

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

### `julia:latest` - unknown; unknown

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

### `julia:latest` - windows version 10.0.26100.3775; amd64

```console
$ docker pull julia@sha256:da8380351f5c20a42e77ef4352cb4bc238c8900a6d5987342775bd9cbcd4854f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3680267445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9b15ba2563f1a95069959638ada6ee1a6e913ef06281f6444e2fa1c2a3baad`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Tue, 15 Apr 2025 21:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 21:58:36 GMT
ENV JULIA_VERSION=1.11.5
# Tue, 15 Apr 2025 21:58:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Tue, 15 Apr 2025 21:58:43 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Tue, 15 Apr 2025 22:00:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 15 Apr 2025 22:00:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8cc15862a2e6faa6b7c2aef9525ad997936d7f213ccbe43f70b1aa57b530c9`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655a1219e626e2d72d38099f28627b8e3d7bd360aa48aaffb44528b9208fd9cd`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c57154cd54d9aad740a4cdc99c11418f28e436c76fbe5797d314f66589ba083`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a2feaaeef37345a6b592063b4b13b54465bc0d4a1df39cb8b7957656c1b3a8`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0acffce31438a2cdb404e35eab8a50ccf4575b51074bd0535ff9f4394d374`  
		Last Modified: Tue, 15 Apr 2025 22:01:01 GMT  
		Size: 285.6 MB (285581419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda492c83d33cc6270f6624469632fde9a3736245e480a6da77f31c2e9964fbd`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.3453; amd64

```console
$ docker pull julia@sha256:4692a238c3a42cf0ad01ac03858884d3c39d65933efc0e3bf99bdf310a5d557b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556462029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da15b5affb2d343f2e5d168430aaaeb121e4339abb5a0283440d268849fa419d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Tue, 15 Apr 2025 22:11:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:11:27 GMT
ENV JULIA_VERSION=1.11.5
# Tue, 15 Apr 2025 22:11:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Tue, 15 Apr 2025 22:11:28 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Tue, 15 Apr 2025 22:12:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 15 Apr 2025 22:12:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0668eb4ab6538a007d7d921f86dc81fc9e022fd4281369049af6b80a4ca828a5`  
		Last Modified: Tue, 15 Apr 2025 22:12:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945d11cd5e04d63d6222d3278f37c4dd6d6994df62da17aac8e71ac22f1db208`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201bd3be521ed32686d3e4564f52d6bd04aa55f25883d5479fc22c38aba4d32f`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5decd5cb85982b35960661bf50aa7eeef035d39f2799fad05c045df687a67a`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39ff4897cace2368d20d6984fed7f68f1a17c1fac2bc1231d8fe911a0f7f62b`  
		Last Modified: Tue, 15 Apr 2025 22:13:29 GMT  
		Size: 285.5 MB (285459956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c626e16efd1d216f79e2bd6ef4ee6c53c79fd08210696141dcfa6c7dd8a1ef0`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.7136; amd64

```console
$ docker pull julia@sha256:3cd406ae39c86f599deea0b1950ddb0785de06e78339947ddc5f32d4f59e36e1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2448173278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f73564b63db4d2693ce368c6caf86faa0efa86aca21d9807d0fd632ed5be3e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Tue, 15 Apr 2025 21:58:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 21:58:31 GMT
ENV JULIA_VERSION=1.11.5
# Tue, 15 Apr 2025 21:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Tue, 15 Apr 2025 21:58:33 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Tue, 15 Apr 2025 22:00:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 15 Apr 2025 22:00:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a6e7d6f7409481b381eecddc0b058c381adb10b23f07ca069bf360461a0623`  
		Last Modified: Tue, 15 Apr 2025 22:00:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9974842900d4f42967d41714437ed0bfec017aef0af21072c184b410e7130faf`  
		Last Modified: Tue, 15 Apr 2025 22:00:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a383d2d34a0b5a3b8cf8fd04f9cefceff4154f59b556504a4e4ec8544bb9a534`  
		Last Modified: Tue, 15 Apr 2025 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a982983cc724b1c66fb2c77b8ee3724c4721302636e902e18f9f21c9277f8c1`  
		Last Modified: Tue, 15 Apr 2025 22:00:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b27e82e0767ec5e7e0405771e027d1e57f91b56a37f25bc0f3dcbdd3e6c77`  
		Last Modified: Tue, 15 Apr 2025 22:00:59 GMT  
		Size: 285.4 MB (285440974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b289b23c8c703f98dfb0a7c384735b1dcae5ef1a94b227bc5378384e8d11740`  
		Last Modified: Tue, 15 Apr 2025 22:00:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
