## `r-base:latest`

```console
$ docker pull r-base@sha256:af3724f65c6d96a70e1e3dcb45cb6e476fe92bdc8643898518f6f3a5c744505f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:fd192ac4edc4e94bdd7d4d62b6dd8c83f6a1303eb48d93ef9a4685fd0a9513f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.8 MB (519758360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4fd0403f8f8106887bb5ea107613015f7e25e54f1f787970bd242dfd50230c`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:13 GMT
ADD file:6293ddf53588d819bfa272e4dbeb8a0b72de03092414e598350b6c9ce5b08ac1 in / 
# Fri, 11 Dec 2020 02:09:13 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 21:25:00 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Dec 2020 21:25:02 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Fri, 11 Dec 2020 21:25:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 21:25:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Fri, 11 Dec 2020 21:25:21 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Dec 2020 21:25:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Dec 2020 21:25:23 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 11 Dec 2020 21:25:23 GMT
ENV R_BASE_VERSION=4.0.3
# Fri, 11 Dec 2020 21:27:14 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 21:27:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ecd924c7226f314c16de965258f37da4aa990c07e494be1116af512706138401`  
		Last Modified: Fri, 11 Dec 2020 02:16:00 GMT  
		Size: 53.1 MB (53113573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fec22ce03e6be2d27efb3e9a90be68b14183859abf0864518e2581aa49fb8f5`  
		Last Modified: Fri, 11 Dec 2020 21:27:45 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d900227a8f4d4d2647927b9fa8da77f0f535ca497bc771c5f8a72b0cc971df`  
		Last Modified: Fri, 11 Dec 2020 21:27:52 GMT  
		Size: 27.4 MB (27441203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c9ad96a035ae2a5bda28a6e666ed7e1bbe5d945180faafd1c2ed611473e728`  
		Last Modified: Fri, 11 Dec 2020 21:27:46 GMT  
		Size: 863.6 KB (863572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f2416c67056dd5c3a5948858ab4578631e13cc36ee43bd8d44dea4ec4693f7`  
		Last Modified: Fri, 11 Dec 2020 21:27:44 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0079bdf52f600362737f2c00e7e7ae11458844ef1d06265caf24115be990c4ab`  
		Last Modified: Fri, 11 Dec 2020 21:29:26 GMT  
		Size: 438.3 MB (438337820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:6ba94de9e7adb0f7cd759594a90b025a8782dbd032c72dabc9bd8d33c6f2f648
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.1 MB (507072736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad039ec4a4b4b25d8b7955589ea37ca166ad971f2fb85bd0a3c1dfa576dc3d20`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Dec 2020 02:49:00 GMT
ADD file:68734186568fd3a803d44d4f42065373a0200929b1ff39d104a24dfe14316ae0 in / 
# Fri, 11 Dec 2020 02:49:04 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:02:39 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Dec 2020 17:02:41 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Fri, 11 Dec 2020 17:03:04 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:03:10 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Fri, 11 Dec 2020 17:03:13 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Dec 2020 17:03:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Dec 2020 17:03:18 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 11 Dec 2020 17:03:20 GMT
ENV R_BASE_VERSION=4.0.3
# Fri, 11 Dec 2020 17:05:40 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:37ba54a7ad02aab7f88ab28bf1de79bd2861de26af6a6998d9b8dab9cc58b2f9`  
		Last Modified: Fri, 11 Dec 2020 02:56:23 GMT  
		Size: 52.0 MB (51961789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc484ab337728ab0a3c81b0016c1b7d0042e4dc5881e2bee0f37111cc38000`  
		Last Modified: Fri, 11 Dec 2020 17:06:04 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1353e5265e09e606d78cfdd681b7dc846953a304e13bf818911949895b3b9353`  
		Last Modified: Fri, 11 Dec 2020 17:06:12 GMT  
		Size: 27.3 MB (27309206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617418dda951dc7cf53cd4c56893d986d78219ef8422a487fbf414e3dfd6a4a2`  
		Last Modified: Fri, 11 Dec 2020 17:06:05 GMT  
		Size: 863.6 KB (863571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073a1e61d66d2451b5f7149251cdbf6de1483ea3bceded8d786dfb5f9bd85bf`  
		Last Modified: Fri, 11 Dec 2020 17:06:04 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab79f74827b044a430446d69c7439babb4bfb3a8e2c11a19ac582bf4f230849a`  
		Last Modified: Fri, 11 Dec 2020 17:07:39 GMT  
		Size: 426.9 MB (426935945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:8a68e56486fafaf86f0360517acaa38d0f87a7f3c193cad868840c68c365cf2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.3 MB (502289342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fec6a10d361fe6e37550dea10bafd04f57b8022a549ad426731caec30ee0e07`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Dec 2020 03:36:34 GMT
ADD file:1dfff915e611826221d8bc1183ad8a3e570ed1e8bb82ced9fe84aac9b1a7f5b7 in / 
# Fri, 11 Dec 2020 03:36:42 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:56:32 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Dec 2020 19:56:43 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Fri, 11 Dec 2020 19:57:26 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:57:37 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Fri, 11 Dec 2020 19:57:39 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Dec 2020 19:57:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Dec 2020 19:57:50 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 11 Dec 2020 19:57:53 GMT
ENV R_BASE_VERSION=4.0.3
# Fri, 11 Dec 2020 20:03:29 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:03:42 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:8f40108d70f3e222c8582866a564ac6dfce4acce813d153cf276e76359b4a55a`  
		Last Modified: Fri, 11 Dec 2020 03:43:39 GMT  
		Size: 57.1 MB (57079097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33127d16c780dffde9eb0fab2057c1d3065546c3008c4bd35782f28a85292b5`  
		Last Modified: Fri, 11 Dec 2020 20:04:04 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744107c00a82c3b05c1797f79e845c57074fff4a8c693971c12dd903dada056a`  
		Last Modified: Fri, 11 Dec 2020 20:04:09 GMT  
		Size: 27.7 MB (27739810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab24ac4715c77204a0943e2492055cf1d866619fcd2969d412fe2239764441`  
		Last Modified: Fri, 11 Dec 2020 20:04:05 GMT  
		Size: 863.6 KB (863571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04b9a364f592f541a68c9ab474a705555d3350c2e9ca19f229ba40532036f7f`  
		Last Modified: Fri, 11 Dec 2020 20:04:04 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091cff983da043bbdef4f62ba8c6d36836e946f99df004f89ae18912779c6491`  
		Last Modified: Fri, 11 Dec 2020 20:05:22 GMT  
		Size: 416.6 MB (416604624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:16762b6b94f3410879a7e89bd182bce692f8145117ffd2601de085cf8ff7ffb2
```

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254993143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9458dd260863c49d65cf903339d43ae709b850ed3389bab14e6ad10c54af1bd`
-	Default Command: `["R"]`

```dockerfile
# Wed, 03 May 2017 17:23:43 GMT
ADD file:7068f688c8173d6cf7a7bead8f8026099fdfcf820d149a673208e68f103e198d in / 
# Wed, 03 May 2017 17:23:44 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2017 22:26:37 GMT
MAINTAINER "Carl Boettiger and Dirk Eddelbuettel" rocker-maintainers@eddelbuettel.com
# Wed, 03 May 2017 22:26:42 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 03 May 2017 22:27:17 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2017 22:27:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 03 May 2017 22:27:23 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 03 May 2017 22:27:24 GMT
ENV LANG=en_US.UTF-8
# Wed, 03 May 2017 22:27:28 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list 	&& echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 03 May 2017 22:27:29 GMT
ENV R_BASE_VERSION=3.4.0
# Wed, 03 May 2017 22:29:44 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}* 		r-base-dev=${R_BASE_VERSION}* 		r-recommended=${R_BASE_VERSION}*         && echo 'options(repos = c(CRAN = "https://cran.rstudio.com/"), download.file.method = "libcurl")' >> /etc/R/Rprofile.site         && echo 'source("/etc/R/Rprofile.site")' >> /etc/littler.r 	&& ln -s /usr/share/doc/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/share/doc/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/share/doc/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/share/doc/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2017 22:29:45 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2f4a4a37d72f27df4df3e784df7933c52ad54360b0263a9941427ebfbc52bd16`  
		Last Modified: Wed, 03 May 2017 17:25:13 GMT  
		Size: 44.4 MB (44377421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3aa7344eecde9aa5d34cd299cb2d7186ae2f87fca0b5eb38a9529f2a6d568c`  
		Last Modified: Wed, 03 May 2017 22:29:52 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92599fb6b027e9ee16c207a5340278252af788ec9d7abb1b9afb1d98a219f537`  
		Last Modified: Wed, 03 May 2017 22:30:23 GMT  
		Size: 36.0 MB (35956442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4ddbbff3ee4147b8bae18e9fc0df5c610abbf20512aa94a3e3110b10d0833`  
		Last Modified: Wed, 03 May 2017 22:29:52 GMT  
		Size: 432.3 KB (432304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f07ae519b0047b8a7c4bab9ea026085213dba1b29fc8ab64a25b86820a7af6`  
		Last Modified: Wed, 03 May 2017 22:29:51 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06a6e301873506409cd13af7a86ca2fd43d4a14a6d240b0e06f239500eb160a`  
		Last Modified: Wed, 03 May 2017 22:31:38 GMT  
		Size: 174.2 MB (174224831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
