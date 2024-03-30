<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.3.3`](#r-base433)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.3.3`

```console
$ docker pull r-base@sha256:4618f5f9acc991f414ebabc4fb37cc479ef00eb24b7b4f79ca1d2fc9fc88140b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.3.3` - linux; amd64

```console
$ docker pull r-base@sha256:13a6ae21697e5cd8be3b4e1ef193dc4cb7c562f4b5ca02f4965e6a8844d24a82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.8 MB (373777292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72151f54dc8191faee452210d1053a4168ea247a424ba021c45e3eaf066630fb`
-	Default Command: `["R"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:41 GMT
ADD file:77b2384f97a0a5676c125b86f783e7ab40180debb7991c6056f1792dc33f367a in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:57:00 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 30 Mar 2024 21:57:00 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Sat, 30 Mar 2024 21:57:09 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:57:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:57:12 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 30 Mar 2024 21:57:12 GMT
ENV LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:57:12 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 30 Mar 2024 21:57:13 GMT
ENV R_BASE_VERSION=4.3.3
# Sat, 30 Mar 2024 21:58:17 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:58:19 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f7635fb521f044eccaf7ecb3cf352ae689043c2d033b3999755c0c9fad1c3836`  
		Last Modified: Sat, 30 Mar 2024 20:55:11 GMT  
		Size: 52.3 MB (52332499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264c83b0f9f9fe753816f764bbeeb4da338a28118f69203478a962430e776912`  
		Last Modified: Sat, 30 Mar 2024 21:58:29 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3cc01e955b926f12c433ea2223e619bc35ae207478e196424bd18d57b61efa`  
		Last Modified: Sat, 30 Mar 2024 21:58:32 GMT  
		Size: 22.8 MB (22848764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844b1bcd104727555cf1e93c7c1a87f9bdae9dde3e22112cec870cdd2b597e00`  
		Last Modified: Sat, 30 Mar 2024 21:58:29 GMT  
		Size: 866.3 KB (866332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1f89e7cd0d15ab3f677b6b55e4656e660e3458b15959aec54f052ff9dd484`  
		Last Modified: Sat, 30 Mar 2024 21:58:29 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc314dc6a16a248d14866c9615dc28f6d652883110ddfd0034346e80209065`  
		Last Modified: Sat, 30 Mar 2024 21:59:02 GMT  
		Size: 297.7 MB (297725992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.3` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:8b37274b0740f697ab4753c6ec550346811738057479442715173851980b042f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360442736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0555de241164bd162b6042fa9dc5b7046c40048c73e66edb4dcab501931b3b22`
-	Default Command: `["R"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:20 GMT
ADD file:fc3581778ead218cf3f2b0cc783c67d5a425cb255a88178c9f2a6f07a1806740 in / 
# Sat, 30 Mar 2024 20:55:21 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:30:20 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 30 Mar 2024 21:30:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Sat, 30 Mar 2024 21:30:30 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:30:32 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:30:32 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 30 Mar 2024 21:30:32 GMT
ENV LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:30:32 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 30 Mar 2024 21:30:32 GMT
ENV R_BASE_VERSION=4.3.3
# Sat, 30 Mar 2024 21:31:53 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:31:58 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b431ee02c5840b16ec0729ce2312ad3bdbd0a4edca10b33678f7132ad29de406`  
		Last Modified: Sat, 30 Mar 2024 20:57:27 GMT  
		Size: 52.2 MB (52193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563ed164f1ed2a724f6e2937d88db638383383f6d5283ec7ffdc19bebb831e87`  
		Last Modified: Sat, 30 Mar 2024 21:32:19 GMT  
		Size: 3.4 KB (3359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db62cb80c94023c2d9f8c02956591cc8b76182268aaeab447888f5e3f465d1`  
		Last Modified: Sat, 30 Mar 2024 21:32:21 GMT  
		Size: 22.8 MB (22836594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bc9da573d53d06f368c983cb0936e592483dff845578c0d051d29fca97ba2c`  
		Last Modified: Sat, 30 Mar 2024 21:32:19 GMT  
		Size: 866.3 KB (866328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c027dd1714db232eaafc003e85ee316c329ec4e87f38c646db0881fd5caf5bc`  
		Last Modified: Sat, 30 Mar 2024 21:32:19 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2c012c235c0c4f3da2e99c7c8f50ea22355a80fbf40d9d7afc4c40fbd4d69c`  
		Last Modified: Sat, 30 Mar 2024 21:32:42 GMT  
		Size: 284.5 MB (284542940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.3` - linux; ppc64le

```console
$ docker pull r-base@sha256:f775ad6748a28a85e4826749e44f5e2eba5f673281f0e07642c43f900cedfb5a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.5 MB (376502791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8e774839f459351637cef2369f4f946572b3aef91f6bf7e0cd17e557be2223`
-	Default Command: `["R"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:36 GMT
ADD file:969150af93cca0492ec38ed28e99d751e4328a4b698b0749dba2a7efb2294919 in / 
# Sat, 30 Mar 2024 20:55:39 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:26:32 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 30 Mar 2024 21:26:34 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Sat, 30 Mar 2024 21:26:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:26:58 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:26:58 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 30 Mar 2024 21:26:58 GMT
ENV LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:27:00 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 30 Mar 2024 21:27:00 GMT
ENV R_BASE_VERSION=4.3.3
# Sat, 30 Mar 2024 21:30:10 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:30:19 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:8890528697eb671e515f58d20d435b6f73354841a85505ed32df7ec7b2749faf`  
		Last Modified: Sat, 30 Mar 2024 20:58:13 GMT  
		Size: 56.2 MB (56249519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc5cf1096431b5c360cc1b59c28226f1a864413a6fddfab787f4001dde81c81`  
		Last Modified: Sat, 30 Mar 2024 21:30:33 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77092bc3d79c43656caf2748d748e45495f9deb4ee04b56e549e8f6e7f22b1c6`  
		Last Modified: Sat, 30 Mar 2024 21:30:35 GMT  
		Size: 23.1 MB (23070729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075f6951b61d7e1afaf6186ce9ac54494f150cd7aa9b8df46afb0a639756f785`  
		Last Modified: Sat, 30 Mar 2024 21:30:33 GMT  
		Size: 866.3 KB (866334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d7e2f51933d94c5d11f4c5b736b87da72c18cdb8c14fec823518a68ae6f47b`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1854d41037d059f69735b972c3ed8ac2dca294ad6e915e1c064d420261412b14`  
		Last Modified: Sat, 30 Mar 2024 21:31:11 GMT  
		Size: 296.3 MB (296312501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.3` - linux; s390x

```console
$ docker pull r-base@sha256:3a543dca6e9b4cd52292fc1ee0719b81996d9de5014bc93280d9bc3e8530a595
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346453415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3b362dbd8e746962c7d27cc28d3c6cd2ca55aa03ae592430580bda2ea222da`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Mar 2024 01:08:50 GMT
ADD file:283bc28845dbc58b098cbb254944cfae0c1d6f16ae79ae7362fad52560500387 in / 
# Tue, 12 Mar 2024 01:08:55 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:19:39 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Mar 2024 04:19:39 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 12 Mar 2024 04:19:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:19:50 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Mar 2024 04:19:50 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Mar 2024 04:19:51 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Mar 2024 04:19:51 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Mar 2024 04:19:51 GMT
ENV R_BASE_VERSION=4.3.3
# Tue, 12 Mar 2024 04:20:49 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:21:00 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:073f53dd9806858358fdd1059a56d049af47a20cad92d4f3e90dc7bcff46e1b1`  
		Last Modified: Tue, 12 Mar 2024 01:23:21 GMT  
		Size: 51.7 MB (51738496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c31cfed1b9d230d2a397e61a7586aae350c5bdde507f494f9eb294fa7e828f6`  
		Last Modified: Tue, 12 Mar 2024 04:22:05 GMT  
		Size: 3.4 KB (3362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e9bd9b0fa94aa5fc24c4b8a5058d9275b468b03f8002b84eac598823d1749c`  
		Last Modified: Tue, 12 Mar 2024 04:22:07 GMT  
		Size: 23.0 MB (22951719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ba7acf6d22a6f403e38ad87493e460797ad26343c48d711dd4bea2ba1f4ee`  
		Last Modified: Tue, 12 Mar 2024 04:22:05 GMT  
		Size: 922.3 KB (922275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4d1d768fbc272150584385277dbafbb9b8718f30e1ebecc85a106d022187e5`  
		Last Modified: Tue, 12 Mar 2024 04:22:05 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32400e4d0960ccf024cb6da7fcffc3b57f2e4aacc190e22863ae4c43bb61293d`  
		Last Modified: Tue, 12 Mar 2024 04:22:33 GMT  
		Size: 270.8 MB (270837215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:4618f5f9acc991f414ebabc4fb37cc479ef00eb24b7b4f79ca1d2fc9fc88140b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:13a6ae21697e5cd8be3b4e1ef193dc4cb7c562f4b5ca02f4965e6a8844d24a82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.8 MB (373777292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72151f54dc8191faee452210d1053a4168ea247a424ba021c45e3eaf066630fb`
-	Default Command: `["R"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:41 GMT
ADD file:77b2384f97a0a5676c125b86f783e7ab40180debb7991c6056f1792dc33f367a in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:57:00 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 30 Mar 2024 21:57:00 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Sat, 30 Mar 2024 21:57:09 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:57:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:57:12 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 30 Mar 2024 21:57:12 GMT
ENV LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:57:12 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 30 Mar 2024 21:57:13 GMT
ENV R_BASE_VERSION=4.3.3
# Sat, 30 Mar 2024 21:58:17 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:58:19 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f7635fb521f044eccaf7ecb3cf352ae689043c2d033b3999755c0c9fad1c3836`  
		Last Modified: Sat, 30 Mar 2024 20:55:11 GMT  
		Size: 52.3 MB (52332499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264c83b0f9f9fe753816f764bbeeb4da338a28118f69203478a962430e776912`  
		Last Modified: Sat, 30 Mar 2024 21:58:29 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3cc01e955b926f12c433ea2223e619bc35ae207478e196424bd18d57b61efa`  
		Last Modified: Sat, 30 Mar 2024 21:58:32 GMT  
		Size: 22.8 MB (22848764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844b1bcd104727555cf1e93c7c1a87f9bdae9dde3e22112cec870cdd2b597e00`  
		Last Modified: Sat, 30 Mar 2024 21:58:29 GMT  
		Size: 866.3 KB (866332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1f89e7cd0d15ab3f677b6b55e4656e660e3458b15959aec54f052ff9dd484`  
		Last Modified: Sat, 30 Mar 2024 21:58:29 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc314dc6a16a248d14866c9615dc28f6d652883110ddfd0034346e80209065`  
		Last Modified: Sat, 30 Mar 2024 21:59:02 GMT  
		Size: 297.7 MB (297725992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:8b37274b0740f697ab4753c6ec550346811738057479442715173851980b042f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360442736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0555de241164bd162b6042fa9dc5b7046c40048c73e66edb4dcab501931b3b22`
-	Default Command: `["R"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:20 GMT
ADD file:fc3581778ead218cf3f2b0cc783c67d5a425cb255a88178c9f2a6f07a1806740 in / 
# Sat, 30 Mar 2024 20:55:21 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:30:20 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 30 Mar 2024 21:30:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Sat, 30 Mar 2024 21:30:30 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:30:32 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:30:32 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 30 Mar 2024 21:30:32 GMT
ENV LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:30:32 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 30 Mar 2024 21:30:32 GMT
ENV R_BASE_VERSION=4.3.3
# Sat, 30 Mar 2024 21:31:53 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:31:58 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b431ee02c5840b16ec0729ce2312ad3bdbd0a4edca10b33678f7132ad29de406`  
		Last Modified: Sat, 30 Mar 2024 20:57:27 GMT  
		Size: 52.2 MB (52193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563ed164f1ed2a724f6e2937d88db638383383f6d5283ec7ffdc19bebb831e87`  
		Last Modified: Sat, 30 Mar 2024 21:32:19 GMT  
		Size: 3.4 KB (3359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db62cb80c94023c2d9f8c02956591cc8b76182268aaeab447888f5e3f465d1`  
		Last Modified: Sat, 30 Mar 2024 21:32:21 GMT  
		Size: 22.8 MB (22836594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bc9da573d53d06f368c983cb0936e592483dff845578c0d051d29fca97ba2c`  
		Last Modified: Sat, 30 Mar 2024 21:32:19 GMT  
		Size: 866.3 KB (866328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c027dd1714db232eaafc003e85ee316c329ec4e87f38c646db0881fd5caf5bc`  
		Last Modified: Sat, 30 Mar 2024 21:32:19 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2c012c235c0c4f3da2e99c7c8f50ea22355a80fbf40d9d7afc4c40fbd4d69c`  
		Last Modified: Sat, 30 Mar 2024 21:32:42 GMT  
		Size: 284.5 MB (284542940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:f775ad6748a28a85e4826749e44f5e2eba5f673281f0e07642c43f900cedfb5a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.5 MB (376502791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8e774839f459351637cef2369f4f946572b3aef91f6bf7e0cd17e557be2223`
-	Default Command: `["R"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:36 GMT
ADD file:969150af93cca0492ec38ed28e99d751e4328a4b698b0749dba2a7efb2294919 in / 
# Sat, 30 Mar 2024 20:55:39 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:26:32 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 30 Mar 2024 21:26:34 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Sat, 30 Mar 2024 21:26:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:26:58 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:26:58 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 30 Mar 2024 21:26:58 GMT
ENV LANG=en_US.UTF-8
# Sat, 30 Mar 2024 21:27:00 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 30 Mar 2024 21:27:00 GMT
ENV R_BASE_VERSION=4.3.3
# Sat, 30 Mar 2024 21:30:10 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:30:19 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:8890528697eb671e515f58d20d435b6f73354841a85505ed32df7ec7b2749faf`  
		Last Modified: Sat, 30 Mar 2024 20:58:13 GMT  
		Size: 56.2 MB (56249519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc5cf1096431b5c360cc1b59c28226f1a864413a6fddfab787f4001dde81c81`  
		Last Modified: Sat, 30 Mar 2024 21:30:33 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77092bc3d79c43656caf2748d748e45495f9deb4ee04b56e549e8f6e7f22b1c6`  
		Last Modified: Sat, 30 Mar 2024 21:30:35 GMT  
		Size: 23.1 MB (23070729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075f6951b61d7e1afaf6186ce9ac54494f150cd7aa9b8df46afb0a639756f785`  
		Last Modified: Sat, 30 Mar 2024 21:30:33 GMT  
		Size: 866.3 KB (866334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d7e2f51933d94c5d11f4c5b736b87da72c18cdb8c14fec823518a68ae6f47b`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1854d41037d059f69735b972c3ed8ac2dca294ad6e915e1c064d420261412b14`  
		Last Modified: Sat, 30 Mar 2024 21:31:11 GMT  
		Size: 296.3 MB (296312501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:3a543dca6e9b4cd52292fc1ee0719b81996d9de5014bc93280d9bc3e8530a595
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346453415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3b362dbd8e746962c7d27cc28d3c6cd2ca55aa03ae592430580bda2ea222da`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Mar 2024 01:08:50 GMT
ADD file:283bc28845dbc58b098cbb254944cfae0c1d6f16ae79ae7362fad52560500387 in / 
# Tue, 12 Mar 2024 01:08:55 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:19:39 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Mar 2024 04:19:39 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 12 Mar 2024 04:19:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:19:50 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Mar 2024 04:19:50 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Mar 2024 04:19:51 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Mar 2024 04:19:51 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Mar 2024 04:19:51 GMT
ENV R_BASE_VERSION=4.3.3
# Tue, 12 Mar 2024 04:20:49 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:21:00 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:073f53dd9806858358fdd1059a56d049af47a20cad92d4f3e90dc7bcff46e1b1`  
		Last Modified: Tue, 12 Mar 2024 01:23:21 GMT  
		Size: 51.7 MB (51738496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c31cfed1b9d230d2a397e61a7586aae350c5bdde507f494f9eb294fa7e828f6`  
		Last Modified: Tue, 12 Mar 2024 04:22:05 GMT  
		Size: 3.4 KB (3362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e9bd9b0fa94aa5fc24c4b8a5058d9275b468b03f8002b84eac598823d1749c`  
		Last Modified: Tue, 12 Mar 2024 04:22:07 GMT  
		Size: 23.0 MB (22951719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ba7acf6d22a6f403e38ad87493e460797ad26343c48d711dd4bea2ba1f4ee`  
		Last Modified: Tue, 12 Mar 2024 04:22:05 GMT  
		Size: 922.3 KB (922275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4d1d768fbc272150584385277dbafbb9b8718f30e1ebecc85a106d022187e5`  
		Last Modified: Tue, 12 Mar 2024 04:22:05 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32400e4d0960ccf024cb6da7fcffc3b57f2e4aacc190e22863ae4c43bb61293d`  
		Last Modified: Tue, 12 Mar 2024 04:22:33 GMT  
		Size: 270.8 MB (270837215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
