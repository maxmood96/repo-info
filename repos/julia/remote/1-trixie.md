## `julia:1-trixie`

```console
$ docker pull julia@sha256:0d11d89a94c97c35ba7f1acc8e77287b47dbd69a24e078b210d11c21f69ea7dd
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
$ docker pull julia@sha256:100a16e7795fe132b16f6d276c5d55a9b9e9b663ef74534d9f1e77e116cb6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8288ace8a3f30304d5f5f6cfe7d0ce2200a3be251f5ad78b2240d3b2c421c9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb54a235ac43c57eac877411d6355c41017d5faef37fde2eb768aa00781efb`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 6.2 MB (6242815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0dd40c781b44127c5eaafbb88fd7a1dc82e5914ed7feafa9c3e3450977a71`  
		Last Modified: Tue, 21 Oct 2025 23:03:12 GMT  
		Size: 289.5 MB (289509752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8184e382675284be5b296eedf07655a48e9e4edf5c410d2fc5d02957a1f6f`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7108d157010090f6c301b858906e7ab22f23a359349fb21a0461a7539c8173b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03255e51f7d62fc8470a4f2ac323c216a74e10df7e3535113bdf885be9c0af`

```dockerfile
```

-	Layers:
	-	`sha256:f0d77c3c948134d3fd7b17e391096b10a5f4e18c99b8199740e998bda7315914`  
		Last Modified: Tue, 21 Oct 2025 23:02:17 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bdf79615d1bf8502b1acf50226bc4edc3b6b948933d6eb8e91a0659bd5d80`  
		Last Modified: Tue, 21 Oct 2025 23:02:18 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:51d8357e427dad5e9664ec71f22cb0bb92f051207ce5e52f6f2212b919ff1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a388e5c76234c765df9be5ee6dab9786d1692abc23d7de21e7fd7bfed3a09537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9cd5ffd680616fec199e43e07c69ffc88c2b0852eb7f918d616adc3140dec`  
		Last Modified: Tue, 21 Oct 2025 18:16:23 GMT  
		Size: 6.2 MB (6153056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3f146333de7f6b9351b4b2301d9e47acec5cc50866e27c948c0542a960d105`  
		Last Modified: Tue, 21 Oct 2025 22:34:41 GMT  
		Size: 310.2 MB (310243585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5d1ba56190d917d38b12f38c22e2b05ffd4db08582102d22b0cbae187c9a1`  
		Last Modified: Tue, 21 Oct 2025 18:16:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6c5bace6b0ee197421606a5b21ee216f04ab2cc1e8a34481019f021cb9756f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740e8034facf342b8cd0d1d019e62ae5ec6ad7b7f19af288ca461beca83bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:259cc1f36a4b91356421af6402bf017844606f27b2f8740b4033bb370cd819e0`  
		Last Modified: Tue, 21 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff67604e4a9232b4d114b4582b87f778a3c9d05cf0968f2a7d1da0df524bb7ea`  
		Last Modified: Tue, 21 Oct 2025 20:02:28 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:9b218ed258b8d54a63292566fdb4b3fb9500bb8f488f3823eb16fb1fbb8e1326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643168051df497002232e3c36e6863975d0bc4f4a4684f0da5effd804d0eabbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2226dfddcc86e89e175e51f92adbe160691f1050abb8b9a84c837c0d8ac6e`  
		Last Modified: Tue, 21 Oct 2025 18:17:16 GMT  
		Size: 6.4 MB (6427772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dcadcb45a78c0e624ef20df5fd71215a81db5ade8f7332e8fa9a217896bb2`  
		Last Modified: Tue, 21 Oct 2025 22:34:30 GMT  
		Size: 231.0 MB (231034237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f938d913ca31948e13e6a2d685fb3d6856737372b93805567106c6e8b0f450`  
		Last Modified: Tue, 21 Oct 2025 18:17:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a4641c1e22d06855f3c86435f1afd4576b3c5ab8ed2a5097c952463e2b29f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3ae68a676abdd1bc2fd91f0a87fb5d9be17345ba3225160b43b1324a12bc`

```dockerfile
```

-	Layers:
	-	`sha256:82c177774996f99c945f5a339402dca10f4f0ecf3ac85c03e722873bc3e3d5fd`  
		Last Modified: Tue, 21 Oct 2025 20:02:32 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc02343c4dbfd7d1a597c2d8bfdb06d5f059f071cc6cb30208a3ea21406adad`  
		Last Modified: Tue, 21 Oct 2025 20:02:34 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json
