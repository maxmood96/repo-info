## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:091624acffb33b5d39db5c41e0374cb0a49d8c99b67129828e8f2a3b1f4e1add
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
$ docker pull julia@sha256:45a86fd9c4434ff8322ec42d55f5104f1318679d59f77914f223bef568a0044b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203477186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c828b9c689624c309b6139c15f164193fc469c17f2418ad96999f6dacc8f6589`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 03 Oct 2023 23:59:11 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Tue, 03 Oct 2023 23:59:11 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Oct 2023 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_VERSION=1.10.0-beta3
# Tue, 03 Oct 2023 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-beta3-linux-x86_64.tar.gz'; 			sha256='f6fb0b8625f608c6b586f96e6f403da827c5f69ee0fa72746e0c3b5b6eb29022'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-beta3-linux-aarch64.tar.gz'; 			sha256='9ee2d8ff367f17efa7d7279415622d85ae3e592a0938cc2c90a41f6d6f5a28d2'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-beta3-linux-i686.tar.gz'; 			sha256='2a18c67f4b3222018b74c5fc0d0c2211784fbd4905c43b55fa714b774b941614'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-beta3-linux-ppc64le.tar.gz'; 			sha256='40c541540f610736813750017ddc7292067438190a1a78ba30604abcd2bc4818'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2023 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa65f6044b964abfb24bf765f640a9db8b4b7ecee5f6fb38bca652d50d309b0c`  
		Last Modified: Fri, 20 Oct 2023 16:03:17 GMT  
		Size: 2.2 MB (2222920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c601b46eda3f5719d7cbf634e068aff8ade6bed348f5b4704e2afd371c8d0`  
		Last Modified: Fri, 20 Oct 2023 16:03:30 GMT  
		Size: 169.8 MB (169836032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8ed20fb993116e1bd190013ea0ab6158d5f6438ed2e8ed53485b7da05a8331`  
		Last Modified: Fri, 20 Oct 2023 16:03:16 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d4b303cfa461873ac47cbff47e832b60eff252f316dc349bd51bc805896b54c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af07d44f288c10eda1de1fdbc25d1bb0c615d97c1b9ddccba72966161a74a833`

```dockerfile
```

-	Layers:
	-	`sha256:724cc05c5c6780d430d5df7e8c6f3bc058c55824f701ffe2d2729f225951be59`  
		Last Modified: Fri, 20 Oct 2023 16:03:17 GMT  
		Size: 2.2 MB (2230074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded2b432593344c95329b6a867c4758cc6a18ad19dd80cd74a2a06a606328581`  
		Last Modified: Fri, 20 Oct 2023 16:03:17 GMT  
		Size: 16.9 KB (16945 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5275ddfdec282f3088ceddbb982a0a6d5028e18095593813b441a0a0efeb1842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196807629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c49ebd2f9d061ba34de4d28991d5812aede09a25471b7d998ad009f6628262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 03 Oct 2023 23:59:11 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Tue, 03 Oct 2023 23:59:11 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Oct 2023 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_VERSION=1.10.0-beta3
# Tue, 03 Oct 2023 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-beta3-linux-x86_64.tar.gz'; 			sha256='f6fb0b8625f608c6b586f96e6f403da827c5f69ee0fa72746e0c3b5b6eb29022'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-beta3-linux-aarch64.tar.gz'; 			sha256='9ee2d8ff367f17efa7d7279415622d85ae3e592a0938cc2c90a41f6d6f5a28d2'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-beta3-linux-i686.tar.gz'; 			sha256='2a18c67f4b3222018b74c5fc0d0c2211784fbd4905c43b55fa714b774b941614'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-beta3-linux-ppc64le.tar.gz'; 			sha256='40c541540f610736813750017ddc7292067438190a1a78ba30604abcd2bc4818'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2023 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc6a6591ea70d098f880a09b6a8d4ddbc69946d890b981eaae68df3a27d0870`  
		Last Modified: Fri, 20 Oct 2023 20:14:16 GMT  
		Size: 2.2 MB (2210559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdbd693c665648eaec3d62d1c6300cd86bdb1eb23c0676c8b307c062a503e6b`  
		Last Modified: Fri, 20 Oct 2023 20:14:23 GMT  
		Size: 164.5 MB (164532613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08bfe81e3102b73cefcbacda7afdceb08ece158ced0966e98831e0974465789`  
		Last Modified: Fri, 20 Oct 2023 20:14:16 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:dbf50408752868a83516f16bfa2155a497deb152596a5f818c32944ddbb95ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b455b6b4e9c8f5c8aa85745350c05f4034a534c216669583c182ecb2f8d0ca3`

```dockerfile
```

-	Layers:
	-	`sha256:005960f76fd77eb62a18f6495e8a6501598d79f62ecb5859d10f20b0ffa70a49`  
		Last Modified: Fri, 20 Oct 2023 20:14:16 GMT  
		Size: 2.2 MB (2230397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11363666a81708aac63e7e8cb4a844064519da1a2b1ebd220cf2a736e4eb2ea8`  
		Last Modified: Fri, 20 Oct 2023 20:14:16 GMT  
		Size: 16.8 KB (16786 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:039a5b869fc45135d5ec2eb679f4fdab1f17072bb595acae154a84925166b193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191235543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de3a80c5ae2598accd9ac171729e2e1a49e6dbe7de4d27e4cbe756c80db2985`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 03 Oct 2023 23:59:11 GMT
ADD file:ec6d51df021532be6c52d882f60a33d5cce8c3bff039efe8b98e923f2658ba45 in / 
# Tue, 03 Oct 2023 23:59:11 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Oct 2023 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_VERSION=1.10.0-beta3
# Tue, 03 Oct 2023 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-beta3-linux-x86_64.tar.gz'; 			sha256='f6fb0b8625f608c6b586f96e6f403da827c5f69ee0fa72746e0c3b5b6eb29022'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-beta3-linux-aarch64.tar.gz'; 			sha256='9ee2d8ff367f17efa7d7279415622d85ae3e592a0938cc2c90a41f6d6f5a28d2'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-beta3-linux-i686.tar.gz'; 			sha256='2a18c67f4b3222018b74c5fc0d0c2211784fbd4905c43b55fa714b774b941614'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-beta3-linux-ppc64le.tar.gz'; 			sha256='40c541540f610736813750017ddc7292067438190a1a78ba30604abcd2bc4818'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2023 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f088164df28359c53d5766709e069e084073984ecf4688687b4c7c529a8926a5`  
		Last Modified: Wed, 11 Oct 2023 17:46:21 GMT  
		Size: 32.4 MB (32402649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0fc5bd3ba0d538b6e372134a26dfd121d2988e9d901da66f03bce5e4098881`  
		Last Modified: Fri, 20 Oct 2023 16:03:02 GMT  
		Size: 2.3 MB (2328532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0406d81cdcf758425d77dbaa2168a524c2bdd31d2df8e8d634344ac15a1140`  
		Last Modified: Fri, 20 Oct 2023 16:03:13 GMT  
		Size: 156.5 MB (156503988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efbcea4e5001ad2da01b7b3af5ea3b4f278c4f2e97e494ad25316d389ebc272`  
		Last Modified: Fri, 20 Oct 2023 16:03:02 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:6b020102b1a6878cc621db94685b3fccecbce9d8e6e7923629bbfe279d5ea153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 KB (16704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc222617dec27466b0fd2689136745b30673a804ebb1d36fc6d45d8cbf32a393`

```dockerfile
```

-	Layers:
	-	`sha256:8f2b8c08a272cb0136f3d29f0dd0232b5e1c6deef543e9ecd937b3eb936dd2ef`  
		Last Modified: Fri, 20 Oct 2023 16:03:02 GMT  
		Size: 16.7 KB (16704 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:1e9d5dbd9cbf9448c09fd0763f9b2f3c91436a498f641c89a1f6be0dda08eec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191550333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af18ceb92adb738a7ed19d40012414128b24fc24c0976e9c70b5e68a5858af3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 03 Oct 2023 23:59:11 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Tue, 03 Oct 2023 23:59:11 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Oct 2023 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Oct 2023 23:59:11 GMT
ENV JULIA_VERSION=1.10.0-beta3
# Tue, 03 Oct 2023 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-beta3-linux-x86_64.tar.gz'; 			sha256='f6fb0b8625f608c6b586f96e6f403da827c5f69ee0fa72746e0c3b5b6eb29022'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-beta3-linux-aarch64.tar.gz'; 			sha256='9ee2d8ff367f17efa7d7279415622d85ae3e592a0938cc2c90a41f6d6f5a28d2'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-beta3-linux-i686.tar.gz'; 			sha256='2a18c67f4b3222018b74c5fc0d0c2211784fbd4905c43b55fa714b774b941614'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-beta3-linux-ppc64le.tar.gz'; 			sha256='40c541540f610736813750017ddc7292067438190a1a78ba30604abcd2bc4818'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Oct 2023 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2023 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b12635ffca02cd73f6066a96e094570ce5cf849c42a93995b01ef11180417a6`  
		Last Modified: Fri, 20 Oct 2023 20:02:25 GMT  
		Size: 2.4 MB (2424847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc10a0cabe8c3327754e7a5b5585f310b5c8e4bc75ca39820f675b5a4f0ca744`  
		Last Modified: Fri, 20 Oct 2023 20:02:35 GMT  
		Size: 153.8 MB (153831401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f350abb677803beed58a2fd65273199e775438b5e4ea80ecc9416cac4148c4cc`  
		Last Modified: Fri, 20 Oct 2023 20:02:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d3e48b89d34a9945805cee943d07038ada96b01d37569445742fa743690cd762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2251383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad5b08cc2f96d07038973019c051c703adf9d86504ad2f30177ff645c0f4fc9`

```dockerfile
```

-	Layers:
	-	`sha256:5eccdd7903971d8e13a1eb48d5ceeb053b504cb08c3a8f172d1793bd1b67cf02`  
		Last Modified: Fri, 20 Oct 2023 20:02:25 GMT  
		Size: 2.2 MB (2234571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa45ce95f92cfb829a7cc920db8c97ecfde5fa9351de57744e9b029c42406b8`  
		Last Modified: Fri, 20 Oct 2023 20:02:25 GMT  
		Size: 16.8 KB (16812 bytes)  
		MIME: application/vnd.in-toto+json
