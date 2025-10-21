## `julia:1-bookworm`

```console
$ docker pull julia@sha256:7ba0f936bdbc0c9460568699a1eee920775aa6b6b4a9a703a4ec7fed23e5d6bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:3716ecef01306a476b8c09a185ce593f84396a76b202d7279b20b5f302a9ab53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319506802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebc009c0e4d24d5233813b2faed333430b17def218ee3c1a78b0389488e6d98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166d7525a95437660d4d60a28192cebc67daf8cf87cf463255b3a47f39f9b96a`  
		Last Modified: Tue, 21 Oct 2025 01:20:45 GMT  
		Size: 5.7 MB (5716254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e9706086cd07adfd6ab3f78cc23eeadcce6825c6b4ee573d33e79620a42bc7`  
		Last Modified: Tue, 21 Oct 2025 02:57:06 GMT  
		Size: 285.6 MB (285561857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07275c5c608463c8f4a290397f12b8753dc1026071a7bbb08d028be99c27016e`  
		Last Modified: Tue, 21 Oct 2025 01:20:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:60aac230a60984179b69a69aaad4a35658ba92af69b96aa8a0f20b74460f28db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04053af7603421d60fff66644cfaab4a4056e4a2913ba58235a53189f2967ec`

```dockerfile
```

-	Layers:
	-	`sha256:ceb88462c4d16a15e51760baf6795cb5bb4a6456b76d019136a7a1e4d3bca4ed`  
		Last Modified: Tue, 21 Oct 2025 11:02:28 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b19adf36b6f10c787bff8ff0948b7c87cf2297ba7572f91bbb4d9123dd7a28`  
		Last Modified: Tue, 21 Oct 2025 11:02:28 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8f95f139a0454ae88ab60e51d8e7978e10b77d35bfff5df963012737b1254a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339278739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f111dcfa2cce9a26a9bf60ec8a1256cd59567a9f2082dacc387aea556e8125c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7930cebf84a215d9eb527b9278102385789e575096e6a1a5decc8dc34c5c007f`  
		Last Modified: Tue, 21 Oct 2025 01:20:23 GMT  
		Size: 5.6 MB (5567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ecafe9dd74b7afce749fd2a7a2d07feb599222cdc503e2ed18d5a7e898aa0e`  
		Last Modified: Tue, 21 Oct 2025 14:09:21 GMT  
		Size: 305.6 MB (305609106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89666ffdb4657ba0f242d14aadbccee5845f9f895e0b792f4f972a77d12ff699`  
		Last Modified: Tue, 21 Oct 2025 01:20:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d9548e9b4d3f01e06b105356b1a389c88393bd420a38ac6e5d4d94acee0b611a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa4a7302e5bfa33333e3315c67bc7d157f9e5404bbedebdde31628f2a2e21e`

```dockerfile
```

-	Layers:
	-	`sha256:4f3fb0b175ab4d2db86b26d791c1392851582a761f19a7ba1aaad87e10d9b396`  
		Last Modified: Tue, 21 Oct 2025 08:03:06 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f3753d84489cdd8c544be5e15f710886cd9e02795772c7069b7cf28c65a3db7`  
		Last Modified: Tue, 21 Oct 2025 08:03:07 GMT  
		Size: 16.7 KB (16703 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:fb04cd056074343941d05b70b0e47e8907ad53764545fcee796d597fd50dcf1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264787273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544e41e0b1ef7fe8ffb9cd575bb1b211ef4ddfeb096d931bd3bda0a7d8705e4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 08 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
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
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da16a04a13fd91c9b5b62797c2a61d343ba9bab5219fa642b715dd5116795550`  
		Last Modified: Tue, 21 Oct 2025 01:18:54 GMT  
		Size: 5.9 MB (5877995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e95e1e7776bdcb2188c5e48159ce18514160a7487c8651ab35645d12eab777e`  
		Last Modified: Tue, 21 Oct 2025 01:18:48 GMT  
		Size: 229.7 MB (229699233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cac31378f470b00bc4f352887212e127c28a50eac3e19abc57a8ba0e554f58e`  
		Last Modified: Tue, 21 Oct 2025 01:18:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f6618a48162b8cc1908edccb21e813f8220558e0092177a4119d9c4078a2604a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0c051da3ebac88268083a72a6272793672e32efce0efd2e5fffb3ba9d4958a`

```dockerfile
```

-	Layers:
	-	`sha256:c9b812472dc3de28b9e661865ab89a4547ec54da3cfd96d292514f6376d76a53`  
		Last Modified: Tue, 21 Oct 2025 11:02:36 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8c739da3d58fdbcecd893cef0f5df93d4d09452ef515c13862b4d4d28287f7`  
		Last Modified: Tue, 21 Oct 2025 11:02:37 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json
