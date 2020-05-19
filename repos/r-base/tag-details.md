<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.0.0`](#r-base400)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.0.0`

```console
$ docker pull r-base@sha256:f0c764cad5eb4eb55fa1bb16b0b101812e7aea305180b5dba54b1110552681d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `r-base:4.0.0` - linux; amd64

```console
$ docker pull r-base@sha256:a77bab0b8a8375ea3d1bc431c9351d34d66e73494c27048429c33d59a58436c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325772299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1785b442d72ca0b2327c3a431d11dab3d26c664b2574af1c1dc4bb2ad13a15`
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
# Sat, 16 May 2020 02:08:42 GMT
ENV R_BASE_VERSION=4.0.0
# Sat, 16 May 2020 02:08:42 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list     && rm /etc/apt/apt.conf.d/default
# Sat, 16 May 2020 02:09:54 GMT
RUN apt-get update 	&& apt-get install -t experimental -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 02:09:54 GMT
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
	-	`sha256:32c8a75adf2b79091ad141b57980ecbc4b1195381a0cba9aacb8d6792bfd6639`  
		Last Modified: Sat, 16 May 2020 02:10:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ac8f4cc18efe873d9f1c836d638d743d8df6b7c10da8099ac03a0fde733d84`  
		Last Modified: Sat, 16 May 2020 02:11:04 GMT  
		Size: 246.2 MB (246177577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:7629aad8bf0073502aa34d0a59d6acc4cadf46b8acc90c9c1c16a07605986fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:a77bab0b8a8375ea3d1bc431c9351d34d66e73494c27048429c33d59a58436c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325772299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1785b442d72ca0b2327c3a431d11dab3d26c664b2574af1c1dc4bb2ad13a15`
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
# Sat, 16 May 2020 02:08:42 GMT
ENV R_BASE_VERSION=4.0.0
# Sat, 16 May 2020 02:08:42 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list     && rm /etc/apt/apt.conf.d/default
# Sat, 16 May 2020 02:09:54 GMT
RUN apt-get update 	&& apt-get install -t experimental -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 02:09:54 GMT
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
	-	`sha256:32c8a75adf2b79091ad141b57980ecbc4b1195381a0cba9aacb8d6792bfd6639`  
		Last Modified: Sat, 16 May 2020 02:10:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ac8f4cc18efe873d9f1c836d638d743d8df6b7c10da8099ac03a0fde733d84`  
		Last Modified: Sat, 16 May 2020 02:11:04 GMT  
		Size: 246.2 MB (246177577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:47c03229f5bce098616f12d8d9f3d0eee2cf6295b570e8da6cacd26249309f98
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286640480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd869eaf95005ddd41f48bf5931830408a0c39869c95edd33f39e96be92d438`
-	Default Command: `["R"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:29 GMT
ADD file:8d6493850808494b9c8355d7605648137017d4ab385d5f2f709e2b004ae55495 in / 
# Thu, 23 Apr 2020 00:59:37 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 09:11:44 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Thu, 23 Apr 2020 09:11:48 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Thu, 23 Apr 2020 09:12:34 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 09:12:40 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 23 Apr 2020 09:12:41 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 23 Apr 2020 09:12:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Apr 2020 09:12:44 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Thu, 23 Apr 2020 09:12:44 GMT
ENV R_BASE_VERSION=3.6.3
# Thu, 23 Apr 2020 09:14:41 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 09:14:47 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9edc88ed1cd036e1398512e49d4ca915c1b089667581f9b64036651a5c5569f8`  
		Last Modified: Thu, 23 Apr 2020 01:06:34 GMT  
		Size: 50.9 MB (50908144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4127a2cf85f285cba8b2c8607b1a93d784fde8c9c4d231b319c9e691a807c4c`  
		Last Modified: Thu, 23 Apr 2020 09:15:07 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a10dcfa11c3feca2751726cf7a0b686e0a2f55779703b02a242ed61b498c38`  
		Last Modified: Thu, 23 Apr 2020 09:15:12 GMT  
		Size: 27.2 MB (27176294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e500848c9067a4f5dbdaf07d4ac207fbc4753e925a3703a201f47e6a6ccc9e`  
		Last Modified: Thu, 23 Apr 2020 09:15:07 GMT  
		Size: 863.4 KB (863390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb0b0f0f38635f33ba64df99fc1194fc2561f9152ac1fd07864d9498dd06ab`  
		Last Modified: Thu, 23 Apr 2020 09:15:07 GMT  
		Size: 299.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908d194086f1b53439bc15f001881e7e91974241220b5714fb707c77b8b9d25c`  
		Last Modified: Thu, 23 Apr 2020 09:15:54 GMT  
		Size: 207.7 MB (207690467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
