## `julia:1-trixie`

```console
$ docker pull julia@sha256:24e227518a8ecf61aa77d7cb029a9c56edffe671cbde99a38c729c7ff9b19b23
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
$ docker pull julia@sha256:cc2b9ebfd013947598603a9f9bbac40d63f957a9410de034d5bcfd83bc9bc927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321605939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86ecce8a3295076bca8832121eb62680831366970ed1f20f941a6820f2e8af8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0889c8bb95aa18b84532dfd502156db42cba2d8c0b30cfb3ec76ab1a04963ce8`  
		Last Modified: Tue, 21 Oct 2025 01:20:32 GMT  
		Size: 6.2 MB (6242738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab07ae5af87e55395d7a78c0d8356268da34776871307c3c515d6397b8d811e`  
		Last Modified: Tue, 21 Oct 2025 11:07:13 GMT  
		Size: 285.6 MB (285584907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0c721bba18679c4fffb0ef0a9df29102aacef9aeef8befd25e0a522d2ffbe5`  
		Last Modified: Tue, 21 Oct 2025 01:20:32 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7fae2b56b1294ef1f7912478183b6cafbd2a13ecd04a5ba206c3139b18cf6a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d00943a8a87a4793a67ca129a6867d9ea36d31a3e7158887fd41a5d000d7003`

```dockerfile
```

-	Layers:
	-	`sha256:10fede0f1789f3caecf9e43d9b4debfe5e892f5385fd4616bb20b21215072863`  
		Last Modified: Tue, 21 Oct 2025 11:02:20 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f811653abaa6097cbcfbe7984430b609094f16072695d852042a1bd976f7880`  
		Last Modified: Tue, 21 Oct 2025 11:02:21 GMT  
		Size: 17.7 KB (17726 bytes)  
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
		Last Modified: Tue, 21 Oct 2025 18:16:16 GMT  
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
		Last Modified: Tue, 21 Oct 2025 18:16:52 GMT  
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
