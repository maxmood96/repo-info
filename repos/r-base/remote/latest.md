## `r-base:latest`

```console
$ docker pull r-base@sha256:56d20a04e8d162b68f93cb5b1a252ddfaff25da2d4ee730dcf07a8bf1e59f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:fa178dc85c3eb4a4871a7daad3c4e89c602997c550b47baa98fa1d26a14988c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303161724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0836c59d7d075653c7dc6666ada9f10e54ed39d1ae56cd8981fc5c6f4a858e62`
-	Default Command: `["R"]`

```dockerfile
# Fri, 15 May 2020 06:34:02 GMT
ADD file:c41a0865e07732f39eac6e95bce852221ac58f789ea781bbeff5b6416bc468f5 in / 
# Fri, 15 May 2020 06:34:03 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:08:23 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Sat, 16 May 2020 02:08:24 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sat, 16 May 2020 02:08:37 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 02:08:40 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 16 May 2020 02:08:40 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 16 May 2020 02:08:40 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 May 2020 02:08:41 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Mon, 08 Jun 2020 18:20:33 GMT
ENV R_BASE_VERSION=4.0.1
# Mon, 08 Jun 2020 18:21:22 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends                 gcc-9-base 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Mon, 08 Jun 2020 18:21:23 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6ba462f539c181ddb608207b74df288fff28dc61404be8bafe0a5f2744c0c743`  
		Last Modified: Fri, 15 May 2020 06:40:58 GMT  
		Size: 51.4 MB (51391137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5c0df656397793dd5751eba6e530bbc06c24a3acddad167faa9500463e69a8`  
		Last Modified: Sat, 16 May 2020 02:10:13 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90624a13808b54c1952d7570f551011d554d5dcc8a23f747aefbe14c0836eb01`  
		Last Modified: Sat, 16 May 2020 02:10:16 GMT  
		Size: 27.3 MB (27337717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de46b85c477ac212b2b4a5ced5df4616a23c00f65c46d038f24f8eb57a905a36`  
		Last Modified: Sat, 16 May 2020 02:10:12 GMT  
		Size: 863.4 KB (863392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d6bab95ae5e8d07f11ff7ed748da87e592428bdde97056f0e9a35b1438e8d1`  
		Last Modified: Sat, 16 May 2020 02:10:11 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ddcb7376ee7d789c7d57394949832135a0dce4f52fb4fcc5a91788cd66d653`  
		Last Modified: Mon, 08 Jun 2020 18:25:38 GMT  
		Size: 223.6 MB (223567340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:c310a29df9f5ddb2f151652c44a102bb9da357c5c09d8b764ec340a20461bea5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292775801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec044253d58d42bdab72fb17aaf4795be59f1836ce75e85b0df936fb0f2683e7`
-	Default Command: `["R"]`

```dockerfile
# Fri, 15 May 2020 12:49:17 GMT
ADD file:bb95bd77704fc5ce5b21931cb334c3bed5ef199d870958f45d51fca1f7ef5507 in / 
# Fri, 15 May 2020 12:49:21 GMT
CMD ["bash"]
# Wed, 20 May 2020 23:31:26 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 20 May 2020 23:31:32 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 20 May 2020 23:32:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 May 2020 23:32:16 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 20 May 2020 23:32:17 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 20 May 2020 23:32:19 GMT
ENV LANG=en_US.UTF-8
# Wed, 20 May 2020 23:32:22 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Mon, 08 Jun 2020 18:40:25 GMT
ENV R_BASE_VERSION=4.0.1
# Mon, 08 Jun 2020 18:42:37 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends                 gcc-9-base 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Mon, 08 Jun 2020 18:42:41 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:07fe8f6133e43947178b01cc2dac0fb6f8e3d007776c62bb2fd90b72ef150789`  
		Last Modified: Fri, 15 May 2020 12:56:20 GMT  
		Size: 50.3 MB (50329002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbdca5aa956482e87f5b395b3bb19fcd372fc07de23ccbe6e9436bf4904f2af`  
		Last Modified: Wed, 20 May 2020 23:35:07 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c219446d0d16dd62835ddc22d00065e55f511d88a59031700779888efc25704`  
		Last Modified: Wed, 20 May 2020 23:35:15 GMT  
		Size: 27.2 MB (27205415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafba0d1879c946554a1e15c982de05ae1584a70f5b65b937218dfebe113624`  
		Last Modified: Wed, 20 May 2020 23:35:08 GMT  
		Size: 863.4 KB (863397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e996a698fde87b2526734e4a9b40257096dc69d06df3749f0bc61406b47e6d`  
		Last Modified: Wed, 20 May 2020 23:35:07 GMT  
		Size: 299.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d653fed26620678cd87f6fd2fe34ba77c9ad42f1ba56f8b4ed4c93bfaf712c4a`  
		Last Modified: Mon, 08 Jun 2020 18:43:47 GMT  
		Size: 214.4 MB (214375804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
