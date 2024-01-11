## `r-base:latest`

```console
$ docker pull r-base@sha256:ed078a1e86eedc5967f386d4b0df91f0781bb3419c52fcc16c49803420a7bd76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:2031e6723c29ab07ad875d8fba9fa60fb7111357d7268f28393353f64592b13d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340466565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f46bbab0fbf852f4ed6c97604f29bf12a8d38628b51564fbb9739b4922eb7d`
-	Default Command: `["R"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:47 GMT
ADD file:bf1a099790136a24feb4eac287781f4d35a1188036c126be1ae0a93f2e5d2adf in / 
# Tue, 19 Dec 2023 01:22:48 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:10:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 19 Dec 2023 04:10:12 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 19 Dec 2023 04:10:22 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:10:25 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 19 Dec 2023 04:10:25 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 19 Dec 2023 04:10:25 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Dec 2023 04:10:26 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 19 Dec 2023 04:10:26 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 19 Dec 2023 04:11:24 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:11:26 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2be50d1418f669b761525b481330d50356bbd66349941bd0ed8e3c04c64c8ada`  
		Last Modified: Tue, 19 Dec 2023 01:28:59 GMT  
		Size: 49.6 MB (49583409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17b7b5242934c0aba511f92c02ce16b993fa8fa24cd2cb7f1b51ab89fc8e9e`  
		Last Modified: Tue, 19 Dec 2023 04:11:40 GMT  
		Size: 3.4 KB (3364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba60adf71939a54c86822562d6b19901b0ebfd652e41a20d6675252b0cc8d7a`  
		Last Modified: Tue, 19 Dec 2023 04:11:43 GMT  
		Size: 25.6 MB (25632406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9757002524d9952f68fb0043191a997d58312019ef47810cd22665058fd58fc6`  
		Last Modified: Tue, 19 Dec 2023 04:11:40 GMT  
		Size: 866.3 KB (866326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56b61288bd2707889b0b3c339ee47d610902d88d881008796107e73191ac567`  
		Last Modified: Tue, 19 Dec 2023 04:11:40 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdf2a03cf1508120d7141f70b206b88ec9523a8ed106de16ea450655d87d64b`  
		Last Modified: Tue, 19 Dec 2023 04:12:09 GMT  
		Size: 264.4 MB (264380708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:a3356ad38618655daad14867ca9a957c3b79f1913c4a1d4a9b2bf3175ba35fde
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.5 MB (326483557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aadb035512070d71ec2e95788dc733b5eaf5f36b8417147b9d13dd9ec9b6732`
-	Default Command: `["R"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:16 GMT
ADD file:ef74fbd95a42ea9067fb58e0cb214318f25e01383dbaf8bd4f65c491328da115 in / 
# Thu, 11 Jan 2024 02:42:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:30:18 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 11 Jan 2024 06:30:18 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 11 Jan 2024 06:30:29 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:30:31 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 11 Jan 2024 06:30:31 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 11 Jan 2024 06:30:31 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jan 2024 06:30:31 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 11 Jan 2024 06:30:31 GMT
ENV R_BASE_VERSION=4.3.2
# Thu, 11 Jan 2024 06:31:34 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:31:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:45c62a2271fe4658739419a2d2f31eed9a7af320ff25f51d28c9961d6625d27b`  
		Last Modified: Thu, 11 Jan 2024 02:48:04 GMT  
		Size: 49.6 MB (49594165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4b9741f43d2d1984698cad3cacae5a833b3afc744d785d02723cb21d755886`  
		Last Modified: Thu, 11 Jan 2024 06:31:45 GMT  
		Size: 3.4 KB (3359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9285e8014e06ba77a1cbacc2dfb44e2d4553a72e910d0ba2c7df89cd33c8b0`  
		Last Modified: Thu, 11 Jan 2024 06:31:47 GMT  
		Size: 25.5 MB (25506713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f05f81ba261fc0925ea290064b3ea6ab9b0f15178e593d9d0ca8a76d53870c8`  
		Last Modified: Thu, 11 Jan 2024 06:31:45 GMT  
		Size: 866.3 KB (866321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8462dc0252eea7abf2840218af5d0960c591b7a05e4458c94c257b940b739dc8`  
		Last Modified: Thu, 11 Jan 2024 06:31:45 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a46cedac0e71c63a6195b2773c903f2cfe7677eb990fc2b136ef6e547388a8`  
		Last Modified: Thu, 11 Jan 2024 06:32:05 GMT  
		Size: 250.5 MB (250512650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:857c8f6dffb79e2339d831779424ca6f7d8a26432d46041fd41bd40e6f82fb01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339247800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc1fb9d836f706d7743c00537e2c73181a01a2c27b37e7fdcc8cd6733d5348d`
-	Default Command: `["R"]`

```dockerfile
# Thu, 11 Jan 2024 02:36:44 GMT
ADD file:7bbfdd0ef6929b558d9177e8e25da2b51a5fc03501fe368eee680082fe61b5af in / 
# Thu, 11 Jan 2024 02:36:49 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:28:36 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 11 Jan 2024 07:28:40 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 11 Jan 2024 07:29:02 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:29:07 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 11 Jan 2024 07:29:07 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 11 Jan 2024 07:29:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jan 2024 07:29:12 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 11 Jan 2024 07:29:13 GMT
ENV R_BASE_VERSION=4.3.2
# Thu, 11 Jan 2024 07:31:37 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:31:39 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:906621e89c1664a87130a19b59bad8b965ec51ec0ccda6544080841d92cc4105`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 53.4 MB (53435747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae82f3e451ea22cc89af9e6d008b744317be532e64116fb53d0773449ea108b`  
		Last Modified: Thu, 11 Jan 2024 07:31:49 GMT  
		Size: 3.4 KB (3373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da95af2c3393b35f8272873bdc31ea16618bb27880a83fa39d8a4473541cfb25`  
		Last Modified: Thu, 11 Jan 2024 07:31:53 GMT  
		Size: 26.0 MB (26039531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1e25861fe3d06e26f40d6f34b622c8b93d43693ecc456d49a40ac78f933050`  
		Last Modified: Thu, 11 Jan 2024 07:31:50 GMT  
		Size: 866.3 KB (866332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a184e090e88d83f83524de37521629f00a8e2276ec334f6358b5188e56dc91b4`  
		Last Modified: Thu, 11 Jan 2024 07:31:49 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe10b28ae840e687a7c232f42ab784b170ddb71cbac70c3f919eacc2eb44f3b`  
		Last Modified: Thu, 11 Jan 2024 07:32:22 GMT  
		Size: 258.9 MB (258902467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:6081b797afc888e2b7b5a2eff8cb905088aaddbbe2eba9124e0083bbda46f009
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307283871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43333f5aa36539430fc2a0877bdd65a0dcdc5da34aee423ab4583d8f874ceac4`
-	Default Command: `["R"]`

```dockerfile
# Thu, 11 Jan 2024 01:47:47 GMT
ADD file:99f7dceada5a4de4b63b031da99463b28215d60590eab63420c2d31adc558936 in / 
# Thu, 11 Jan 2024 01:47:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:28:32 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 11 Jan 2024 08:28:32 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 11 Jan 2024 08:28:41 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:28:44 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 11 Jan 2024 08:28:44 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 11 Jan 2024 08:28:44 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jan 2024 08:28:45 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 11 Jan 2024 08:28:45 GMT
ENV R_BASE_VERSION=4.3.2
# Thu, 11 Jan 2024 08:29:46 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:30:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f29a37bb4112320796c8c57ad72bde831042b4c9adba3e230ca29fb2c897ee05`  
		Last Modified: Thu, 11 Jan 2024 01:52:41 GMT  
		Size: 49.1 MB (49091868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bc678b5a73939476ed627c2b590efb825545ffdc356715714cdb6de7c07e2c`  
		Last Modified: Thu, 11 Jan 2024 08:30:28 GMT  
		Size: 3.4 KB (3359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aaa3c498078e539acc969af30074f5a2445cf24b4c3cb7ce822789bdac1a6`  
		Last Modified: Thu, 11 Jan 2024 08:30:31 GMT  
		Size: 25.5 MB (25484572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f4d7c6a12ef37065a0354bff718b0e8ae041d7920a9ab289d50d0430095dea`  
		Last Modified: Thu, 11 Jan 2024 08:30:28 GMT  
		Size: 922.3 KB (922276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faada46a48cbf169a77e9438b9dea8edc1544f0ed56e3046a905822f1941558`  
		Last Modified: Thu, 11 Jan 2024 08:30:28 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a66fa751d342069e5d3ae7e78bce0796f6aa7401f6c127d560588129c2ebbc2`  
		Last Modified: Thu, 11 Jan 2024 08:30:52 GMT  
		Size: 231.8 MB (231781448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
