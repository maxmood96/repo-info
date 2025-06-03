## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:40958b700dfc7c11f9b2e7ffc8becd8acb4dbf2753a511666c27c6ebc3281306
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

### `buildpack-deps:oracular` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1bfe220e2f64382ba383f7b06f6456d42fa6f6684e72235e3147985f2a66ee8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286870888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0741ef6159eca9896344afd13620e2cb46b5f6bf2b1a9f18a9aa4b426105e618`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:8e4ff40a1983cd8e3a737555205d0155f8245cf78c17eba45447c5ff8bf42a62 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ad109e5dce93c39830a72466a5071a150963a59aaf6898904da6372c54117c25`  
		Last Modified: Fri, 23 May 2025 21:42:21 GMT  
		Size: 30.7 MB (30677976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2b8cee836776204d1ab24be8c1d658151b007d82d4fe58787962f5d3eac961`  
		Last Modified: Tue, 03 Jun 2025 04:15:38 GMT  
		Size: 15.4 MB (15398586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9993a6828fb10acefc205deaace840d58b1960a35205080c36060e559fd42b`  
		Last Modified: Tue, 03 Jun 2025 05:11:58 GMT  
		Size: 46.7 MB (46668151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0dab58c612328a4002eab3d75e71e5dfefe33401c26d4ee99f1b6af6dc70e0`  
		Last Modified: Tue, 03 Jun 2025 06:12:23 GMT  
		Size: 194.1 MB (194126175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0bda419c5eda6bf448d81e58d2b2e9467707744c2a8a6757dfa341a8376ce6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11456338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aa085bf54279b687e7cd9e23ce11ecf23a90d0506d67c197cb842471c73632`

```dockerfile
```

-	Layers:
	-	`sha256:8066bb05fe46b3e0fdfbe6e7a7ed766c43bb76bbe505b982c3a871b4c1a5ef1b`  
		Last Modified: Tue, 03 Jun 2025 06:12:21 GMT  
		Size: 11.4 MB (11446136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e41eaee28ce9ce223d9f3c8f5f92fa04dafaac3afb0459d042a0412be472c5b`  
		Last Modified: Tue, 03 Jun 2025 06:12:21 GMT  
		Size: 10.2 KB (10202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:55828ba6d959452dc75c82f103bc1427d015b746a14038e6fa757027b97582c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248788782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e8e8ad222907dd9c3438dda8cd815f3b04bb161beb3619bfa4f5eb05aa3da8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:4bd97a769ac0690d3e7b50b15f6e685a8b191f6fb2a06a7ef3ac828715a8068a in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7a3f105306feae40c7cb270b7035492092da412b5fc113c7216ed37da473f3d9`  
		Last Modified: Fri, 23 May 2025 21:42:34 GMT  
		Size: 27.6 MB (27572634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da83b7fa93057f388593602c3bda3fb3e5ccfee1a1b433dc035980fae16e2d61`  
		Last Modified: Tue, 03 Jun 2025 04:17:37 GMT  
		Size: 14.1 MB (14064341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd4ac349e7cdcd51bdf615f609a68fe1f91db10ae98f1afd412a034ffffd256`  
		Last Modified: Tue, 03 Jun 2025 05:13:30 GMT  
		Size: 49.5 MB (49479820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02faceaaafdb6021e108b19d470c70d78949f948562d8996686af53a4dc92a02`  
		Last Modified: Tue, 03 Jun 2025 06:20:53 GMT  
		Size: 157.7 MB (157671987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dffb1fde3abfc280e57ba2430c0308f77cb74fd618a2e909d14db8f2cef1d5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11234403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dd27a72e54de12af69ab5ce0fa778590faf2440f88897d3f8e41fd5921aab3`

```dockerfile
```

-	Layers:
	-	`sha256:6d51421d50baad77c40168c7205b9cf0b6277c8d19e111d52a72b33c265a169e`  
		Last Modified: Tue, 03 Jun 2025 06:20:49 GMT  
		Size: 11.2 MB (11224140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b513c71ec60c998b1d2f9e666cf63de13897043fbad4e71eaa7cf24c98dfed5`  
		Last Modified: Tue, 03 Jun 2025 06:20:49 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d66e21c163272bbc1a84f3083baba15063cb494c03bacf58724ce9ddd851c506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280563201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1570bd4689ea6184c7bdde8552c456d77ae777422e73e988dc4a79a3a65cb9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:458f2262832f9254682efb663e94ed73cf9f068bc4799f5a25ffb533a869ed44 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d825962f62a727b0760fe9a4f96a67a09a0d2a8077e99007e7681149f2ab3fd`  
		Last Modified: Fri, 21 Mar 2025 09:40:50 GMT  
		Size: 30.3 MB (30320224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eacb0abd365e7ac96a553eb11a8b04ca8a62c023926633845107e9e215227a7`  
		Last Modified: Wed, 09 Apr 2025 06:11:20 GMT  
		Size: 15.3 MB (15330068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28478c451efafdd58825833b7a96ab18f7d12cc4d2cf5871b329ac70bc3074e5`  
		Last Modified: Wed, 09 Apr 2025 14:00:14 GMT  
		Size: 46.5 MB (46534730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e4ac0edbe0b1bf373a838ed269c9224b4e44d69dfded6f05134683d137bc95`  
		Last Modified: Wed, 09 Apr 2025 18:26:22 GMT  
		Size: 188.4 MB (188378179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e085c6ef282908fd44c5e8e2c062c49a41016186a1226c6050272d2b785114a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11428912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b6f66c08970aa2ca22c9f2f3f28641aa7754e957b4e46fab99ca6b381804f`

```dockerfile
```

-	Layers:
	-	`sha256:cddb8653758f5b78d7a915707cffb429f08e15976bb6097944ae84c1e104b23b`  
		Last Modified: Wed, 09 Apr 2025 18:26:18 GMT  
		Size: 11.4 MB (11418629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41cfe2e4ab977b85c3e2b4937b588f702c731979807a89acde4752097b631ae`  
		Last Modified: Wed, 09 Apr 2025 18:26:17 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f90d501fe401ad938fe71a1bc80687a8e1b19bb12bbb85200c2a48aeedc2041c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302253805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66528d11ea66362687924c82cf524ef4102cffe6c860149033bd7b687c41e8eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:1b338c439eae4a20ee7d1b84db98f2f0664cd0c53c3843407f28a1b33a48c0ae in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8617c693189c511af931ec6b7aa3573654d8d3d3274b061f881929dc7e9e831e`  
		Last Modified: Fri, 21 Mar 2025 09:41:03 GMT  
		Size: 35.1 MB (35116459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eca3df5efb1d2a7a155d29563d34a4cc59b77f1356adfd169ce229390b6bd91`  
		Last Modified: Wed, 09 Apr 2025 04:30:59 GMT  
		Size: 17.5 MB (17490417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdbf25494c1d33658a8d848c137015fdf810bc230f9fa986642899a607aab15`  
		Last Modified: Wed, 09 Apr 2025 07:39:13 GMT  
		Size: 51.8 MB (51818048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c732b52206caeeae18937373be417f9071c7502917174bb680d74b867d9307`  
		Last Modified: Wed, 09 Apr 2025 13:41:21 GMT  
		Size: 197.8 MB (197828881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4121f8709350df1f0b3018e36879888c4814127a77b462a5ca1d7e4a80c00478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11344939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6cb192cb4d53082754c17b55d321439c82600cb3bcb3bcb30ddd0b392c9542`

```dockerfile
```

-	Layers:
	-	`sha256:5c234cedcbb845b6053bd306e97a4ac27427092e43bcd3b89dbbc4842402e8d0`  
		Last Modified: Wed, 09 Apr 2025 13:41:16 GMT  
		Size: 11.3 MB (11334706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62473be04f1c9f1f92c2169536875d423e597d308d44476846c8ff6ece4a25d5`  
		Last Modified: Wed, 09 Apr 2025 13:41:15 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7a07c45844ca69f5a6b3e46f2c4ff9cec65c99a359c3db0d720a94e349541b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 MB (378982155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dfb95fc0deffdff66b2b4625e8b16257435515597c48ea7d29572794c3bf67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:e17f3a566611e6e6aaf40f0cf67dace1148c4e227e136a582732abd5470cc4bb in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:17143e5c2a0de46dd660097f35b7d1c381a1cfd489bea2cdd1a596a3e3b08cda`  
		Last Modified: Fri, 21 Mar 2025 09:41:10 GMT  
		Size: 31.8 MB (31808054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f1c68219c9767213bddad50e7129bda08a3407ab786d2bb7b5a54df5e760ea`  
		Last Modified: Wed, 09 Apr 2025 05:21:45 GMT  
		Size: 16.2 MB (16187400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff1351043fedb7e8229fe0f7f54e7d9a6728f389ecd49c4378c8f4a18d98c04`  
		Last Modified: Wed, 09 Apr 2025 08:46:47 GMT  
		Size: 54.6 MB (54603679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c63de24acdbd03cbc02a42295bbdb4b8d76a4a21a7feb144a1c9467108b1062`  
		Last Modified: Wed, 09 Apr 2025 11:24:08 GMT  
		Size: 276.4 MB (276383022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:76b3f8610f614164c04bd03042ae03b0f5f4ebdc653384bf723afe8306ff4961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11400817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcaa0c60af0f9f202e1ce8713ea7360ab69262f5ed3af5d97d0131a5859ee8d0`

```dockerfile
```

-	Layers:
	-	`sha256:55dc3f41832622fe3e0fa5d8245762f0e708442c29c2352c29e729573ef22ddc`  
		Last Modified: Wed, 09 Apr 2025 11:23:32 GMT  
		Size: 11.4 MB (11390582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e75181ba371400030cc90cc4288850be4885bc37fd9f9e078bd76b355b072c`  
		Last Modified: Wed, 09 Apr 2025 11:23:30 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:26c918c01186f0195cf4de0b6b7e88635b302f5e075bc8150ecc0d5f4b968bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266106494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29fe10f38df9863f72be781f8ccb898e20f546334bf8f6895f9eb37cb722985b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:eb903d7651ff3dbf09f650f4f09293336b52876503a80b8a4055a1ee62e3681c in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eb0749c1557961032471b04d5d1ae0eb7c6319cc8c49244b9e349a1baf046b25`  
		Last Modified: Fri, 23 May 2025 21:42:53 GMT  
		Size: 30.8 MB (30838341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4ac8e25728fec411be64a8d6a2f3e5312d6aa9e0894a84e88bcab877eba1ae`  
		Last Modified: Tue, 03 Jun 2025 04:17:23 GMT  
		Size: 17.0 MB (16962576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769d57f65904d05b379d26a14b3229969e463ab70b9a753c429a50c9dac25be`  
		Last Modified: Tue, 03 Jun 2025 05:17:50 GMT  
		Size: 48.1 MB (48099244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288ceee80a8da0407fe28b9cc87a804ac12e9b855d4063670f583ed1876221c`  
		Last Modified: Tue, 03 Jun 2025 07:02:00 GMT  
		Size: 170.2 MB (170206333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:100faae70925c07f6e779e6e633b05324710c809a1e19042015a758d8f45f811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11253753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2b23277f1518dfbdf2ebdacab0acb99819afc1904d531fbaa1d70ea9094ac4`

```dockerfile
```

-	Layers:
	-	`sha256:2db1bb354c6dc7d02596d2f32670594e6a8c344f3c862612ebaea48c6cb842e6`  
		Last Modified: Tue, 03 Jun 2025 07:01:57 GMT  
		Size: 11.2 MB (11243550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8b4ec98daacb20b6aa66df18cfca0a645b8fa182bdf423b1c8aaac42b4696f0`  
		Last Modified: Tue, 03 Jun 2025 07:01:57 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
