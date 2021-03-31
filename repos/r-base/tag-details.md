<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.0.4`](#r-base404)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.0.4`

```console
$ docker pull r-base@sha256:2fca5275e982e6524de032e45f2833645b64c6c1648384f8aebcfe970b448ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.0.4` - linux; amd64

```console
$ docker pull r-base@sha256:113d93a47de8e5e233cb2f73373fbac6cb96a818cea3dd616d49186d65d23d5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322899704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dd8148598f927fd02ac08bca0d3ccde628ea34a669f75ea292e900b2385309`
-	Default Command: `["R"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:05 GMT
ADD file:43e0ccd9ab01bd6f5c0a9aef5f2ea7c9ee9af30fdf11c8a9c591587a4d089c08 in / 
# Tue, 30 Mar 2021 21:51:06 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 13:59:48 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 31 Mar 2021 13:59:50 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 31 Mar 2021 14:00:07 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:00:10 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 31 Mar 2021 14:00:10 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 31 Mar 2021 14:00:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 31 Mar 2021 14:00:12 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 31 Mar 2021 14:00:12 GMT
ENV R_BASE_VERSION=4.0.4
# Wed, 31 Mar 2021 14:01:26 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:01:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:225ef05ef5535d13824643cc5f8d3e28d2d9fb76b074b6ec850f2d382becdd39`  
		Last Modified: Tue, 30 Mar 2021 21:57:29 GMT  
		Size: 54.9 MB (54868148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd07a5385f181125214dab9f13824e95ff6d85e268411e3e8d44aec5b74e3d0`  
		Last Modified: Wed, 31 Mar 2021 14:01:52 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebb54f13df4909a223c89a1b2008237b1f18f13314eb9ee909794f43b61173f`  
		Last Modified: Wed, 31 Mar 2021 14:01:59 GMT  
		Size: 25.6 MB (25627788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddc18d0a329020dbc8130e1377241e6c79fa9f4621595e207cff4bf58313f96`  
		Last Modified: Wed, 31 Mar 2021 14:01:54 GMT  
		Size: 864.6 KB (864592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758c7a4df06a1983be6c311c6ce5ddd02e39b2f8081f0afbccc15dd748a34690`  
		Last Modified: Wed, 31 Mar 2021 14:01:53 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b73484d95845fddf0bd4b13003bd074799523b6a722ac577ff56cca22ead36`  
		Last Modified: Wed, 31 Mar 2021 14:02:30 GMT  
		Size: 241.5 MB (241536948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.4` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:f29496d04d20e06f7d45a2801df0d7ff58e1179316c482e28ead2228e3eb53e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310543008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7055a4c66d4f04f8f7b5f4f85f7c05f396140ca6c41b73f9afe50cc4218b02`
-	Default Command: `["R"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:33 GMT
ADD file:f973554eedc62f5f46e9f38329e793a03f86e59390a1556f79308a27e73077cb in / 
# Tue, 30 Mar 2021 21:50:42 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:21:36 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 31 Mar 2021 14:21:40 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 31 Mar 2021 14:22:02 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:22:11 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 31 Mar 2021 14:22:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 31 Mar 2021 14:22:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 31 Mar 2021 14:22:15 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 31 Mar 2021 14:22:16 GMT
ENV R_BASE_VERSION=4.0.4
# Wed, 31 Mar 2021 14:23:58 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:24:03 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6c5abdff1282a06d2e6071056f94730d9de00eed3f6e167672759eb8fc9eb6e6`  
		Last Modified: Tue, 30 Mar 2021 21:57:31 GMT  
		Size: 53.6 MB (53555204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206f37d68995d36705e4f0d305852785158e659b5543570040b4fd8117c7ab42`  
		Last Modified: Wed, 31 Mar 2021 14:24:28 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5932c12088ccba0fa70a51b7e2892bbd1ba7b6c90498dc185fad40b526b96bc3`  
		Last Modified: Wed, 31 Mar 2021 14:24:33 GMT  
		Size: 25.6 MB (25628300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c6782189f1d92288d4bbfb6c1163badb6c20f80364b69bc80729faca2e0dc3`  
		Last Modified: Wed, 31 Mar 2021 14:24:28 GMT  
		Size: 864.6 KB (864597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafe8b6bb42f6fc8b04a61c3ad571e686e1ad0f08b6699c19d69d23bc5678846`  
		Last Modified: Wed, 31 Mar 2021 14:24:28 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27321d0f3669b21fa8c32f742892b61241d66f69b0526eeed89304124d62a05`  
		Last Modified: Wed, 31 Mar 2021 14:25:13 GMT  
		Size: 230.5 MB (230492678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.4` - linux; ppc64le

```console
$ docker pull r-base@sha256:ab164eba73b3445e2920bb87cb929dd0d0069a4b16fb42f789b9766d076d7ea9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320786790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3dee9f921f1ad8d99b9e688adb6fdd6f3187d41852b03a5f23232db672fb90d`
-	Default Command: `["R"]`

```dockerfile
# Tue, 30 Mar 2021 22:38:18 GMT
ADD file:edfcf9830c92f6132c01327ed8606a0f69870c393e5c0c7df42b6a56f64ed7d8 in / 
# Tue, 30 Mar 2021 22:38:25 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 16:33:43 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 31 Mar 2021 16:33:59 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 31 Mar 2021 16:35:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 16:36:08 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 31 Mar 2021 16:36:15 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 31 Mar 2021 16:36:19 GMT
ENV LANG=en_US.UTF-8
# Wed, 31 Mar 2021 16:36:30 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 31 Mar 2021 16:36:37 GMT
ENV R_BASE_VERSION=4.0.4
# Wed, 31 Mar 2021 16:47:47 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 16:47:53 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:4f44d41ee258a066a0c0b50b69d17bc36cebed954d5b1b5450cde5e7e38b6adc`  
		Last Modified: Tue, 30 Mar 2021 22:44:44 GMT  
		Size: 58.8 MB (58783345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1167c53c0bfd631e4e48cd0c2d406117f3a5744523b691e6a805bb565b36bfcc`  
		Last Modified: Wed, 31 Mar 2021 16:48:19 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b9eccbf4f4bfb7743d559571fe285f192b419219725f7e82d52d0f69ebe4f6`  
		Last Modified: Wed, 31 Mar 2021 16:48:24 GMT  
		Size: 25.9 MB (25850460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fb9ebcf49646bba04e9867a706faa0e1106d08c81f9cbb33478463e8a26416`  
		Last Modified: Wed, 31 Mar 2021 16:48:20 GMT  
		Size: 864.6 KB (864597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fea0f6b1edbea02a58a4bc1ced3906453a77dc78ab8394fb0140375d92ca9b`  
		Last Modified: Wed, 31 Mar 2021 16:48:19 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4f2b64e7bf12b4233155bd92d035c666865967e5e8c3ca800d62195ed5d06c`  
		Last Modified: Wed, 31 Mar 2021 16:49:02 GMT  
		Size: 235.3 MB (235286148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.4` - linux; s390x

```console
$ docker pull r-base@sha256:254e46f6da1ce20c02be7f4d5844bffa73c989ab95bde57302ad3404f2949e0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289262036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bb97e2f0177423bd859138e4e362ffdaa935edbd30f0fcdbb1e2d4a47afa64`
-	Default Command: `["R"]`

```dockerfile
# Tue, 30 Mar 2021 21:43:44 GMT
ADD file:8e1fa69c0f021a22f6b57a9caba4481a9da0cf39f239442db53eb11eacfbb45c in / 
# Tue, 30 Mar 2021 21:43:47 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:15:37 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 31 Mar 2021 02:15:39 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 31 Mar 2021 02:15:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 02:15:53 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 31 Mar 2021 02:15:54 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 31 Mar 2021 02:15:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 31 Mar 2021 02:15:55 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 31 Mar 2021 02:15:55 GMT
ENV R_BASE_VERSION=4.0.4
# Wed, 31 Mar 2021 02:17:09 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 02:17:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ca6391c3ba05dc203d2d8e0b8b0b4b2351b46f0ac20ce212409979a3060a7c71`  
		Last Modified: Tue, 30 Mar 2021 21:47:45 GMT  
		Size: 53.1 MB (53148482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749ce88b09f7367764e7639c47eab569213a01677050d4df02c1ea6909df17b8`  
		Last Modified: Wed, 31 Mar 2021 02:17:46 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8ba913a43f80e8e393cd3e31ad5f98e515cbf6b39ca9c2a0b049f8c0c5ec06`  
		Last Modified: Wed, 31 Mar 2021 02:17:49 GMT  
		Size: 25.6 MB (25632738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e977b3e3c3ec5d5e311ebecc068758159efe7d2d567aa7b5d9a0d3e3186b2f`  
		Last Modified: Wed, 31 Mar 2021 02:17:47 GMT  
		Size: 920.2 KB (920155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c805fcdb14d2e6cf6df0bd8025d91f9d381b0457729e620d366c577689db71f`  
		Last Modified: Wed, 31 Mar 2021 02:17:46 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93211c767e5c6138c810c33e46f3859714cf339a51ad5fad042eedb27b027a7`  
		Last Modified: Wed, 31 Mar 2021 02:18:11 GMT  
		Size: 209.6 MB (209558437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:2fca5275e982e6524de032e45f2833645b64c6c1648384f8aebcfe970b448ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:113d93a47de8e5e233cb2f73373fbac6cb96a818cea3dd616d49186d65d23d5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322899704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dd8148598f927fd02ac08bca0d3ccde628ea34a669f75ea292e900b2385309`
-	Default Command: `["R"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:05 GMT
ADD file:43e0ccd9ab01bd6f5c0a9aef5f2ea7c9ee9af30fdf11c8a9c591587a4d089c08 in / 
# Tue, 30 Mar 2021 21:51:06 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 13:59:48 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 31 Mar 2021 13:59:50 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 31 Mar 2021 14:00:07 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:00:10 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 31 Mar 2021 14:00:10 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 31 Mar 2021 14:00:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 31 Mar 2021 14:00:12 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 31 Mar 2021 14:00:12 GMT
ENV R_BASE_VERSION=4.0.4
# Wed, 31 Mar 2021 14:01:26 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:01:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:225ef05ef5535d13824643cc5f8d3e28d2d9fb76b074b6ec850f2d382becdd39`  
		Last Modified: Tue, 30 Mar 2021 21:57:29 GMT  
		Size: 54.9 MB (54868148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd07a5385f181125214dab9f13824e95ff6d85e268411e3e8d44aec5b74e3d0`  
		Last Modified: Wed, 31 Mar 2021 14:01:52 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebb54f13df4909a223c89a1b2008237b1f18f13314eb9ee909794f43b61173f`  
		Last Modified: Wed, 31 Mar 2021 14:01:59 GMT  
		Size: 25.6 MB (25627788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddc18d0a329020dbc8130e1377241e6c79fa9f4621595e207cff4bf58313f96`  
		Last Modified: Wed, 31 Mar 2021 14:01:54 GMT  
		Size: 864.6 KB (864592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758c7a4df06a1983be6c311c6ce5ddd02e39b2f8081f0afbccc15dd748a34690`  
		Last Modified: Wed, 31 Mar 2021 14:01:53 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b73484d95845fddf0bd4b13003bd074799523b6a722ac577ff56cca22ead36`  
		Last Modified: Wed, 31 Mar 2021 14:02:30 GMT  
		Size: 241.5 MB (241536948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:f29496d04d20e06f7d45a2801df0d7ff58e1179316c482e28ead2228e3eb53e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310543008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7055a4c66d4f04f8f7b5f4f85f7c05f396140ca6c41b73f9afe50cc4218b02`
-	Default Command: `["R"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:33 GMT
ADD file:f973554eedc62f5f46e9f38329e793a03f86e59390a1556f79308a27e73077cb in / 
# Tue, 30 Mar 2021 21:50:42 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:21:36 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 31 Mar 2021 14:21:40 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 31 Mar 2021 14:22:02 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:22:11 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 31 Mar 2021 14:22:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 31 Mar 2021 14:22:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 31 Mar 2021 14:22:15 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 31 Mar 2021 14:22:16 GMT
ENV R_BASE_VERSION=4.0.4
# Wed, 31 Mar 2021 14:23:58 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:24:03 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6c5abdff1282a06d2e6071056f94730d9de00eed3f6e167672759eb8fc9eb6e6`  
		Last Modified: Tue, 30 Mar 2021 21:57:31 GMT  
		Size: 53.6 MB (53555204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206f37d68995d36705e4f0d305852785158e659b5543570040b4fd8117c7ab42`  
		Last Modified: Wed, 31 Mar 2021 14:24:28 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5932c12088ccba0fa70a51b7e2892bbd1ba7b6c90498dc185fad40b526b96bc3`  
		Last Modified: Wed, 31 Mar 2021 14:24:33 GMT  
		Size: 25.6 MB (25628300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c6782189f1d92288d4bbfb6c1163badb6c20f80364b69bc80729faca2e0dc3`  
		Last Modified: Wed, 31 Mar 2021 14:24:28 GMT  
		Size: 864.6 KB (864597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafe8b6bb42f6fc8b04a61c3ad571e686e1ad0f08b6699c19d69d23bc5678846`  
		Last Modified: Wed, 31 Mar 2021 14:24:28 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27321d0f3669b21fa8c32f742892b61241d66f69b0526eeed89304124d62a05`  
		Last Modified: Wed, 31 Mar 2021 14:25:13 GMT  
		Size: 230.5 MB (230492678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:ab164eba73b3445e2920bb87cb929dd0d0069a4b16fb42f789b9766d076d7ea9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320786790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3dee9f921f1ad8d99b9e688adb6fdd6f3187d41852b03a5f23232db672fb90d`
-	Default Command: `["R"]`

```dockerfile
# Tue, 30 Mar 2021 22:38:18 GMT
ADD file:edfcf9830c92f6132c01327ed8606a0f69870c393e5c0c7df42b6a56f64ed7d8 in / 
# Tue, 30 Mar 2021 22:38:25 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 16:33:43 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 31 Mar 2021 16:33:59 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 31 Mar 2021 16:35:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 16:36:08 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 31 Mar 2021 16:36:15 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 31 Mar 2021 16:36:19 GMT
ENV LANG=en_US.UTF-8
# Wed, 31 Mar 2021 16:36:30 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 31 Mar 2021 16:36:37 GMT
ENV R_BASE_VERSION=4.0.4
# Wed, 31 Mar 2021 16:47:47 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 16:47:53 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:4f44d41ee258a066a0c0b50b69d17bc36cebed954d5b1b5450cde5e7e38b6adc`  
		Last Modified: Tue, 30 Mar 2021 22:44:44 GMT  
		Size: 58.8 MB (58783345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1167c53c0bfd631e4e48cd0c2d406117f3a5744523b691e6a805bb565b36bfcc`  
		Last Modified: Wed, 31 Mar 2021 16:48:19 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b9eccbf4f4bfb7743d559571fe285f192b419219725f7e82d52d0f69ebe4f6`  
		Last Modified: Wed, 31 Mar 2021 16:48:24 GMT  
		Size: 25.9 MB (25850460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fb9ebcf49646bba04e9867a706faa0e1106d08c81f9cbb33478463e8a26416`  
		Last Modified: Wed, 31 Mar 2021 16:48:20 GMT  
		Size: 864.6 KB (864597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fea0f6b1edbea02a58a4bc1ced3906453a77dc78ab8394fb0140375d92ca9b`  
		Last Modified: Wed, 31 Mar 2021 16:48:19 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4f2b64e7bf12b4233155bd92d035c666865967e5e8c3ca800d62195ed5d06c`  
		Last Modified: Wed, 31 Mar 2021 16:49:02 GMT  
		Size: 235.3 MB (235286148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:254e46f6da1ce20c02be7f4d5844bffa73c989ab95bde57302ad3404f2949e0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289262036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bb97e2f0177423bd859138e4e362ffdaa935edbd30f0fcdbb1e2d4a47afa64`
-	Default Command: `["R"]`

```dockerfile
# Tue, 30 Mar 2021 21:43:44 GMT
ADD file:8e1fa69c0f021a22f6b57a9caba4481a9da0cf39f239442db53eb11eacfbb45c in / 
# Tue, 30 Mar 2021 21:43:47 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:15:37 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 31 Mar 2021 02:15:39 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 31 Mar 2021 02:15:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 02:15:53 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 31 Mar 2021 02:15:54 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 31 Mar 2021 02:15:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 31 Mar 2021 02:15:55 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 31 Mar 2021 02:15:55 GMT
ENV R_BASE_VERSION=4.0.4
# Wed, 31 Mar 2021 02:17:09 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 02:17:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ca6391c3ba05dc203d2d8e0b8b0b4b2351b46f0ac20ce212409979a3060a7c71`  
		Last Modified: Tue, 30 Mar 2021 21:47:45 GMT  
		Size: 53.1 MB (53148482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749ce88b09f7367764e7639c47eab569213a01677050d4df02c1ea6909df17b8`  
		Last Modified: Wed, 31 Mar 2021 02:17:46 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8ba913a43f80e8e393cd3e31ad5f98e515cbf6b39ca9c2a0b049f8c0c5ec06`  
		Last Modified: Wed, 31 Mar 2021 02:17:49 GMT  
		Size: 25.6 MB (25632738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e977b3e3c3ec5d5e311ebecc068758159efe7d2d567aa7b5d9a0d3e3186b2f`  
		Last Modified: Wed, 31 Mar 2021 02:17:47 GMT  
		Size: 920.2 KB (920155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c805fcdb14d2e6cf6df0bd8025d91f9d381b0457729e620d366c577689db71f`  
		Last Modified: Wed, 31 Mar 2021 02:17:46 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93211c767e5c6138c810c33e46f3859714cf339a51ad5fad042eedb27b027a7`  
		Last Modified: Wed, 31 Mar 2021 02:18:11 GMT  
		Size: 209.6 MB (209558437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
