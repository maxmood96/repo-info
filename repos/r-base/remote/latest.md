## `r-base:latest`

```console
$ docker pull r-base@sha256:ff80a23f69bd11e78cb5c384111b79333fda3f2e55020b66dffcb4ece5174d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:94efd8866f9c98e0ce6aa6c090f870764784a3bf20fbf15dfff0e709d81fc684
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350140890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c13832c443d9ef54d22292957d04d5f2cd57d6d48156af054558779c039300`
-	Default Command: `["R"]`

```dockerfile
# Wed, 12 Apr 2023 00:21:33 GMT
ADD file:28aeff48a52e156907bf710c1e3cd7ac329d157f36816ca755bcea5177269765 in / 
# Wed, 12 Apr 2023 00:21:33 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:24:28 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 12 Apr 2023 07:24:28 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 12 Apr 2023 07:24:39 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:24:41 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 12 Apr 2023 07:24:41 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 12 Apr 2023 07:24:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 12 Apr 2023 07:24:42 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 21 Apr 2023 19:30:18 GMT
ENV R_BASE_VERSION=4.3.0
# Fri, 21 Apr 2023 19:30:18 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 21 Apr 2023 19:32:33 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 21 Apr 2023 19:32:35 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1c6654873ad3f068a7ff34cc7f44a13003d6eb6f2261ac42d1cac07ac8ed4e0e`  
		Last Modified: Wed, 12 Apr 2023 00:26:11 GMT  
		Size: 49.3 MB (49292939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbbc3c9763a62e02e37d3253b4f51ad63b8c54fb82f81f56a4cc85e232ba641`  
		Last Modified: Wed, 12 Apr 2023 07:26:57 GMT  
		Size: 3.4 KB (3362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7646a74d00d95ce663ebea307a3f24fb87504a5a48565c115b22c329d20f1796`  
		Last Modified: Wed, 12 Apr 2023 07:26:58 GMT  
		Size: 25.2 MB (25157493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba968619bce4e2ca71622e5a3f11f14baabf371c9691e17a56ac8e2d0563969e`  
		Last Modified: Wed, 12 Apr 2023 07:26:56 GMT  
		Size: 865.8 KB (865846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aeb334e91685fd5e7520810b69513d0a96806791043047b6060813440ab99fb`  
		Last Modified: Wed, 12 Apr 2023 07:26:55 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2040db772b17d98d2c1562b3da0522735cbe88f031e1d80ea9203fd05bcd3c`  
		Last Modified: Fri, 21 Apr 2023 19:32:46 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd1c1d597649474249f2ecfbad71b058f5d2e1dd98adcd6d79170eb6477db06`  
		Last Modified: Fri, 21 Apr 2023 19:33:17 GMT  
		Size: 274.8 MB (274820605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:6be4e05a10a22e42ca9ce12e89a3496c35de517c41345a691c7fae989ac8618c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321696075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb171d7c656b07647244bdde238a2819e9dee621202aaa7cbf35ed8cf711f9e`
-	Default Command: `["R"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:46 GMT
ADD file:80a4d0d891f9f28bd3948de18579583b6c11a4a8805b6230daaa0ac2a35c453d in / 
# Wed, 12 Apr 2023 00:40:46 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 03:14:34 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 12 Apr 2023 03:14:34 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 12 Apr 2023 03:14:44 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 03:14:46 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 12 Apr 2023 03:14:46 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 12 Apr 2023 03:14:46 GMT
ENV LANG=en_US.UTF-8
# Wed, 12 Apr 2023 03:14:47 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 12 Apr 2023 03:14:47 GMT
ENV R_BASE_VERSION=4.2.3
# Wed, 12 Apr 2023 03:14:47 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 12 Apr 2023 03:16:45 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 03:16:49 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d1d33b0463b9cb723855fca4aff8cdc62c34a1907b920e8e626bd38d7577387f`  
		Last Modified: Wed, 12 Apr 2023 00:44:53 GMT  
		Size: 49.3 MB (49345366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14713ff22710d8236db54cc044463e0fe76c30e886891d410b14a938c637ac2e`  
		Last Modified: Wed, 12 Apr 2023 03:17:03 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8aeb9c8fe2e295c2b3a2fea6a6498c3037b7a49a0e54376b387cdcc70af07`  
		Last Modified: Wed, 12 Apr 2023 03:17:03 GMT  
		Size: 25.0 MB (24982728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65dc3869ed093b5204a7a0a99a9e8ec1c4f4d7606b3bd9178c7bdb6b447feda1`  
		Last Modified: Wed, 12 Apr 2023 03:17:01 GMT  
		Size: 865.9 KB (865850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6824938d3e4f2d95fd7262fa044aa52ab3114a201c9b36d95bb44e2447fe8e`  
		Last Modified: Wed, 12 Apr 2023 03:17:01 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a63c57f8e04a06247a0854efa50e538419a5e41ef1c20a87725663c2bf3f288`  
		Last Modified: Wed, 12 Apr 2023 03:17:01 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31275e575d0f0c74f798a81a94efc9cc49fae227956a2216b31cd38e953a0e5a`  
		Last Modified: Wed, 12 Apr 2023 03:17:21 GMT  
		Size: 246.5 MB (246498129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:ad733b9b4a87e03010934e45919108b91edda68db1af152852ff0fbebb42a081
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338307418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9be4dafc6800be01321196dcd9ffb4fc9522bfc17143f27022d314c17451f2e`
-	Default Command: `["R"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:00 GMT
ADD file:107d4f159f2bc5b04467e08852422f5c78548e0f92853bd29d5d2b05b387d3a9 in / 
# Wed, 12 Apr 2023 00:10:03 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:00:06 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 12 Apr 2023 07:00:09 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 12 Apr 2023 07:00:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:00:42 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 12 Apr 2023 07:00:43 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 12 Apr 2023 07:00:44 GMT
ENV LANG=en_US.UTF-8
# Wed, 12 Apr 2023 07:00:49 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 12 Apr 2023 07:00:50 GMT
ENV R_BASE_VERSION=4.2.3
# Wed, 12 Apr 2023 07:00:52 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 12 Apr 2023 07:04:52 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:05:04 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a4fca5aa8bf3f9957686fb6705daa645629edb94592f35c71e46e52a1742ed1a`  
		Last Modified: Wed, 12 Apr 2023 00:15:06 GMT  
		Size: 53.3 MB (53299985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccc92c826b071e57f3b9730b591c447939c384fd0951960d6e73c4821bae145`  
		Last Modified: Wed, 12 Apr 2023 07:05:22 GMT  
		Size: 3.4 KB (3366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b353e675eb05b48bb03cfd6c97c6a529edc801a1b0d92f5b66979718503acad`  
		Last Modified: Wed, 12 Apr 2023 07:05:25 GMT  
		Size: 25.6 MB (25556057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f05dceb3b5e9b5ef9cf56dd7755c08657578ca4e044b825f7b7342a468b73c1`  
		Last Modified: Wed, 12 Apr 2023 07:05:21 GMT  
		Size: 865.9 KB (865855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da64538026eabb52f89dd3e3ead28c549abdf6db2c74f0b1907e132f41d4bb2`  
		Last Modified: Wed, 12 Apr 2023 07:05:20 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee3887d18fba6a5e77903beb7b737cd07688f7630defc6adb1243a51c613f31`  
		Last Modified: Wed, 12 Apr 2023 07:05:20 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af209be74a69a79b44a799b71006a0a6a130773a48e5ba48d2e90f8d0a8113`  
		Last Modified: Wed, 12 Apr 2023 07:06:12 GMT  
		Size: 258.6 MB (258581511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:5db119dd09422f7cd85ef7eb7f42cb408aaa728ae58c62e24b596080ce71efde
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310282773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b410a5480cc8fdf77c67773c70bfee119bba763c32bda0b8c9ddb0e750cbd`
-	Default Command: `["R"]`

```dockerfile
# Wed, 12 Apr 2023 00:02:57 GMT
ADD file:a04191f521f5135016e837ec503a63f4e8488c1a13030ba67c96cc8f68da9d50 in / 
# Wed, 12 Apr 2023 00:03:03 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:35:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 12 Apr 2023 07:35:25 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 12 Apr 2023 07:35:37 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:35:41 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 12 Apr 2023 07:35:42 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 12 Apr 2023 07:35:42 GMT
ENV LANG=en_US.UTF-8
# Wed, 12 Apr 2023 07:35:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 21 Apr 2023 19:52:52 GMT
ENV R_BASE_VERSION=4.3.0
# Fri, 21 Apr 2023 19:52:52 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 21 Apr 2023 19:54:31 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 21 Apr 2023 19:54:50 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0d66e85e2f078d0a3241d6085f175f28d3ed3f6304a2561cc20fd703234bd4bc`  
		Last Modified: Wed, 12 Apr 2023 00:06:14 GMT  
		Size: 47.7 MB (47670408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb07fd41a284e9cb798fd1388efdc6525fb96c3a7e1d40f6538cf169d9bb85f4`  
		Last Modified: Wed, 12 Apr 2023 07:37:49 GMT  
		Size: 3.4 KB (3364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76b4b9303d4e9a21a275bbf2c9c9e01fe531c3ccc255fc13b0df969ed1adb8`  
		Last Modified: Wed, 12 Apr 2023 07:37:51 GMT  
		Size: 24.8 MB (24822520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a55da99748773d917a67ef4b00a484126374ab47d5fc5c96bc0be307199cc5d`  
		Last Modified: Wed, 12 Apr 2023 07:37:48 GMT  
		Size: 921.0 KB (921011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a513236c23b8e51e5b1f6943275adefd6c5ce2af49398a7df8f060d0aa699a`  
		Last Modified: Wed, 12 Apr 2023 07:37:48 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853a986bb5b5081170f04719cf7b318d5bc03a11d8cad300c6d047f737070abc`  
		Last Modified: Fri, 21 Apr 2023 19:55:00 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52e9d7eebdb498c9a01645e7e70d7af4a1af66e17aa923be2c1e32cea4bb27b`  
		Last Modified: Fri, 21 Apr 2023 19:55:26 GMT  
		Size: 236.9 MB (236864826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
