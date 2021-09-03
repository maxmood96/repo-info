## `r-base:latest`

```console
$ docker pull r-base@sha256:7a55c99a48f8759a209c21c06cb2c44ec52d7bbe472957e31e5c29d497484db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:8da10a720b26d6b6c2d32cb743f90cb9bf54f4b536e471c3da23342510380fb7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324307880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176db8b917ff130dca4fa65bd1bc571e450cde8c2f5d71bf130394ca5579019f`
-	Default Command: `["R"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:58 GMT
ADD file:34bf1f6ddafae4895f45a110a2d7ea6139557d82a9508b85d7518a54be80aa91 in / 
# Fri, 03 Sep 2021 01:23:59 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 13:34:39 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 03 Sep 2021 13:34:41 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Fri, 03 Sep 2021 13:35:03 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 13:35:07 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Fri, 03 Sep 2021 13:35:07 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 03 Sep 2021 13:35:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Sep 2021 13:35:08 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 03 Sep 2021 13:35:08 GMT
ENV R_BASE_VERSION=4.1.1
# Fri, 03 Sep 2021 13:35:09 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 03 Sep 2021 13:36:12 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 13:36:14 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:931337f74a7f142aabe368b4eb63c0e810923f0f0d4f6f018794c6213a4c07ca`  
		Last Modified: Fri, 03 Sep 2021 01:32:30 GMT  
		Size: 55.5 MB (55464641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6757576bd2e192afd6cf59dbdc918b17943ad406c681366ad3317bca84e5e2e`  
		Last Modified: Fri, 03 Sep 2021 13:36:28 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8202d4b1ddd23c53d9e4245804e40b5a8e73163b20181e9cf2c02f27bb5b6f7`  
		Last Modified: Fri, 03 Sep 2021 13:36:32 GMT  
		Size: 25.6 MB (25639660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1083f8a27132de38911b25dbe58bc8a16b67fa9ee241a5a9cba37efaeccbad12`  
		Last Modified: Fri, 03 Sep 2021 13:36:26 GMT  
		Size: 864.6 KB (864587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9b19473be7a57899c83282fb42b7a718d4f99a3f9bbe013998a8cd83751ab9`  
		Last Modified: Fri, 03 Sep 2021 13:36:27 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b650082ab77a5d9f391d6f1e1f49c6eb8d6649be477818b2b69df976bd82c8aa`  
		Last Modified: Fri, 03 Sep 2021 13:36:26 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ef86dac7405f9734937ffde56147822f89f22b950bcff00a87c8493c3244a8`  
		Last Modified: Fri, 03 Sep 2021 13:37:08 GMT  
		Size: 242.3 MB (242336475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:15bcdf78a283096928a79a276f3bf4b7bf8390e564df6527b79cc6634a414248
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312412401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b01c676c4159ccf0e5bd8fa641aec2d26e2256ab57bfcdf9344322c208896b`
-	Default Command: `["R"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:59 GMT
ADD file:024a3f01f7d5ed6ce6f4ee6507a0dbb6edefe3267e1672fb07b5e5eae29a47b7 in / 
# Fri, 03 Sep 2021 00:42:59 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:10:42 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 03 Sep 2021 01:10:43 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Fri, 03 Sep 2021 01:10:51 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 01:10:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Fri, 03 Sep 2021 01:10:54 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 03 Sep 2021 01:10:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Sep 2021 01:10:55 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 03 Sep 2021 01:10:55 GMT
ENV R_BASE_VERSION=4.1.1
# Fri, 03 Sep 2021 01:10:56 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 03 Sep 2021 01:11:41 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 01:11:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:cb1c1f26816daf4a362d7ca0dfd432a0efc976e7a23fda91e6d7940176af45d5`  
		Last Modified: Fri, 03 Sep 2021 00:53:52 GMT  
		Size: 54.5 MB (54510227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69dfdee9e07adfba86c978fafba78a0738db857066ab384103a0410832152b6`  
		Last Modified: Fri, 03 Sep 2021 01:12:06 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8907b089dd3c59e93a8693c3c61c4bb71122ad5ded0362d201d63f710648c824`  
		Last Modified: Fri, 03 Sep 2021 01:12:09 GMT  
		Size: 25.6 MB (25628679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0473cb5f95596271207ba1b29cf10816c4d62bd726bcf7e12fa7c371ed2b5c`  
		Last Modified: Fri, 03 Sep 2021 01:12:04 GMT  
		Size: 864.6 KB (864588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4f43e99cba990721b85bc5659d4679c3954d763a05006fac93c32e1c45d759`  
		Last Modified: Fri, 03 Sep 2021 01:12:03 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7595359e054f4bda42eb4cc050d0e1c0761a46d6f163026e7865de86bc41d3d0`  
		Last Modified: Fri, 03 Sep 2021 01:12:03 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5d55ad1075740960a588a8ccf04c28e59d14d82a81ba1c80e5247e644a4f64`  
		Last Modified: Fri, 03 Sep 2021 01:12:33 GMT  
		Size: 231.4 MB (231406391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:617559accc990c254a4ff30d43605d99c4de2a770191715667cc25a57b00fa57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322579703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4059f6fd409984d90ddd1fce6ac7dc0049dc269105b326db7ab06dc42796d6`
-	Default Command: `["R"]`

```dockerfile
# Fri, 03 Sep 2021 01:28:03 GMT
ADD file:3c352e1c5b975bab6ba80213fc86e0b5836f9976e755be58fccd6f003941ca8b in / 
# Fri, 03 Sep 2021 01:28:12 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 18:07:19 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 03 Sep 2021 18:07:40 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Fri, 03 Sep 2021 18:08:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 18:09:03 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Fri, 03 Sep 2021 18:09:10 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 03 Sep 2021 18:09:15 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Sep 2021 18:09:24 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 03 Sep 2021 18:09:28 GMT
ENV R_BASE_VERSION=4.1.1
# Fri, 03 Sep 2021 18:09:43 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 03 Sep 2021 18:16:58 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 18:17:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:61eff2bf557a409d063c940d589dc8f98bf037655ffc94d8e30b546974554826`  
		Last Modified: Fri, 03 Sep 2021 01:47:00 GMT  
		Size: 59.5 MB (59526125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce611fbe8ab05ce2c89df4861eda9fa9a9ac574620f25260b3392fc1dbf77770`  
		Last Modified: Fri, 03 Sep 2021 18:17:44 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ebd15523833a8c3199a65b13cc3cf32a3c2519b0ffc145fe94c832b7ad527d`  
		Last Modified: Fri, 03 Sep 2021 18:17:44 GMT  
		Size: 25.8 MB (25847783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7784100ddcd38691f40bcbff901986458cd1db182a9f421257bc99102bae1a50`  
		Last Modified: Fri, 03 Sep 2021 18:17:40 GMT  
		Size: 864.6 KB (864587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e932154d909477bfe626a1240d5f45735b0e128fdbf67a9a8f91ebdecb3772`  
		Last Modified: Fri, 03 Sep 2021 18:17:40 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ce1c57788b3101614032507e56e512abe5141f74980255a57f6d2867a8c194`  
		Last Modified: Fri, 03 Sep 2021 18:17:40 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7ca859214f67b7844bed90bf073802c0fa78e0e2a27926fdc9a4ac983d64d6`  
		Last Modified: Fri, 03 Sep 2021 18:22:34 GMT  
		Size: 236.3 MB (236338666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:52ccb45f6f96e9cedbb058b310dc0caacd7f9748afe480e39ecb4715b141143a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.6 MB (290559707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a64d6071962e4b3e7c867f48dbb6819681f3fe1c5402a5974a427c9999f25cf`
-	Default Command: `["R"]`

```dockerfile
# Fri, 03 Sep 2021 00:47:47 GMT
ADD file:54f05be13650e2f59f5ca102e738802e756fa0f0264cf9f12db6ed40461387c8 in / 
# Fri, 03 Sep 2021 00:47:55 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:55:30 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 03 Sep 2021 04:55:31 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Fri, 03 Sep 2021 04:55:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:55:44 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Fri, 03 Sep 2021 04:55:44 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 03 Sep 2021 04:55:45 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Sep 2021 04:55:45 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 03 Sep 2021 04:55:46 GMT
ENV R_BASE_VERSION=4.1.1
# Fri, 03 Sep 2021 04:55:46 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Fri, 03 Sep 2021 04:56:48 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:56:58 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:09142d8bf3fde8b878e8f7bddf00b824e1f1b97647c8d5dbc3df6e87335828e7`  
		Last Modified: Fri, 03 Sep 2021 00:55:37 GMT  
		Size: 53.7 MB (53749639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4648cdd0007a319c9ba52dfc82fe89f92272e2bb31958751f2553e6cffa8c2f`  
		Last Modified: Fri, 03 Sep 2021 04:57:16 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbf8f83134375ad028e51a28afe00788a01e7fd96bda84acbcc035ba40ca613`  
		Last Modified: Fri, 03 Sep 2021 04:57:16 GMT  
		Size: 25.6 MB (25632465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155060aa124f1134652641018462f345fd6f748b0c95993e4d34459394738769`  
		Last Modified: Fri, 03 Sep 2021 04:57:14 GMT  
		Size: 920.2 KB (920153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85edeed1a86b9b07232533e58a0cef13de02f2d2be69f48ddeed25f117ee0af9`  
		Last Modified: Fri, 03 Sep 2021 04:57:14 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ec4773a81fd65cbed18bc538a2a54bb2a651c184c292c08cbc1c48d813666`  
		Last Modified: Fri, 03 Sep 2021 04:57:14 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731e213d1154e560dfc6583e424fc46f8fa42729f4ef0001759990ccb429cca3`  
		Last Modified: Fri, 03 Sep 2021 04:57:35 GMT  
		Size: 210.3 MB (210254933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
