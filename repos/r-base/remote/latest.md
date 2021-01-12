## `r-base:latest`

```console
$ docker pull r-base@sha256:48ac678d94655687624f1d42d1fda3d418db0af26c597c938a6e46c3912f4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:013a57208c0f594cf8dd3a77231c9d21ec0e73c41917e473ca6f27d975d0b2a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326307092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46153a29f5298d9b235bf41e30fdf0b2c8645533e1e7df4673be61ad57da319`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:33 GMT
ADD file:ec3a8744e6d19825f056cd444a8fc650e7f8f9a94a6c88884237da472b219fd6 in / 
# Tue, 12 Jan 2021 00:35:33 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 18:48:09 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Jan 2021 18:48:11 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 12 Jan 2021 18:48:26 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 18:48:31 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Jan 2021 18:48:31 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Jan 2021 18:48:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Jan 2021 18:48:33 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Jan 2021 18:48:34 GMT
ENV R_BASE_VERSION=4.0.3
# Tue, 12 Jan 2021 18:49:53 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 18:49:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6699a6ece22e14f81c71026455810d95b56a6dd5c0812217320f30bf1b4bd75c`  
		Last Modified: Tue, 12 Jan 2021 00:43:46 GMT  
		Size: 53.6 MB (53566282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bc959df2e0e5e8c0a6b3f5f1d294daa24bf959eff57b11899d2c5d099cb266`  
		Last Modified: Tue, 12 Jan 2021 18:50:20 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788c4063177bcd5b97525d0e80de069acefc9665d2f582fc6def555ed126a4cf`  
		Last Modified: Tue, 12 Jan 2021 18:50:26 GMT  
		Size: 27.5 MB (27504858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff6cc5b5b8014b403dd778fd85d2a2962dda65c5d5575ab96238ff13e74b7ae`  
		Last Modified: Tue, 12 Jan 2021 18:50:27 GMT  
		Size: 864.6 KB (864590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ae1b23c4e4b7bd908b0bb3150b2c4a22109920ddcb3d59f047df85fda9c348`  
		Last Modified: Tue, 12 Jan 2021 18:50:18 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cfccf269579f235b81d291ac0b5cac2f205a6ef6310def7a5f0ae0df277dd7`  
		Last Modified: Tue, 12 Jan 2021 18:51:06 GMT  
		Size: 244.4 MB (244369165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:e31a075cbeb0256a4fe2e669949f3992abec2d7cd97bec2912751255f1587472
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313958566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d932921ca97dde580761916f9ac239a3a10b27e10931d257aeaefecba12b40`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Jan 2021 00:46:23 GMT
ADD file:48fbb35da8de6ff711480aa027f137139f79e852973afb58dea3460bf0283006 in / 
# Tue, 12 Jan 2021 00:46:35 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 15:22:18 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Jan 2021 15:22:21 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 12 Jan 2021 15:23:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 15:23:10 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Jan 2021 15:23:11 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Jan 2021 15:23:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Jan 2021 15:23:14 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Jan 2021 15:23:15 GMT
ENV R_BASE_VERSION=4.0.3
# Tue, 12 Jan 2021 15:27:05 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 15:27:13 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f37f58c0cf881aabae111871e3d6ad56dbcda59b0d0d2705993a3166055432e2`  
		Last Modified: Tue, 12 Jan 2021 00:55:48 GMT  
		Size: 52.4 MB (52428385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b793f7620b8cdda19e82994b6ee67d1d5fad6f3fbcc64e8a176ea2304b8bf8`  
		Last Modified: Tue, 12 Jan 2021 15:27:31 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e626d2e32874b67a52ff73cea3640e1ba344c5550b0f7c9ec8a46fdd44468e9`  
		Last Modified: Tue, 12 Jan 2021 15:27:38 GMT  
		Size: 27.4 MB (27354395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f134905dea39aa262760fedd4c6359822954642fdfe0b1f7bf5167c99463e6c8`  
		Last Modified: Tue, 12 Jan 2021 15:27:32 GMT  
		Size: 864.6 KB (864593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84722b1ad051355487f597d47f73dc00327312195204ec6b51ef0610b4fe1fa4`  
		Last Modified: Tue, 12 Jan 2021 15:27:32 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b560dbef9e322244c6b63a27b699e51cabbb6a47ee9a1de809ca2e7092562bc6`  
		Last Modified: Tue, 12 Jan 2021 15:28:23 GMT  
		Size: 233.3 MB (233308961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:139d4698204b39dd9f33be02e2dac63a5bc88dffc679357d3a5c457c929de863
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324529438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a24688a5bbb3249b725ca6d38eb2329c1c2d8e89f301b09763e020635734c1`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Jan 2021 00:28:12 GMT
ADD file:7c5aef981ec69d203ed3041958d604b3c221d38286982325e933a4aea004fd00 in / 
# Tue, 12 Jan 2021 00:28:23 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 12:54:51 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Jan 2021 12:55:22 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 12 Jan 2021 12:56:58 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 12:57:17 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Jan 2021 12:57:24 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Jan 2021 12:57:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Jan 2021 12:57:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Jan 2021 12:57:49 GMT
ENV R_BASE_VERSION=4.0.3
# Tue, 12 Jan 2021 13:09:41 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 13:09:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6168374c1cd1389f3d510ecd4c9bd0520534b68b8f0f32d0479e4fa2e3e9d69e`  
		Last Modified: Tue, 12 Jan 2021 00:36:39 GMT  
		Size: 57.6 MB (57562274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a18c049e4f1d3122ce4fcc8aa472880ed62bdb9c30004e3220a381156bafb4`  
		Last Modified: Tue, 12 Jan 2021 13:10:13 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15505cef7e245a6456323c3f6293294160de098922762dfca14350f289538bb`  
		Last Modified: Tue, 12 Jan 2021 13:10:17 GMT  
		Size: 27.8 MB (27794114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231bf04f1dee3c8e578421445abca648fa407871cac53d09b21d11f112f165f3`  
		Last Modified: Tue, 12 Jan 2021 13:10:13 GMT  
		Size: 864.6 KB (864592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333fae2e7ae74eb979d942af51c586744886d092384d423f8ab90339254a73d0`  
		Last Modified: Tue, 12 Jan 2021 13:10:13 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c678d06179ba47f5b8e2aa668d8498f0b99941c3cc2f44f215f76a415575d5`  
		Last Modified: Tue, 12 Jan 2021 13:10:52 GMT  
		Size: 238.3 MB (238306202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:fa199886bedfdb7388dd4f993b9c2365937bc62a6a704084c30d2051ec81d68b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291817775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce25e85e3805bebfa4d2ef0e687b732eec3d60c87d6211be5ec49126d59e377b`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Jan 2021 00:43:20 GMT
ADD file:79d77ce0e127a883c7393aaca5f89cab2b36703e9d08104596c40e09674d59f1 in / 
# Tue, 12 Jan 2021 00:43:23 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:58:19 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Jan 2021 02:58:20 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 12 Jan 2021 02:58:32 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:58:35 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Jan 2021 02:58:35 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Jan 2021 02:58:35 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Jan 2021 02:58:36 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Jan 2021 02:58:37 GMT
ENV R_BASE_VERSION=4.0.3
# Tue, 12 Jan 2021 03:00:10 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:00:33 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:deacf9aa62ade6e1002e481ea38b97d12b800eae2cb010989bdf011c18c51650`  
		Last Modified: Tue, 12 Jan 2021 01:01:15 GMT  
		Size: 52.1 MB (52108018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beb7061eb3cbd983566deb7ffcce8dfdee9d022ba267c60e74d01d1c07906f2`  
		Last Modified: Tue, 12 Jan 2021 03:01:08 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc4dd911ad9cd61fcfa326a909b3d2c7b7bc5d0cd09b5be9a12606b3cd28df2`  
		Last Modified: Tue, 12 Jan 2021 03:01:09 GMT  
		Size: 27.2 MB (27202505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38cfc05f022a4702289843696fe5120b243eca1cc6db91dfe4e2f23f0cedd7f`  
		Last Modified: Tue, 12 Jan 2021 03:01:09 GMT  
		Size: 920.2 KB (920163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84133159b6c7664a09dc38a73f778bddcf71f8da27f6462c4780fe9a73a37669`  
		Last Modified: Tue, 12 Jan 2021 03:01:08 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a5d757409c836febb87e4a55b9c3e34af980cc36dd4726503c943f9c7ab18c`  
		Last Modified: Tue, 12 Jan 2021 03:01:32 GMT  
		Size: 211.6 MB (211584860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
