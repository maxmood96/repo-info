## `r-base:latest`

```console
$ docker pull r-base@sha256:496dd67b2448d3cca978442a2ddbbeae9e8c10d073fe82ce2436360acb737a43
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
$ docker pull r-base@sha256:494dfc2a85b63204a3450fa8d9d6c9a857fd2202d0feaca75f1127f95bef7aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364708441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014f5d020f5c5039d4b847bcca25ea85d6118dc24957e5f15e1b78063ee77dde`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1763337600'
# Wed, 19 Nov 2025 08:09:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 19 Nov 2025 08:09:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 19 Nov 2025 08:09:55 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 08:09:57 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 19 Nov 2025 08:09:57 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 19 Nov 2025 08:09:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 19 Nov 2025 08:09:58 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 19 Nov 2025 08:09:58 GMT
ENV R_BASE_VERSION=4.5.2
# Wed, 19 Nov 2025 08:11:57 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 08:11:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3415dbe8c9fa5c426374b6be2cb753ee1cd73c4fc4d9120de95ac3d35fa936f1`  
		Last Modified: Wed, 19 Nov 2025 07:09:23 GMT  
		Size: 53.3 MB (53334633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee15d7328451f48b518c9e137d6488124f54bbc898fa6c6dc9161eb590a2727e`  
		Last Modified: Wed, 19 Nov 2025 08:13:31 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b6e66dc83eaf112b2bef24c190e1faa0c272fbb867c3d05d70f7cfe91133fb`  
		Last Modified: Wed, 19 Nov 2025 08:13:34 GMT  
		Size: 27.3 MB (27280799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec65360ce90369cedde9dd388bd067e37397bb4c202ac6c7d5b2605a53ecd20`  
		Last Modified: Wed, 19 Nov 2025 08:13:31 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729e10c5c0f3b7dc8c2590a669046fadccfc6136278fefc060fb7c428418206`  
		Last Modified: Wed, 19 Nov 2025 08:13:31 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8f7be0cae17a1aa67b20839b83bf9ee19e0c42ae1668a14ced35e906eb2cde`  
		Last Modified: Wed, 19 Nov 2025 10:10:09 GMT  
		Size: 283.2 MB (283220857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:0460b7d14ac8a09da35fe672bc13d6971bd2aadb885695714e9d34e2d2b9a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12947036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8cd14b2342ab207bca0f8f6a7cb7521e272de44ec46100ac97f82ef2478bbb`

```dockerfile
```

-	Layers:
	-	`sha256:a40a4fc179c775a9e557cf82472af22ab59f758472cfbcb7169fc23e17ab0d60`  
		Last Modified: Wed, 19 Nov 2025 10:13:39 GMT  
		Size: 12.9 MB (12928899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84dd5fd94dc8d0de837e7f4666728f7c73fe26e0c39a3abdaa288e898f80ffa9`  
		Last Modified: Wed, 19 Nov 2025 10:13:40 GMT  
		Size: 18.1 KB (18137 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:9532735ee76dc7ff0b5e53d6954719ec8c6ccbfe8e207eabb9b33fed9d39791f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332636197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6ce297eec1b7ed1693256c5cbe2e0dbcdccac09f8d3038f55bf25a91e98ead`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 17:12:19 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 18 Nov 2025 17:12:19 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 18 Nov 2025 17:12:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 17:12:29 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 18 Nov 2025 17:12:29 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 18 Nov 2025 17:12:29 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Nov 2025 17:12:29 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 18 Nov 2025 17:12:29 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 18 Nov 2025 17:13:14 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 17:13:14 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:963b067f9eecc96262cd77759b1e1e10770c29e86028729532e1addf32185ef1`  
		Last Modified: Tue, 18 Nov 2025 16:21:20 GMT  
		Size: 48.4 MB (48370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dea34b0b304b671b1e68ea1b207c737440ae67aad5d87fea93f9e8420dd6724`  
		Last Modified: Tue, 18 Nov 2025 17:14:15 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ecf2cdce502d1692f7146779e4274647b22693ed82609ae90042f0a81e8de`  
		Last Modified: Tue, 18 Nov 2025 17:14:22 GMT  
		Size: 26.9 MB (26940450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bed3a14f9d98c89602bbeb6774bb80b9d7b0452cc722d3a2e63a8a3ab38c8ef`  
		Last Modified: Tue, 18 Nov 2025 17:14:16 GMT  
		Size: 924.5 KB (924544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00846d50bc4627b5d8b632a8ad345b1732ff83526244f1f8d175ce0db34a6901`  
		Last Modified: Tue, 18 Nov 2025 17:14:15 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d5c40ea17843ad266953330db3f2491fc42ae42375ffeb8cf9f689a93e8e36`  
		Last Modified: Tue, 18 Nov 2025 18:36:44 GMT  
		Size: 256.4 MB (256396605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:31ccf4a4cb9692779e87d4aaf6b7a56e202041902da372db7eacfe71f439fce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12752420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be81ebf30a90d6785fdaf74635f84bc1e1aa73517fed050a95ad5e95a0eefee5`

```dockerfile
```

-	Layers:
	-	`sha256:7498527058ac4d9de775ca551123c7d01493b4ae8c9d92228e3acbbf4fa55716`  
		Last Modified: Tue, 18 Nov 2025 19:14:13 GMT  
		Size: 12.7 MB (12734322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf6d64b58d9193a810329c01ae22c94ee7bbdf8674b057c9aa8a3885b1b3d8c`  
		Last Modified: Tue, 18 Nov 2025 19:14:14 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json
