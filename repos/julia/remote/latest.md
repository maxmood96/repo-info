## `julia:latest`

```console
$ docker pull julia@sha256:d2375e33738225f57caa34096ad0a15c699512027931324c62ed1949d797a2ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:16aa86a6452c0c122c5ae7a6777a4f4fd6784905c00c10f0e4670d5c4b763217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210679546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e55098468339ab1b30a5ed80fd17d792da157f92441e1af2fc942214a2cc616`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 May 2024 13:40:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_VERSION=1.10.3
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.3-linux-x86_64.tar.gz'; 			sha256='81b910c922fff0e27ae1f256f2cc803db81f3960215281eddd2d484721928c70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.3-linux-aarch64.tar.gz'; 			sha256='2d52a61826872b3170c65f99a954bd9d21a31211cb50948056d924f811a0024f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.3-linux-i686.tar.gz'; 			sha256='f13be078c5ee7c98fd6a39a537199c253543acbd49bedc243f397cd51c7aeb58'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.3-linux-ppc64le.tar.gz'; 			sha256='61e4398df70129ce8184a2b84a12e9d862e92f35b526cd0297b5f2791ca628ba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 May 2024 13:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 13:40:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cda921d6dd2e362ccd5d45ec2fa260398a73e553c2c877bd19bb053e23b746`  
		Last Modified: Fri, 24 May 2024 14:53:45 GMT  
		Size: 5.5 MB (5515175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccb85e884c9e2809810eb6076ab556428c4e2a34256e90623506bbd0efc64b3`  
		Last Modified: Fri, 24 May 2024 14:53:47 GMT  
		Size: 176.0 MB (176013590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653f8bddebf5aaddbbe5c3ebc61b7dcc481dde6a7e3de5a3d35433c4daed2b0c`  
		Last Modified: Fri, 24 May 2024 14:53:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:8767f94e8140190e7c0f17345aa465a380c982dff37201dd962e838732c9db9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b6bf4e5d7c169150ad1fa64ca80cf08ab8b9513bc41c5b27c8d32d72278dca`

```dockerfile
```

-	Layers:
	-	`sha256:f601dd8171684c8e9b9791916a7db2f2c597dc2c473069b7fd6b04df82c89c54`  
		Last Modified: Fri, 24 May 2024 14:53:45 GMT  
		Size: 2.4 MB (2414589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:347fecacc7b2611a08ee618f8af891a0a22bf9eb37ce6aec7f58493121e97e10`  
		Last Modified: Fri, 24 May 2024 14:53:45 GMT  
		Size: 18.3 KB (18312 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:300dad596d13584a6387e50a535d915d98e9ea7a4144e2608dfcafdc4e49aae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212683876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3e93216c0aca724a435f3d375922f4ded22e0c6bb5130faa21b6d063fa3003`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 May 2024 13:40:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_VERSION=1.10.3
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.3-linux-x86_64.tar.gz'; 			sha256='81b910c922fff0e27ae1f256f2cc803db81f3960215281eddd2d484721928c70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.3-linux-aarch64.tar.gz'; 			sha256='2d52a61826872b3170c65f99a954bd9d21a31211cb50948056d924f811a0024f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.3-linux-i686.tar.gz'; 			sha256='f13be078c5ee7c98fd6a39a537199c253543acbd49bedc243f397cd51c7aeb58'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.3-linux-ppc64le.tar.gz'; 			sha256='61e4398df70129ce8184a2b84a12e9d862e92f35b526cd0297b5f2791ca628ba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 May 2024 13:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 13:40:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa053fb67d67a437e7d881b9c7529188bc7f949e90f10cb2c511315b3c89ad`  
		Last Modified: Tue, 14 May 2024 17:32:52 GMT  
		Size: 5.3 MB (5339363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0085814b24d7d066c94ea36087f196110630de72ecc808c11d9761416caf7c47`  
		Last Modified: Fri, 24 May 2024 15:47:00 GMT  
		Size: 178.2 MB (178164642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9271ef3181800c0d5f274c31f0107710e7b4789223e01165b24b64b024d45387`  
		Last Modified: Fri, 24 May 2024 15:46:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:ce3cf7b00eaad6537de052aa083023a8c051f32c048ae93148d545de8b66e0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c7fce6e9cd4950f9b1d2698a5de7b4c9b97ac0d4cdf8ad457d89d2e5fc0124`

```dockerfile
```

-	Layers:
	-	`sha256:6b511aa494989e937cbdb567ce25e25908dad8dfbdfd4f3ff1088d0e662bc0ec`  
		Last Modified: Fri, 24 May 2024 15:46:55 GMT  
		Size: 2.4 MB (2413853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c36c2eeb96c2d5f708ac0ef155aa92628fccb94a95994abd8a4b11d2d5bc145`  
		Last Modified: Fri, 24 May 2024 15:46:55 GMT  
		Size: 18.2 KB (18163 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:158c7238174b8138a5eae4439c50056184b4fbfa936fee7d5757b96b5a58446e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193383608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3dab469be081e0d0b4fff85f9b96e121fa4546aee96813a354b6f56524075c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 May 2024 13:40:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_VERSION=1.10.3
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.3-linux-x86_64.tar.gz'; 			sha256='81b910c922fff0e27ae1f256f2cc803db81f3960215281eddd2d484721928c70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.3-linux-aarch64.tar.gz'; 			sha256='2d52a61826872b3170c65f99a954bd9d21a31211cb50948056d924f811a0024f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.3-linux-i686.tar.gz'; 			sha256='f13be078c5ee7c98fd6a39a537199c253543acbd49bedc243f397cd51c7aeb58'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.3-linux-ppc64le.tar.gz'; 			sha256='61e4398df70129ce8184a2b84a12e9d862e92f35b526cd0297b5f2791ca628ba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 May 2024 13:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 13:40:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a0d458b23e31e2e2e903e2c2c34a073358cfec94bb28fcd13c88bea5cb3d43`  
		Last Modified: Fri, 24 May 2024 20:54:11 GMT  
		Size: 5.7 MB (5672142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a7a1d2c95551039fa722f0fc6d02e8de0374d38008ac0991e081c128c872c`  
		Last Modified: Fri, 24 May 2024 20:54:15 GMT  
		Size: 157.5 MB (157548460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef72620705d1c885992b2136b182cf89c537ef355fe598c16640a7d88076f00f`  
		Last Modified: Fri, 24 May 2024 20:54:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:b8a8de61e7625fa414d5d4744502bc4ddb84649b99132d9cd77ac1d20296ee96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91321eb5b8bcdd5f576b120dc3b172c0d6722a2b9c3f22556b866ac596ca14e4`

```dockerfile
```

-	Layers:
	-	`sha256:4fdd3f3a228e0472e34fd882fe75fdd62a40371ad4ba6025976ed756b8018451`  
		Last Modified: Fri, 24 May 2024 20:54:12 GMT  
		Size: 2.4 MB (2411661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb7d1444d58b66de09fe957962876494a1b76da3c25a12342d52994d9f1eb4c`  
		Last Modified: Fri, 24 May 2024 20:54:11 GMT  
		Size: 18.3 KB (18261 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:6a191181819716a957e9665eb6b3a750e95d9b8fe3755fb11a47839daa4b4c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193867984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f8e29cf7971e6a7c99ab680f4a13cb8000e5a0006427b85924566905f8c459`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 May 2024 13:40:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_VERSION=1.10.3
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.3-linux-x86_64.tar.gz'; 			sha256='81b910c922fff0e27ae1f256f2cc803db81f3960215281eddd2d484721928c70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.3-linux-aarch64.tar.gz'; 			sha256='2d52a61826872b3170c65f99a954bd9d21a31211cb50948056d924f811a0024f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.3-linux-i686.tar.gz'; 			sha256='f13be078c5ee7c98fd6a39a537199c253543acbd49bedc243f397cd51c7aeb58'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.3-linux-ppc64le.tar.gz'; 			sha256='61e4398df70129ce8184a2b84a12e9d862e92f35b526cd0297b5f2791ca628ba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 May 2024 13:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 13:40:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e3dfb42059f32c4dafe0538df9be69eab297a1e3043c2dce4da269ef34e06`  
		Last Modified: Tue, 14 May 2024 13:24:04 GMT  
		Size: 6.0 MB (6047044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8efd8566b5f3713553d482f6d8372901d531e62d9377ad749bc6926a832485`  
		Last Modified: Fri, 24 May 2024 15:13:14 GMT  
		Size: 154.7 MB (154679411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b7e2c3c5d52c501dccb0e909708d45d247210c3993401563c4afe9afff755`  
		Last Modified: Fri, 24 May 2024 15:13:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:0f2b42baa4022853cb402b4f85b39a3cec8c733f430264262e7c53abc89f13a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5dc99af7eb6b816e3c93482ce2ed16124f033897cb2f99149eeb092bd5c7b0`

```dockerfile
```

-	Layers:
	-	`sha256:97db1f94b176e4a68bfc560ef3e1b32aa678fb28f76c1368911ef99bd2c26817`  
		Last Modified: Fri, 24 May 2024 15:13:10 GMT  
		Size: 2.4 MB (2418047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:254d4c7d319105b2858691cfb66d78234d42eb2b0540916486ef5561e581a331`  
		Last Modified: Fri, 24 May 2024 15:13:09 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2461; amd64

```console
$ docker pull julia@sha256:1e4b7f5b44aa6558e933498902b86501ba7267ba62adb6f0938c8c4b71aba877
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299825052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2e252caf683ad4b7724e209776f69c1b734015a97c1e2f4f045baae5ca07f3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:51:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:51:17 GMT
ENV JULIA_VERSION=1.10.3
# Wed, 15 May 2024 21:51:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.3-win64.exe
# Wed, 15 May 2024 21:51:18 GMT
ENV JULIA_SHA256=688e746f3d8700ba44a6cbc9ce04ccead4cd921f093af80259e10d0b0c5448c8
# Wed, 15 May 2024 21:52:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 15 May 2024 21:52:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fd7d46b7dbed13742df5e22d2267ea056cdb3f70bc8f9147389bc632163f1b`  
		Last Modified: Wed, 15 May 2024 21:52:30 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0ed11d25d34f3a16d4292fde1a9e6b7da15fea76c4aa3308f487796b6273e2`  
		Last Modified: Wed, 15 May 2024 21:52:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8ff38bb3d607ec5a47b5be099ab8ff355f2dfe94e0f9f89b8f1618e460a6f`  
		Last Modified: Wed, 15 May 2024 21:52:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0caba2abc5dcf37b39c313426a082246e87ca46087766af4432c54ecee5c6f`  
		Last Modified: Wed, 15 May 2024 21:52:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd124ff2baef897040b4efae42ab088239a99b382bf1a8e825861118af18719`  
		Last Modified: Wed, 15 May 2024 21:52:52 GMT  
		Size: 187.1 MB (187147246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e8b432882aec9f9a09afb6546b7c41c6da75cd8a4531c7f2d0b019fd1f2ca2`  
		Last Modified: Wed, 15 May 2024 21:52:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.5820; amd64

```console
$ docker pull julia@sha256:0824a81f2228a9f89ee654725201e60dd26d2aaa87f13fead1b9517945785bab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2366981500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190274e4a5cc0e7316ca0b3308f72cc73637f9c2a18f529aaff476a77aa02a38`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:51:17 GMT
ENV JULIA_VERSION=1.10.3
# Wed, 15 May 2024 21:51:18 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.3-win64.exe
# Wed, 15 May 2024 21:51:18 GMT
ENV JULIA_SHA256=688e746f3d8700ba44a6cbc9ce04ccead4cd921f093af80259e10d0b0c5448c8
# Wed, 15 May 2024 21:54:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 15 May 2024 21:54:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95f7df4e233b6e548287dfbdf0622b0b4d84cd86154ff0d63e47049392ecdf`  
		Last Modified: Wed, 15 May 2024 21:54:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b32820487a45df2280409928ff790e234e6c79f9d3d7235e0495e2df5720712`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccad58740d7837c41c1e0e413a860785eeada06bfb27fe96c451654d39b506a5`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091220304dc5c00c8cef2c0ca080036b7e423ed795b3a9aa722ff1be599b59`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2e77e63490e0ccc5caece135d676366ebff3aa29b0923fb4532fc767c24bc2`  
		Last Modified: Wed, 15 May 2024 21:55:17 GMT  
		Size: 187.3 MB (187263593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a090ae4dfda2b9a05f0870b2113b9347e2ba5d0af072a66fe5d8f1464c83d`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
