## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:aa4ba788fbe6337914ff8cce1d3587294978e5b15d3ec84c01c31e0b31764c1a
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
$ docker pull julia@sha256:3ddfc2888f1adbd89fdf078e8aff3d803de93815d5ce32f948a12dfc231979c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286966905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1f61868aa3ee4459ac14e07d9a242fd5935a497536b30ac3910a9cf2d1072a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Jul 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc2-linux-x86_64.tar.gz'; 			sha256='7416f969669761e3507ebb7b505075ca234a1785b438304c2b016f5ee00058ea'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc2-linux-aarch64.tar.gz'; 			sha256='947f48e9bf65217782b33be4ce0a9e4c07b5101121871da954c230bb63db9ab0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc2-linux-i686.tar.gz'; 			sha256='611428bdc5bef1e96f6a86ee5064ef0e22e3612891b8a27e7a129742dad4fe97'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc2-linux-ppc64le.tar.gz'; 			sha256='3ccbc68c091e6f52a490aeaac46ec24d528e1a41f4b817b7c715111dff169bbe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbb938a4c07faeb1ce96606f9974ed9a9bef13f712dfca59a77d1953fc9f45e`  
		Last Modified: Mon, 29 Jul 2024 21:57:08 GMT  
		Size: 2.4 MB (2426544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e105ca3ae034e8a0e5b8169af2dad94153f9dd4be4962f6cc3ae52eb91661ec`  
		Last Modified: Mon, 29 Jul 2024 21:57:13 GMT  
		Size: 253.1 MB (253111661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75c3311dcf38329a98064103b6e64c0c8ecc662676e4806c0ec963d4fcdc418`  
		Last Modified: Mon, 29 Jul 2024 21:57:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:9afbc7a572f85f6d2687ff56df6f6ddc59e81329635c709e799620e658277cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d792542b4f8208990a0e1126eb4e3697359716bbb4e0bad1fa7244dd60a5476a`

```dockerfile
```

-	Layers:
	-	`sha256:1025e1edb03ab0c393bdfe5110fbba106f30304d1156f3e3b2f8a788570ee3fc`  
		Last Modified: Mon, 29 Jul 2024 21:57:08 GMT  
		Size: 2.7 MB (2702845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcabec1d3d2a3a612cc3ef7e85f55270845360b61e20827fa031a60a55a5ce8c`  
		Last Modified: Mon, 29 Jul 2024 21:57:07 GMT  
		Size: 16.8 KB (16801 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1a3687484629cfbec446979fba94b7a1148d77da5976ba6be3502af1350311a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282533573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ed100676fc3da37009fc419bcddcff7b73873a1bc83167bda03edc73a50b6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Jul 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc2-linux-x86_64.tar.gz'; 			sha256='7416f969669761e3507ebb7b505075ca234a1785b438304c2b016f5ee00058ea'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc2-linux-aarch64.tar.gz'; 			sha256='947f48e9bf65217782b33be4ce0a9e4c07b5101121871da954c230bb63db9ab0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc2-linux-i686.tar.gz'; 			sha256='611428bdc5bef1e96f6a86ee5064ef0e22e3612891b8a27e7a129742dad4fe97'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc2-linux-ppc64le.tar.gz'; 			sha256='3ccbc68c091e6f52a490aeaac46ec24d528e1a41f4b817b7c715111dff169bbe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a9d12ed3370fd9d003064e602b24acd65bdaf4509a3c1d1f8f7d2b089e44f3`  
		Last Modified: Mon, 29 Jul 2024 21:58:18 GMT  
		Size: 2.4 MB (2415142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e684c22ab290503d7472f7038a9ebdc9df6b9b13f038b6f73b695742d7f24`  
		Last Modified: Mon, 29 Jul 2024 21:58:22 GMT  
		Size: 250.0 MB (250041975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5059e177ecbc8b2868dc9b617e7c545bb963cc7489ab40938aa4696e844c5`  
		Last Modified: Mon, 29 Jul 2024 21:58:17 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:934659b0afb842ae183ffc3ccfdfda20b0a5e5c437df1ee821a0fdcf82244b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992f7133870097e3055dd01b49a94371999077bfcc678d6a2520efb79e17ac70`

```dockerfile
```

-	Layers:
	-	`sha256:ab68db13dc2eb586c3d3d845357388db7337568d0ad4eb927462301bcd62bff2`  
		Last Modified: Mon, 29 Jul 2024 21:58:18 GMT  
		Size: 2.7 MB (2703095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:123ef4c71e306a8743e8f159ce6eceaf899e8eb5c13a99708c90ce32e2d3549b`  
		Last Modified: Mon, 29 Jul 2024 21:58:17 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:14835065e77b933d85deedbbe77061946458f4ce2cf50a45ed8cfe158dc063e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265841254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7c862fa8c9d52e7717c4f56b66e3d5f002f669bf884c9fb8775e5c9091193d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:35 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Tue, 23 Jul 2024 03:54:36 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Jul 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc2-linux-x86_64.tar.gz'; 			sha256='7416f969669761e3507ebb7b505075ca234a1785b438304c2b016f5ee00058ea'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc2-linux-aarch64.tar.gz'; 			sha256='947f48e9bf65217782b33be4ce0a9e4c07b5101121871da954c230bb63db9ab0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc2-linux-i686.tar.gz'; 			sha256='611428bdc5bef1e96f6a86ee5064ef0e22e3612891b8a27e7a129742dad4fe97'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc2-linux-ppc64le.tar.gz'; 			sha256='3ccbc68c091e6f52a490aeaac46ec24d528e1a41f4b817b7c715111dff169bbe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a601c0942f94d447b4890c05f1cf3aa55f6a78f4f1c42adf061a9a1ea285fa8`  
		Last Modified: Mon, 29 Jul 2024 21:56:58 GMT  
		Size: 2.5 MB (2533044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ab24659fc352863d47f30e8f8f129edd3c6cbf752b1c27e772264f16314838`  
		Last Modified: Mon, 29 Jul 2024 21:57:04 GMT  
		Size: 230.9 MB (230894033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0b737fdb0ae06a1bf775fe90af233ffc78a29d45f3caeaaa372437214d238f`  
		Last Modified: Mon, 29 Jul 2024 21:56:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:96dcfa45b30c4fc421cc0045d4a0fa8debaaff7fe8707529ec10b327037ee887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecc8996ec7aefc8118efd53cabf14a78b25b19238f7d293664f7b6f96d9e2e0`

```dockerfile
```

-	Layers:
	-	`sha256:cc78fba63af1609ca35aa4ba96aef082c7a30a9619eeae4517af48a23a681f30`  
		Last Modified: Mon, 29 Jul 2024 21:56:58 GMT  
		Size: 2.7 MB (2699948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762d859dd4c207c175dc0dc4b9a732f121ff532d40f75edee3384038c3cbf239`  
		Last Modified: Mon, 29 Jul 2024 21:56:58 GMT  
		Size: 16.8 KB (16775 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:301ffe922c71d43863b73a152d9684073a222ca428a9a5f63b00ebdee9d59a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278932699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095c2b325e2886db65b85218ba83c79372c2d83301424c89d6ad738ef33febbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Jul 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc2-linux-x86_64.tar.gz'; 			sha256='7416f969669761e3507ebb7b505075ca234a1785b438304c2b016f5ee00058ea'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc2-linux-aarch64.tar.gz'; 			sha256='947f48e9bf65217782b33be4ce0a9e4c07b5101121871da954c230bb63db9ab0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc2-linux-i686.tar.gz'; 			sha256='611428bdc5bef1e96f6a86ee5064ef0e22e3612891b8a27e7a129742dad4fe97'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc2-linux-ppc64le.tar.gz'; 			sha256='3ccbc68c091e6f52a490aeaac46ec24d528e1a41f4b817b7c715111dff169bbe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86144fbef12278f03ca188ac253ef10628ad658b066b7617ea42f57f5b6d4182`  
		Last Modified: Mon, 29 Jul 2024 22:00:14 GMT  
		Size: 2.6 MB (2629954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4856319c6f0b11174e6d643c588aae35c681027fbd3d04a405d815edab81e3`  
		Last Modified: Mon, 29 Jul 2024 22:00:20 GMT  
		Size: 241.0 MB (240997171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0881fad9b1620bded692ce67c5401520f4c4601fe96c9d0ccaed1b254d2684f1`  
		Last Modified: Mon, 29 Jul 2024 22:00:14 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1d750d74c567234349ed3a91f1a36cb9b4c39a0ab454ae2d0e3d0f4767530778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2724069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8094acc86f4c8f75ab5a5fb2a0287c107824efb3267f95fc4b9bbee6539ca821`

```dockerfile
```

-	Layers:
	-	`sha256:2b29242358b1f7c12447397c2981d753293c11a21d29ae6ab7dfc5ee5f111b8c`  
		Last Modified: Mon, 29 Jul 2024 22:00:14 GMT  
		Size: 2.7 MB (2707234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8fe52974ad8f541bd466a9585a6a22e94dc5f6474e0e3ead5584176e97e097d`  
		Last Modified: Mon, 29 Jul 2024 22:00:14 GMT  
		Size: 16.8 KB (16835 bytes)  
		MIME: application/vnd.in-toto+json
