<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.3.3`](#r-base433)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.3.3`

```console
$ docker pull r-base@sha256:2312ee286f4ba0f3d7bdf53ee1f082db68d25f1e9d62f27a0d8f062ba5145509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.3.3` - linux; amd64

```console
$ docker pull r-base@sha256:fd808d8a2743369426ac4ec6f5dcb753c147f9d95bf58f20478583afa196c684
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.2 MB (374155176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4218bf6b57fdd0df925f73f791c3a7cc798cb3a8fd491535801e089e685d254e`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Apr 2024 01:53:13 GMT
ADD file:f52df68480a4f4b019c4ccf809927839b337aee1176e28fc9810a53b1b8146c8 in / 
# Wed, 10 Apr 2024 01:53:14 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:55:59 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 10 Apr 2024 12:56:00 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 10 Apr 2024 12:56:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:56:13 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 10 Apr 2024 12:56:13 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 10 Apr 2024 12:56:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Apr 2024 12:56:13 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 10 Apr 2024 12:56:13 GMT
ENV R_BASE_VERSION=4.3.3
# Wed, 10 Apr 2024 12:57:30 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:57:32 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bc5ec5e91c5d709afa0648dd0c8f1a32bfd6cb4361cc16d9e7a6dd966e286c4a`  
		Last Modified: Wed, 10 Apr 2024 01:59:20 GMT  
		Size: 52.3 MB (52332326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a463830c4650fdd909bef0def81b16544bfc0f86d74ee36142c8e7787ebf8e1b`  
		Last Modified: Wed, 10 Apr 2024 12:57:43 GMT  
		Size: 3.4 KB (3366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1e0860c738a623ee650235fce791ce1b7ac628a3152e5a1f93baf8f9c3c6e7`  
		Last Modified: Wed, 10 Apr 2024 12:57:45 GMT  
		Size: 22.8 MB (22849180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6924d178e1f1ea24e6ff1d3d3637341bee03030093c0b7e40b07e6fc88a5291`  
		Last Modified: Wed, 10 Apr 2024 12:57:43 GMT  
		Size: 866.3 KB (866339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac87ee9fb288acaf171b94b626d75df2c100b136bb25ca169ba81d627affda3`  
		Last Modified: Wed, 10 Apr 2024 12:57:42 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6265a077cc353036f7593b0a45070c736a31448d640e84784c911aed3b01263`  
		Last Modified: Wed, 10 Apr 2024 12:58:16 GMT  
		Size: 298.1 MB (298103616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.3` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:21e7f70ed7f21e11b8efbd7c23127ecb76c10b54c0e0bf54dbc67e477335efaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353905147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd4434ff8fd0c3d53adb1d243704401e5ba643d464ca20b1e30a643d3dd77ec`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 04:12:08 GMT
ADD file:bde6752542e4e995769792177622825fd367491a317b6d18fcf5ecee7e44bb26 in / 
# Wed, 24 Apr 2024 04:12:08 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:47:25 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 04:47:25 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 24 Apr 2024 04:47:37 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:47:39 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 24 Apr 2024 04:47:39 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 04:47:39 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 04:47:40 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 24 Apr 2024 04:47:40 GMT
ENV R_BASE_VERSION=4.3.3
# Wed, 24 Apr 2024 04:48:52 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:48:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ad22d5f94f78d49cac32cb85d727d7c0ad9591d78322e8703c671bc6df55a2b5`  
		Last Modified: Wed, 24 Apr 2024 04:17:34 GMT  
		Size: 52.2 MB (52199437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86935bad0e68976a7e230dedea4cb980294557c652f40f8ae7d1015ecae866a2`  
		Last Modified: Wed, 24 Apr 2024 04:49:08 GMT  
		Size: 3.4 KB (3364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45529fd363ac7bfe2fcdf4939d5367949076f74184a8c1c041f201f9b6b2f6f5`  
		Last Modified: Wed, 24 Apr 2024 04:49:10 GMT  
		Size: 28.8 MB (28816547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b238dffa428a3bed2f5d990a09c216569e4060558b4332aabbc2827b3f03c`  
		Last Modified: Wed, 24 Apr 2024 04:49:08 GMT  
		Size: 866.3 KB (866330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63033486a1492c86f9b9c82a3fbeded35f1cfc740cef1966a7eca8c452271e1f`  
		Last Modified: Wed, 24 Apr 2024 04:49:07 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f404da278492437a05823a81d45fde94f282e4a5944eaee44dea03d1750a20a0`  
		Last Modified: Wed, 24 Apr 2024 04:49:30 GMT  
		Size: 272.0 MB (272019117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.3` - linux; ppc64le

```console
$ docker pull r-base@sha256:07377d998209d95c3a29f674df7a7cee86e06905616f2c809a9def71609bf704
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.9 MB (376885814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0e1ffd7098e4e935aa61c82b7e6c79420902f4c1359fb8c1b49d636059e968`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Apr 2024 01:28:29 GMT
ADD file:193248d1bc625911c89a98335ea79bb3b150c617f0d592617d53111697f46973 in / 
# Wed, 10 Apr 2024 01:28:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:20:40 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 10 Apr 2024 12:20:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 10 Apr 2024 12:21:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:21:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 10 Apr 2024 12:21:13 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 10 Apr 2024 12:21:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Apr 2024 12:21:15 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 10 Apr 2024 12:21:16 GMT
ENV R_BASE_VERSION=4.3.3
# Wed, 10 Apr 2024 12:25:01 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:25:11 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:462810f8d1325bd2e552b3d4de71c2d19a8d4a6ba90e851363a3edba7e1eebb1`  
		Last Modified: Wed, 10 Apr 2024 01:34:13 GMT  
		Size: 56.3 MB (56250110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7f0067283b2a09f05e16ff0e351e201a81de40c7359d64b91a779fe9d27665`  
		Last Modified: Wed, 10 Apr 2024 12:25:25 GMT  
		Size: 3.4 KB (3367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f3a89dbabdf4b13d4a6988728ec5b9b94f55abc026fc679493d1689edce462`  
		Last Modified: Wed, 10 Apr 2024 12:25:28 GMT  
		Size: 23.1 MB (23070725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492c0867930b9e1ddf5df50124ce43c369402059ab10a3203764104b7b3f45e7`  
		Last Modified: Wed, 10 Apr 2024 12:25:26 GMT  
		Size: 866.3 KB (866335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041de7ad0e798b9bd5e44d3f6e78e9e108e6f426a33141f1c85f8c1a9b534c5b`  
		Last Modified: Wed, 10 Apr 2024 12:25:25 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a9ec63efea8076dd962ea0266fc9d9e487a879f62ea91b456c9077794b2d8`  
		Last Modified: Wed, 10 Apr 2024 12:26:05 GMT  
		Size: 296.7 MB (296694927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.3` - linux; s390x

```console
$ docker pull r-base@sha256:be136c9da9333d955e232e1849fdd594e6758654664deba7cd02ba23a697f93b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347748164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137775cad7e7ce66b1df1bfad7eebf0de99d2b46ea3edb2b5ba75d578d2302b6`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Apr 2024 01:33:53 GMT
ADD file:19a79084cf1c7ac5a03ae781ebdc7c6d8fe545c99714224979d7e2a0b2fd0ec5 in / 
# Wed, 10 Apr 2024 01:33:56 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 11:35:29 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 10 Apr 2024 11:35:32 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 10 Apr 2024 11:36:03 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 11:36:10 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 10 Apr 2024 11:36:11 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 10 Apr 2024 11:36:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Apr 2024 11:36:14 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 10 Apr 2024 11:36:14 GMT
ENV R_BASE_VERSION=4.3.3
# Wed, 10 Apr 2024 11:39:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 11:40:10 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f41f30e09b733b618c212c42fd18a7262bc91c28c3663ef65e03b659c16c3e9d`  
		Last Modified: Wed, 10 Apr 2024 01:50:28 GMT  
		Size: 51.8 MB (51761762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83c443b8e160410dc50a373c5883a8b48086fa07eaf0ac0bfce5e0d2446b835`  
		Last Modified: Wed, 10 Apr 2024 11:41:48 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e662f4db244493ed4ee024a44b463bfec0d6fbabe86c156c767767c4aefd516a`  
		Last Modified: Wed, 10 Apr 2024 11:41:51 GMT  
		Size: 23.0 MB (22951749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b180674f307b11dad1b7eed66ba7a21883abe13b65493c29bcf8709331b66506`  
		Last Modified: Wed, 10 Apr 2024 11:41:48 GMT  
		Size: 922.3 KB (922276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58be9b3e572027c36275497bd41911269b2443b954f6bd734218bbc56888bab9`  
		Last Modified: Wed, 10 Apr 2024 11:41:48 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400d31a40f062aecff5db480c9c08d71408d91942c3b1889d6053099510cd2aa`  
		Last Modified: Wed, 10 Apr 2024 11:42:22 GMT  
		Size: 272.1 MB (272108666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:2312ee286f4ba0f3d7bdf53ee1f082db68d25f1e9d62f27a0d8f062ba5145509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:fd808d8a2743369426ac4ec6f5dcb753c147f9d95bf58f20478583afa196c684
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.2 MB (374155176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4218bf6b57fdd0df925f73f791c3a7cc798cb3a8fd491535801e089e685d254e`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Apr 2024 01:53:13 GMT
ADD file:f52df68480a4f4b019c4ccf809927839b337aee1176e28fc9810a53b1b8146c8 in / 
# Wed, 10 Apr 2024 01:53:14 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:55:59 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 10 Apr 2024 12:56:00 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 10 Apr 2024 12:56:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:56:13 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 10 Apr 2024 12:56:13 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 10 Apr 2024 12:56:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Apr 2024 12:56:13 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 10 Apr 2024 12:56:13 GMT
ENV R_BASE_VERSION=4.3.3
# Wed, 10 Apr 2024 12:57:30 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:57:32 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bc5ec5e91c5d709afa0648dd0c8f1a32bfd6cb4361cc16d9e7a6dd966e286c4a`  
		Last Modified: Wed, 10 Apr 2024 01:59:20 GMT  
		Size: 52.3 MB (52332326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a463830c4650fdd909bef0def81b16544bfc0f86d74ee36142c8e7787ebf8e1b`  
		Last Modified: Wed, 10 Apr 2024 12:57:43 GMT  
		Size: 3.4 KB (3366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1e0860c738a623ee650235fce791ce1b7ac628a3152e5a1f93baf8f9c3c6e7`  
		Last Modified: Wed, 10 Apr 2024 12:57:45 GMT  
		Size: 22.8 MB (22849180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6924d178e1f1ea24e6ff1d3d3637341bee03030093c0b7e40b07e6fc88a5291`  
		Last Modified: Wed, 10 Apr 2024 12:57:43 GMT  
		Size: 866.3 KB (866339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac87ee9fb288acaf171b94b626d75df2c100b136bb25ca169ba81d627affda3`  
		Last Modified: Wed, 10 Apr 2024 12:57:42 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6265a077cc353036f7593b0a45070c736a31448d640e84784c911aed3b01263`  
		Last Modified: Wed, 10 Apr 2024 12:58:16 GMT  
		Size: 298.1 MB (298103616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:21e7f70ed7f21e11b8efbd7c23127ecb76c10b54c0e0bf54dbc67e477335efaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353905147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd4434ff8fd0c3d53adb1d243704401e5ba643d464ca20b1e30a643d3dd77ec`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 04:12:08 GMT
ADD file:bde6752542e4e995769792177622825fd367491a317b6d18fcf5ecee7e44bb26 in / 
# Wed, 24 Apr 2024 04:12:08 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:47:25 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 04:47:25 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 24 Apr 2024 04:47:37 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:47:39 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 24 Apr 2024 04:47:39 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 04:47:39 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 04:47:40 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 24 Apr 2024 04:47:40 GMT
ENV R_BASE_VERSION=4.3.3
# Wed, 24 Apr 2024 04:48:52 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:48:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ad22d5f94f78d49cac32cb85d727d7c0ad9591d78322e8703c671bc6df55a2b5`  
		Last Modified: Wed, 24 Apr 2024 04:17:34 GMT  
		Size: 52.2 MB (52199437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86935bad0e68976a7e230dedea4cb980294557c652f40f8ae7d1015ecae866a2`  
		Last Modified: Wed, 24 Apr 2024 04:49:08 GMT  
		Size: 3.4 KB (3364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45529fd363ac7bfe2fcdf4939d5367949076f74184a8c1c041f201f9b6b2f6f5`  
		Last Modified: Wed, 24 Apr 2024 04:49:10 GMT  
		Size: 28.8 MB (28816547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b238dffa428a3bed2f5d990a09c216569e4060558b4332aabbc2827b3f03c`  
		Last Modified: Wed, 24 Apr 2024 04:49:08 GMT  
		Size: 866.3 KB (866330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63033486a1492c86f9b9c82a3fbeded35f1cfc740cef1966a7eca8c452271e1f`  
		Last Modified: Wed, 24 Apr 2024 04:49:07 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f404da278492437a05823a81d45fde94f282e4a5944eaee44dea03d1750a20a0`  
		Last Modified: Wed, 24 Apr 2024 04:49:30 GMT  
		Size: 272.0 MB (272019117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:07377d998209d95c3a29f674df7a7cee86e06905616f2c809a9def71609bf704
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.9 MB (376885814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0e1ffd7098e4e935aa61c82b7e6c79420902f4c1359fb8c1b49d636059e968`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Apr 2024 01:28:29 GMT
ADD file:193248d1bc625911c89a98335ea79bb3b150c617f0d592617d53111697f46973 in / 
# Wed, 10 Apr 2024 01:28:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:20:40 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 10 Apr 2024 12:20:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 10 Apr 2024 12:21:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:21:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 10 Apr 2024 12:21:13 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 10 Apr 2024 12:21:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Apr 2024 12:21:15 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 10 Apr 2024 12:21:16 GMT
ENV R_BASE_VERSION=4.3.3
# Wed, 10 Apr 2024 12:25:01 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:25:11 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:462810f8d1325bd2e552b3d4de71c2d19a8d4a6ba90e851363a3edba7e1eebb1`  
		Last Modified: Wed, 10 Apr 2024 01:34:13 GMT  
		Size: 56.3 MB (56250110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7f0067283b2a09f05e16ff0e351e201a81de40c7359d64b91a779fe9d27665`  
		Last Modified: Wed, 10 Apr 2024 12:25:25 GMT  
		Size: 3.4 KB (3367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f3a89dbabdf4b13d4a6988728ec5b9b94f55abc026fc679493d1689edce462`  
		Last Modified: Wed, 10 Apr 2024 12:25:28 GMT  
		Size: 23.1 MB (23070725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492c0867930b9e1ddf5df50124ce43c369402059ab10a3203764104b7b3f45e7`  
		Last Modified: Wed, 10 Apr 2024 12:25:26 GMT  
		Size: 866.3 KB (866335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041de7ad0e798b9bd5e44d3f6e78e9e108e6f426a33141f1c85f8c1a9b534c5b`  
		Last Modified: Wed, 10 Apr 2024 12:25:25 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a9ec63efea8076dd962ea0266fc9d9e487a879f62ea91b456c9077794b2d8`  
		Last Modified: Wed, 10 Apr 2024 12:26:05 GMT  
		Size: 296.7 MB (296694927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:be136c9da9333d955e232e1849fdd594e6758654664deba7cd02ba23a697f93b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347748164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137775cad7e7ce66b1df1bfad7eebf0de99d2b46ea3edb2b5ba75d578d2302b6`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Apr 2024 01:33:53 GMT
ADD file:19a79084cf1c7ac5a03ae781ebdc7c6d8fe545c99714224979d7e2a0b2fd0ec5 in / 
# Wed, 10 Apr 2024 01:33:56 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 11:35:29 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 10 Apr 2024 11:35:32 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 10 Apr 2024 11:36:03 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 11:36:10 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 10 Apr 2024 11:36:11 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 10 Apr 2024 11:36:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Apr 2024 11:36:14 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 10 Apr 2024 11:36:14 GMT
ENV R_BASE_VERSION=4.3.3
# Wed, 10 Apr 2024 11:39:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 11:40:10 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f41f30e09b733b618c212c42fd18a7262bc91c28c3663ef65e03b659c16c3e9d`  
		Last Modified: Wed, 10 Apr 2024 01:50:28 GMT  
		Size: 51.8 MB (51761762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83c443b8e160410dc50a373c5883a8b48086fa07eaf0ac0bfce5e0d2446b835`  
		Last Modified: Wed, 10 Apr 2024 11:41:48 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e662f4db244493ed4ee024a44b463bfec0d6fbabe86c156c767767c4aefd516a`  
		Last Modified: Wed, 10 Apr 2024 11:41:51 GMT  
		Size: 23.0 MB (22951749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b180674f307b11dad1b7eed66ba7a21883abe13b65493c29bcf8709331b66506`  
		Last Modified: Wed, 10 Apr 2024 11:41:48 GMT  
		Size: 922.3 KB (922276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58be9b3e572027c36275497bd41911269b2443b954f6bd734218bbc56888bab9`  
		Last Modified: Wed, 10 Apr 2024 11:41:48 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400d31a40f062aecff5db480c9c08d71408d91942c3b1889d6053099510cd2aa`  
		Last Modified: Wed, 10 Apr 2024 11:42:22 GMT  
		Size: 272.1 MB (272108666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
