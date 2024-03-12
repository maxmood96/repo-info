## `r-base:latest`

```console
$ docker pull r-base@sha256:8c5da70a043e10da25b83cee65dbcc102ccbfbfd4e050d6c25b2a9d2adbd85e3
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
$ docker pull r-base@sha256:52db6804775a7d4ba8f18ccbbd350eb901bd3fb26004039b2d53eaa02e655aa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (353995110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d2d34bec33c130576d85e0354a89bb6810f5947b3967118be21db16c56bc7c`
-	Default Command: `["R"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:53 GMT
ADD file:84a74589525ee8c23c5f03b46e981779c3a844eb1650ace0c0f608d665f71690 in / 
# Tue, 13 Feb 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:33:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Feb 2024 07:33:04 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 13 Feb 2024 07:33:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:33:16 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:33:17 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 07:33:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:33:17 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 01 Mar 2024 01:19:55 GMT
ENV R_BASE_VERSION=4.3.3
# Fri, 01 Mar 2024 01:21:18 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Mar 2024 01:21:23 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1dd8c22b346593e149ade1aa99ea3d35442a7aa0f7d3e32abb41db5e4ff20379`  
		Last Modified: Tue, 13 Feb 2024 00:48:35 GMT  
		Size: 52.2 MB (52194113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d56ebea94b2a04482bb5e0b668deb9677812b98cc51928aa266ab558fd7fb`  
		Last Modified: Tue, 13 Feb 2024 07:34:47 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5666500bb0e142ac423bbd25d4a3e3ddaa5187e1d126570958064081b8c21e96`  
		Last Modified: Tue, 13 Feb 2024 07:34:49 GMT  
		Size: 25.3 MB (25330316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55a0e1551eaf53744747f1e40cde0a99598382047683211bb69b4bbcd7bebc0`  
		Last Modified: Tue, 13 Feb 2024 07:34:47 GMT  
		Size: 866.3 KB (866324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40da1c2ff00f634d6818de07b40d839045cba1a4e17dd7f138c1c7fe0bb99a50`  
		Last Modified: Tue, 13 Feb 2024 07:34:47 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db60940ab39aaacafc2e5f422bcfb45f5fe29c97ce68eb0b028ee65eb6a158fe`  
		Last Modified: Fri, 01 Mar 2024 01:22:03 GMT  
		Size: 275.6 MB (275600654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:2d9a972b8eb7b8045f05c10059a8bdac56225d840125d4b295cebd9212d55965
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369563385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae21f285259e5bccdb5cb5fe3f5ac31451682c34125274e9f0026e5e8dc26bf`
-	Default Command: `["R"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:09 GMT
ADD file:fb513218e649a1afb3e363333714c9f9699093574358ac0b47cd3046f1eb5186 in / 
# Tue, 13 Feb 2024 00:41:12 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:41:37 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Feb 2024 07:41:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 13 Feb 2024 07:41:57 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:42:00 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:42:01 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 07:42:01 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:42:02 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 01 Mar 2024 01:04:33 GMT
ENV R_BASE_VERSION=4.3.3
# Fri, 01 Mar 2024 01:08:27 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Mar 2024 01:08:37 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:26cad4a1d56e1b4700207ff4bc765a669dfe6bc2d3fc942e890febbeec77c519`  
		Last Modified: Tue, 13 Feb 2024 00:47:17 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd9bbffa1d774c9166592815a0e576368265a592d044b5c1bbb75f2191580`  
		Last Modified: Tue, 13 Feb 2024 07:44:07 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a3a9cb161be3007849862bd630cc904e4bbe2b7f0b39f3c06d6997fbfa89a6`  
		Last Modified: Tue, 13 Feb 2024 07:44:11 GMT  
		Size: 25.9 MB (25860108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627fa6d14c62e04f5d17bba4581773ba388912eefbf32b6268257d1eb52d3106`  
		Last Modified: Tue, 13 Feb 2024 07:44:08 GMT  
		Size: 866.3 KB (866339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141427271f0a75234f3cc23f329380f76a19dc3937bc7b500da9d54f0c5810e4`  
		Last Modified: Tue, 13 Feb 2024 07:44:07 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc793901541e015838bf537a62431cec42b3732e3a488a038d8aeb2b4572f429`  
		Last Modified: Fri, 01 Mar 2024 01:09:26 GMT  
		Size: 286.6 MB (286598391 bytes)  
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
