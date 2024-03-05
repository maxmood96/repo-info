## `julia:bullseye`

```console
$ docker pull julia@sha256:3580a20e17b1fc3edea688c49644d6a07952d8176b333af3a1025cf8dce75a1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:d50e08ab84e13f17e26892fd72324f9a067e8f9051bbd841cf42a8265d3aa032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205976861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2558d0355fad659e48f464d3f4bc6ff8dc05e9ec0466baf103f20ad5f5dc67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 02 Mar 2024 06:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_VERSION=1.10.2
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414b48eed1002ad4d3623273101977a658a384091c57440a3041f085d3273578`  
		Last Modified: Tue, 05 Mar 2024 00:50:18 GMT  
		Size: 2.4 MB (2426544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e246120aceba1a79a2b56db63122d199fa621dac980ece1304de0d67bb08879`  
		Last Modified: Tue, 05 Mar 2024 00:50:22 GMT  
		Size: 172.1 MB (172127520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1425a8a1e12cca500ad3c853bd2f40412c88464ad292e8895955c91a917654d1`  
		Last Modified: Tue, 05 Mar 2024 00:50:17 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:ceb512c51ee6bcb252729b3e606797847adbdebe222c64f2047d0cf32e47254a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55033c73a930d8642d3b2387a09c4ac9ead229709d223f116c43f43207f0f493`

```dockerfile
```

-	Layers:
	-	`sha256:5b54ac848c429bb1fc85f5cd403f13af79fcd5ee5010e684f19c14f9b3f23f08`  
		Last Modified: Tue, 05 Mar 2024 00:50:18 GMT  
		Size: 2.7 MB (2717977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7019d9dd16376e4b76d761cf199928a7678558f849863c93ca7b6c55f2ab0fca`  
		Last Modified: Tue, 05 Mar 2024 00:50:17 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b541f456f1e13a016f7d3bbab4aa8805e0dffc761b83cfc46ff355833705fc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.4 MB (198390942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e0de39ed3db4f73cdf85c2d2d9fcea8532a1d45cd4e1e2780ce24121aae44a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 02 Mar 2024 06:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_VERSION=1.10.2
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd381bc5ce074386a44640a70f3d2d53921e7cda7c6386a20616c9fab4cee5`  
		Last Modified: Wed, 14 Feb 2024 00:41:34 GMT  
		Size: 2.4 MB (2415040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540c24d3de90f7b22fd0674c6ca29e43a47e2bb6f8eab5a3efe1ca55cc4b98e0`  
		Last Modified: Tue, 05 Mar 2024 00:59:35 GMT  
		Size: 165.9 MB (165904455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12738feca009cdd77e9b56cb3f365f98b61217b11546b20e90cb3cb53fe1d4c1`  
		Last Modified: Tue, 05 Mar 2024 00:59:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:05358f9d13653ca8bee2d0ae6e95c7716b96145f191be5a9be1a81796ecafd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6051a960f619cd78100d246a11fb0d0fc2ce4c85d23ca3a924aa81df369978`

```dockerfile
```

-	Layers:
	-	`sha256:aea239e0394a09e79efb0ae1420365eb1e90a0c68009c07423320fd97d630985`  
		Last Modified: Tue, 05 Mar 2024 00:59:29 GMT  
		Size: 2.7 MB (2717223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1978f21450519413f8ce000c5dd4e9e45d2aa5e221e1f3a8556c81ce6083366f`  
		Last Modified: Tue, 05 Mar 2024 00:59:28 GMT  
		Size: 17.4 KB (17383 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:a1a49ff9631482576ad6231ab3a1658bc603bc6cc8f819d7145e270886f9947a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191341224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8a6a53258d3d91636a17ea31d3c8cb6277c7ff8f62d42ee74bc5f7c8deb4f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:18 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 02 Mar 2024 06:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_VERSION=1.10.2
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5edfd6deb940d14ca7b14552940fe736623d4d1b7da4b385d817fd7bdda7090`  
		Last Modified: Tue, 05 Mar 2024 00:50:11 GMT  
		Size: 2.5 MB (2533059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146b7ccca96bcf33969b4103662ba7ec0cc5a3554556b1f35e72435100d4e223`  
		Last Modified: Tue, 05 Mar 2024 00:50:15 GMT  
		Size: 156.4 MB (156400351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ddff5ab2329636f521b3c3682b0f5c52ab64a5f684340ff34e88a82b8ffa77`  
		Last Modified: Tue, 05 Mar 2024 00:50:11 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f7d6a524e00728590a99dc3e998c463259ce04983713422d291b897897389fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a468d38c46b18bbb36820fc9281a9f6ec97eafa2caf2b094af9b8b0a7b3b21c0`

```dockerfile
```

-	Layers:
	-	`sha256:b951a908069cc6024c0541462d767d8dd75eb5fd0e8e19ad9c77e7e7adba9e6e`  
		Last Modified: Tue, 05 Mar 2024 00:50:12 GMT  
		Size: 2.7 MB (2715077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b490e15bad93c892623838a998bfbe340ca474475ca09bb0a6e719f72a2acb85`  
		Last Modified: Tue, 05 Mar 2024 00:50:11 GMT  
		Size: 17.5 KB (17509 bytes)  
		MIME: application/vnd.in-toto+json
