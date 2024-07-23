## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:c44ee239f238e4bf7700aa0b9b3b6b592b25ab89f390fb6dac3b0eaca7b03b7c
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

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:8bdba05d98152938ecbc0b5b0d97e6ed7279bef239f80b9863c06b55f7953234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287428294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7653ffcfe902d209f5ca767cf726dce4b69f37ccc480fbdb93e6e895c195536d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Jun 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc1-linux-x86_64.tar.gz'; 			sha256='d9d7ca81087185abbb8a375c41f734deea6ea26aef2dc40d99467f8c5c7cc8d6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc1-linux-aarch64.tar.gz'; 			sha256='192e6c92969a84b8f76e113286b81b166fe04a7c5ff6c6b44a73e494c9f7f3a5'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc1-linux-i686.tar.gz'; 			sha256='546aed60e6b6e5e5568562f299ddf1987d01f369f0243db0b8694ee83ced9809'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc1-linux-ppc64le.tar.gz'; 			sha256='79870070dfc7b283691199da017f5db9dc86a8ed2260acfbb34f7e12fa9af8be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f6a175425ff028f586e7fedc90ccdc0475f99c9ee9a87ba52b855df835739b`  
		Last Modified: Tue, 23 Jul 2024 07:15:26 GMT  
		Size: 2.4 MB (2426500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ff607bbdbd1025ee937c174ca1a68108cc66cbc56026f79d4c4fc1a28dcf44`  
		Last Modified: Tue, 23 Jul 2024 07:15:32 GMT  
		Size: 253.6 MB (253573094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5004070cb81761563ae8712a9cc329f48e9df01cb8eb664fe46ae75e6ea396c3`  
		Last Modified: Tue, 23 Jul 2024 07:15:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d81baaaa1f231c3b1fb11c2e3dac4a49a75b6abadf08cba4edf5d0b63199d73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa536a42395f0d03b0d4d864c4af88a05baba698379e652d6a74eb36e4b8e01`

```dockerfile
```

-	Layers:
	-	`sha256:3177f2e775c231c7ba878ca80506d0c4065390519c7ac94eef2dac4c2e0d7737`  
		Last Modified: Tue, 23 Jul 2024 07:15:26 GMT  
		Size: 2.7 MB (2702845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5720f0640a1829c60ee766dd3d7c66f6cb8e599eda3193f5cf08c65de4fc4e5`  
		Last Modified: Tue, 23 Jul 2024 07:15:26 GMT  
		Size: 16.8 KB (16800 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d5726e0dc657db2f5d69f345eb1d419a66a03dd0a8871930317b796596d61fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284561590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6746bd0e02359b72baaaec5e511be64fa0d4a7b9b3c29758c183d0bbb5ee36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Jun 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc1-linux-x86_64.tar.gz'; 			sha256='d9d7ca81087185abbb8a375c41f734deea6ea26aef2dc40d99467f8c5c7cc8d6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc1-linux-aarch64.tar.gz'; 			sha256='192e6c92969a84b8f76e113286b81b166fe04a7c5ff6c6b44a73e494c9f7f3a5'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc1-linux-i686.tar.gz'; 			sha256='546aed60e6b6e5e5568562f299ddf1987d01f369f0243db0b8694ee83ced9809'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc1-linux-ppc64le.tar.gz'; 			sha256='79870070dfc7b283691199da017f5db9dc86a8ed2260acfbb34f7e12fa9af8be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92d98b488a344d738b3aa093dccddd045a799ca29d31cd6a0b8f8675cec7d08`  
		Last Modified: Tue, 02 Jul 2024 15:35:27 GMT  
		Size: 2.4 MB (2415070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e992fed0c4368a45b807c7c0c1dc07d89572c176ac1344bfac5b20aaa82c93`  
		Last Modified: Tue, 02 Jul 2024 15:35:32 GMT  
		Size: 252.1 MB (252076532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea429636a9c6e334cf89c06e4a6e9947fb635ef8f3c62fb71c8137ca03c8c3f3`  
		Last Modified: Tue, 02 Jul 2024 15:35:27 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8b39bd8da43063ec835738002713d06ad5cc4e23ae9b9823b70b7d2ac170b3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04380dc26c9eaefa15b42a35ac335ccc0b57885e2cc180afc2ae4ecdc46b6ffd`

```dockerfile
```

-	Layers:
	-	`sha256:455b7006a76ac487f53973c29d7a94393de9b0b011d465831bfad6a09928a510`  
		Last Modified: Tue, 02 Jul 2024 15:35:27 GMT  
		Size: 2.7 MB (2680416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d6dbbca013190b4caedb91d3b07efca162b8c843718a645ba19642c0c7e785`  
		Last Modified: Tue, 02 Jul 2024 15:35:27 GMT  
		Size: 17.1 KB (17098 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:e366e1e7086ea9e09cea6037b1de775a44cb2110f5d2dc452946762db655dca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266225958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accbfecf95b7c53e08ce8758cbe8461c3a2c2ea191d0268e3081077bb70b4cc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Jun 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc1-linux-x86_64.tar.gz'; 			sha256='d9d7ca81087185abbb8a375c41f734deea6ea26aef2dc40d99467f8c5c7cc8d6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc1-linux-aarch64.tar.gz'; 			sha256='192e6c92969a84b8f76e113286b81b166fe04a7c5ff6c6b44a73e494c9f7f3a5'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc1-linux-i686.tar.gz'; 			sha256='546aed60e6b6e5e5568562f299ddf1987d01f369f0243db0b8694ee83ced9809'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc1-linux-ppc64le.tar.gz'; 			sha256='79870070dfc7b283691199da017f5db9dc86a8ed2260acfbb34f7e12fa9af8be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05422d5ef8970a0eb4dc61532c3109c74933559735cc8ecdfdf3db46bc4e8870`  
		Last Modified: Tue, 23 Jul 2024 06:15:50 GMT  
		Size: 2.5 MB (2533040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc568583b70a72f7c1a8d628d8fa61b118d491618c0bb97c4f8508e10487b5b`  
		Last Modified: Tue, 23 Jul 2024 06:15:56 GMT  
		Size: 231.3 MB (231278741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b1b2662fd87f082d9950f3aa9a3a46100e0084c40651b119c247dc55775d8b`  
		Last Modified: Tue, 23 Jul 2024 06:15:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:470e09ab26a2a78be0e6a0d411497e17df64361776c26dc9148982c6562b67a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bc725f8ec6f1d32869d2aae08e3be75e349f43816201144cfc4fd82436a99f`

```dockerfile
```

-	Layers:
	-	`sha256:440dbf535369105c4613d10c5bd95a6b00e553c06c961f732cde5b8752a44ce0`  
		Last Modified: Tue, 23 Jul 2024 06:15:50 GMT  
		Size: 2.7 MB (2699948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a0e76432c802fec1b04ac8b7248976f9a4a4a7fe78adf9ff1c7a50a70c90313`  
		Last Modified: Tue, 23 Jul 2024 06:15:50 GMT  
		Size: 16.8 KB (16775 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:20076fd986ee4804f3f8a38b194277a4507580a87fa612c3436778bb55b604ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279509136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bbca7da1655f70ba5a61bd7448638fd818952ee011c389998dae80d78b4002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Jun 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc1-linux-x86_64.tar.gz'; 			sha256='d9d7ca81087185abbb8a375c41f734deea6ea26aef2dc40d99467f8c5c7cc8d6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc1-linux-aarch64.tar.gz'; 			sha256='192e6c92969a84b8f76e113286b81b166fe04a7c5ff6c6b44a73e494c9f7f3a5'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc1-linux-i686.tar.gz'; 			sha256='546aed60e6b6e5e5568562f299ddf1987d01f369f0243db0b8694ee83ced9809'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc1-linux-ppc64le.tar.gz'; 			sha256='79870070dfc7b283691199da017f5db9dc86a8ed2260acfbb34f7e12fa9af8be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6081646ddd04e654c8e83f1ff2f59b285687662bc8ab28253d4f29ca3658b4`  
		Last Modified: Tue, 02 Jul 2024 10:49:32 GMT  
		Size: 2.6 MB (2629955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af92b19d4d438bd8007cb594531a8d9f3777f6fcb0af63302f18544ac9a3990`  
		Last Modified: Tue, 02 Jul 2024 10:49:40 GMT  
		Size: 241.6 MB (241579624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a174ad934084b2e96d5bc768a15a7b3d2d9361784dbbca62ca98aa2bdec17de9`  
		Last Modified: Tue, 02 Jul 2024 10:49:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0896337ae5ffdfef8507e90819015d7b2802c9631eb7de5f47bca19cdb63c7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2701390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fee33c76c08942a21341c75e71f250579887e247f8ff3f154628b6c5cc08f06`

```dockerfile
```

-	Layers:
	-	`sha256:528410bb5a6e43387c6b88092bff4a5156374918f353ffd00fcd7215bd7c704c`  
		Last Modified: Tue, 02 Jul 2024 10:49:31 GMT  
		Size: 2.7 MB (2684555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09711be9df7fd695001a8ed079ac8d8e2fbee74922c1e6be02d7e93fb31a72c2`  
		Last Modified: Tue, 02 Jul 2024 10:49:31 GMT  
		Size: 16.8 KB (16835 bytes)  
		MIME: application/vnd.in-toto+json
