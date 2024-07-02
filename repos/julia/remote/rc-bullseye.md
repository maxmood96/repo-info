## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:a02593f11027d2762852ad262f751b1d367dac85b090ec41c8d0007d04cf0dd9
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
$ docker pull julia@sha256:af75d5926114654284560d7a78301ba1243bcbe6d35d33baeba14d4f273cec4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287422299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb1fc50b6c2fdfb4f67fcccc92368ff5b0f6ef5de55ebe3e6d38eac053639d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b4e874d4a6b5f5f4e94ac15287f31a7ef95a62c1ec8ce16889be4876a53bd2`  
		Last Modified: Tue, 02 Jul 2024 03:04:19 GMT  
		Size: 2.4 MB (2426525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e62554b108c95480d1ba2cda312bcbd5a419316b2da376834e099eff51506f1`  
		Last Modified: Tue, 02 Jul 2024 03:04:25 GMT  
		Size: 253.6 MB (253573118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b8ea1ea19a3d4a3043bbfaedc9b3d79f0b0b97ecd07f0baf14810cd7d26cb`  
		Last Modified: Tue, 02 Jul 2024 03:04:19 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:a6a8f23c17376bb112991b5dd510c4df7aa9a1206504d38ed8bf9a955c44a523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ea023f9c5e8b90078638170750cedec17c58e4bb23649c78135fa343ddbaf`

```dockerfile
```

-	Layers:
	-	`sha256:9565d4c62f4dac0272b4d5f98c9c3db096d44c73825a1dbea474c9bf2dabc288`  
		Last Modified: Tue, 02 Jul 2024 03:04:19 GMT  
		Size: 2.7 MB (2680166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57643c569c848fdae1fdb5e461131dc16fcd3ef6031d8218d94bdfc364d278c`  
		Last Modified: Tue, 02 Jul 2024 03:04:19 GMT  
		Size: 16.8 KB (16801 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:836ca8e6612216caa2908a463e9d857fd5ec6855c993b7c83931a0699986aa47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284374724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5dc5c97eaa3c68ff58b21260d3dc1fd65a6cb5eabfb14f27b0f505201dee52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a289260116b1c3c73ee0d213092f2968055bc4e4dcc23be1a3648691b1c644`  
		Last Modified: Thu, 27 Jun 2024 00:01:34 GMT  
		Size: 2.2 MB (2210831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2bc0971e2c00099661f80be4e35cc3c52787d6793ab3bbbb1f2bb2ac40ddb0`  
		Last Modified: Thu, 27 Jun 2024 00:01:39 GMT  
		Size: 252.1 MB (252076546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9505bcceb754c94c32667b7f9857cf045b509f7b4c66acda91a26dfe384de802`  
		Last Modified: Thu, 27 Jun 2024 00:01:34 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b4903e5a4095ec5d61e053374ee93136f95a2fe8d252dd79a8b3108db2b61274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e67ae4ce63ba3fc7fa42bb1478624ba26976732538f5cb38aececcbad2ed92c`

```dockerfile
```

-	Layers:
	-	`sha256:4d0b22f05054fdc641492804925a7b6ee8e5de1ab4e498ead30cba976839de11`  
		Last Modified: Thu, 27 Jun 2024 00:01:34 GMT  
		Size: 2.7 MB (2680378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e1e24eb8b2f383867be12de28ccb0a34e730890630d22a2abff8f3db2317239`  
		Last Modified: Thu, 27 Jun 2024 00:01:34 GMT  
		Size: 17.1 KB (17098 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:5024bd4357d1fcf61ea1b0f1df608af33cb00931756eb2bef1a61ce96f20458f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266220602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a278c1dd1bcd0607fbf953509b3410acc788f8cd8b4ca67fbb56021eb28d6dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
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
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73be08143cbf3c49f218c2b755fd3f91d35df8a5255a80aab25f6587ba2cfcc3`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 2.5 MB (2533012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a417a4938ec7082be804f5681b7b5bec24f445077a16ce78d1fef1d83acaef6`  
		Last Modified: Tue, 02 Jul 2024 03:04:17 GMT  
		Size: 231.3 MB (231278766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0f46bdd554530cd1b8d018de85f73fed8548a8f935513fd99bffd350695cb`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:314a9f6fc5af5e519e7e8a8a2c66812c614c558e3df63ac3f171f2ff06aff834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5ebde18f31d9117dd9d498de2876c05657e37211ff16871837a8230a3e9c34`

```dockerfile
```

-	Layers:
	-	`sha256:1ab04e617b8769919a11dfa935233d823b6a0072420b9230a0b384264dd6cdcd`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 2.7 MB (2677269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dff4c913f67debeef3e12ecc810575af09ffa64b059035fd81519b32a7a740b`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 16.8 KB (16774 bytes)  
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
