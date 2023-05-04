<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.3.0`](#r-base430)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.3.0`

```console
$ docker pull r-base@sha256:1938730007f06379bf506c98ed860b33b2310572760e07810675cde09eea56af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.3.0` - linux; amd64

```console
$ docker pull r-base@sha256:157acbe58cb30e19974c438622faac2391e6c6e59394b7d80eb62334a3e1a962
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 MB (336293440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcb907f9de40b8457c40acee0b68c40c9b1615e972cb790dbc9837f5ece1d73`
-	Default Command: `["R"]`

```dockerfile
# Tue, 02 May 2023 23:48:15 GMT
ADD file:27b4229d808812579f1eb7609d08a5bb2177380a480279009a4ea17e05193323 in / 
# Tue, 02 May 2023 23:48:16 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:21:45 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 03 May 2023 22:21:46 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 03 May 2023 22:22:00 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:22:03 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 03 May 2023 22:22:03 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 03 May 2023 22:22:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 03 May 2023 22:22:03 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 03 May 2023 22:22:04 GMT
ENV R_BASE_VERSION=4.3.0
# Wed, 03 May 2023 22:22:04 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 03 May 2023 22:24:00 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:24:02 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:56c7136ddbfad3eea4cd5c38c0703e58fd25630219d5462a9099387c4b3a4160`  
		Last Modified: Tue, 02 May 2023 23:52:53 GMT  
		Size: 49.3 MB (49299248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fcdcc91a6decc4daaa550a314607547d473fced34fdf8fa11ff5d186a989fe`  
		Last Modified: Wed, 03 May 2023 22:24:15 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d61cab462a3f50000df4d96522d023f43218662709e10cbadc1c5a3cf8f2fbe`  
		Last Modified: Wed, 03 May 2023 22:24:16 GMT  
		Size: 25.2 MB (25165628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fc804098ddade4ca07b4a75d441073309e272796dede6c657a0e1ff37e38b2`  
		Last Modified: Wed, 03 May 2023 22:24:13 GMT  
		Size: 865.9 KB (865851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be6f23be5f8d3623373487b0e2249a630c173aa58bf25d712a714cc66dd6c2c`  
		Last Modified: Wed, 03 May 2023 22:24:13 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31631317ae9296807ef359039e524151b249e5e4cdd9dace5bc1e62f2d7b7f7e`  
		Last Modified: Wed, 03 May 2023 22:24:14 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cea77e9be3236da8a7eaef187017822ec2b0c0189c6628247c11fdee613877`  
		Last Modified: Wed, 03 May 2023 22:24:42 GMT  
		Size: 261.0 MB (260958713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.0` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:fde78e1b857dd0e8eaad5730eb9070f507eb96961cceefb18350c5be7857a07a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322467089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2ad7027fe8ec5c14fcbf86209e7413212105cddd7554c5bef786c46867691e`
-	Default Command: `["R"]`

```dockerfile
# Wed, 03 May 2023 00:24:01 GMT
ADD file:963c63c0aac9182210ae8c781047d25685e67bae65725505733a64de642b2b38 in / 
# Wed, 03 May 2023 00:24:01 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:27:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 03 May 2023 18:27:06 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 03 May 2023 18:27:18 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:27:19 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 03 May 2023 18:27:20 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 03 May 2023 18:27:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 03 May 2023 18:27:20 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 03 May 2023 18:27:20 GMT
ENV R_BASE_VERSION=4.3.0
# Wed, 03 May 2023 18:27:21 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 03 May 2023 18:29:26 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:29:30 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bded3796ed4449fe413c08ee04196c911ef419f9e245178303b88c7351e53623`  
		Last Modified: Wed, 03 May 2023 00:28:09 GMT  
		Size: 49.3 MB (49345336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b6f0a4e7965f4daa4282697c525cf2f94ef931ec06375e3d0a848a938f9cf`  
		Last Modified: Wed, 03 May 2023 18:29:50 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc1240a92f6182bcc7a9a22055a9a515787209df0fd3321be2d5728a848861f`  
		Last Modified: Wed, 03 May 2023 18:29:50 GMT  
		Size: 25.0 MB (24984125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a96dafdc15cb45a43d69b4a0f9c77c1b1a42a229d88d992ff3c0583f37abf16`  
		Last Modified: Wed, 03 May 2023 18:29:48 GMT  
		Size: 865.8 KB (865846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5edf7ce4519e90cc593f7b0990a28029e6b2452c987973f1c233afa8ca89730`  
		Last Modified: Wed, 03 May 2023 18:29:48 GMT  
		Size: 346.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb198f907ad587babf31cc75a480cf3d4a1383a25398c1a2d4d00540ff654cbb`  
		Last Modified: Wed, 03 May 2023 18:29:48 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c541a6193af986e2e180811ebf9dd64a82182513e6211becaa8e5728cb7c33`  
		Last Modified: Wed, 03 May 2023 18:30:08 GMT  
		Size: 247.3 MB (247267784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.0` - linux; ppc64le

```console
$ docker pull r-base@sha256:f84334040c57a42c4424a421fc20f673799e4b568f7a1bd74f5028a159bdb127
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339086471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedcbbf2eb9328077bfcd8e3efa357ec3cd674f00b27e3d7bd7dffd8d0a88ba`
-	Default Command: `["R"]`

```dockerfile
# Wed, 03 May 2023 00:33:35 GMT
ADD file:f54f5308138566009df9867a9e17d06810cb24a49786ebfdb8f2d83aa44bd004 in / 
# Wed, 03 May 2023 00:33:38 GMT
CMD ["bash"]
# Thu, 04 May 2023 00:52:09 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 04 May 2023 00:52:11 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 04 May 2023 00:52:37 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 00:52:42 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 04 May 2023 00:52:43 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 00:52:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 May 2023 00:52:45 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 04 May 2023 00:52:46 GMT
ENV R_BASE_VERSION=4.3.0
# Thu, 04 May 2023 00:52:48 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Thu, 04 May 2023 00:56:26 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 00:56:30 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c7778701ecf3e4c7947d5854ffadbfcc47a1bea59eeede267cc1563d0c205014`  
		Last Modified: Wed, 03 May 2023 00:38:50 GMT  
		Size: 53.3 MB (53307302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66bde9f479501a388f0b05d077e44d65524bbba1ee00f0dcbe703bad4534989`  
		Last Modified: Thu, 04 May 2023 00:56:41 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e618648d81125407cb42fcf36722736651dd097ba30c339a03bf4e9a8eb480`  
		Last Modified: Thu, 04 May 2023 00:56:43 GMT  
		Size: 25.6 MB (25560947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe19135c5349f7250145ae537652ad2d7773f5c17b239681c8e8d715b80f179`  
		Last Modified: Thu, 04 May 2023 00:56:39 GMT  
		Size: 865.9 KB (865852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b0b041784b86a1a06053e7950eaa748db7f632097dae4d8cc8cd14a8f90861`  
		Last Modified: Thu, 04 May 2023 00:56:38 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e7ee8a60f067de2ef718e7cb15b003582717cfdd918f4c54cd0ceaeac3e4a5`  
		Last Modified: Thu, 04 May 2023 00:56:38 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31d894101d3b038b49d338d7b2b136e522ad6078faf61b1460f8af4b087e93d`  
		Last Modified: Thu, 04 May 2023 00:57:33 GMT  
		Size: 259.3 MB (259348368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.0` - linux; s390x

```console
$ docker pull r-base@sha256:74364e52d5158adf7b032915291238f40886f7b5793e0f9475b15796c74697f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297534615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a4b993911ca773cdd0bccd1fee384c7af5afe2577fd8452e89419f8504c567`
-	Default Command: `["R"]`

```dockerfile
# Wed, 03 May 2023 03:43:00 GMT
ADD file:c572e15c46e19b472f04f1dfa7a84a66dc4b542578a96178c0d56e11644d77c2 in / 
# Wed, 03 May 2023 03:43:02 GMT
CMD ["bash"]
# Wed, 03 May 2023 23:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 03 May 2023 23:07:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 03 May 2023 23:07:14 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:07:17 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 03 May 2023 23:07:17 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 03 May 2023 23:07:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 03 May 2023 23:07:17 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 03 May 2023 23:07:18 GMT
ENV R_BASE_VERSION=4.3.0
# Wed, 03 May 2023 23:07:18 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 03 May 2023 23:09:19 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:09:25 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:14c2fbffb8254eb141a0d2ee16eb3282dd281a0afa9d6aa17ba7b5020dc35812`  
		Last Modified: Wed, 03 May 2023 03:45:54 GMT  
		Size: 47.7 MB (47675930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18598ee8dbd717641d2b5d04ec5aa5d8066fad3dc4211a88194f2f2971aae1de`  
		Last Modified: Wed, 03 May 2023 23:09:45 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41756abdb1e9d3b3efa708278ef98b4d4dc454b5097af18dfdd83922ef1e103`  
		Last Modified: Wed, 03 May 2023 23:09:46 GMT  
		Size: 24.8 MB (24832327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab7bed939c5d0c665f53cab437a2c5b803e2a4981f8117b17bdaffffb533a84`  
		Last Modified: Wed, 03 May 2023 23:09:44 GMT  
		Size: 921.0 KB (921012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0835d3f5b2796f881ac88f98e741930b32962050a42412ee06760390f33ea2a`  
		Last Modified: Wed, 03 May 2023 23:09:44 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5437c2b8b2406785d01e31c6611be54bd1adfe2209b1a23a5d31a476fff1df7d`  
		Last Modified: Wed, 03 May 2023 23:09:44 GMT  
		Size: 291.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec58f390328f63ab422e0f46f384d6c0a21d01af9808e53a24c253c9f25b0c60`  
		Last Modified: Wed, 03 May 2023 23:10:08 GMT  
		Size: 224.1 MB (224101348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:1938730007f06379bf506c98ed860b33b2310572760e07810675cde09eea56af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:157acbe58cb30e19974c438622faac2391e6c6e59394b7d80eb62334a3e1a962
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 MB (336293440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcb907f9de40b8457c40acee0b68c40c9b1615e972cb790dbc9837f5ece1d73`
-	Default Command: `["R"]`

```dockerfile
# Tue, 02 May 2023 23:48:15 GMT
ADD file:27b4229d808812579f1eb7609d08a5bb2177380a480279009a4ea17e05193323 in / 
# Tue, 02 May 2023 23:48:16 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:21:45 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 03 May 2023 22:21:46 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 03 May 2023 22:22:00 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:22:03 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 03 May 2023 22:22:03 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 03 May 2023 22:22:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 03 May 2023 22:22:03 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 03 May 2023 22:22:04 GMT
ENV R_BASE_VERSION=4.3.0
# Wed, 03 May 2023 22:22:04 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 03 May 2023 22:24:00 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:24:02 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:56c7136ddbfad3eea4cd5c38c0703e58fd25630219d5462a9099387c4b3a4160`  
		Last Modified: Tue, 02 May 2023 23:52:53 GMT  
		Size: 49.3 MB (49299248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fcdcc91a6decc4daaa550a314607547d473fced34fdf8fa11ff5d186a989fe`  
		Last Modified: Wed, 03 May 2023 22:24:15 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d61cab462a3f50000df4d96522d023f43218662709e10cbadc1c5a3cf8f2fbe`  
		Last Modified: Wed, 03 May 2023 22:24:16 GMT  
		Size: 25.2 MB (25165628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fc804098ddade4ca07b4a75d441073309e272796dede6c657a0e1ff37e38b2`  
		Last Modified: Wed, 03 May 2023 22:24:13 GMT  
		Size: 865.9 KB (865851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be6f23be5f8d3623373487b0e2249a630c173aa58bf25d712a714cc66dd6c2c`  
		Last Modified: Wed, 03 May 2023 22:24:13 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31631317ae9296807ef359039e524151b249e5e4cdd9dace5bc1e62f2d7b7f7e`  
		Last Modified: Wed, 03 May 2023 22:24:14 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cea77e9be3236da8a7eaef187017822ec2b0c0189c6628247c11fdee613877`  
		Last Modified: Wed, 03 May 2023 22:24:42 GMT  
		Size: 261.0 MB (260958713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:fde78e1b857dd0e8eaad5730eb9070f507eb96961cceefb18350c5be7857a07a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322467089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2ad7027fe8ec5c14fcbf86209e7413212105cddd7554c5bef786c46867691e`
-	Default Command: `["R"]`

```dockerfile
# Wed, 03 May 2023 00:24:01 GMT
ADD file:963c63c0aac9182210ae8c781047d25685e67bae65725505733a64de642b2b38 in / 
# Wed, 03 May 2023 00:24:01 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:27:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 03 May 2023 18:27:06 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 03 May 2023 18:27:18 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:27:19 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 03 May 2023 18:27:20 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 03 May 2023 18:27:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 03 May 2023 18:27:20 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 03 May 2023 18:27:20 GMT
ENV R_BASE_VERSION=4.3.0
# Wed, 03 May 2023 18:27:21 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 03 May 2023 18:29:26 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:29:30 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bded3796ed4449fe413c08ee04196c911ef419f9e245178303b88c7351e53623`  
		Last Modified: Wed, 03 May 2023 00:28:09 GMT  
		Size: 49.3 MB (49345336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b6f0a4e7965f4daa4282697c525cf2f94ef931ec06375e3d0a848a938f9cf`  
		Last Modified: Wed, 03 May 2023 18:29:50 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc1240a92f6182bcc7a9a22055a9a515787209df0fd3321be2d5728a848861f`  
		Last Modified: Wed, 03 May 2023 18:29:50 GMT  
		Size: 25.0 MB (24984125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a96dafdc15cb45a43d69b4a0f9c77c1b1a42a229d88d992ff3c0583f37abf16`  
		Last Modified: Wed, 03 May 2023 18:29:48 GMT  
		Size: 865.8 KB (865846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5edf7ce4519e90cc593f7b0990a28029e6b2452c987973f1c233afa8ca89730`  
		Last Modified: Wed, 03 May 2023 18:29:48 GMT  
		Size: 346.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb198f907ad587babf31cc75a480cf3d4a1383a25398c1a2d4d00540ff654cbb`  
		Last Modified: Wed, 03 May 2023 18:29:48 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c541a6193af986e2e180811ebf9dd64a82182513e6211becaa8e5728cb7c33`  
		Last Modified: Wed, 03 May 2023 18:30:08 GMT  
		Size: 247.3 MB (247267784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:f84334040c57a42c4424a421fc20f673799e4b568f7a1bd74f5028a159bdb127
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339086471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedcbbf2eb9328077bfcd8e3efa357ec3cd674f00b27e3d7bd7dffd8d0a88ba`
-	Default Command: `["R"]`

```dockerfile
# Wed, 03 May 2023 00:33:35 GMT
ADD file:f54f5308138566009df9867a9e17d06810cb24a49786ebfdb8f2d83aa44bd004 in / 
# Wed, 03 May 2023 00:33:38 GMT
CMD ["bash"]
# Thu, 04 May 2023 00:52:09 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 04 May 2023 00:52:11 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 04 May 2023 00:52:37 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 00:52:42 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 04 May 2023 00:52:43 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 00:52:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 May 2023 00:52:45 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 04 May 2023 00:52:46 GMT
ENV R_BASE_VERSION=4.3.0
# Thu, 04 May 2023 00:52:48 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Thu, 04 May 2023 00:56:26 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 00:56:30 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c7778701ecf3e4c7947d5854ffadbfcc47a1bea59eeede267cc1563d0c205014`  
		Last Modified: Wed, 03 May 2023 00:38:50 GMT  
		Size: 53.3 MB (53307302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66bde9f479501a388f0b05d077e44d65524bbba1ee00f0dcbe703bad4534989`  
		Last Modified: Thu, 04 May 2023 00:56:41 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e618648d81125407cb42fcf36722736651dd097ba30c339a03bf4e9a8eb480`  
		Last Modified: Thu, 04 May 2023 00:56:43 GMT  
		Size: 25.6 MB (25560947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe19135c5349f7250145ae537652ad2d7773f5c17b239681c8e8d715b80f179`  
		Last Modified: Thu, 04 May 2023 00:56:39 GMT  
		Size: 865.9 KB (865852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b0b041784b86a1a06053e7950eaa748db7f632097dae4d8cc8cd14a8f90861`  
		Last Modified: Thu, 04 May 2023 00:56:38 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e7ee8a60f067de2ef718e7cb15b003582717cfdd918f4c54cd0ceaeac3e4a5`  
		Last Modified: Thu, 04 May 2023 00:56:38 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31d894101d3b038b49d338d7b2b136e522ad6078faf61b1460f8af4b087e93d`  
		Last Modified: Thu, 04 May 2023 00:57:33 GMT  
		Size: 259.3 MB (259348368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:74364e52d5158adf7b032915291238f40886f7b5793e0f9475b15796c74697f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297534615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a4b993911ca773cdd0bccd1fee384c7af5afe2577fd8452e89419f8504c567`
-	Default Command: `["R"]`

```dockerfile
# Wed, 03 May 2023 03:43:00 GMT
ADD file:c572e15c46e19b472f04f1dfa7a84a66dc4b542578a96178c0d56e11644d77c2 in / 
# Wed, 03 May 2023 03:43:02 GMT
CMD ["bash"]
# Wed, 03 May 2023 23:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 03 May 2023 23:07:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 03 May 2023 23:07:14 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:07:17 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 03 May 2023 23:07:17 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 03 May 2023 23:07:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 03 May 2023 23:07:17 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 03 May 2023 23:07:18 GMT
ENV R_BASE_VERSION=4.3.0
# Wed, 03 May 2023 23:07:18 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 03 May 2023 23:09:19 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:09:25 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:14c2fbffb8254eb141a0d2ee16eb3282dd281a0afa9d6aa17ba7b5020dc35812`  
		Last Modified: Wed, 03 May 2023 03:45:54 GMT  
		Size: 47.7 MB (47675930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18598ee8dbd717641d2b5d04ec5aa5d8066fad3dc4211a88194f2f2971aae1de`  
		Last Modified: Wed, 03 May 2023 23:09:45 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41756abdb1e9d3b3efa708278ef98b4d4dc454b5097af18dfdd83922ef1e103`  
		Last Modified: Wed, 03 May 2023 23:09:46 GMT  
		Size: 24.8 MB (24832327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab7bed939c5d0c665f53cab437a2c5b803e2a4981f8117b17bdaffffb533a84`  
		Last Modified: Wed, 03 May 2023 23:09:44 GMT  
		Size: 921.0 KB (921012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0835d3f5b2796f881ac88f98e741930b32962050a42412ee06760390f33ea2a`  
		Last Modified: Wed, 03 May 2023 23:09:44 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5437c2b8b2406785d01e31c6611be54bd1adfe2209b1a23a5d31a476fff1df7d`  
		Last Modified: Wed, 03 May 2023 23:09:44 GMT  
		Size: 291.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec58f390328f63ab422e0f46f384d6c0a21d01af9808e53a24c253c9f25b0c60`  
		Last Modified: Wed, 03 May 2023 23:10:08 GMT  
		Size: 224.1 MB (224101348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
