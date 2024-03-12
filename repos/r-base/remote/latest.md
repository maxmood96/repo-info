## `r-base:latest`

```console
$ docker pull r-base@sha256:cced6ee1ac8aae8065b038245ed5dc2f63d646987367e21c732efb9dad552577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:3b5c502ccd9d4a6c0937a6bfc51e02741bdc7c520fe458ce4d9c136553df42b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.7 MB (374678894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3540962403816b3791ac26e8e28426eb62736a976aa8082a8ce2fec5bedff69d`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Mar 2024 01:23:19 GMT
ADD file:522a6d12a8a3032c984d93fd141274f1cb7cc1e9a6942e3b36cbf803bbe36a12 in / 
# Tue, 12 Mar 2024 01:23:20 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:38:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Mar 2024 05:38:24 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 12 Mar 2024 05:38:34 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:38:36 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Mar 2024 05:38:36 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Mar 2024 05:38:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Mar 2024 05:38:37 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Mar 2024 05:38:37 GMT
ENV R_BASE_VERSION=4.3.3
# Tue, 12 Mar 2024 05:39:56 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:39:59 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6f920f542b4ac4c8439263aaa577872294912b5aaa038e252993d921098eff73`  
		Last Modified: Tue, 12 Mar 2024 01:29:24 GMT  
		Size: 52.4 MB (52360825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0355365fe68af3b081f0dee83d0937112251e3c9fad882d064f1c6d6f5b8341`  
		Last Modified: Tue, 12 Mar 2024 05:40:07 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39601750d73073cd35038f2dd11e73818771bfc1ee48c2f85239e4e1ad258431`  
		Last Modified: Tue, 12 Mar 2024 05:40:10 GMT  
		Size: 22.8 MB (22848808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f27d6c95dc52bec636648bc5a2039b042e3ffd4c9027e4d7f8e4288c559a`  
		Last Modified: Tue, 12 Mar 2024 05:40:08 GMT  
		Size: 866.3 KB (866324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4c6b25f7328da9f2ed01fd8dd881cf78a3c39d5506a1321a8f0913aed1fc05`  
		Last Modified: Tue, 12 Mar 2024 05:40:07 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95cd703b689932b551eed321490a8590243aa01d3e8d1b9b5ee128e7d32de97`  
		Last Modified: Tue, 12 Mar 2024 05:40:41 GMT  
		Size: 298.6 MB (298599227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:274fca226913f6ed429c7d06ffad8f672ea216c7b75977dc2d4a56520c71000d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.3 MB (361325941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9878ce70e0af357274854f98f46697ac2ee2caa956b6a2c2800c2fe61bed7df4`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Mar 2024 00:47:08 GMT
ADD file:aa95db2c8e57643981efcdec0f1d6b86b507e56fdab54a8247748679a6433c70 in / 
# Tue, 12 Mar 2024 00:47:09 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 09:51:32 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Mar 2024 09:51:33 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 12 Mar 2024 09:51:41 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 09:51:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Mar 2024 09:51:43 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Mar 2024 09:51:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Mar 2024 09:51:44 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Mar 2024 09:51:44 GMT
ENV R_BASE_VERSION=4.3.3
# Tue, 12 Mar 2024 09:53:12 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 09:53:17 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9753ceab8e9b6188a30d0d3bb81834420e64806a562e2bf8fe628f8f5abe3bd1`  
		Last Modified: Tue, 12 Mar 2024 00:52:29 GMT  
		Size: 52.2 MB (52191334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceee06904560795a4916e1cd81cdaf716d954bdd6f98bd793cf9bcd7b9332d7c`  
		Last Modified: Tue, 12 Mar 2024 09:53:30 GMT  
		Size: 3.4 KB (3367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac5ef4d116ed294a57eb78f193dfa2cc36e7fd155170ba99dc87aedf04c315b`  
		Last Modified: Tue, 12 Mar 2024 09:53:32 GMT  
		Size: 22.8 MB (22836615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f7a949fa738298ba5f2ea7c1c8907c84e3ac9628d7ddd6b767d25eb27bfb89`  
		Last Modified: Tue, 12 Mar 2024 09:53:30 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7fc2c6b0cf3fea2d9567a4530e1c71a8c9893b776a342734e2fdd0cced99f0`  
		Last Modified: Tue, 12 Mar 2024 09:53:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c2a95c70e02953a1748af290fd7a5be971f77797ff307ecb362454f215844e`  
		Last Modified: Tue, 12 Mar 2024 09:53:54 GMT  
		Size: 285.4 MB (285427953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:76527ce1fb5b34445d5ce54ae8bad5c7c66665fafb014b7232b89136c51cc9ac
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.4 MB (377417753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da3087172bc5400fa06c93426c70499d2af28cce4d5b9ce5b0a8b5e0b108737`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Mar 2024 00:33:43 GMT
ADD file:28eae816397952c51c49be5b893eefaf784b74fcc86be5f7530f348f3bd79748 in / 
# Tue, 12 Mar 2024 00:33:54 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 08:24:03 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Mar 2024 08:24:15 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 12 Mar 2024 08:25:30 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:25:41 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Mar 2024 08:25:44 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Mar 2024 08:25:46 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Mar 2024 08:25:55 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Mar 2024 08:25:57 GMT
ENV R_BASE_VERSION=4.3.3
# Tue, 12 Mar 2024 08:37:27 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:37:45 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a330bc7a744677f7e934fa2e18de7eb61220cadc075ee5145cd435289dd3d817`  
		Last Modified: Tue, 12 Mar 2024 00:41:14 GMT  
		Size: 56.2 MB (56240830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cbd57ac68b4f2ca05d8d94e1e348d61756587284f9630d6b72098686fa54a9`  
		Last Modified: Tue, 12 Mar 2024 08:38:05 GMT  
		Size: 3.4 KB (3370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3fdf9947102b1f896157c6603b18ab3ed195e5430d52fdd28d1915faa6d4c4`  
		Last Modified: Tue, 12 Mar 2024 08:38:08 GMT  
		Size: 23.1 MB (23070822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532eac2900e4c26029758ff18b608c0f33c3a025b3e7d6d43edaa9775d03d7ab`  
		Last Modified: Tue, 12 Mar 2024 08:38:05 GMT  
		Size: 866.3 KB (866343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd901328940683def3b362b76d081a0ca9ed22525a04cea071eebfe31a7aadd3`  
		Last Modified: Tue, 12 Mar 2024 08:38:05 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dcd8a6d2af2645dba22339499a5915e21ab24076def56fea86e78845f7cac4`  
		Last Modified: Tue, 12 Mar 2024 08:38:44 GMT  
		Size: 297.2 MB (297236038 bytes)  
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
