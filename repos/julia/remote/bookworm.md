## `julia:bookworm`

```console
$ docker pull julia@sha256:b0cfc314abf40fbe8c80efb3d0a545cb5a8581d2d38e33d9c0f3b7693b054c08
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
$ docker pull julia@sha256:c46feee3cfafa729a5ad78624cadd79196096ed1c8ab29d1144cc95424dd2a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327513118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df869af6edafa7ffd25493fdd62f715d16aa5de2def73d865ec67bf173cc15e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:20:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Apr 2026 01:20:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:20:58 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Apr 2026 01:20:58 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 22 Apr 2026 01:20:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Apr 2026 01:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:59 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df787f5d537204cdd4899275702302405b60e14ef8602446cc681d03e9acf35`  
		Last Modified: Wed, 22 Apr 2026 01:21:44 GMT  
		Size: 5.7 MB (5718731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e84301b651da737d3955089a62c1c914403f4df08813ddb6f1f83a4540ec1f`  
		Last Modified: Wed, 22 Apr 2026 01:21:50 GMT  
		Size: 293.6 MB (293557766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2839935aa6ca28ec0539e7f25e13bd31f9bc50588f2f45058b988a1def97342d`  
		Last Modified: Wed, 22 Apr 2026 01:21:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d4a66e62c072a519fac41799a618cd781eae55f53965df670bfa416cb6ac2d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e883bbcebaf94f544d58e1176e494d1a3faba0d996a191b0c6ba037e1fcf683`

```dockerfile
```

-	Layers:
	-	`sha256:5a929cf177bfd6fcb422867b62b869c7bbfc44f369a16b80c82e156c1cb62b32`  
		Last Modified: Wed, 22 Apr 2026 01:21:44 GMT  
		Size: 2.6 MB (2567696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:476faf99ad5574fb05f117ec466ebd7aec77b2e68a6660a55070a2ee936b0987`  
		Last Modified: Wed, 22 Apr 2026 01:21:44 GMT  
		Size: 16.5 KB (16547 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3865c40f3632455ba2defd295c94a6c2a96e55b3f3cce5613c05632b611eeb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347943822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19944bd88746c8cc6be93643cf4f826e2dc313e77db9ccee5b1ddf95f8400c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:20:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Apr 2026 01:21:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:21:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Apr 2026 01:21:12 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 22 Apr 2026 01:21:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Apr 2026 01:21:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18df875ebc767c6a8c6d59ebf2b550cc357858d9199fe33b28b3f32960782393`  
		Last Modified: Wed, 22 Apr 2026 01:21:59 GMT  
		Size: 5.6 MB (5568625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84833207baee110c3e79722c9a5535e400745e4b8a2b9c3b1673940e2de700bb`  
		Last Modified: Wed, 22 Apr 2026 01:22:06 GMT  
		Size: 314.3 MB (314258712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc92b52f3e82bb36de3f935fdeaf3749fd7282b1124e73bac44dac45544f354`  
		Last Modified: Wed, 22 Apr 2026 01:21:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f6bb0be34e7e9812082959859c87a62e6cb4d0cac0ac7c159d4498ba27a23e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb118907dbfa99217f865c086e3a2cc4ccbb3c699d2e2c7f9e9f8f0328e60352`

```dockerfile
```

-	Layers:
	-	`sha256:4cc118d11eda0ec6c12c52a40ef06e7924e13f12dca593ffa286611da0cc557e`  
		Last Modified: Wed, 22 Apr 2026 01:21:59 GMT  
		Size: 2.6 MB (2567971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1748d22e06030fb958c2ab7e79ecfc1ef5b6019996f9c0e10fbb1859fc0a733f`  
		Last Modified: Wed, 22 Apr 2026 01:21:58 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:4348ffd7c7626d80e22d0e3e8c0854e8372c85d1ec55f0d33e1aad825d3893f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.6 MB (267555488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e892ed12cad376535155859442bf9b0d86201a121197138d1ef4c9648240260`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:16:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:17:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Apr 2026 01:17:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:17:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Apr 2026 01:17:01 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 22 Apr 2026 01:17:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Apr 2026 01:17:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:17:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ceab9188c99bb4807b7b5b31c76962e728b9040bd3676ebeeabf72b13d039523`  
		Last Modified: Wed, 22 Apr 2026 00:16:30 GMT  
		Size: 29.2 MB (29221696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e752b9778894afbf661c4278eb1cfab03331aecb02e5bba7f789aba1baf47c83`  
		Last Modified: Wed, 22 Apr 2026 01:17:33 GMT  
		Size: 5.9 MB (5879526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc8726729d01a135fe03018b8340ac77d6d514f38fa67f7150713f1a3f7a57f`  
		Last Modified: Wed, 22 Apr 2026 01:17:38 GMT  
		Size: 232.5 MB (232453897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49187383d82367599539246296d8b2c881ed03a50763091174a0f835f4a46e5`  
		Last Modified: Wed, 22 Apr 2026 01:17:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d0ba5acf131843f38679a347550dab8a7b737f347aedc3d8624462faaf691560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3028d63fbd07bf061effdbb9d6442cb1fefb4413fd0a343a23eb1c83c98f54f8`

```dockerfile
```

-	Layers:
	-	`sha256:b596b91cd4078fae66c93fdc347d8ff12ba817e10e73364767c7db17a3cabc04`  
		Last Modified: Wed, 22 Apr 2026 01:17:33 GMT  
		Size: 2.6 MB (2564843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6eafea050913f4024e6d49f7fd68a923a8e70a1d0ac3b5224b76fea8703fd2`  
		Last Modified: Wed, 22 Apr 2026 01:17:33 GMT  
		Size: 16.5 KB (16513 bytes)  
		MIME: application/vnd.in-toto+json
