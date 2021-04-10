<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.0.5`](#r-base405)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.0.5`

```console
$ docker pull r-base@sha256:eef69960e471af78073aa1e2abacaaa555ac85b401611590ee160130c6845846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.0.5` - linux; amd64

```console
$ docker pull r-base@sha256:af1b9007d8c81d0cc3cf8d11eed912537623b08a0bf8697ddba18f091bed64ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323897200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8020514dfa2784462c2ab3d5a1d402ae370067dfd4065c36de0c8ba09ab56b`
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
# Fri, 02 Apr 2021 18:38:49 GMT
ENV R_BASE_VERSION=4.0.5
# Fri, 02 Apr 2021 18:38:50 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 02 Apr 2021 18:39:56 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Apr 2021 18:39:58 GMT
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
	-	`sha256:bf4aad63e756385206bdfa2a4730ead3d2ed716f1fd74169adb4c0690080534c`  
		Last Modified: Fri, 02 Apr 2021 18:40:21 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacc3d4038d7a8e85d8e39f0d96ad8648830ccb99c32e9f62170981433ae0ff2`  
		Last Modified: Fri, 02 Apr 2021 18:41:04 GMT  
		Size: 242.5 MB (242534151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.5` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:04ee057922d716542df86dee50448cec991b9e8d875671cecf2e591ec69f89f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311476289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917fbf45f92c3a87dee003685ab1979ab729995d6ae9b4fa3dbb917f283bd55a`
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
# Fri, 02 Apr 2021 19:25:14 GMT
ENV R_BASE_VERSION=4.0.5
# Fri, 02 Apr 2021 19:25:17 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 02 Apr 2021 19:27:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Apr 2021 19:27:06 GMT
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
	-	`sha256:7deb90318bb05ae2bafb8f5f89905821bbcdfa7e0cd51ef970821d275c5fb6e8`  
		Last Modified: Fri, 02 Apr 2021 19:27:23 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b694158ddafd8f34e2523c4936f239f1bcca716d6ff449c65d1a438b946ccffd`  
		Last Modified: Fri, 02 Apr 2021 19:28:13 GMT  
		Size: 231.4 MB (231425663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.5` - linux; ppc64le

```console
$ docker pull r-base@sha256:95d0fa7b1456ccbd1a8a210b813fe59b70a713083313a80953746c6d710a2878
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321717753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03a067e1f4c4a1cf934cf453918a85bc96e7bca346eef202dae379bf18c7135`
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
# Fri, 02 Apr 2021 18:47:39 GMT
ENV R_BASE_VERSION=4.0.5
# Fri, 02 Apr 2021 18:48:58 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 02 Apr 2021 19:21:12 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Apr 2021 19:21:38 GMT
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
	-	`sha256:bdb9547c29c72e68fff1cda0a3c5edf3367fe7b57cfbf9aec3f04d9a6894fb52`  
		Last Modified: Fri, 02 Apr 2021 19:22:22 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d290a46527a6d907edf0271ad2ea036291dc04cb492591e5a1df471696a128d`  
		Last Modified: Fri, 02 Apr 2021 19:23:07 GMT  
		Size: 236.2 MB (236216817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.5` - linux; s390x

```console
$ docker pull r-base@sha256:0127fb5d7bbc1930c71e76a42287b50bbf14d0e056ac3c91a39d3b0164c03734
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290206045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec02a8e01328c65764727f8bcdd032657cd2b0bd0c2ad61206238e73f2f6aa8b`
-	Default Command: `["R"]`

```dockerfile
# Sat, 10 Apr 2021 00:43:21 GMT
ADD file:cbb92f87e30bd8cc63c16886113e2e636b347f735c288a6e62d83db81455575f in / 
# Sat, 10 Apr 2021 00:43:24 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 05:54:38 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Sat, 10 Apr 2021 05:54:39 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sat, 10 Apr 2021 05:54:49 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 05:54:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 10 Apr 2021 05:54:52 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 10 Apr 2021 05:54:52 GMT
ENV LANG=en_US.UTF-8
# Sat, 10 Apr 2021 05:54:53 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 10 Apr 2021 05:54:53 GMT
ENV R_BASE_VERSION=4.0.5
# Sat, 10 Apr 2021 05:54:54 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Sat, 10 Apr 2021 05:55:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 05:55:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:55b653bc1866bdeeed6dc1bd5685b5ea5c25a7a504ccfbf942b97608d3e73c1c`  
		Last Modified: Sat, 10 Apr 2021 00:46:58 GMT  
		Size: 53.1 MB (53148208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d952f5f43487233d6fb0a6aada35e38e8bf98b6f93f3803d0927088a8527937`  
		Last Modified: Sat, 10 Apr 2021 05:56:18 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad90ef69e5e37acc356988ca8a6df7f01ef772d47659ebe9c5d96c4e7c7eaf3`  
		Last Modified: Sat, 10 Apr 2021 05:56:18 GMT  
		Size: 25.6 MB (25632464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769f986f8d0c29a47767f6333e74a05dbc56ef6d043ad346492177fb7b5c890c`  
		Last Modified: Sat, 10 Apr 2021 05:56:16 GMT  
		Size: 920.2 KB (920156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba088adb99632990a7a2519cfc487d7e2a9a1035b9e64abc98eb0109a98e8612`  
		Last Modified: Sat, 10 Apr 2021 05:56:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eade0b6328848247d318db860a095be58a12a434c71b40c9dc19d755cdd93747`  
		Last Modified: Sat, 10 Apr 2021 05:56:16 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bc3452e7f082bbdf9245d83ab09f9d3ab086be6cb8e3bad40a0c87d8268b4a`  
		Last Modified: Sat, 10 Apr 2021 05:56:39 GMT  
		Size: 210.5 MB (210502700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:eef69960e471af78073aa1e2abacaaa555ac85b401611590ee160130c6845846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:af1b9007d8c81d0cc3cf8d11eed912537623b08a0bf8697ddba18f091bed64ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323897200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8020514dfa2784462c2ab3d5a1d402ae370067dfd4065c36de0c8ba09ab56b`
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
# Fri, 02 Apr 2021 18:38:49 GMT
ENV R_BASE_VERSION=4.0.5
# Fri, 02 Apr 2021 18:38:50 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 02 Apr 2021 18:39:56 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Apr 2021 18:39:58 GMT
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
	-	`sha256:bf4aad63e756385206bdfa2a4730ead3d2ed716f1fd74169adb4c0690080534c`  
		Last Modified: Fri, 02 Apr 2021 18:40:21 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacc3d4038d7a8e85d8e39f0d96ad8648830ccb99c32e9f62170981433ae0ff2`  
		Last Modified: Fri, 02 Apr 2021 18:41:04 GMT  
		Size: 242.5 MB (242534151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:04ee057922d716542df86dee50448cec991b9e8d875671cecf2e591ec69f89f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311476289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917fbf45f92c3a87dee003685ab1979ab729995d6ae9b4fa3dbb917f283bd55a`
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
# Fri, 02 Apr 2021 19:25:14 GMT
ENV R_BASE_VERSION=4.0.5
# Fri, 02 Apr 2021 19:25:17 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 02 Apr 2021 19:27:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Apr 2021 19:27:06 GMT
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
	-	`sha256:7deb90318bb05ae2bafb8f5f89905821bbcdfa7e0cd51ef970821d275c5fb6e8`  
		Last Modified: Fri, 02 Apr 2021 19:27:23 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b694158ddafd8f34e2523c4936f239f1bcca716d6ff449c65d1a438b946ccffd`  
		Last Modified: Fri, 02 Apr 2021 19:28:13 GMT  
		Size: 231.4 MB (231425663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:95d0fa7b1456ccbd1a8a210b813fe59b70a713083313a80953746c6d710a2878
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321717753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03a067e1f4c4a1cf934cf453918a85bc96e7bca346eef202dae379bf18c7135`
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
# Fri, 02 Apr 2021 18:47:39 GMT
ENV R_BASE_VERSION=4.0.5
# Fri, 02 Apr 2021 18:48:58 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 02 Apr 2021 19:21:12 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Apr 2021 19:21:38 GMT
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
	-	`sha256:bdb9547c29c72e68fff1cda0a3c5edf3367fe7b57cfbf9aec3f04d9a6894fb52`  
		Last Modified: Fri, 02 Apr 2021 19:22:22 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d290a46527a6d907edf0271ad2ea036291dc04cb492591e5a1df471696a128d`  
		Last Modified: Fri, 02 Apr 2021 19:23:07 GMT  
		Size: 236.2 MB (236216817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:0127fb5d7bbc1930c71e76a42287b50bbf14d0e056ac3c91a39d3b0164c03734
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290206045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec02a8e01328c65764727f8bcdd032657cd2b0bd0c2ad61206238e73f2f6aa8b`
-	Default Command: `["R"]`

```dockerfile
# Sat, 10 Apr 2021 00:43:21 GMT
ADD file:cbb92f87e30bd8cc63c16886113e2e636b347f735c288a6e62d83db81455575f in / 
# Sat, 10 Apr 2021 00:43:24 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 05:54:38 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Sat, 10 Apr 2021 05:54:39 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sat, 10 Apr 2021 05:54:49 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 05:54:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 10 Apr 2021 05:54:52 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 10 Apr 2021 05:54:52 GMT
ENV LANG=en_US.UTF-8
# Sat, 10 Apr 2021 05:54:53 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 10 Apr 2021 05:54:53 GMT
ENV R_BASE_VERSION=4.0.5
# Sat, 10 Apr 2021 05:54:54 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Sat, 10 Apr 2021 05:55:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 05:55:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:55b653bc1866bdeeed6dc1bd5685b5ea5c25a7a504ccfbf942b97608d3e73c1c`  
		Last Modified: Sat, 10 Apr 2021 00:46:58 GMT  
		Size: 53.1 MB (53148208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d952f5f43487233d6fb0a6aada35e38e8bf98b6f93f3803d0927088a8527937`  
		Last Modified: Sat, 10 Apr 2021 05:56:18 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad90ef69e5e37acc356988ca8a6df7f01ef772d47659ebe9c5d96c4e7c7eaf3`  
		Last Modified: Sat, 10 Apr 2021 05:56:18 GMT  
		Size: 25.6 MB (25632464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769f986f8d0c29a47767f6333e74a05dbc56ef6d043ad346492177fb7b5c890c`  
		Last Modified: Sat, 10 Apr 2021 05:56:16 GMT  
		Size: 920.2 KB (920156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba088adb99632990a7a2519cfc487d7e2a9a1035b9e64abc98eb0109a98e8612`  
		Last Modified: Sat, 10 Apr 2021 05:56:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eade0b6328848247d318db860a095be58a12a434c71b40c9dc19d755cdd93747`  
		Last Modified: Sat, 10 Apr 2021 05:56:16 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bc3452e7f082bbdf9245d83ab09f9d3ab086be6cb8e3bad40a0c87d8268b4a`  
		Last Modified: Sat, 10 Apr 2021 05:56:39 GMT  
		Size: 210.5 MB (210502700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
