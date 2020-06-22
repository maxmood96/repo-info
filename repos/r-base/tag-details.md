<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.0.2`](#r-base402)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.0.2`

```console
$ docker pull r-base@sha256:039e677fc531aed856df47ca8ab40e7ea454493b0b15fbf38e1143f865347dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `r-base:4.0.2` - linux; amd64

```console
$ docker pull r-base@sha256:5f5cdb7ae769411227be584403f929a35d2371f287a4612fc73b620447097673
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324169884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c050954e1f03f86d1fc0bca2e94eb122735f0b59a5804251501b9a79ab1c39`
-	Default Command: `["R"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:49 GMT
ADD file:63ef8f38bb25d9c0e944d04e91b6d6c6eb32289709829d3bb80998e94ff2a506 in / 
# Tue, 09 Jun 2020 01:23:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:53:26 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Jun 2020 16:53:26 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 09 Jun 2020 16:53:36 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:53:39 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 09 Jun 2020 16:53:39 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 09 Jun 2020 16:53:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2020 16:53:40 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Mon, 22 Jun 2020 19:41:17 GMT
ENV R_BASE_VERSION=4.0.2
# Mon, 22 Jun 2020 19:42:17 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Mon, 22 Jun 2020 19:42:18 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0ab9185ddfe50c951de582032c5e29e21a851a328056e6bee6299e0ff55ec807`  
		Last Modified: Tue, 09 Jun 2020 01:28:27 GMT  
		Size: 51.4 MB (51413498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe522cb8773f50b648207a771978f0815a06186e0161550134a9f1d0de90b7c`  
		Last Modified: Tue, 09 Jun 2020 16:54:45 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eab703bf1e186115f3189a1eea62e8e6aa53fa0db81fb1ca2bcf78b43078b6`  
		Last Modified: Tue, 09 Jun 2020 16:54:50 GMT  
		Size: 27.3 MB (27340715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea3885c55a302cb44bfb5e9e1d1779665790f28bbcf6bcd796d97becd8df4e7`  
		Last Modified: Tue, 09 Jun 2020 16:54:45 GMT  
		Size: 863.4 KB (863390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617ce4a72943a95a48c077b1d62af317e3a71a25d277d4ace5cd6a1de6b33c81`  
		Last Modified: Tue, 09 Jun 2020 16:54:45 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f33388c070574c387b5090875820c0c97e4e21902d829bb571efbded7a8f76a`  
		Last Modified: Mon, 22 Jun 2020 19:43:01 GMT  
		Size: 244.6 MB (244550143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:55ddef85481c0a0232765ef7c3bbbb7d6eec6ee2d4928aa120cbfc5959c93596
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d949262030c2220466323153b70428dea45f3f19db8fe87a6beece59a056e42`
-	Default Command: `["R"]`

```dockerfile
# Tue, 09 Jun 2020 01:55:08 GMT
ADD file:3705d77b7f9ddcac964099514289de1ff74f3618435e1c0846d112f5075abfae in / 
# Tue, 09 Jun 2020 01:55:11 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:21:22 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Jun 2020 04:21:25 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 09 Jun 2020 04:21:47 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:21:55 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 09 Jun 2020 04:21:56 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 09 Jun 2020 04:21:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2020 04:21:59 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Mon, 22 Jun 2020 20:13:12 GMT
ENV R_BASE_VERSION=4.0.2
# Mon, 22 Jun 2020 20:15:23 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Mon, 22 Jun 2020 20:15:27 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a2b4880979f186e2b0fb3aceb4435b72654989a46906ae64e190d06c969f2926`  
		Last Modified: Tue, 09 Jun 2020 02:00:48 GMT  
		Size: 50.4 MB (50353822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783b3c4723c1792fe2ea047df23720951cdd4586b19f8756a99ea66454d2c4e`  
		Last Modified: Tue, 09 Jun 2020 04:24:03 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d932b1fde92845f1962ac0c0a0c20f619e7c82a688c4653eeb4121f7a0e1f94c`  
		Last Modified: Tue, 09 Jun 2020 04:24:10 GMT  
		Size: 27.2 MB (27206094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca4df11ef3ca50a8d31123fe13b77a4718003e0e640256b4997d90cf4289f80`  
		Last Modified: Tue, 09 Jun 2020 04:24:03 GMT  
		Size: 863.4 KB (863381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a724903da064e59ae94dd3780e483c073274509cfdbd71140ac29557564c726`  
		Last Modified: Tue, 09 Jun 2020 04:24:02 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475943a23e0f73f1eabbe27aeffe59b73e1b332944d76802e23aa32ea841704d`  
		Last Modified: Mon, 22 Jun 2020 20:16:41 GMT  
		Size: 225.4 MB (225420487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:039e677fc531aed856df47ca8ab40e7ea454493b0b15fbf38e1143f865347dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:5f5cdb7ae769411227be584403f929a35d2371f287a4612fc73b620447097673
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324169884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c050954e1f03f86d1fc0bca2e94eb122735f0b59a5804251501b9a79ab1c39`
-	Default Command: `["R"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:49 GMT
ADD file:63ef8f38bb25d9c0e944d04e91b6d6c6eb32289709829d3bb80998e94ff2a506 in / 
# Tue, 09 Jun 2020 01:23:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:53:26 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Jun 2020 16:53:26 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 09 Jun 2020 16:53:36 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:53:39 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 09 Jun 2020 16:53:39 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 09 Jun 2020 16:53:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2020 16:53:40 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Mon, 22 Jun 2020 19:41:17 GMT
ENV R_BASE_VERSION=4.0.2
# Mon, 22 Jun 2020 19:42:17 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Mon, 22 Jun 2020 19:42:18 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0ab9185ddfe50c951de582032c5e29e21a851a328056e6bee6299e0ff55ec807`  
		Last Modified: Tue, 09 Jun 2020 01:28:27 GMT  
		Size: 51.4 MB (51413498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe522cb8773f50b648207a771978f0815a06186e0161550134a9f1d0de90b7c`  
		Last Modified: Tue, 09 Jun 2020 16:54:45 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eab703bf1e186115f3189a1eea62e8e6aa53fa0db81fb1ca2bcf78b43078b6`  
		Last Modified: Tue, 09 Jun 2020 16:54:50 GMT  
		Size: 27.3 MB (27340715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea3885c55a302cb44bfb5e9e1d1779665790f28bbcf6bcd796d97becd8df4e7`  
		Last Modified: Tue, 09 Jun 2020 16:54:45 GMT  
		Size: 863.4 KB (863390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617ce4a72943a95a48c077b1d62af317e3a71a25d277d4ace5cd6a1de6b33c81`  
		Last Modified: Tue, 09 Jun 2020 16:54:45 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f33388c070574c387b5090875820c0c97e4e21902d829bb571efbded7a8f76a`  
		Last Modified: Mon, 22 Jun 2020 19:43:01 GMT  
		Size: 244.6 MB (244550143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:55ddef85481c0a0232765ef7c3bbbb7d6eec6ee2d4928aa120cbfc5959c93596
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d949262030c2220466323153b70428dea45f3f19db8fe87a6beece59a056e42`
-	Default Command: `["R"]`

```dockerfile
# Tue, 09 Jun 2020 01:55:08 GMT
ADD file:3705d77b7f9ddcac964099514289de1ff74f3618435e1c0846d112f5075abfae in / 
# Tue, 09 Jun 2020 01:55:11 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:21:22 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Jun 2020 04:21:25 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 09 Jun 2020 04:21:47 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:21:55 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 09 Jun 2020 04:21:56 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 09 Jun 2020 04:21:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2020 04:21:59 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Mon, 22 Jun 2020 20:13:12 GMT
ENV R_BASE_VERSION=4.0.2
# Mon, 22 Jun 2020 20:15:23 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Mon, 22 Jun 2020 20:15:27 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a2b4880979f186e2b0fb3aceb4435b72654989a46906ae64e190d06c969f2926`  
		Last Modified: Tue, 09 Jun 2020 02:00:48 GMT  
		Size: 50.4 MB (50353822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783b3c4723c1792fe2ea047df23720951cdd4586b19f8756a99ea66454d2c4e`  
		Last Modified: Tue, 09 Jun 2020 04:24:03 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d932b1fde92845f1962ac0c0a0c20f619e7c82a688c4653eeb4121f7a0e1f94c`  
		Last Modified: Tue, 09 Jun 2020 04:24:10 GMT  
		Size: 27.2 MB (27206094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca4df11ef3ca50a8d31123fe13b77a4718003e0e640256b4997d90cf4289f80`  
		Last Modified: Tue, 09 Jun 2020 04:24:03 GMT  
		Size: 863.4 KB (863381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a724903da064e59ae94dd3780e483c073274509cfdbd71140ac29557564c726`  
		Last Modified: Tue, 09 Jun 2020 04:24:02 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475943a23e0f73f1eabbe27aeffe59b73e1b332944d76802e23aa32ea841704d`  
		Last Modified: Mon, 22 Jun 2020 20:16:41 GMT  
		Size: 225.4 MB (225420487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
