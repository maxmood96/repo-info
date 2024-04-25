<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.0`](#r-base440)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.0`

```console
$ docker pull r-base@sha256:f65678c037bc1ace4c7d03de6d7c0aaba589ab49d559df156c49e40a5889a781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.4.0` - linux; amd64

```console
$ docker pull r-base@sha256:eb0603d7a9166998854ab03f5605925112125c9c7e539ec1c3ede722ee6f682a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368381410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaf5974ca0a589e0b277419a48853c487d6859f8bd5069b5715023b8c65eb29`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 03:30:21 GMT
ADD file:b8a11a0dc4e697e9f924afdacd33c6c1a4744e43ff2938c4539b5650bc3207a4 in / 
# Wed, 24 Apr 2024 03:30:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:21:25 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 10:21:25 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 24 Apr 2024 10:21:39 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:21:42 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 24 Apr 2024 10:21:42 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 10:21:42 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 10:21:42 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 24 Apr 2024 19:20:52 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 19:22:02 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 19:22:04 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:efa2370e55f34d719cde5ccb31ebc8ceacbdfc1b76afe2aae60adf06d58474c5`  
		Last Modified: Wed, 24 Apr 2024 03:36:14 GMT  
		Size: 52.3 MB (52338640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454a54641079befe290c026365915481cd19d2b18e278f574a8a7aeb7bf0afd9`  
		Last Modified: Wed, 24 Apr 2024 10:23:08 GMT  
		Size: 3.4 KB (3365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ce36e8384de9bb121516c8ae8ce951e7c5e9ec057c3bc653b10b7e2cb98e5d`  
		Last Modified: Wed, 24 Apr 2024 10:23:12 GMT  
		Size: 28.9 MB (28850714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c61650b18b9b4f6eb4d47d8de678959f88969459d76ae6348b0368eb0a3546d`  
		Last Modified: Wed, 24 Apr 2024 10:23:08 GMT  
		Size: 866.3 KB (866336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153ace5bc4c33a5b5dfdb8b1d4437b1541322996a516d04573d858ed6285bb08`  
		Last Modified: Wed, 24 Apr 2024 10:23:08 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62f95624abfa16756af0dc53d48ca1c3868150cc1267d75b0ee254b3b9745f3`  
		Last Modified: Wed, 24 Apr 2024 19:22:53 GMT  
		Size: 286.3 MB (286322006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.4.0` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:538725a3c26102dafee810c9bc7e041f6323b5d1080610ba1b5706224c4b0bb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355574540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc2f1b1b64da0cfc53b85f0812212a793496ff7590a8b83e3debac425502d2a`
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
# Wed, 24 Apr 2024 23:04:51 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 23:05:56 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 23:06:00 GMT
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
	-	`sha256:00527f8af5745df9cbecbd01261351e937178cea99803e1780bc907a885634e8`  
		Last Modified: Wed, 24 Apr 2024 23:06:42 GMT  
		Size: 273.7 MB (273688510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.4.0` - linux; ppc64le

```console
$ docker pull r-base@sha256:0f40e5c0457907f8e4de593898ad6019a004d37943898268786872fcb9d617f5
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.2 MB (371155285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5c922b54c2a0a8489ad59526a810b94da859b50ce3201df63794cc3c426f24`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 03:23:25 GMT
ADD file:96a5c70b6b470689ae9f76bf58dbbdca302ccda081b6d6fb25d3249c5a22038c in / 
# Wed, 24 Apr 2024 03:23:29 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:16:47 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 08:16:51 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 24 Apr 2024 08:17:44 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:17:51 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 24 Apr 2024 08:17:52 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 08:17:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 08:17:56 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 24 Apr 2024 19:41:40 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 19:45:41 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 19:45:50 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ce4f206e19e1d340400f7cf79402f651c42ad37cfaf199791fb616c2c0c64fbb`  
		Last Modified: Wed, 24 Apr 2024 03:29:58 GMT  
		Size: 56.3 MB (56253275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342cb9b4cf381376caf65e07cde6c10754f69ee8673d5959efd0add9b24acf08`  
		Last Modified: Wed, 24 Apr 2024 08:23:47 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0a4a51056ecc9880ea2650f967e1a6fc712547a01c70c2d5b4a47446adc6b9`  
		Last Modified: Wed, 24 Apr 2024 08:23:51 GMT  
		Size: 29.9 MB (29907814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bd971110690404c6347711ccc651f642afbaf15c4261ec933fce73ea57792e`  
		Last Modified: Wed, 24 Apr 2024 08:23:48 GMT  
		Size: 866.3 KB (866330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8628d4bbdb7398ef216f0e395e60d9179d4c7046580583a6a12f80d399269b`  
		Last Modified: Wed, 24 Apr 2024 08:23:47 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b0721da05742768975020bd73315493aafa11cdc5cbecc0f1e97e11528aae3`  
		Last Modified: Wed, 24 Apr 2024 19:46:48 GMT  
		Size: 284.1 MB (284124153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.4.0` - linux; s390x

```console
$ docker pull r-base@sha256:7c9470d91c8f5508a31cbc15eebd86320dd9f74e3d89584d1d8d2840709f038f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (341965940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9872e42e391772bb1e023456c0f4f6b9a2a79e7d5a0183b213cd492b3b23df7c`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 03:46:09 GMT
ADD file:b0ed4b1191abf951ca60b74db08f035e1da25f6bcc32e8a7f9397ce5484c52d2 in / 
# Wed, 24 Apr 2024 03:46:11 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:20:33 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 07:20:36 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 24 Apr 2024 07:21:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:21:14 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 24 Apr 2024 07:21:15 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 07:21:15 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 07:21:16 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 24 Apr 2024 21:34:31 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 21:35:39 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 21:35:51 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a1899f214a24ff2437842a08743ccd4bad2c8e5cff4d87f6220c3f36c1c34149`  
		Last Modified: Wed, 24 Apr 2024 03:51:16 GMT  
		Size: 51.8 MB (51766844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf476a95acc368f50d17f0ed06c6588603cd672eba9acf02bb00e3505208e0`  
		Last Modified: Wed, 24 Apr 2024 07:24:02 GMT  
		Size: 3.4 KB (3367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b675a2dd1b8461319bef9550ae019795f9ae610a7f8a2d87383444a35f40132c`  
		Last Modified: Wed, 24 Apr 2024 07:24:05 GMT  
		Size: 28.0 MB (28023162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59023c09ff9059f34e51d4cf21a9da36b6566d6a8aac91a05c171bbd7d97f61`  
		Last Modified: Wed, 24 Apr 2024 07:24:02 GMT  
		Size: 922.3 KB (922279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68665d493596ddd7d75e51b083c1379803db4132a5725a7e988aaf7b3694c20`  
		Last Modified: Wed, 24 Apr 2024 07:24:02 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e001f3a99e38aefc680e476beffcce70ce86564947bed6b66598a8aa80e3c`  
		Last Modified: Wed, 24 Apr 2024 21:36:48 GMT  
		Size: 261.2 MB (261249938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:f65678c037bc1ace4c7d03de6d7c0aaba589ab49d559df156c49e40a5889a781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:eb0603d7a9166998854ab03f5605925112125c9c7e539ec1c3ede722ee6f682a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368381410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaf5974ca0a589e0b277419a48853c487d6859f8bd5069b5715023b8c65eb29`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 03:30:21 GMT
ADD file:b8a11a0dc4e697e9f924afdacd33c6c1a4744e43ff2938c4539b5650bc3207a4 in / 
# Wed, 24 Apr 2024 03:30:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:21:25 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 10:21:25 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 24 Apr 2024 10:21:39 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:21:42 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 24 Apr 2024 10:21:42 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 10:21:42 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 10:21:42 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 24 Apr 2024 19:20:52 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 19:22:02 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 19:22:04 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:efa2370e55f34d719cde5ccb31ebc8ceacbdfc1b76afe2aae60adf06d58474c5`  
		Last Modified: Wed, 24 Apr 2024 03:36:14 GMT  
		Size: 52.3 MB (52338640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454a54641079befe290c026365915481cd19d2b18e278f574a8a7aeb7bf0afd9`  
		Last Modified: Wed, 24 Apr 2024 10:23:08 GMT  
		Size: 3.4 KB (3365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ce36e8384de9bb121516c8ae8ce951e7c5e9ec057c3bc653b10b7e2cb98e5d`  
		Last Modified: Wed, 24 Apr 2024 10:23:12 GMT  
		Size: 28.9 MB (28850714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c61650b18b9b4f6eb4d47d8de678959f88969459d76ae6348b0368eb0a3546d`  
		Last Modified: Wed, 24 Apr 2024 10:23:08 GMT  
		Size: 866.3 KB (866336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153ace5bc4c33a5b5dfdb8b1d4437b1541322996a516d04573d858ed6285bb08`  
		Last Modified: Wed, 24 Apr 2024 10:23:08 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62f95624abfa16756af0dc53d48ca1c3868150cc1267d75b0ee254b3b9745f3`  
		Last Modified: Wed, 24 Apr 2024 19:22:53 GMT  
		Size: 286.3 MB (286322006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:538725a3c26102dafee810c9bc7e041f6323b5d1080610ba1b5706224c4b0bb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355574540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc2f1b1b64da0cfc53b85f0812212a793496ff7590a8b83e3debac425502d2a`
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
# Wed, 24 Apr 2024 23:04:51 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 23:05:56 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 23:06:00 GMT
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
	-	`sha256:00527f8af5745df9cbecbd01261351e937178cea99803e1780bc907a885634e8`  
		Last Modified: Wed, 24 Apr 2024 23:06:42 GMT  
		Size: 273.7 MB (273688510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:0f40e5c0457907f8e4de593898ad6019a004d37943898268786872fcb9d617f5
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.2 MB (371155285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5c922b54c2a0a8489ad59526a810b94da859b50ce3201df63794cc3c426f24`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 03:23:25 GMT
ADD file:96a5c70b6b470689ae9f76bf58dbbdca302ccda081b6d6fb25d3249c5a22038c in / 
# Wed, 24 Apr 2024 03:23:29 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:16:47 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 08:16:51 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 24 Apr 2024 08:17:44 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:17:51 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 24 Apr 2024 08:17:52 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 08:17:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 08:17:56 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 24 Apr 2024 19:41:40 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 19:45:41 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 19:45:50 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ce4f206e19e1d340400f7cf79402f651c42ad37cfaf199791fb616c2c0c64fbb`  
		Last Modified: Wed, 24 Apr 2024 03:29:58 GMT  
		Size: 56.3 MB (56253275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342cb9b4cf381376caf65e07cde6c10754f69ee8673d5959efd0add9b24acf08`  
		Last Modified: Wed, 24 Apr 2024 08:23:47 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0a4a51056ecc9880ea2650f967e1a6fc712547a01c70c2d5b4a47446adc6b9`  
		Last Modified: Wed, 24 Apr 2024 08:23:51 GMT  
		Size: 29.9 MB (29907814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bd971110690404c6347711ccc651f642afbaf15c4261ec933fce73ea57792e`  
		Last Modified: Wed, 24 Apr 2024 08:23:48 GMT  
		Size: 866.3 KB (866330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8628d4bbdb7398ef216f0e395e60d9179d4c7046580583a6a12f80d399269b`  
		Last Modified: Wed, 24 Apr 2024 08:23:47 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b0721da05742768975020bd73315493aafa11cdc5cbecc0f1e97e11528aae3`  
		Last Modified: Wed, 24 Apr 2024 19:46:48 GMT  
		Size: 284.1 MB (284124153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:7c9470d91c8f5508a31cbc15eebd86320dd9f74e3d89584d1d8d2840709f038f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (341965940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9872e42e391772bb1e023456c0f4f6b9a2a79e7d5a0183b213cd492b3b23df7c`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 03:46:09 GMT
ADD file:b0ed4b1191abf951ca60b74db08f035e1da25f6bcc32e8a7f9397ce5484c52d2 in / 
# Wed, 24 Apr 2024 03:46:11 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:20:33 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 07:20:36 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 24 Apr 2024 07:21:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:21:14 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 24 Apr 2024 07:21:15 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 07:21:15 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 07:21:16 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 24 Apr 2024 21:34:31 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 21:35:39 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 21:35:51 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a1899f214a24ff2437842a08743ccd4bad2c8e5cff4d87f6220c3f36c1c34149`  
		Last Modified: Wed, 24 Apr 2024 03:51:16 GMT  
		Size: 51.8 MB (51766844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf476a95acc368f50d17f0ed06c6588603cd672eba9acf02bb00e3505208e0`  
		Last Modified: Wed, 24 Apr 2024 07:24:02 GMT  
		Size: 3.4 KB (3367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b675a2dd1b8461319bef9550ae019795f9ae610a7f8a2d87383444a35f40132c`  
		Last Modified: Wed, 24 Apr 2024 07:24:05 GMT  
		Size: 28.0 MB (28023162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59023c09ff9059f34e51d4cf21a9da36b6566d6a8aac91a05c171bbd7d97f61`  
		Last Modified: Wed, 24 Apr 2024 07:24:02 GMT  
		Size: 922.3 KB (922279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68665d493596ddd7d75e51b083c1379803db4132a5725a7e988aaf7b3694c20`  
		Last Modified: Wed, 24 Apr 2024 07:24:02 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e001f3a99e38aefc680e476beffcce70ce86564947bed6b66598a8aa80e3c`  
		Last Modified: Wed, 24 Apr 2024 21:36:48 GMT  
		Size: 261.2 MB (261249938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
