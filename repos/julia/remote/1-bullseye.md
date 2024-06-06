## `julia:1-bullseye`

```console
$ docker pull julia@sha256:8fcd93162e2b75c2d9d62c1c32795c2160b5e4727781ea5fef34ab67681952a2
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

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:389a3208c3ecbd1ee7e4a9c5b7570cb61d5b70cf0fbcd914344bd629f1a6a10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209880083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fc1740e6eca76efae6c9ae5ed217bf819a617a24482a51ccde720ae5b50771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e6504f1c9c60163a5aa465dbec54e12079c83694d97e223a3068f494ba7a6`  
		Last Modified: Thu, 06 Jun 2024 00:57:01 GMT  
		Size: 2.2 MB (2223213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1fee503b34b889d2aafda1cfaef2cab5633a8b86734dd55802866a192ce888`  
		Last Modified: Thu, 06 Jun 2024 00:57:04 GMT  
		Size: 176.2 MB (176222562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b86f2e8fd126fd75ba68129952cc122c07225254224a7f6e7d82d01b27a413`  
		Last Modified: Thu, 06 Jun 2024 00:57:01 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:531738d51f88dd486b1bb32681bd5cd5e25fccb414633f8924d1b683bb45fb95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c85f37a8f8a66970e53f05dc0b5c46dbbd9b2550da1039eef95b9c17bf31c8`

```dockerfile
```

-	Layers:
	-	`sha256:90a679c2e3538e088bf5f9fa9d30f651f90f94b846e6eb3c803219307536505a`  
		Last Modified: Thu, 06 Jun 2024 00:57:02 GMT  
		Size: 2.7 MB (2681384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107e8c215e8dde0c7733cb391e6224bcae8b6e8018a1f473927addf70577e233`  
		Last Modified: Thu, 06 Jun 2024 00:57:01 GMT  
		Size: 17.0 KB (17024 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:240d642067f877f09e23b6f91b1b85294dcd0997de37e93fbe47f296b266a80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210461605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ba0a8dcdbc5ad8ed9a1d1a5d0fe91ba41733fd447c0c6647ff20f6cecdbe57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897c1e111b67daa80cabbb9efbcdda65fc08c835692e6d76dc59e22093a19ce1`  
		Last Modified: Tue, 14 May 2024 17:34:13 GMT  
		Size: 2.2 MB (2210820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf400ca250bfe14bdfc5d8302578b0c560ef989b606d2df29ab6415d02e3791`  
		Last Modified: Fri, 24 May 2024 15:49:51 GMT  
		Size: 178.2 MB (178163507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b461c0e460a3b830cfe8c1e6fea48acc4a01dc6ba1c7fe5aa40f3c07cf2fecec`  
		Last Modified: Fri, 24 May 2024 15:49:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:305e850cd73b2bde16ff788a69d501b2f662ca87b67595ef682130091a2acd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce798b9e135c2a082fff6eb29502853543b26be8ae3b18078f526bd95757259a`

```dockerfile
```

-	Layers:
	-	`sha256:08b502c33b7c3da5a64eca7853611b6a34f7a59838a1608ffa22f19f2ca23d99`  
		Last Modified: Fri, 24 May 2024 15:49:48 GMT  
		Size: 2.7 MB (2680629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55b6acad519f2a0558e88895e497c9e3a40339c43b63c86a664d19991f6b336f`  
		Last Modified: Fri, 24 May 2024 15:49:47 GMT  
		Size: 17.0 KB (16984 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:0fcbbdd0fea60c63df3998536245d7fe8a2d6e19bdbe1edffc1d4843815a47a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192323349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca3dbcf6daa1b80eb1e9ecfd75c0212baed70f2943bef34576e921c148f4ae5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
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
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a343812afafc4f784e183448791f5c1220bbbba627b63ec0ed92cfefe1b67574`  
		Last Modified: Thu, 06 Jun 2024 00:57:13 GMT  
		Size: 2.3 MB (2329038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd646f5068897a6a0a7dd6eb55284ee7d699ee671c3ef95c698da5e9535dac6b`  
		Last Modified: Thu, 06 Jun 2024 00:57:17 GMT  
		Size: 157.6 MB (157569891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b11fcb084308586abdf2a4287ed3825d24f8c48e30884409cf5a8a47fe4fb3`  
		Last Modified: Thu, 06 Jun 2024 00:57:13 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:5632467c5e8c96f4c0ce19e3fefa746ecde1d1d68b9730f74d8397115050ccf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a7f91a9c54ce2a1cd0cb01b43f9c4662c253bce73ebfea7f026903397e1b08`

```dockerfile
```

-	Layers:
	-	`sha256:60918f11b890724b3ab837c04a5eb5c4806b2ffec8723c13dbbe2d741b7b2fe2`  
		Last Modified: Thu, 06 Jun 2024 00:57:13 GMT  
		Size: 2.7 MB (2678482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b830c83d9a4295588e0148816b3fc2d44cff3da1e2d1f104baa1fd7c925e24`  
		Last Modified: Thu, 06 Jun 2024 00:57:13 GMT  
		Size: 17.0 KB (16993 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:7dae48c0e1c20167698d1af93d96c99bc001dd73442c1c5d28f589b7def82a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192416569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b3efd3aa77d6369d12c42dbee378b89e8f99e8ea21e2a583b240212fbffc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b34723e47ba2ee8e054a2104e7b86857769fefadca33b43ee36fcf92e586140`  
		Last Modified: Tue, 14 May 2024 13:26:18 GMT  
		Size: 2.4 MB (2425682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f528bf9e27fcb50cf00c13dc4ffff071806d443180b03ebec59a1603e56df`  
		Last Modified: Fri, 24 May 2024 15:14:49 GMT  
		Size: 154.7 MB (154679356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022a878f84e3ff3a612d805f160ba51fcb84d12afd59098afb1fa42e83ed487f`  
		Last Modified: Fri, 24 May 2024 15:14:44 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:5c71f0770078718b8814e663712d6b2756280032ffa087b0fc853d04abc4304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2701822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7364deab3c34d05f17dc8a56df944e48fbbbd6d66965f3a192145f77257b2fd2`

```dockerfile
```

-	Layers:
	-	`sha256:2cd5acd06a461ef7754a9585ac250ccc1653768b13140c43b4d0ab14b1bff3f9`  
		Last Modified: Fri, 24 May 2024 15:14:45 GMT  
		Size: 2.7 MB (2684807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25b537e20e232764f91c6c433037495a50f809a57716542f2250ff9fca28faff`  
		Last Modified: Fri, 24 May 2024 15:14:44 GMT  
		Size: 17.0 KB (17015 bytes)  
		MIME: application/vnd.in-toto+json
