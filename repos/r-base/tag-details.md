<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.5.1`](#r-base451)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.5.1`

```console
$ docker pull r-base@sha256:cbb1ea8643bccc7f07842cc210f2968b9235a3e53ccc4534999f81d9cbeddec7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `r-base:4.5.1` - linux; amd64

```console
$ docker pull r-base@sha256:8cd921cf375f97a849ddf154f639011df2c79560d1365f909075186d654671a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.4 MB (357431714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f43a399fd2946301d44547f825eb2b3b3328facef824b72948508f17bee87c`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1751241600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:8428338b5b0c78b619fd003ce0b25251e613f875f63f2cc98f8197270957b1ae`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 49.3 MB (49263873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f879b361de72d93eaa80e597f2aaaef9897af7ca629549843aa927e1c28aa9`  
		Last Modified: Tue, 01 Jul 2025 02:25:53 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7661b49decbd5e15eab610163e0ac6cf404976c731aa25f2c59985dd92b8cec0`  
		Last Modified: Tue, 01 Jul 2025 02:25:55 GMT  
		Size: 26.9 MB (26896954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0549860d5ad1dfddf1dad471eedbe5b1241a8b945ba6400ce6bc4ec95f474df`  
		Last Modified: Tue, 01 Jul 2025 02:25:53 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12deef81f7daea0516292c2ced591da972c476c820fd1666d46359ca7a58b89d`  
		Last Modified: Tue, 01 Jul 2025 02:25:53 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23807225136c643a9e52bb4b3c3c01dc777104ff40802cecdbabb57552293d55`  
		Last Modified: Tue, 01 Jul 2025 06:14:13 GMT  
		Size: 280.4 MB (280398735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.1` - unknown; unknown

```console
$ docker pull r-base@sha256:346f5152b22c0cf105df0df96d73c9687874e0757f451373d794503141a7c1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12941956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5d0c754b7038057014722a249b6f9ec84c3ff76827798f9e1d684ca91346db`

```dockerfile
```

-	Layers:
	-	`sha256:fa8fffeec6a8507edd9f0508afe332b38bc89d6cb6f22be892b86604a6a8f97a`  
		Last Modified: Tue, 01 Jul 2025 06:13:26 GMT  
		Size: 12.9 MB (12923815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1816da1082088e428b158d053992f0be2883e1c6c093982cdec4afb96c571970`  
		Last Modified: Tue, 01 Jul 2025 06:13:27 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.1` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:0d29725b3a78d483a111ddb579279373cace43a5801fc7cdcd161defda8de189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344490156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19ff8d12c5ead0a9a2c5a47ea9791ee8d76128753bef019153e86c2795556cf`
-	Default Command: `["R"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1749513600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2584ee33622825de68aac8f6321753e02da0f3221630beb0c925bab76ac076f1`  
		Last Modified: Tue, 10 Jun 2025 22:52:06 GMT  
		Size: 49.6 MB (49621526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9123f61ecfd11f8267d0e9fe82accaa3d09b4e765833e45f6f56605fe4194393`  
		Last Modified: Fri, 13 Jun 2025 19:50:08 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba869059508fe73d836c0a8de37f007ed2a8440a77d9d46c8d92096bc3b8a58e`  
		Last Modified: Fri, 13 Jun 2025 19:50:12 GMT  
		Size: 26.8 MB (26801076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eb9fb7a00277c1c775aec74e446bb433101ad1529ba30cdfb840b43f72f074`  
		Last Modified: Fri, 13 Jun 2025 19:50:10 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541854bf33a3ba388d77c3aba2f06751d705f4831a2cc4911ab2f937b276d0e5`  
		Last Modified: Fri, 13 Jun 2025 19:50:10 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2e0c728d04fe27c5a82b63454343c93a0861b4244ecd49c78dfe3421aec6fb`  
		Last Modified: Sat, 14 Jun 2025 01:27:55 GMT  
		Size: 267.2 MB (267195408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.1` - unknown; unknown

```console
$ docker pull r-base@sha256:c3194c532a4f6ea138cca008d95902a3808484305e1436b47026736094ee7064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13039996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730b00c70bf4e075d9eb0e096580f9c9e7ce9a33f9711a131412a61365182dc4`

```dockerfile
```

-	Layers:
	-	`sha256:6229fe6abd50955f0a27a19f350c7cf1eab6162692fa9065798e246647335af4`  
		Last Modified: Fri, 13 Jun 2025 21:13:30 GMT  
		Size: 13.0 MB (13021715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ced8295d3a32e3cb84c449abbfe699ee2d7fb0181776c02f9bc24a0db8a2e03`  
		Last Modified: Fri, 13 Jun 2025 21:13:31 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.1` - linux; ppc64le

```console
$ docker pull r-base@sha256:01b1b13dcccd17a9ceb10bb41e4554a74c6fd68f5ac762507b840ed122c6dbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 MB (351412957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474ec4a78cc54ecde539d03bea86d358974909ba71a0b48a45ed98434a5ee5e8`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1751241600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1b728f09c0d4a884c7e578388880f5403741a8474ca8476b12d102d5483ef593`  
		Last Modified: Tue, 01 Jul 2025 01:18:12 GMT  
		Size: 53.1 MB (53097233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f597ee12961e0ffe5f8457ec007f22abff4ff8d6cc3802a7e15052b135b5318`  
		Last Modified: Tue, 01 Jul 2025 04:41:41 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7b92365820ee2fc3b32f526e360f67d5c51e14682fe6b9124caefd1dc9021`  
		Last Modified: Tue, 01 Jul 2025 04:41:42 GMT  
		Size: 27.2 MB (27166511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e81148b0bb6f393f5e27b61dcbb5610ab6ae53fe0a3453377262b21068159dc`  
		Last Modified: Tue, 01 Jul 2025 04:41:41 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b39caabe6e2dd51c279b9f24e144adb4d56613711d7edcbba76c028a0864b34`  
		Last Modified: Tue, 01 Jul 2025 04:41:40 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfb43541d2aebd71f3ccda6ea7d86b0fcd1e731b2879231f2390fa9fe5e1a`  
		Last Modified: Tue, 01 Jul 2025 04:41:34 GMT  
		Size: 270.3 MB (270277063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.1` - unknown; unknown

```console
$ docker pull r-base@sha256:15701e8f985d51e15fb2f488dc0688ef3ce0a58659bf31c8fbc42b3ce7fa7f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12947645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631562c7ae2184ecb793c18887d5254fde9e3d082f299e477467827564cd6f52`

```dockerfile
```

-	Layers:
	-	`sha256:dab138bcc5ac1b7932c08af3db54f414190313470b74d3fb03660470eecd325c`  
		Last Modified: Tue, 01 Jul 2025 06:13:48 GMT  
		Size: 12.9 MB (12929464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b19b1caf55b917967aae0336a8f481f3cec518fd1297b243de99746a1d54cc40`  
		Last Modified: Tue, 01 Jul 2025 06:13:49 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.1` - linux; s390x

```console
$ docker pull r-base@sha256:1bb9d1d056836a6aeecdfab213f7c7e429984a850c72c93f3d244f8b379d9b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324638461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56beb3cbbe9b4f5a401a271c042cba98a9a64d5e94daaa99764e1956bbec9c16`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1751241600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:fe21c97c0cb8e48407e6d6b9e8a182aca6131bfbfd02bc56f0254723e44651ce`  
		Last Modified: Tue, 01 Jul 2025 01:18:03 GMT  
		Size: 49.3 MB (49343659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e3bc1e84ced161d4f0dd9932a79589f0b3753fefafdf9402ea45c60c009227`  
		Last Modified: Tue, 01 Jul 2025 05:15:54 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dc306906d0fc0c75553bc0f32a5439b1251dc2986dda30b2240c8019ef5235`  
		Last Modified: Tue, 01 Jul 2025 05:15:55 GMT  
		Size: 26.9 MB (26867828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b66d8cbbd2bcb5123536395d26e936553a15dc2dd524a854121d7031fe306`  
		Last Modified: Tue, 01 Jul 2025 05:15:54 GMT  
		Size: 924.5 KB (924545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f075431737ff48f943d3f0e6742efd359d0cdda3daf3e4103261f0b7a20ba`  
		Last Modified: Tue, 01 Jul 2025 05:15:53 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0374936323e91e084ecf324ab662e6772464148028b07d2d6e72e8a433351de`  
		Last Modified: Tue, 01 Jul 2025 05:13:37 GMT  
		Size: 247.5 MB (247498770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.1` - unknown; unknown

```console
$ docker pull r-base@sha256:05cdcfec18c2da93d4cace3e76049e7c9666d4b278b64779862ca9c35ad34fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12753097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9435f842f0c1e1cce44e6fb6c3aa4dbf854935b9239f05678c1d9fdbb817db`

```dockerfile
```

-	Layers:
	-	`sha256:f992def439024861366ab605571f4ef53da75a4bb3487ba73b0598c46b7c2326`  
		Last Modified: Tue, 01 Jul 2025 06:13:59 GMT  
		Size: 12.7 MB (12734956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d184292fe5235fa71e5b94c74537ed06ec7e6d42eb4c49e63ab99576caed53b`  
		Last Modified: Tue, 01 Jul 2025 06:14:00 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:cbb1ea8643bccc7f07842cc210f2968b9235a3e53ccc4534999f81d9cbeddec7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:8cd921cf375f97a849ddf154f639011df2c79560d1365f909075186d654671a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.4 MB (357431714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f43a399fd2946301d44547f825eb2b3b3328facef824b72948508f17bee87c`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1751241600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:8428338b5b0c78b619fd003ce0b25251e613f875f63f2cc98f8197270957b1ae`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 49.3 MB (49263873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f879b361de72d93eaa80e597f2aaaef9897af7ca629549843aa927e1c28aa9`  
		Last Modified: Tue, 01 Jul 2025 02:25:53 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7661b49decbd5e15eab610163e0ac6cf404976c731aa25f2c59985dd92b8cec0`  
		Last Modified: Tue, 01 Jul 2025 02:25:55 GMT  
		Size: 26.9 MB (26896954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0549860d5ad1dfddf1dad471eedbe5b1241a8b945ba6400ce6bc4ec95f474df`  
		Last Modified: Tue, 01 Jul 2025 02:25:53 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12deef81f7daea0516292c2ced591da972c476c820fd1666d46359ca7a58b89d`  
		Last Modified: Tue, 01 Jul 2025 02:25:53 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23807225136c643a9e52bb4b3c3c01dc777104ff40802cecdbabb57552293d55`  
		Last Modified: Tue, 01 Jul 2025 06:14:13 GMT  
		Size: 280.4 MB (280398735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:346f5152b22c0cf105df0df96d73c9687874e0757f451373d794503141a7c1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12941956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5d0c754b7038057014722a249b6f9ec84c3ff76827798f9e1d684ca91346db`

```dockerfile
```

-	Layers:
	-	`sha256:fa8fffeec6a8507edd9f0508afe332b38bc89d6cb6f22be892b86604a6a8f97a`  
		Last Modified: Tue, 01 Jul 2025 06:13:26 GMT  
		Size: 12.9 MB (12923815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1816da1082088e428b158d053992f0be2883e1c6c093982cdec4afb96c571970`  
		Last Modified: Tue, 01 Jul 2025 06:13:27 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:0d29725b3a78d483a111ddb579279373cace43a5801fc7cdcd161defda8de189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344490156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19ff8d12c5ead0a9a2c5a47ea9791ee8d76128753bef019153e86c2795556cf`
-	Default Command: `["R"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1749513600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2584ee33622825de68aac8f6321753e02da0f3221630beb0c925bab76ac076f1`  
		Last Modified: Tue, 10 Jun 2025 22:52:06 GMT  
		Size: 49.6 MB (49621526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9123f61ecfd11f8267d0e9fe82accaa3d09b4e765833e45f6f56605fe4194393`  
		Last Modified: Fri, 13 Jun 2025 19:50:08 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba869059508fe73d836c0a8de37f007ed2a8440a77d9d46c8d92096bc3b8a58e`  
		Last Modified: Fri, 13 Jun 2025 19:50:12 GMT  
		Size: 26.8 MB (26801076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eb9fb7a00277c1c775aec74e446bb433101ad1529ba30cdfb840b43f72f074`  
		Last Modified: Fri, 13 Jun 2025 19:50:10 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541854bf33a3ba388d77c3aba2f06751d705f4831a2cc4911ab2f937b276d0e5`  
		Last Modified: Fri, 13 Jun 2025 19:50:10 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2e0c728d04fe27c5a82b63454343c93a0861b4244ecd49c78dfe3421aec6fb`  
		Last Modified: Sat, 14 Jun 2025 01:27:55 GMT  
		Size: 267.2 MB (267195408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:c3194c532a4f6ea138cca008d95902a3808484305e1436b47026736094ee7064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13039996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730b00c70bf4e075d9eb0e096580f9c9e7ce9a33f9711a131412a61365182dc4`

```dockerfile
```

-	Layers:
	-	`sha256:6229fe6abd50955f0a27a19f350c7cf1eab6162692fa9065798e246647335af4`  
		Last Modified: Fri, 13 Jun 2025 21:13:30 GMT  
		Size: 13.0 MB (13021715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ced8295d3a32e3cb84c449abbfe699ee2d7fb0181776c02f9bc24a0db8a2e03`  
		Last Modified: Fri, 13 Jun 2025 21:13:31 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:01b1b13dcccd17a9ceb10bb41e4554a74c6fd68f5ac762507b840ed122c6dbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 MB (351412957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474ec4a78cc54ecde539d03bea86d358974909ba71a0b48a45ed98434a5ee5e8`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1751241600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1b728f09c0d4a884c7e578388880f5403741a8474ca8476b12d102d5483ef593`  
		Last Modified: Tue, 01 Jul 2025 01:18:12 GMT  
		Size: 53.1 MB (53097233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f597ee12961e0ffe5f8457ec007f22abff4ff8d6cc3802a7e15052b135b5318`  
		Last Modified: Tue, 01 Jul 2025 04:41:41 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7b92365820ee2fc3b32f526e360f67d5c51e14682fe6b9124caefd1dc9021`  
		Last Modified: Tue, 01 Jul 2025 04:41:42 GMT  
		Size: 27.2 MB (27166511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e81148b0bb6f393f5e27b61dcbb5610ab6ae53fe0a3453377262b21068159dc`  
		Last Modified: Tue, 01 Jul 2025 04:41:41 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b39caabe6e2dd51c279b9f24e144adb4d56613711d7edcbba76c028a0864b34`  
		Last Modified: Tue, 01 Jul 2025 04:41:40 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfb43541d2aebd71f3ccda6ea7d86b0fcd1e731b2879231f2390fa9fe5e1a`  
		Last Modified: Tue, 01 Jul 2025 04:41:34 GMT  
		Size: 270.3 MB (270277063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:15701e8f985d51e15fb2f488dc0688ef3ce0a58659bf31c8fbc42b3ce7fa7f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12947645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631562c7ae2184ecb793c18887d5254fde9e3d082f299e477467827564cd6f52`

```dockerfile
```

-	Layers:
	-	`sha256:dab138bcc5ac1b7932c08af3db54f414190313470b74d3fb03660470eecd325c`  
		Last Modified: Tue, 01 Jul 2025 06:13:48 GMT  
		Size: 12.9 MB (12929464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b19b1caf55b917967aae0336a8f481f3cec518fd1297b243de99746a1d54cc40`  
		Last Modified: Tue, 01 Jul 2025 06:13:49 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:1bb9d1d056836a6aeecdfab213f7c7e429984a850c72c93f3d244f8b379d9b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324638461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56beb3cbbe9b4f5a401a271c042cba98a9a64d5e94daaa99764e1956bbec9c16`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1751241600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:fe21c97c0cb8e48407e6d6b9e8a182aca6131bfbfd02bc56f0254723e44651ce`  
		Last Modified: Tue, 01 Jul 2025 01:18:03 GMT  
		Size: 49.3 MB (49343659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e3bc1e84ced161d4f0dd9932a79589f0b3753fefafdf9402ea45c60c009227`  
		Last Modified: Tue, 01 Jul 2025 05:15:54 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dc306906d0fc0c75553bc0f32a5439b1251dc2986dda30b2240c8019ef5235`  
		Last Modified: Tue, 01 Jul 2025 05:15:55 GMT  
		Size: 26.9 MB (26867828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b66d8cbbd2bcb5123536395d26e936553a15dc2dd524a854121d7031fe306`  
		Last Modified: Tue, 01 Jul 2025 05:15:54 GMT  
		Size: 924.5 KB (924545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f075431737ff48f943d3f0e6742efd359d0cdda3daf3e4103261f0b7a20ba`  
		Last Modified: Tue, 01 Jul 2025 05:15:53 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0374936323e91e084ecf324ab662e6772464148028b07d2d6e72e8a433351de`  
		Last Modified: Tue, 01 Jul 2025 05:13:37 GMT  
		Size: 247.5 MB (247498770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:05cdcfec18c2da93d4cace3e76049e7c9666d4b278b64779862ca9c35ad34fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12753097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9435f842f0c1e1cce44e6fb6c3aa4dbf854935b9239f05678c1d9fdbb817db`

```dockerfile
```

-	Layers:
	-	`sha256:f992def439024861366ab605571f4ef53da75a4bb3487ba73b0598c46b7c2326`  
		Last Modified: Tue, 01 Jul 2025 06:13:59 GMT  
		Size: 12.7 MB (12734956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d184292fe5235fa71e5b94c74537ed06ec7e6d42eb4c49e63ab99576caed53b`  
		Last Modified: Tue, 01 Jul 2025 06:14:00 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
