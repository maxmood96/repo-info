## `julia:1-bookworm`

```console
$ docker pull julia@sha256:44a89078569d8932e7b6c544c4509546bb7431766aa03e599b6154d120f5de21
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
$ docker pull julia@sha256:a879e8217bb6bb4740c216155c5630f1e0f21a6948f256a331c6c1a79f896de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210887618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f84d44afc2d14ff4b561eb76bae715bdd31129e86ff0f6791061fbe636404c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48a89b4c3533ee4403f6fdd8ac997bf223860345ad5360b41094ad14419c110`  
		Last Modified: Thu, 06 Jun 2024 00:55:58 GMT  
		Size: 5.5 MB (5515177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792c21caaf6f08a834da045c0821a9cd9c645a76ddf189010a2390aa8f71a9f`  
		Last Modified: Thu, 06 Jun 2024 00:56:05 GMT  
		Size: 176.2 MB (176221654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d488bc95724052fdeb6c62b6f335e058c54ea4ddb1bc93ba5d75d14ea02cd8d8`  
		Last Modified: Thu, 06 Jun 2024 00:55:58 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:170a940e737672dfe3470f7bf514bb31f2faa9210bcca1bca287e6c4730b903e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa5475877d113fe27cd2f633e3d6dc61e4f5fe3e8c644441490292cd074ba6f`

```dockerfile
```

-	Layers:
	-	`sha256:743f73785305b02616f57890eb10f9173de3248e329c6feec69f98da5e304204`  
		Last Modified: Thu, 06 Jun 2024 00:55:58 GMT  
		Size: 2.4 MB (2414588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d38480df263440248c54e6c6f5abcf48b3679ddc66a606b4293a44e73d1d7e8`  
		Last Modified: Thu, 06 Jun 2024 00:55:58 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

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

### `julia:1-bookworm` - unknown; unknown

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

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:f08acaba8914db5340e080f8997e3f06f62b5aafe16f3ff41ac90fe49f8a9e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193405039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e937ebcaa9418572c592f465a18e6ba8176f9fa2a1396dbe3dc0698f0e275cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdea35d43c4f9376d1b8a70568de8c3afa30fb0156016e66bed57e29d0783be9`  
		Last Modified: Thu, 06 Jun 2024 00:55:58 GMT  
		Size: 5.7 MB (5672192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb403e27996572ed8305f323b2680290bbd026117f43607d9f96ca83b77346a`  
		Last Modified: Thu, 06 Jun 2024 00:56:01 GMT  
		Size: 157.6 MB (157569834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66c15e8bc21f2f8f77c088b722bef529d41d463fe34b4a7e6895c774ddf69d`  
		Last Modified: Thu, 06 Jun 2024 00:55:58 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d5456d8d1efa5fe9f30c27227940a499b06153d3d9cbdb2ccd02ed9ee10191ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cb0ca24c2c898ad5a8fe8ffe56f84dbcd89e2e1ce6cd2c30d25d7bd5735d9e`

```dockerfile
```

-	Layers:
	-	`sha256:4aaa57c2eed2006793d0efc6045335663cc77e90bb68b6995bb3d06f5ba930e6`  
		Last Modified: Thu, 06 Jun 2024 00:55:58 GMT  
		Size: 2.4 MB (2411660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d697f5040dcaa5826d048300e6c2df16cf5a4847730d9ce78c590be3f9f3f43`  
		Last Modified: Thu, 06 Jun 2024 00:55:57 GMT  
		Size: 18.1 KB (18143 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

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

### `julia:1-bookworm` - unknown; unknown

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
