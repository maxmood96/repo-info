<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.5.2`](#r-base452)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.5.2`

```console
$ docker pull r-base@sha256:ef384c978485e7b4b1ae26b9309a091152c273c89f31c467fb4c9eb5f53dcb4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `r-base:4.5.2` - linux; amd64

```console
$ docker pull r-base@sha256:8eb4f85ad14880de972db0aeec37d722461f111edaf360a58e03e9bb6d8d7037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384549136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02485e698d2e8875afd909f0b1b629888661efcf230354fdd65b5255ec4c234`
-	Default Command: `["R"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 23:04:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Mon, 08 Dec 2025 23:04:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Mon, 08 Dec 2025 23:04:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:04:51 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Mon, 08 Dec 2025 23:04:51 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 08 Dec 2025 23:04:51 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 23:04:51 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Mon, 08 Dec 2025 23:04:51 GMT
ENV R_BASE_VERSION=4.5.2
# Mon, 08 Dec 2025 23:05:35 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:35 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d07e7493d30660e90d785732f6efa7dbc2cb9ffe13064e2383c3338b574466d9`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 48.5 MB (48512513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4063caaf49a312ad9cc846024ac33af0069c507e893fa448c5b070681db45ce`  
		Last Modified: Mon, 08 Dec 2025 23:06:25 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de36adf48bc1301828f9a400ce0c5c0227b0b81e959fa0a349033ddc712f62c`  
		Last Modified: Mon, 08 Dec 2025 23:06:27 GMT  
		Size: 27.0 MB (26994970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fa3379d0a81dc7185db193422a29ffefc9171594ba821570b2e85683e79c67`  
		Last Modified: Mon, 08 Dec 2025 23:06:25 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6726f43cd8522cda2f81fc746a0dce9d34d57a9dca852d2bee0479c91c0ea237`  
		Last Modified: Mon, 08 Dec 2025 23:06:25 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5003a381326ad66e999c998e8010f95667841750f1eead8d9de641c044fa17`  
		Last Modified: Mon, 08 Dec 2025 23:06:36 GMT  
		Size: 308.2 MB (308169508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:f007a127806cb5c702ce685cc1ea3de894ae0a0ffb0ea282ab6546565a3f604e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12974140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f544a48419b312442aa4751d5d3d82dee651d8bbb32c9a177239e49ff65a8d`

```dockerfile
```

-	Layers:
	-	`sha256:986cb6f9304083f2623e274010470a9a2e51e03e2fac378df09b566d0c99bfce`  
		Last Modified: Tue, 09 Dec 2025 01:14:05 GMT  
		Size: 13.0 MB (12956042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6293866d45a29a55a4438cbc536198c893e57e7bfc2d215158c8f45e349c57af`  
		Last Modified: Tue, 09 Dec 2025 01:14:06 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:5c8815cb39c3d94101091cbefd899ab15a357566263df04ceb41412d2f94d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365567266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c35a3eb38919959c025ccc212ffb037fc36a94346d68a76b205684dfa92d5c9`
-	Default Command: `["R"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 23:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Mon, 08 Dec 2025 23:07:31 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Mon, 08 Dec 2025 23:07:39 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:07:41 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Mon, 08 Dec 2025 23:07:41 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 08 Dec 2025 23:07:41 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 23:07:41 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Mon, 08 Dec 2025 23:07:41 GMT
ENV R_BASE_VERSION=4.5.2
# Mon, 08 Dec 2025 23:08:28 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:980892eaed7a52ea486458964bd611659e21bc061abbc845e2c0e0044e32f492`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 48.6 MB (48599339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9583f8f5e499d471da74bcdfd438f896f2a2c3b60151dd8d0886bf7ed01d47d4`  
		Last Modified: Mon, 08 Dec 2025 23:09:25 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b52bb93b89e353592c0553b461f90ece3e4dcef112cd35828a2e57199d296da`  
		Last Modified: Mon, 08 Dec 2025 23:09:30 GMT  
		Size: 26.9 MB (26850226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20f266859d2325a9a36522c6b2ed4ecaa8012147598b16c938246440a450796`  
		Last Modified: Mon, 08 Dec 2025 23:09:26 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111428ae8986683d8647ba108400092f32ea7acfbc4231579b17b42cdc4db260`  
		Last Modified: Mon, 08 Dec 2025 23:09:26 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc9b446eaae0c6d6179d3e7dc9a034b4910a56050c8d68f90ad230e21f83f4b`  
		Last Modified: Mon, 08 Dec 2025 23:09:53 GMT  
		Size: 289.2 MB (289245560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:b71f3b307f755497152112a19c2d78ad287e6327d81edac6f08ccf6ee83f734b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13063387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e5b483283d02dd823dcab89afd3aac6e90885af7a2a06437289451f6ac3763`

```dockerfile
```

-	Layers:
	-	`sha256:ae843fcd9cdd6808bafd78ba0f70299f5089a49e35e1d5a5c565c5ab02eabb29`  
		Last Modified: Tue, 09 Dec 2025 01:14:16 GMT  
		Size: 13.0 MB (13045149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ddffb3059cabfad4c5a8df6a7aee5a08c36c2bf4539170066ddfb169f80de1`  
		Last Modified: Tue, 09 Dec 2025 01:14:16 GMT  
		Size: 18.2 KB (18238 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:09b8f0ed4a2e78657ec4fd9979e841ba1b18e4fe11b765c7ec22708eaa608e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 MB (376990240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1782b21a3c30ab21763349e9a358260ec1a66162ed8cf8ec6ebfb45836971e89`
-	Default Command: `["R"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1765152000'
# Tue, 09 Dec 2025 14:12:30 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Dec 2025 14:12:30 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 09 Dec 2025 14:12:57 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:12:59 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 09 Dec 2025 14:12:59 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 09 Dec 2025 14:12:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Dec 2025 14:13:00 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 09 Dec 2025 14:13:00 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 09 Dec 2025 14:15:36 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:15:36 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c77c02bf0ec741c5e6279842de5ec989f964c7c81eeb1105d5fbd8ab26246bd0`  
		Last Modified: Tue, 09 Dec 2025 09:18:56 GMT  
		Size: 53.4 MB (53413788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1f165120af8f32e56369dd716d78674f173c1eb15914c7f931d6e61472f7bd`  
		Last Modified: Tue, 09 Dec 2025 14:17:21 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e814f0efec36b941f47937fc1cf4d98cfb365170b1c19a6df00f0afe5d3840`  
		Last Modified: Tue, 09 Dec 2025 14:17:23 GMT  
		Size: 27.3 MB (27281358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd865361ba48ccf6a6e83969fcede89fca724083ecb701ff8ff17584fe5a6c55`  
		Last Modified: Tue, 09 Dec 2025 14:17:21 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f93d1858c8451812a691860fdedf978f7f145d3c3a1c6ef0c24449f9252933d`  
		Last Modified: Tue, 09 Dec 2025 14:17:21 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62239fd20b66a015e3626e9521b02553d33a87ad8b656764651041ba83d19dfa`  
		Last Modified: Tue, 09 Dec 2025 14:17:33 GMT  
		Size: 295.4 MB (295422944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:4bf01bf4af4608bd18b72ad3925bee678c98290cd48bb8d3588265da7fe3d68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12958736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c42607dfc658d76983d987ef1cdff922cc055376009df485422f1f900e8a9b`

```dockerfile
```

-	Layers:
	-	`sha256:ef9f9394f6236dfd480ba9c7ac8887dd0879cc088de8922223b4ca797ac1aaa1`  
		Last Modified: Tue, 09 Dec 2025 16:13:46 GMT  
		Size: 12.9 MB (12940598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e02c608cad9ffc2cef988f184c03576f750672f5057c0a951bfc5958a84bf2df`  
		Last Modified: Tue, 09 Dec 2025 16:13:47 GMT  
		Size: 18.1 KB (18138 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; s390x

```console
$ docker pull r-base@sha256:43e69fbc63a18227caa005921474265d2e7040c54219368db30cbc7ebd7bc434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343380310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f1032d19e6c30c497d89bdb5f502d1d1141e7f107e5d96eaf97c6a80175978`
-	Default Command: `["R"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1765152000'
# Tue, 09 Dec 2025 12:09:56 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Dec 2025 12:09:56 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 09 Dec 2025 12:10:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 12:10:07 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 09 Dec 2025 12:10:07 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 09 Dec 2025 12:10:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Dec 2025 12:10:07 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 09 Dec 2025 12:10:07 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 09 Dec 2025 12:10:56 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 12:10:56 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6ad4d5a8b1668f11bbabc575605b837454e88e85306364c279679a1eb23d3849`  
		Last Modified: Tue, 09 Dec 2025 11:11:10 GMT  
		Size: 48.3 MB (48319839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cb1340c75993f221586fdfe645a5e8f4b742a0303f9f6eee3738ff5261e642`  
		Last Modified: Tue, 09 Dec 2025 12:12:18 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6746bd6cb686df283d04b8dffd03eb92841a3f6f8f2d12a8b1400db08b23fe`  
		Last Modified: Tue, 09 Dec 2025 12:12:19 GMT  
		Size: 26.9 MB (26940796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2488a1e2b5cfc0ff6ea1814ae888117beb5be05025e8e99f945cd1a52aaceca`  
		Last Modified: Tue, 09 Dec 2025 12:12:18 GMT  
		Size: 924.5 KB (924545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994c3a889e04b8c714cd3fabab933f4abefd1baa8beef332cc41fd57735508bb`  
		Last Modified: Tue, 09 Dec 2025 12:12:18 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d73910e554c070cf1fc820ab28d06fafb973e913a65c89aed6d201a8d6ecc7`  
		Last Modified: Tue, 09 Dec 2025 12:12:24 GMT  
		Size: 267.2 MB (267191466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:28f45dbb04bfa7537b9e574e072d38c5df754e8f9260682bbe27613d302e0c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12764081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cff3f18f1b2a5f0a30ae06a0850d78eb4f6292d37c3aa3d25a7fbf71f2f1d4`

```dockerfile
```

-	Layers:
	-	`sha256:75e53dec4319bc558ab8a6fa7b065f1b69ae45b68594d6e70684b26df25f9723`  
		Last Modified: Tue, 09 Dec 2025 13:13:47 GMT  
		Size: 12.7 MB (12745983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d82a5e1ca8ca6a52b4b4e5b28013accfe71e603c88be14d9fb9decda627feb87`  
		Last Modified: Tue, 09 Dec 2025 13:13:54 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:ef384c978485e7b4b1ae26b9309a091152c273c89f31c467fb4c9eb5f53dcb4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:8eb4f85ad14880de972db0aeec37d722461f111edaf360a58e03e9bb6d8d7037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384549136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02485e698d2e8875afd909f0b1b629888661efcf230354fdd65b5255ec4c234`
-	Default Command: `["R"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 23:04:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Mon, 08 Dec 2025 23:04:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Mon, 08 Dec 2025 23:04:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:04:51 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Mon, 08 Dec 2025 23:04:51 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 08 Dec 2025 23:04:51 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 23:04:51 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Mon, 08 Dec 2025 23:04:51 GMT
ENV R_BASE_VERSION=4.5.2
# Mon, 08 Dec 2025 23:05:35 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:35 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d07e7493d30660e90d785732f6efa7dbc2cb9ffe13064e2383c3338b574466d9`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 48.5 MB (48512513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4063caaf49a312ad9cc846024ac33af0069c507e893fa448c5b070681db45ce`  
		Last Modified: Mon, 08 Dec 2025 23:06:25 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de36adf48bc1301828f9a400ce0c5c0227b0b81e959fa0a349033ddc712f62c`  
		Last Modified: Mon, 08 Dec 2025 23:06:27 GMT  
		Size: 27.0 MB (26994970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fa3379d0a81dc7185db193422a29ffefc9171594ba821570b2e85683e79c67`  
		Last Modified: Mon, 08 Dec 2025 23:06:25 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6726f43cd8522cda2f81fc746a0dce9d34d57a9dca852d2bee0479c91c0ea237`  
		Last Modified: Mon, 08 Dec 2025 23:06:25 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5003a381326ad66e999c998e8010f95667841750f1eead8d9de641c044fa17`  
		Last Modified: Mon, 08 Dec 2025 23:06:36 GMT  
		Size: 308.2 MB (308169508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f007a127806cb5c702ce685cc1ea3de894ae0a0ffb0ea282ab6546565a3f604e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12974140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f544a48419b312442aa4751d5d3d82dee651d8bbb32c9a177239e49ff65a8d`

```dockerfile
```

-	Layers:
	-	`sha256:986cb6f9304083f2623e274010470a9a2e51e03e2fac378df09b566d0c99bfce`  
		Last Modified: Tue, 09 Dec 2025 01:14:05 GMT  
		Size: 13.0 MB (12956042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6293866d45a29a55a4438cbc536198c893e57e7bfc2d215158c8f45e349c57af`  
		Last Modified: Tue, 09 Dec 2025 01:14:06 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:5c8815cb39c3d94101091cbefd899ab15a357566263df04ceb41412d2f94d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365567266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c35a3eb38919959c025ccc212ffb037fc36a94346d68a76b205684dfa92d5c9`
-	Default Command: `["R"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 23:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Mon, 08 Dec 2025 23:07:31 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Mon, 08 Dec 2025 23:07:39 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:07:41 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Mon, 08 Dec 2025 23:07:41 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 08 Dec 2025 23:07:41 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 23:07:41 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Mon, 08 Dec 2025 23:07:41 GMT
ENV R_BASE_VERSION=4.5.2
# Mon, 08 Dec 2025 23:08:28 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:980892eaed7a52ea486458964bd611659e21bc061abbc845e2c0e0044e32f492`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 48.6 MB (48599339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9583f8f5e499d471da74bcdfd438f896f2a2c3b60151dd8d0886bf7ed01d47d4`  
		Last Modified: Mon, 08 Dec 2025 23:09:25 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b52bb93b89e353592c0553b461f90ece3e4dcef112cd35828a2e57199d296da`  
		Last Modified: Mon, 08 Dec 2025 23:09:30 GMT  
		Size: 26.9 MB (26850226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20f266859d2325a9a36522c6b2ed4ecaa8012147598b16c938246440a450796`  
		Last Modified: Mon, 08 Dec 2025 23:09:26 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111428ae8986683d8647ba108400092f32ea7acfbc4231579b17b42cdc4db260`  
		Last Modified: Mon, 08 Dec 2025 23:09:26 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc9b446eaae0c6d6179d3e7dc9a034b4910a56050c8d68f90ad230e21f83f4b`  
		Last Modified: Mon, 08 Dec 2025 23:09:53 GMT  
		Size: 289.2 MB (289245560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:b71f3b307f755497152112a19c2d78ad287e6327d81edac6f08ccf6ee83f734b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13063387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e5b483283d02dd823dcab89afd3aac6e90885af7a2a06437289451f6ac3763`

```dockerfile
```

-	Layers:
	-	`sha256:ae843fcd9cdd6808bafd78ba0f70299f5089a49e35e1d5a5c565c5ab02eabb29`  
		Last Modified: Tue, 09 Dec 2025 01:14:16 GMT  
		Size: 13.0 MB (13045149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ddffb3059cabfad4c5a8df6a7aee5a08c36c2bf4539170066ddfb169f80de1`  
		Last Modified: Tue, 09 Dec 2025 01:14:16 GMT  
		Size: 18.2 KB (18238 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:09b8f0ed4a2e78657ec4fd9979e841ba1b18e4fe11b765c7ec22708eaa608e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 MB (376990240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1782b21a3c30ab21763349e9a358260ec1a66162ed8cf8ec6ebfb45836971e89`
-	Default Command: `["R"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1765152000'
# Tue, 09 Dec 2025 14:12:30 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Dec 2025 14:12:30 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 09 Dec 2025 14:12:57 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:12:59 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 09 Dec 2025 14:12:59 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 09 Dec 2025 14:12:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Dec 2025 14:13:00 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 09 Dec 2025 14:13:00 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 09 Dec 2025 14:15:36 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:15:36 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c77c02bf0ec741c5e6279842de5ec989f964c7c81eeb1105d5fbd8ab26246bd0`  
		Last Modified: Tue, 09 Dec 2025 09:18:56 GMT  
		Size: 53.4 MB (53413788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1f165120af8f32e56369dd716d78674f173c1eb15914c7f931d6e61472f7bd`  
		Last Modified: Tue, 09 Dec 2025 14:17:21 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e814f0efec36b941f47937fc1cf4d98cfb365170b1c19a6df00f0afe5d3840`  
		Last Modified: Tue, 09 Dec 2025 14:17:23 GMT  
		Size: 27.3 MB (27281358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd865361ba48ccf6a6e83969fcede89fca724083ecb701ff8ff17584fe5a6c55`  
		Last Modified: Tue, 09 Dec 2025 14:17:21 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f93d1858c8451812a691860fdedf978f7f145d3c3a1c6ef0c24449f9252933d`  
		Last Modified: Tue, 09 Dec 2025 14:17:21 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62239fd20b66a015e3626e9521b02553d33a87ad8b656764651041ba83d19dfa`  
		Last Modified: Tue, 09 Dec 2025 14:17:33 GMT  
		Size: 295.4 MB (295422944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:4bf01bf4af4608bd18b72ad3925bee678c98290cd48bb8d3588265da7fe3d68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12958736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c42607dfc658d76983d987ef1cdff922cc055376009df485422f1f900e8a9b`

```dockerfile
```

-	Layers:
	-	`sha256:ef9f9394f6236dfd480ba9c7ac8887dd0879cc088de8922223b4ca797ac1aaa1`  
		Last Modified: Tue, 09 Dec 2025 16:13:46 GMT  
		Size: 12.9 MB (12940598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e02c608cad9ffc2cef988f184c03576f750672f5057c0a951bfc5958a84bf2df`  
		Last Modified: Tue, 09 Dec 2025 16:13:47 GMT  
		Size: 18.1 KB (18138 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:43e69fbc63a18227caa005921474265d2e7040c54219368db30cbc7ebd7bc434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343380310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f1032d19e6c30c497d89bdb5f502d1d1141e7f107e5d96eaf97c6a80175978`
-	Default Command: `["R"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1765152000'
# Tue, 09 Dec 2025 12:09:56 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Dec 2025 12:09:56 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 09 Dec 2025 12:10:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 12:10:07 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 09 Dec 2025 12:10:07 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 09 Dec 2025 12:10:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Dec 2025 12:10:07 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 09 Dec 2025 12:10:07 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 09 Dec 2025 12:10:56 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 12:10:56 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6ad4d5a8b1668f11bbabc575605b837454e88e85306364c279679a1eb23d3849`  
		Last Modified: Tue, 09 Dec 2025 11:11:10 GMT  
		Size: 48.3 MB (48319839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cb1340c75993f221586fdfe645a5e8f4b742a0303f9f6eee3738ff5261e642`  
		Last Modified: Tue, 09 Dec 2025 12:12:18 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6746bd6cb686df283d04b8dffd03eb92841a3f6f8f2d12a8b1400db08b23fe`  
		Last Modified: Tue, 09 Dec 2025 12:12:19 GMT  
		Size: 26.9 MB (26940796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2488a1e2b5cfc0ff6ea1814ae888117beb5be05025e8e99f945cd1a52aaceca`  
		Last Modified: Tue, 09 Dec 2025 12:12:18 GMT  
		Size: 924.5 KB (924545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994c3a889e04b8c714cd3fabab933f4abefd1baa8beef332cc41fd57735508bb`  
		Last Modified: Tue, 09 Dec 2025 12:12:18 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d73910e554c070cf1fc820ab28d06fafb973e913a65c89aed6d201a8d6ecc7`  
		Last Modified: Tue, 09 Dec 2025 12:12:24 GMT  
		Size: 267.2 MB (267191466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:28f45dbb04bfa7537b9e574e072d38c5df754e8f9260682bbe27613d302e0c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12764081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cff3f18f1b2a5f0a30ae06a0850d78eb4f6292d37c3aa3d25a7fbf71f2f1d4`

```dockerfile
```

-	Layers:
	-	`sha256:75e53dec4319bc558ab8a6fa7b065f1b69ae45b68594d6e70684b26df25f9723`  
		Last Modified: Tue, 09 Dec 2025 13:13:47 GMT  
		Size: 12.7 MB (12745983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d82a5e1ca8ca6a52b4b4e5b28013accfe71e603c88be14d9fb9decda627feb87`  
		Last Modified: Tue, 09 Dec 2025 13:13:54 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json
