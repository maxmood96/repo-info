<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.0`](#r-base440)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.0`

```console
$ docker pull r-base@sha256:a5da8dc22464dd0521f8b6de6b19df0cc19586900682656b20fc8f771499ff04
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
$ docker pull r-base@sha256:a5da8dc22464dd0521f8b6de6b19df0cc19586900682656b20fc8f771499ff04
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
