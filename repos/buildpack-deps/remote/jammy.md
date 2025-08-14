## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:5396af43ad900e5c10f816c57ad4cf4c44e4ff4cc19131ab67b420d44b542257
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:dd1627168a751abaefffbb4e811255d2e0ef1075a9a3f8e034f30fb14dcefce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249068482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23acdfca5430ee173cfc0cf2ab580c28041784a97175709f1a9a64f8c62a48a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1718e536deb534924f0e24d75c0ad8cbe941526cffc1ff3ec1e0d1c6ec3f68`  
		Last Modified: Tue, 12 Aug 2025 17:23:37 GMT  
		Size: 7.1 MB (7106301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0af6b0da3685a9691a0c2dc93fd4622ce033ebe2d18799fe3d2f24527356a2`  
		Last Modified: Tue, 12 Aug 2025 17:52:57 GMT  
		Size: 39.5 MB (39487694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558d4871c89a9656849b711074a941b6ce1e7c52056b987e8dc64d6321dd72e1`  
		Last Modified: Tue, 12 Aug 2025 19:23:44 GMT  
		Size: 172.9 MB (172937494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fea8a2353b3b26ebf6a3c51842bb2ca4ec125238090040e56724cfa1f600e3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11849661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d1b7316ad364a3ebc7510f25ad8b80a2725c2a695d3c0193b5fcb501780fe0`

```dockerfile
```

-	Layers:
	-	`sha256:811c95706a19631886a6172000c333dcc37cacb7f08b21cd25ba365f52cffe14`  
		Last Modified: Tue, 12 Aug 2025 19:19:23 GMT  
		Size: 11.8 MB (11839458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7219780dece2581c29f036c32310e67008bdfca32f1287957b42f0d046ed8ea8`  
		Last Modified: Tue, 12 Aug 2025 19:19:24 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:61eb61f4939fb599777908e2d7cfd2e7c54a3f1f06f62a8b6862b454d5904acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216289201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78817c75aa2fcd4b6d51c5993b43a2147f8bfba8f5dad16a30db50fff0842e81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:56dd1608fa49343c3815b8373825d581303e97b21994ce0e1d099bf09251caea in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6530e67fdf3958f32e486561f05a1170b5fbcd419c51eb435b13993ecadad7b3`  
		Last Modified: Tue, 12 Aug 2025 17:02:44 GMT  
		Size: 26.6 MB (26642919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247ab3b4ef805c703a200af320c236c49a0ffab6a53a288323350767589e6b1c`  
		Last Modified: Tue, 12 Aug 2025 17:22:41 GMT  
		Size: 7.0 MB (7010313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac244b8047a8ede8039467f8c639786b33bbeeeb871907f772115d141b28e78`  
		Last Modified: Tue, 12 Aug 2025 17:53:06 GMT  
		Size: 42.2 MB (42249779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbecffd20289cdb76c33929bb9f82cf3a9a1c4ed27004d521d4a2d563bf2eef`  
		Last Modified: Tue, 12 Aug 2025 20:37:08 GMT  
		Size: 140.4 MB (140386190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:df47b0ef50b18dd091ee293fee516cfb90a5699da0d498bcf191d3f94ddae9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11638946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ae8be12ab5525145ee4dac7e6fcc8b8428f75c17732764dcafc00b4746c11`

```dockerfile
```

-	Layers:
	-	`sha256:53a8298e490c3e2a91086c0c7459471d67b4c50b2d7b1f2fd08db4cb7fe9b9d2`  
		Last Modified: Tue, 12 Aug 2025 19:19:33 GMT  
		Size: 11.6 MB (11628683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a49aca3d2bdd551d8414cdef9b175ed6c0a87fcc059597f43277c3425266ccbb`  
		Last Modified: Tue, 12 Aug 2025 19:19:34 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5ec0cc596f9b16c0272bef32e4e492bd97eb61695ecc6142ecc2d45f13d958eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240189821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f907ec24386639ab35735da250178471bc6afe8a6165a0fd91c2288142c067b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476a9430580cac739e29f524f2d4fa032c5bfb4d16c97a34238459efc663af4e`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 7.1 MB (7051909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff81fac6a1179a5e3cbb2d54ab761676b2cfd9b578137b5d20d478f05d90d7e0`  
		Last Modified: Tue, 12 Aug 2025 22:14:13 GMT  
		Size: 39.4 MB (39385763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac68d2b387230141ce1231c60450fa4a1bf83adda8f2bd322305af6d6b0b0aa8`  
		Last Modified: Wed, 13 Aug 2025 07:54:06 GMT  
		Size: 166.4 MB (166392902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b973706da48f0399f980a899744e461e4167f011973a1d895eae0e8302ef65b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11845408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37549d57162fecbe4d229056743a82c480b430cbe9c27febe538b310cae705b0`

```dockerfile
```

-	Layers:
	-	`sha256:8141b6c73622d13c696a55c519e3c5503a814f26df1305dd9fa8af1d2dccec4b`  
		Last Modified: Wed, 13 Aug 2025 07:20:37 GMT  
		Size: 11.8 MB (11835125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51db83f3b2d985342085353fddfd4c05ab32107e617d9d51adadaa81c0fba8f3`  
		Last Modified: Wed, 13 Aug 2025 07:20:38 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a505d31ad11ed552e1260209cc61c368fe147da81343ac88f1f9e6c8f5127342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269794910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6515e2b005e2d7648234e2c623bf29e819abbbe2617ca0348a96b7f908677de2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeace24228f2ecb190bb960497ccea7acc7d82389a0af77723f03f86f2a09b7`  
		Last Modified: Tue, 12 Aug 2025 17:25:05 GMT  
		Size: 8.2 MB (8184873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b14242d8340dade2d7f016981f02241d8ec2f1f4d9662de8bcace23ae887ee`  
		Last Modified: Tue, 12 Aug 2025 23:15:45 GMT  
		Size: 43.8 MB (43767590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b2414cbf52fe6e47090c4e372dacd24a711b5bda0bea961f5245d606a66534`  
		Last Modified: Wed, 13 Aug 2025 14:03:41 GMT  
		Size: 183.4 MB (183399302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8deca3fb32b738f68ba0fce4a9c1840ba0089d883797a660d3df9ac0cffb7a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11809058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30efd2f4add223d5be198f2acfbd881679d02e70668a2154eb01378db31e179`

```dockerfile
```

-	Layers:
	-	`sha256:4c331e148b2fc49fa903393f79b9676916bfe84f2cb9e27a39775e3d5bd2a742`  
		Last Modified: Wed, 13 Aug 2025 13:19:43 GMT  
		Size: 11.8 MB (11798823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e11573693c8bdee889e9a6bfa8eba4e81d879da660fde2054a5926ad0b971e`  
		Last Modified: Wed, 13 Aug 2025 13:19:44 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:489fdef8a51f95eeb931b30ec800babfb1dd29a9f366528da25ac83106eacb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274258651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a385dac04ac1c7c81b9397256e98f2b55de964751874884d25380766c0a69d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:35770e06fa2c1cc2b759aaab361c62ab900fac2d6b612a4403b76189d7f2ce82 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1de6ca2b6a61e33f0f8fae9da1d47f9afcb02341cbe72eeb6eed6979ef59b090`  
		Last Modified: Tue, 12 Aug 2025 17:04:15 GMT  
		Size: 27.0 MB (27042020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2831747a0034f903385b005efb41ad90f86cbeed2dfb31e5afbe06beb4de45b9`  
		Last Modified: Tue, 12 Aug 2025 17:26:12 GMT  
		Size: 7.1 MB (7118185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328660fbda39277d782f765a5900fe7c253fb97800d915b2c262f417749954f0`  
		Last Modified: Tue, 12 Aug 2025 20:48:45 GMT  
		Size: 42.3 MB (42304868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa27faef0952308c571df3bdefad5e4c2300bdd3124664ca7930e9385a81eebb`  
		Last Modified: Wed, 13 Aug 2025 04:30:39 GMT  
		Size: 197.8 MB (197793578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dccd3e3c1e9bb3802e510740651b6e5d31ec5503a793b7032d544fb089b6741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11790062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead826dc2aaff8f2478f12b1725767670bde5dbdf969a4c77e57687fef3e4432`

```dockerfile
```

-	Layers:
	-	`sha256:38e489bd7739ba64d6fbfdbdefbc126a132251d72089f44b03fad3ae2b448bf9`  
		Last Modified: Wed, 13 Aug 2025 04:19:43 GMT  
		Size: 11.8 MB (11779827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b09b98a3270112cd0b0a9ea23e1c59ef3742f0d27f9c9817ba56135aecfdb1c`  
		Last Modified: Wed, 13 Aug 2025 04:19:44 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f89e1277957b1b3ec7bb2288a1d991258e71cffc08ddecabd523267f9485e548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223034479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03626449db70ee6a4ef367a5ee089ded1175d8f3e26496421f34da7ef41eaf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0293d5d0eb0a90906be37fa32ed26eaa292a9ab825eef1a4106c976ab7f20027`  
		Last Modified: Tue, 12 Aug 2025 17:23:38 GMT  
		Size: 7.0 MB (7018601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9455ea007ea1cb6f92358b80c5cc2d8e856f38a7b615dc9a8d263bee53c22e`  
		Last Modified: Tue, 12 Aug 2025 18:42:39 GMT  
		Size: 39.4 MB (39421944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93c63667f095e082a1a87b80f06b25f524315c1c859a31ad4f48dd0af0dd01`  
		Last Modified: Tue, 12 Aug 2025 22:36:49 GMT  
		Size: 148.6 MB (148590715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13c372f571e35669de27f7274bc5db0eaeeab065fd3f5a0eb7ce3b7fe71d4b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11663550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3c0cd1a038413510524c11b73a8ed63b1c2f213edc02edaa982728383932e7`

```dockerfile
```

-	Layers:
	-	`sha256:281382a14f9084ce8230311a797e0b7ac74b94bbfd1a6d005aeeeefa59f4ae5f`  
		Last Modified: Tue, 12 Aug 2025 22:19:55 GMT  
		Size: 11.7 MB (11653347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:344a1f8a29609491e64a15e8d7241c12bb6c70bff2f1f759169efb2c2c69a1d5`  
		Last Modified: Tue, 12 Aug 2025 22:19:56 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
