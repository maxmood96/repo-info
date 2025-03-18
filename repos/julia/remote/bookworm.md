## `julia:bookworm`

```console
$ docker pull julia@sha256:0feb8a691687fcdb88fa3cd6820dbb520400f64df48d0abfbd4d9af4933aebf6
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

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:abedded0d1772aaeb02c6bba4109b7fd0745b4880c73eb811b30373d985d48b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16b02d491ef44bf1edb4d4b55af7ed0859b2231bdb1cacb7dfb56f2d7d11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf165c807d409f1e5e47644d10a56e62f760b04977240ccb92cb44373c0b0f69`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 5.7 MB (5713383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b6fe754913bc7659f03d356590438cc4eedd2dd68f4df602467584df07ac2`  
		Last Modified: Mon, 17 Mar 2025 23:13:45 GMT  
		Size: 268.5 MB (268484621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ec09870a2c14b826ec97c7163f20459b189d4ac71ce5fc48c61be5cbf30db`  
		Last Modified: Mon, 17 Mar 2025 23:13:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:90638797f1b5d7e05dc89684f27edd24d0ec9c90049a8b4a7bd0ba55d5f49895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb188174850f12a03f938d4afbdc70ce9d2f1e201caf8312806b2c15c8016aa`

```dockerfile
```

-	Layers:
	-	`sha256:0485ab72220e8c25e8c44fd4643cb6401c32a43d460248901e04551b66c7a690`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.4 MB (2445468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7d10aaca52976692b814b68272ef08141b566e335fb00c2d7a87c20e54059e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:eeb119ace5e39198c25fc10194a3e527cca20a21a5f42be9bb3f4c7a129683ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317583649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3e8ed6f2b03b1a18667cde280597179def0a536dfe1b0941271150dd354a9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a4aaada2b3862a7dad4be3eabf21322d8fe15e579b6d990f418d5729f21e24`  
		Last Modified: Tue, 18 Mar 2025 06:55:17 GMT  
		Size: 5.5 MB (5538335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b5454458138da5ba9fe3a5612344698239e4ce7cccebc1442aefcd2fac5283`  
		Last Modified: Tue, 18 Mar 2025 06:59:47 GMT  
		Size: 284.0 MB (284000907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9014adfe736e1292ca0a2341d33c768c0c2a3e43d3590e3c36f32dda40efdcd0`  
		Last Modified: Tue, 18 Mar 2025 06:59:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:49ce593e431a1b1a1f9cecebfd266eae68b658d8532b77263ad4acdb27831957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a3c7b9bb9c000f077378b7d4d3548a52523ad02d3ce751ecbd82754dd64de`

```dockerfile
```

-	Layers:
	-	`sha256:8bb798543bd7cd500d1522d9f8d7288c3462aac1a9b8986e07d125c9cacc33ed`  
		Last Modified: Tue, 18 Mar 2025 06:59:39 GMT  
		Size: 2.4 MB (2445791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee5ed5ecccaa9980b8a8a3b274c024563745cfbc0d45a336bb7bc11bdede768`  
		Last Modified: Tue, 18 Mar 2025 06:59:39 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:9f6cb4ab8de753dbdf08958fadb970ea57420a25940a9c66889d2675e1b30261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252906412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6160838c86bb01311ab4312fadcb5c79febbc02a9db5bec211474b6ae2d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c313be324d81319409f757b6a9214e6e4505edd1870d857ef9335183bf456`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 5.9 MB (5872272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e1e548a3d059caccea690a9ccc930a0ba4003bac183b117a14c4ef5eb0be5`  
		Last Modified: Mon, 17 Mar 2025 23:25:50 GMT  
		Size: 217.8 MB (217844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e28391a0fe4d76f864c7f5f2ad1d677cd00da4cfc75068849cd664e65683`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:66caada27c36606986912deb412ff68f7f7ec9bddf54775f6a16093eab0cfb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118730f876ef85874545babb36fc06e2768e0d5b721d060f23817c42124b3bc`

```dockerfile
```

-	Layers:
	-	`sha256:76a154e6def364e394399ef31951b53809301692945ecf7401bee9a909343563`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 2.4 MB (2442541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c82965d60d3d4aa1404ef241e92932d6ceef303d9cfac5e6b23310f702ee2b`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:1ba285447b58d69f2a8cf7dd81c774d8ffe8da52c179eb72495c3e84bbd5eedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266930234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369ba8676195a79a7dcb49c492566e495d6c53eaed98a726a3ff5b69704de59f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcecc6791487c13003672c8bfe5461fcab47a2fa30369108c0788271e54f4ea`  
		Last Modified: Tue, 18 Mar 2025 05:24:05 GMT  
		Size: 6.2 MB (6249617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283562312fe22731a911d721809a87d2088eb42c1baeebbb3e55ed009502b50e`  
		Last Modified: Tue, 18 Mar 2025 05:27:56 GMT  
		Size: 228.6 MB (228632430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c052ac9ee68cef1a7afd6d5e8ee8e943ac38f10c5be5d53096113b388f40f431`  
		Last Modified: Tue, 18 Mar 2025 05:27:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:24c699308abc5ebcb6ff3cf36bba6694d2d6adf72232e9a9915f07890f73fb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abe8ca19cc0312d55d34c730ccf22434386cbbbd86d7e8bff95e8721b535f7a`

```dockerfile
```

-	Layers:
	-	`sha256:0a7294068e5cea16a4741f5f6baec607ccf15724c7addd711b92aee956d864e6`  
		Last Modified: Tue, 18 Mar 2025 05:27:50 GMT  
		Size: 2.4 MB (2449900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd7889a058af3baca864724dc156c16db054ebd38418ebafbfc887d90eef688`  
		Last Modified: Tue, 18 Mar 2025 05:27:49 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json
