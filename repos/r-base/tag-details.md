<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.0`](#r-base440)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.0`

```console
$ docker pull r-base@sha256:36b9e82d1d0a652923ad9322ab3f52f10c935e2ed0f3e49d978cde95a3ab78b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.4.0` - linux; amd64

```console
$ docker pull r-base@sha256:252289eddf8ab1be4daa806389e07558d4813f1e800e24ab4dc337ff0c0dffe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366018778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad77890fc68f0c058854c8fb2bdb19685ad9f12e8b51d412207d7ab43d369be5`
-	Default Command: `["R"]`

```dockerfile
# Tue, 14 May 2024 01:30:16 GMT
ADD file:7496a8a75f4744a39550a0ba17dae1225503232d27a03ceffdd47b5c7496d5de in / 
# Tue, 14 May 2024 01:30:16 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:24:52 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 14 May 2024 09:24:53 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 14 May 2024 09:25:04 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:25:06 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 14 May 2024 09:25:07 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 14 May 2024 09:25:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 May 2024 09:25:07 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 14 May 2024 09:25:07 GMT
ENV R_BASE_VERSION=4.4.0
# Tue, 14 May 2024 09:26:22 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:26:24 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b6f1021887c3594f59c8eb101447edb6c5351c38c0cf447c87e410dc535562a8`  
		Last Modified: Tue, 14 May 2024 01:36:12 GMT  
		Size: 52.6 MB (52640763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ec592ee79f9867676c79c55e167461dd39abdd0a9739d0fb0f60cb36b59f31`  
		Last Modified: Tue, 14 May 2024 09:26:37 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5963ba480267b016d674d82a8780e0f216586bc039a0ba744f76e8e5e455a078`  
		Last Modified: Tue, 14 May 2024 09:26:39 GMT  
		Size: 23.1 MB (23104119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8113e50ab54470d68ac07dc5dd3b12f5667900d9a6a87b30800186333a34e214`  
		Last Modified: Tue, 14 May 2024 09:26:38 GMT  
		Size: 866.3 KB (866329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b76612ee0fbaa737509c1843797aa51470c9aea35bd9f649180aa585763bc1`  
		Last Modified: Tue, 14 May 2024 09:26:37 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0361537bad2753bdea4a3bea9179533c9e3297f307aac873a6bd7b72482ad5e`  
		Last Modified: Tue, 14 May 2024 09:27:09 GMT  
		Size: 289.4 MB (289403863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.4.0` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:dc365bbbabe47f5867c5039a3eca6cfb8989533184453f9a6da2d937d94551f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.4 MB (353380253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752058e7b56f0b3eeb29f7b889daddb5a7b2e2a516adb33b30a3ce77b5183b69`
-	Default Command: `["R"]`

```dockerfile
# Tue, 14 May 2024 00:41:08 GMT
ADD file:d7aee0a25e3d206c1ca526373ab1236a244025e76ee8802b2de9c7851fc7fc80 in / 
# Tue, 14 May 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:32:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 14 May 2024 07:32:25 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 14 May 2024 07:32:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:32:35 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 14 May 2024 07:32:35 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 14 May 2024 07:32:35 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 May 2024 07:32:36 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 14 May 2024 07:32:36 GMT
ENV R_BASE_VERSION=4.4.0
# Tue, 14 May 2024 07:33:42 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:33:47 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:25b146dc3d2d8d07e05474869061ffbe0ccb76a9c19a029a9eb03dfe587453f9`  
		Last Modified: Tue, 14 May 2024 00:46:09 GMT  
		Size: 52.9 MB (52912074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d31376aa94ef88de5243dd80b15ff7afa44bbf90459d710d0a0080dba6c8fe7`  
		Last Modified: Tue, 14 May 2024 07:34:07 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a34777fcf44f167e8a01ee0cddd7cf2e2bce3aecea4d87bbb52be6b1f477f0`  
		Last Modified: Tue, 14 May 2024 07:34:09 GMT  
		Size: 23.1 MB (23088415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff9278b8d15887377797e776fbd8163cf3c89a0f1f7cc73b4f572391868f1c`  
		Last Modified: Tue, 14 May 2024 07:34:07 GMT  
		Size: 866.3 KB (866325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e6758f6de5eed082c1c652224c51b33634f957b19beba44d1c62448f65af7`  
		Last Modified: Tue, 14 May 2024 07:34:07 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca41a6ac985daf41f3112b93887bccc9722f54db209b3d407bcd61b2c58399c`  
		Last Modified: Tue, 14 May 2024 07:34:30 GMT  
		Size: 276.5 MB (276509734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.4.0` - linux; ppc64le

```console
$ docker pull r-base@sha256:5c835795b0c48bf4c4322bc5b28a64c5eb980f82b34369cce3b51dab07536395
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368223189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16028726ab2a1077e7816638e2fb2c5b12ea4ed50f6d4be52f6e726265ebbab`
-	Default Command: `["R"]`

```dockerfile
# Tue, 14 May 2024 01:21:47 GMT
ADD file:1e419951dadece1f9151a37e9ad50f8131769e122c138fa53d258e388386961d in / 
# Tue, 14 May 2024 01:21:49 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:43:47 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 14 May 2024 06:43:49 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 14 May 2024 06:44:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:44:13 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 14 May 2024 06:44:14 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 14 May 2024 06:44:15 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 May 2024 06:44:17 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 14 May 2024 06:44:18 GMT
ENV R_BASE_VERSION=4.4.0
# Tue, 14 May 2024 06:46:27 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:46:36 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d17c53859f4c9ab9a4d5fad8696f2c0eb323a7e2f067d4d131095bd5ef2b0f91`  
		Last Modified: Tue, 14 May 2024 01:27:03 GMT  
		Size: 56.5 MB (56531498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180128dece77677940845de8acf8d46de2c9f943636d0e23bf131cfd03bcda2a`  
		Last Modified: Tue, 14 May 2024 06:46:46 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e988622673af21144b72d12ab316b2ce798e5b427b5e990337a6e5c072fae093`  
		Last Modified: Tue, 14 May 2024 06:46:49 GMT  
		Size: 23.3 MB (23324208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b5a18f6949880ab8fb7a6d174f03dc4b3e11efa9e0fb6d9fca7cebcb74c2b9`  
		Last Modified: Tue, 14 May 2024 06:46:46 GMT  
		Size: 866.3 KB (866325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca97636c42ec2db938a4d8c79d523505a4e19f53d3d7b315d55ea0c671bf6f98`  
		Last Modified: Tue, 14 May 2024 06:46:46 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51bf1950e17b42c206180c126c91b9c91391840f7b812076b50de8420c353fc`  
		Last Modified: Tue, 14 May 2024 06:47:23 GMT  
		Size: 287.5 MB (287497450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.4.0` - linux; s390x

```console
$ docker pull r-base@sha256:a501f28b33b955ee7e1180d49c859be143489655c118ae796d9db851a49d92a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340504135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830d2a03c4e6bd5bfc02415f803ed546b1e2e218881a37c6b064566d672b2a32`
-	Default Command: `["R"]`

```dockerfile
# Tue, 14 May 2024 00:44:50 GMT
ADD file:4648ccf21b5ed0ffb91f4df711a7a846c609705bfcc60f590fcd41b3c5fab226 in / 
# Tue, 14 May 2024 00:44:53 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:28:23 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 14 May 2024 06:28:23 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 14 May 2024 06:28:32 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:28:34 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 14 May 2024 06:28:34 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 14 May 2024 06:28:34 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 May 2024 06:28:34 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 14 May 2024 06:28:34 GMT
ENV R_BASE_VERSION=4.4.0
# Tue, 14 May 2024 06:29:26 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:29:34 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b6988741f7ba3983b538f656a90da504a35a297351fdda81be0d7cec90e792d9`  
		Last Modified: Tue, 14 May 2024 00:49:38 GMT  
		Size: 52.3 MB (52291052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff92db65b6e69c1dd9e3575ee013a8d8dac7ec98854383aca53b9e6f47444a8`  
		Last Modified: Tue, 14 May 2024 06:29:51 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bdc6c4a5334f01bbc14bdc54a71d34203f3b34cd4d49cd369383ab47bc1f71`  
		Last Modified: Tue, 14 May 2024 06:29:54 GMT  
		Size: 23.2 MB (23212121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718c99a6688fd5793ecf592b33f9d707dbcd8b1a571f8652ba4c700e4e2cd641`  
		Last Modified: Tue, 14 May 2024 06:29:51 GMT  
		Size: 922.3 KB (922276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670caf69c64588165992cf781709e3085db6f82c88a6ed6929c8d6e267874e1c`  
		Last Modified: Tue, 14 May 2024 06:29:51 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a8f87f7d50d7fe7ce7ff23fd7a8e0d7b09511c04cc9ec077927b9a6182ceda`  
		Last Modified: Tue, 14 May 2024 06:30:18 GMT  
		Size: 264.1 MB (264074982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:36b9e82d1d0a652923ad9322ab3f52f10c935e2ed0f3e49d978cde95a3ab78b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:252289eddf8ab1be4daa806389e07558d4813f1e800e24ab4dc337ff0c0dffe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366018778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad77890fc68f0c058854c8fb2bdb19685ad9f12e8b51d412207d7ab43d369be5`
-	Default Command: `["R"]`

```dockerfile
# Tue, 14 May 2024 01:30:16 GMT
ADD file:7496a8a75f4744a39550a0ba17dae1225503232d27a03ceffdd47b5c7496d5de in / 
# Tue, 14 May 2024 01:30:16 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:24:52 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 14 May 2024 09:24:53 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 14 May 2024 09:25:04 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:25:06 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 14 May 2024 09:25:07 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 14 May 2024 09:25:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 May 2024 09:25:07 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 14 May 2024 09:25:07 GMT
ENV R_BASE_VERSION=4.4.0
# Tue, 14 May 2024 09:26:22 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:26:24 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b6f1021887c3594f59c8eb101447edb6c5351c38c0cf447c87e410dc535562a8`  
		Last Modified: Tue, 14 May 2024 01:36:12 GMT  
		Size: 52.6 MB (52640763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ec592ee79f9867676c79c55e167461dd39abdd0a9739d0fb0f60cb36b59f31`  
		Last Modified: Tue, 14 May 2024 09:26:37 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5963ba480267b016d674d82a8780e0f216586bc039a0ba744f76e8e5e455a078`  
		Last Modified: Tue, 14 May 2024 09:26:39 GMT  
		Size: 23.1 MB (23104119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8113e50ab54470d68ac07dc5dd3b12f5667900d9a6a87b30800186333a34e214`  
		Last Modified: Tue, 14 May 2024 09:26:38 GMT  
		Size: 866.3 KB (866329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b76612ee0fbaa737509c1843797aa51470c9aea35bd9f649180aa585763bc1`  
		Last Modified: Tue, 14 May 2024 09:26:37 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0361537bad2753bdea4a3bea9179533c9e3297f307aac873a6bd7b72482ad5e`  
		Last Modified: Tue, 14 May 2024 09:27:09 GMT  
		Size: 289.4 MB (289403863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:dc365bbbabe47f5867c5039a3eca6cfb8989533184453f9a6da2d937d94551f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.4 MB (353380253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752058e7b56f0b3eeb29f7b889daddb5a7b2e2a516adb33b30a3ce77b5183b69`
-	Default Command: `["R"]`

```dockerfile
# Tue, 14 May 2024 00:41:08 GMT
ADD file:d7aee0a25e3d206c1ca526373ab1236a244025e76ee8802b2de9c7851fc7fc80 in / 
# Tue, 14 May 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:32:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 14 May 2024 07:32:25 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 14 May 2024 07:32:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:32:35 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 14 May 2024 07:32:35 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 14 May 2024 07:32:35 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 May 2024 07:32:36 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 14 May 2024 07:32:36 GMT
ENV R_BASE_VERSION=4.4.0
# Tue, 14 May 2024 07:33:42 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:33:47 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:25b146dc3d2d8d07e05474869061ffbe0ccb76a9c19a029a9eb03dfe587453f9`  
		Last Modified: Tue, 14 May 2024 00:46:09 GMT  
		Size: 52.9 MB (52912074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d31376aa94ef88de5243dd80b15ff7afa44bbf90459d710d0a0080dba6c8fe7`  
		Last Modified: Tue, 14 May 2024 07:34:07 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a34777fcf44f167e8a01ee0cddd7cf2e2bce3aecea4d87bbb52be6b1f477f0`  
		Last Modified: Tue, 14 May 2024 07:34:09 GMT  
		Size: 23.1 MB (23088415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff9278b8d15887377797e776fbd8163cf3c89a0f1f7cc73b4f572391868f1c`  
		Last Modified: Tue, 14 May 2024 07:34:07 GMT  
		Size: 866.3 KB (866325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e6758f6de5eed082c1c652224c51b33634f957b19beba44d1c62448f65af7`  
		Last Modified: Tue, 14 May 2024 07:34:07 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca41a6ac985daf41f3112b93887bccc9722f54db209b3d407bcd61b2c58399c`  
		Last Modified: Tue, 14 May 2024 07:34:30 GMT  
		Size: 276.5 MB (276509734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:5c835795b0c48bf4c4322bc5b28a64c5eb980f82b34369cce3b51dab07536395
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368223189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16028726ab2a1077e7816638e2fb2c5b12ea4ed50f6d4be52f6e726265ebbab`
-	Default Command: `["R"]`

```dockerfile
# Tue, 14 May 2024 01:21:47 GMT
ADD file:1e419951dadece1f9151a37e9ad50f8131769e122c138fa53d258e388386961d in / 
# Tue, 14 May 2024 01:21:49 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:43:47 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 14 May 2024 06:43:49 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 14 May 2024 06:44:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:44:13 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 14 May 2024 06:44:14 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 14 May 2024 06:44:15 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 May 2024 06:44:17 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 14 May 2024 06:44:18 GMT
ENV R_BASE_VERSION=4.4.0
# Tue, 14 May 2024 06:46:27 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:46:36 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d17c53859f4c9ab9a4d5fad8696f2c0eb323a7e2f067d4d131095bd5ef2b0f91`  
		Last Modified: Tue, 14 May 2024 01:27:03 GMT  
		Size: 56.5 MB (56531498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180128dece77677940845de8acf8d46de2c9f943636d0e23bf131cfd03bcda2a`  
		Last Modified: Tue, 14 May 2024 06:46:46 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e988622673af21144b72d12ab316b2ce798e5b427b5e990337a6e5c072fae093`  
		Last Modified: Tue, 14 May 2024 06:46:49 GMT  
		Size: 23.3 MB (23324208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b5a18f6949880ab8fb7a6d174f03dc4b3e11efa9e0fb6d9fca7cebcb74c2b9`  
		Last Modified: Tue, 14 May 2024 06:46:46 GMT  
		Size: 866.3 KB (866325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca97636c42ec2db938a4d8c79d523505a4e19f53d3d7b315d55ea0c671bf6f98`  
		Last Modified: Tue, 14 May 2024 06:46:46 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51bf1950e17b42c206180c126c91b9c91391840f7b812076b50de8420c353fc`  
		Last Modified: Tue, 14 May 2024 06:47:23 GMT  
		Size: 287.5 MB (287497450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:a501f28b33b955ee7e1180d49c859be143489655c118ae796d9db851a49d92a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340504135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830d2a03c4e6bd5bfc02415f803ed546b1e2e218881a37c6b064566d672b2a32`
-	Default Command: `["R"]`

```dockerfile
# Tue, 14 May 2024 00:44:50 GMT
ADD file:4648ccf21b5ed0ffb91f4df711a7a846c609705bfcc60f590fcd41b3c5fab226 in / 
# Tue, 14 May 2024 00:44:53 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:28:23 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 14 May 2024 06:28:23 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 14 May 2024 06:28:32 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:28:34 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 14 May 2024 06:28:34 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 14 May 2024 06:28:34 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 May 2024 06:28:34 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 14 May 2024 06:28:34 GMT
ENV R_BASE_VERSION=4.4.0
# Tue, 14 May 2024 06:29:26 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:29:34 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b6988741f7ba3983b538f656a90da504a35a297351fdda81be0d7cec90e792d9`  
		Last Modified: Tue, 14 May 2024 00:49:38 GMT  
		Size: 52.3 MB (52291052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff92db65b6e69c1dd9e3575ee013a8d8dac7ec98854383aca53b9e6f47444a8`  
		Last Modified: Tue, 14 May 2024 06:29:51 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bdc6c4a5334f01bbc14bdc54a71d34203f3b34cd4d49cd369383ab47bc1f71`  
		Last Modified: Tue, 14 May 2024 06:29:54 GMT  
		Size: 23.2 MB (23212121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718c99a6688fd5793ecf592b33f9d707dbcd8b1a571f8652ba4c700e4e2cd641`  
		Last Modified: Tue, 14 May 2024 06:29:51 GMT  
		Size: 922.3 KB (922276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670caf69c64588165992cf781709e3085db6f82c88a6ed6929c8d6e267874e1c`  
		Last Modified: Tue, 14 May 2024 06:29:51 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a8f87f7d50d7fe7ce7ff23fd7a8e0d7b09511c04cc9ec077927b9a6182ceda`  
		Last Modified: Tue, 14 May 2024 06:30:18 GMT  
		Size: 264.1 MB (264074982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
