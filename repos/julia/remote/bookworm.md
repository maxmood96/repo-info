## `julia:bookworm`

```console
$ docker pull julia@sha256:8daf075796cbb51bf55feb60fc42d0dd51d52e2191e06cb61f1e6614fdca1e5d
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
$ docker pull julia@sha256:85001266b33f1661bead8d273681da4f25cbb112ec57239330b866050afabf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327517243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3520d0ed73ae9c4aba6a415dd1d51987980cfea07cadfac11932ec6bb1faf15e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:20:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 24 Jun 2026 01:20:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:20:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 24 Jun 2026 01:20:55 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 24 Jun 2026 01:20:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 24 Jun 2026 01:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e870ac1d3febd0cdfb12d7d57a364ced9f6d7e9f04feeb88829392f5b8604f`  
		Last Modified: Wed, 24 Jun 2026 01:21:39 GMT  
		Size: 5.7 MB (5721512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c0f76303fd773befdfe9a6cd9b224a1e47696138a3d22a0057f912d67ec655`  
		Last Modified: Wed, 24 Jun 2026 01:21:45 GMT  
		Size: 293.6 MB (293557721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e25abb4711a141bbb59b16a83d57223b9b992d6aea74c9fc736ed9d48ae6d1`  
		Last Modified: Wed, 24 Jun 2026 01:21:38 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:195dbebea59be5836c8b6ebf30d5f197d331f2d3f9679366862b7153a0660d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47de61b0882abc555ca57b2102be4c586e14bb21bc756d86bfab9200f73619f`

```dockerfile
```

-	Layers:
	-	`sha256:ebae78db5460ed709152ba9678ef6232d79cf37cf03d4fb03ba8fd58fbe7535a`  
		Last Modified: Wed, 24 Jun 2026 01:21:39 GMT  
		Size: 2.6 MB (2567732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43720a303899b74335bda021869c5f81b973705aff3208d3d1b793beb571bcb9`  
		Last Modified: Wed, 24 Jun 2026 01:21:39 GMT  
		Size: 16.5 KB (16547 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b03514f8bdad9b46375f27445ac9f15c4beb78410cf895663b4662871d4b914f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (347951941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5530f0a09b639fa370451570c999891950d05a7c4c5aed3c34b0a90990f78d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:20:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 24 Jun 2026 01:21:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:21:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 24 Jun 2026 01:21:01 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 24 Jun 2026 01:21:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 24 Jun 2026 01:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccff35babe08bf7952aef6beefef9022bdc7c5e83cfd38797cd0461ccece649f`  
		Last Modified: Wed, 24 Jun 2026 01:21:48 GMT  
		Size: 5.6 MB (5570447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9174403a9efbb324fbdb28efaf2684f390cae93ebd59b2ca63e7e5923127ff`  
		Last Modified: Wed, 24 Jun 2026 01:21:54 GMT  
		Size: 314.3 MB (314258707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f69ad8afe85647b05f88aa1d6f90f0ba80f451e2fdd4ca01743fd7cc53209b5`  
		Last Modified: Wed, 24 Jun 2026 01:21:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:4b9d0139973fddbd5d176a027c3e69828dd09a9acd8f19d5101f9e9ae44d5834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a398ce4764a73718b27ccbb9a53295d91e5dca4469bbe32d856a762cfddbb`

```dockerfile
```

-	Layers:
	-	`sha256:b3297b43e9af53ce882e9f7ac558ad77d8bf583ef8efbbdf1f2cd2a83309058e`  
		Last Modified: Wed, 24 Jun 2026 01:21:47 GMT  
		Size: 2.6 MB (2568007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8b71d1812017c60cd107db541b05e400b61a6093ca82ab879867dc792de6b7`  
		Last Modified: Wed, 24 Jun 2026 01:21:47 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:423ca6f259c21d25a533bb7ef7170e409c4b7753f01ff4cf69e03c3fada04983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.6 MB (267560142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbf2f187faac2099c1f94f5a808beb9bb44810d3d11b163fe924f164245ceb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:16:53 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 24 Jun 2026 01:16:53 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:16:53 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 24 Jun 2026 01:16:53 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 24 Jun 2026 01:16:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 24 Jun 2026 01:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:16:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df519b11ac99d8e2d452cbd55f824e658d0b86f649745abaaf8cbe33e2736a30`  
		Last Modified: Wed, 24 Jun 2026 00:28:03 GMT  
		Size: 29.2 MB (29225809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600e1bfb9d4bac78b48134d1651747655bbfd337865198fdaab4cd273e9e8cc`  
		Last Modified: Wed, 24 Jun 2026 01:17:25 GMT  
		Size: 5.9 MB (5879991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8c5f74a6a373cae591a42d9eb0c84c9c71c7e627e703fed13c996e442daab1`  
		Last Modified: Wed, 24 Jun 2026 01:17:29 GMT  
		Size: 232.5 MB (232453969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacd6d0a464c5c1ace9e1596d1d5078d290d6452f19b58f63cafc693e36d5247`  
		Last Modified: Wed, 24 Jun 2026 01:17:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:28fd582ff0415a3148a3f3ba1ea7e6b00a53fb6d9ff40b9caa232922b96a4bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bbedf6fe5061dab39ffd220761cfc8c7897a692fc3c54ef5713bb71a48da2b9`

```dockerfile
```

-	Layers:
	-	`sha256:c408004df27eed2b36aee51c2505e9bc6c361862c56f339e8258341dd05e0fd1`  
		Last Modified: Wed, 24 Jun 2026 01:17:25 GMT  
		Size: 2.6 MB (2564879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fe30707383ce295ac098bae297fb4345b51681cd4ebeab019d347b946083ad`  
		Last Modified: Wed, 24 Jun 2026 01:17:24 GMT  
		Size: 16.5 KB (16513 bytes)  
		MIME: application/vnd.in-toto+json
