## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:a703fac9fb07fb2c8f83e9b0f766d7d43e29fb44769a0724753f4edccab04998
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

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:05f037723a8daa90787e6a1637211ec41ce3b0bca77ca6596fb29ca637908007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278607273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef6cacbdf5590762e0385cd5204d975695279bbc6f6faed361216b0278db670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bca5f89848ce8fced9fabc99051bd86546e9b21ec911faa12d1b57517b419d`  
		Last Modified: Tue, 04 Feb 2025 12:25:48 GMT  
		Size: 13.6 MB (13612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c239591c8fa2f14b9d884080d6e6888af267d5581800cd9aca9df2581c579ded`  
		Last Modified: Tue, 04 Feb 2025 16:17:54 GMT  
		Size: 47.7 MB (47706161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4002a449dfbeebc197aa37c9540569c67552048e4ea6f3e29d4680d8877810fd`  
		Last Modified: Tue, 04 Feb 2025 16:18:04 GMT  
		Size: 187.5 MB (187534589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea56b9ef0ade587ac7c02b1d7068c32d6912c34bb3d22b99d146ece0c29e3819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11357581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91971766cecd1a460eb600747d6a6ecea74bedbcc256fa7547a9559067f3d6d6`

```dockerfile
```

-	Layers:
	-	`sha256:979f5fc4fdb0e002a48d35db1f28d78516b135296692a750da8f1a69c430293b`  
		Last Modified: Tue, 04 Feb 2025 06:14:12 GMT  
		Size: 11.3 MB (11347397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc3bec74ae7fe6478fd68bdace1f3df91ce527a4f98599bc376e52bbeb84cab`  
		Last Modified: Tue, 04 Feb 2025 06:14:12 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a8063e16aa00352527c494c88db26b986642914bbbaf2ae11eff1a9dce222c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239555626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c2944a8f2d054f7fcc49e168834e886ddbcdde7978a6a1765ad002ceb10d16`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Tue, 04 Feb 2025 08:31:36 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26a8223ab81b7619d0fa204eaa4a52bd9e82a52dc44e8e3fd181d828b57c69`  
		Last Modified: Wed, 12 Feb 2025 05:51:46 GMT  
		Size: 12.8 MB (12770649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dcbc6f6efd6544a8f23370c197b454bcf746c394d4ef4477af75913c1ea6ca`  
		Last Modified: Thu, 13 Feb 2025 17:03:07 GMT  
		Size: 51.1 MB (51083749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654590271f69745bae650f5b5a14f6fe175182f2949c93ddc44376f48ac1ef3`  
		Last Modified: Mon, 10 Feb 2025 19:55:56 GMT  
		Size: 148.8 MB (148826245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:248cdce7aad846f6c45bc7cbf1c8937b15df5cc91ae44afd5bf2f8f5fef24abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10706832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd890ed0d72a0ccfdb191b5cc79ca39569fac0d19436f44b145282a6f661ff75`

```dockerfile
```

-	Layers:
	-	`sha256:3453a1ed9dd3d3439403625d29b42cb6cb1882f6cf07d5322eebad7bf5dedffa`  
		Last Modified: Mon, 10 Feb 2025 19:56:03 GMT  
		Size: 10.7 MB (10696588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f47fb8834788bae1b47b7033cf2e9dd9bba9979ab8d6fcb95bc7869ecdb542`  
		Last Modified: Wed, 05 Feb 2025 00:31:45 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2c6b1a58e492bb9a47160cacd347d60ee6ffd9943b91ee02e8e9a6ef5b84464e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267319864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c08849ed55e172a675511112c2162cdf2ed1e0d55ec8e5b7f29b1c42c1cd94b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e873299a39c8bb8cb3b5d978575339de6ade976cca414b5727de8d362ef599f2`  
		Last Modified: Wed, 05 Feb 2025 03:41:50 GMT  
		Size: 13.4 MB (13447918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94ea46ec0243a993d7c367da2602e0a5008adad8e66c3b027175cdc919418bf`  
		Last Modified: Wed, 05 Feb 2025 03:41:52 GMT  
		Size: 47.7 MB (47732701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1a6fdf4c84ab05014514daab209ab340e6a23ddbcfa591380a07f0fa77e247`  
		Last Modified: Wed, 05 Feb 2025 03:51:43 GMT  
		Size: 177.2 MB (177245647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:804e3d87410f925c0a5a35315bdcdeb5688e8419532c1332ba991684eb953058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10929069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0fb44f3945084d3ac354133e3f6ffb57f10ce3cc0ee648d0469a1ab150f572`

```dockerfile
```

-	Layers:
	-	`sha256:c3b40c8bff9fa4ed8aec00534cb79f33a2af63ae628a15e0d20bf9106593a5b8`  
		Last Modified: Wed, 05 Feb 2025 01:52:57 GMT  
		Size: 10.9 MB (10918805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a196ab7620ae4f5e60f8ce810b0c4aeb5125d3cf8af61beb9e8dca5d0db349`  
		Last Modified: Mon, 10 Feb 2025 19:56:35 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b813b439e19eaaa358006b2250abe0756c7df963cb911f89e5dc95b545b69e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293737886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa47ee4b1ae682716337bb1992e71949fce392598aa62efd275530a08096aec6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3acc4132c7aebe44f31c42e40cc094c5403d3a66fea37f2373bf78812b25b`  
		Last Modified: Fri, 21 Feb 2025 19:15:01 GMT  
		Size: 16.0 MB (15958943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5d3f04eecd25f382d7c6ac4ac3b8ddc8aa83c84e0baeb7ee7fd926a1b15c3`  
		Last Modified: Mon, 10 Feb 2025 19:56:49 GMT  
		Size: 53.0 MB (52978348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6c75564449b4b840326fbbfc9ba1d0274c65967ff754c561f0b3a0860bd08`  
		Last Modified: Mon, 10 Feb 2025 19:57:01 GMT  
		Size: 190.4 MB (190410771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f91972bf24fe309c8ddd186a45ca9566907cb942d1594db981420cf4dc7f1911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10876299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83891e5182b9fe2df7f60289056fe6046ed8f7f6178fe8666ad828a049cb0a55`

```dockerfile
```

-	Layers:
	-	`sha256:0add828bbddda2d8f9340ea658036489d627f64bfb1e00bee1c0af1eaabe9888`  
		Last Modified: Tue, 04 Feb 2025 22:20:32 GMT  
		Size: 10.9 MB (10866083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4d28b4b661ed3c8297228f1ff6fbb32c36872152281ac91c03e35337353967`  
		Last Modified: Tue, 04 Feb 2025 22:20:31 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d31f5bdb9913880c43a5a00471c71bf67e54951ad0562d4ecfd3df1a803ebbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.2 MB (333185891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb0ade06c43af8ab75177b46cd822d33e79229563b4910a508c8b1c3ad48f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Tue, 04 Feb 2025 07:00:41 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ff2b444c4e8d1278840900c3e27c00e5987f3c54a529299dbf9a2ed443657`  
		Last Modified: Mon, 10 Feb 2025 19:57:15 GMT  
		Size: 14.3 MB (14317230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec5a422d511e6bec6d017fced317ebf97a5f77ec1f6eff36a777fc69635d1c3`  
		Last Modified: Fri, 21 Feb 2025 19:15:41 GMT  
		Size: 56.2 MB (56219937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25582887dbbebf13b474bcce046935f9057ec77b7d60eb19fafce7fdcf42f073`  
		Last Modified: Tue, 04 Feb 2025 10:24:52 GMT  
		Size: 231.7 MB (231664814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54aa815e93779c56670198616f3acdade74b3796475166f25881215682c4187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10870736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5808c0276f6f621d004fff61facb2f629fbaf4021749d5cb1299d184f771cc65`

```dockerfile
```

-	Layers:
	-	`sha256:40943108eb855797811a4ec15d39627861040402ea56a026d39ea8de5439224c`  
		Last Modified: Mon, 10 Feb 2025 19:57:36 GMT  
		Size: 10.9 MB (10860520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0dbedfe5b565ffed2c797524ab8f0e8765c8c9e9475f416aeb3a57a9df3cdc9`  
		Last Modified: Tue, 04 Feb 2025 10:24:20 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:67c77d8fdcd166ca80eaeee0794f1fc7ccd5362760d2cf986e0323c7c9135551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256678193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79228f6922fd66015df503ab1d71231682b202cd71d4c6117e59c25ea491afdd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Tue, 04 Feb 2025 08:21:20 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacc91036ba2e7e50d76ff2b2593ea149a0df971bb8069b913263b87ff517ac5`  
		Last Modified: Mon, 10 Feb 2025 19:57:43 GMT  
		Size: 14.9 MB (14937386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae03e34cf459247f3c12fdf3d38cb8c622dd2d321ebd9a1ced772465e12c97`  
		Last Modified: Fri, 21 Feb 2025 19:16:06 GMT  
		Size: 49.5 MB (49455632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50100993944871564e604715d5e88e5fe803699b627d7e0f6cd41b985876a837`  
		Last Modified: Mon, 10 Feb 2025 19:57:57 GMT  
		Size: 162.3 MB (162257612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1cea42efb0ced412235a6862bd14a16149399655225043be3e1824c8579bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10722142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c8b95b843ee78137f174f4fd2a4624cdb61f30ee742e1c93c504f860a23c99`

```dockerfile
```

-	Layers:
	-	`sha256:68df2b44fc0a9a89806e7c73df41db5dcb5d96f26ec3908a4112ffc1146d8915`  
		Last Modified: Tue, 04 Feb 2025 18:10:06 GMT  
		Size: 10.7 MB (10711958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f075dda01916f2ca7466af9d3268cc6aeb6002f1a368a613c9e5f1258a5f3b3`  
		Last Modified: Tue, 04 Feb 2025 18:10:04 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
