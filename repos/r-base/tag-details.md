<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.2`](#r-base442)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.2`

```console
$ docker pull r-base@sha256:ff0c913d0dee7c54eb3e14d80653765697865a6e4ba8bdd3550d8eaa8b25042e
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

### `r-base:4.4.2` - linux; amd64

```console
$ docker pull r-base@sha256:cdeeabb201527cabe0b045ff805d27a7108d79eb72dc21760a40f1d07d187563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.4 MB (355414164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242d80afc1301227a452e5055448e7c8f718009c98bb84197a26e473193f84dd`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1740355200'
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:4339d58b51096c923edc311f519af6a5c9ce7315d655d9d677c2ef5b2dbf3baf`  
		Last Modified: Tue, 25 Feb 2025 01:29:54 GMT  
		Size: 47.5 MB (47471282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a134b4fcf0acc50e44c8894b7b26096b90fd63d60da52f0e4447118964bbaa22`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b92e1bc78e68cd3a972e1930d3108907377a5d8e06d57d44baa2aea86af674b`  
		Last Modified: Tue, 25 Feb 2025 02:25:51 GMT  
		Size: 26.8 MB (26781831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1e7e88026e4c02ce9903067ca18c7e567adea841a9f4f7621538fe979a5e7d`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 866.7 KB (866745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3583e7ca6ec2db9ee7ae915c7ae1e3c438d933e3101513576a13ccd27b4f56b`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ce9742a15c11601098a5a7c9533c65aad7b4565d2c2a72310530de127e4308`  
		Last Modified: Tue, 25 Feb 2025 02:25:55 GMT  
		Size: 280.3 MB (280290644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.2` - unknown; unknown

```console
$ docker pull r-base@sha256:8b6f7d91859485958ef08983406785960e3ae48af10cbee96a5df487a824ecc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a262a8b118d52156737f48699f575ac04b78b64787e57adb2fc353802710fc`

```dockerfile
```

-	Layers:
	-	`sha256:b8bd42907f383e5fe14ac0cb260c5fc541cfd82d29820249a5b0f4cd07d410d0`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 12.6 MB (12577945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faba31f646dbb977363c3d5e8e15f6e9076b11d7890c8911cdeb38d77b9b0087`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:feaff63863ff449976a4ba3935ef815b77236294f52c5e7749a179092772a456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343060806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2d7cb391a8ad97658e36d9e3ac3014ffe230acae3e71543bf476a955ac1d33`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1738540800'
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9b5d10d37c435444f1e303e9933bb6b72d4c5f46abb75cc41cb7eddc7a5c66f4`  
		Last Modified: Tue, 04 Feb 2025 01:40:18 GMT  
		Size: 48.7 MB (48735376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b561b12143d13a46709b42dfee0f2dbdc72bc271249f8817f0fada6909fcd757`  
		Last Modified: Tue, 04 Feb 2025 08:20:49 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb107f11593a94c6388a47ea22d62e66646da22745b67118bc36e08de37c19`  
		Last Modified: Tue, 04 Feb 2025 08:20:50 GMT  
		Size: 26.7 MB (26651466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f952a94ddc9838b2f68d14540c74283fad846a72a0f910c5c8c128e980e1854f`  
		Last Modified: Tue, 04 Feb 2025 08:20:49 GMT  
		Size: 866.7 KB (866747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7541110fc0c0befbfc08f682ab775e07fe5a9e041c548eecab7ff0ec82e01`  
		Last Modified: Tue, 04 Feb 2025 08:20:49 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ce0a50daa176f3e2b6cc79f429d3043da4584c3aab2113c817a42dbc37b62`  
		Last Modified: Tue, 04 Feb 2025 08:20:56 GMT  
		Size: 266.8 MB (266803559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.2` - unknown; unknown

```console
$ docker pull r-base@sha256:3149c5bb2907e3f4e5332181f6b657c30b8a450c54838667dc13a28771ea280f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12750597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516df7662c64ea4a8960670f3cef76593e2a46d224733df49da9e95d3e0513ca`

```dockerfile
```

-	Layers:
	-	`sha256:0d93949adee1a856b79d52c9c03efea0764ee7d95dc6cb3b60b7b6a76f3210c6`  
		Last Modified: Tue, 04 Feb 2025 08:20:50 GMT  
		Size: 12.7 MB (12732317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12d675d7cd4cb99b4db057362b6d34591e124f9e64f21c3fca0c50ded88face`  
		Last Modified: Tue, 04 Feb 2025 08:20:49 GMT  
		Size: 18.3 KB (18280 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:d4e0efd6df9bf5175ecb9ddcbcfeca849bf4eb3044cf093afbdb1e3994a32acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352734034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01743cc3c36eadb8a1e50bdb5452c8411fb0a3ccf6d9e2cafe24724142a49166`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1738540800'
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e6ea63efe3465a432aa2c59a14423e7ea72d35c4e4bd9e6d1285b38add0090d1`  
		Last Modified: Tue, 04 Feb 2025 01:40:28 GMT  
		Size: 52.1 MB (52139238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2392d0fb29c62a5444ad91164be4c73738dafcbd47114e388fdbbd0a7499e15`  
		Last Modified: Tue, 04 Feb 2025 07:00:09 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685699e5ec42b6cd57917202843ade41c6a8866d0fefc7bdee74bcc039ee9889`  
		Last Modified: Tue, 04 Feb 2025 07:00:10 GMT  
		Size: 27.0 MB (27017037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f68366bb05e28a7b9c764b21b27b6aa245aa9bf0f7c7a2baf058d9002c4018`  
		Last Modified: Tue, 04 Feb 2025 07:00:09 GMT  
		Size: 866.7 KB (866746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfdb00e49d847c4572d662226ebe8bd847b066188ec5b44e3df2e29a06eb550`  
		Last Modified: Tue, 04 Feb 2025 07:00:09 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce68c57f0e45f4304d77365c24c1defd4d0df59fece2a71fe266fef985ac414`  
		Last Modified: Tue, 04 Feb 2025 07:00:29 GMT  
		Size: 272.7 MB (272707352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.2` - unknown; unknown

```console
$ docker pull r-base@sha256:722344987c92956f4e94ff8e3ba45f9c0245fb2c55c72b765868272736ab0c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12650123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea891fb62b4c902eec1236c4e2fc6b80a81b7899b00f20d95d52f7acc5da7636`

```dockerfile
```

-	Layers:
	-	`sha256:62957fb136c5e7723c4b0bc2db20a711a37767a51383bc5698295a69e9bd0a2c`  
		Last Modified: Tue, 04 Feb 2025 07:00:10 GMT  
		Size: 12.6 MB (12631942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c327b1f2634e41c6ebcab128436b62194e7c1b4bba96693da5d3dde2abf4b4`  
		Last Modified: Tue, 04 Feb 2025 07:00:09 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.2` - linux; s390x

```console
$ docker pull r-base@sha256:95c5f6404861c7bb12dc11c95c0b6e466619a3336056da5197fb90f580ed1b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325854810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a4ef5e96a192727c4cffc6fd62e5dec2b9d8818eda1fb290e6c0fa4337aa56`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1738540800'
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:27e3d5eecd9c93e60cd8a324bcd909d8591a2b8b1a3b865d569bcd832394b458`  
		Last Modified: Tue, 04 Feb 2025 01:40:46 GMT  
		Size: 48.4 MB (48414755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6838c9688637e1cf401883ffd7c776bf86fbe1998e0b2a83443ab6600f492704`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215196f92162946281eb3aa6e77e6a8360d89bcffc2e045c7861b312c60d616e`  
		Last Modified: Tue, 04 Feb 2025 07:09:37 GMT  
		Size: 26.7 MB (26724292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df95244a01085303551ed900643ce2d62094995194709615a44bf9ce78898bb`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 923.5 KB (923491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a19bbfb41d90ff010e2b206306155936798a6b2b3e2bde16fccd855537f057`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b997d676e67d6818ef054b7fdb19b3661c1d0f18dfc19053cc0595b6fb4289`  
		Last Modified: Tue, 04 Feb 2025 07:09:42 GMT  
		Size: 249.8 MB (249788613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.2` - unknown; unknown

```console
$ docker pull r-base@sha256:a51c20b2d943ff77b5027f7bf94d41e26a7abeceeb5946dc5bc8811996b91289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12457079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c64da36f4b391be4f086d75686cb85e297e2f55116d6d399965ac5845ff378e`

```dockerfile
```

-	Layers:
	-	`sha256:cb7d3faaa1a5cc8775ce3c701fb86467ed2eefcbbd43848e68f2685f1045228f`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 12.4 MB (12438938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eff428b08ef8a1cc71d6b8e4437840ce29e760ffe922c5c3801cfef6080dd4b`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:ff0c913d0dee7c54eb3e14d80653765697865a6e4ba8bdd3550d8eaa8b25042e
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
$ docker pull r-base@sha256:cdeeabb201527cabe0b045ff805d27a7108d79eb72dc21760a40f1d07d187563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.4 MB (355414164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242d80afc1301227a452e5055448e7c8f718009c98bb84197a26e473193f84dd`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1740355200'
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:4339d58b51096c923edc311f519af6a5c9ce7315d655d9d677c2ef5b2dbf3baf`  
		Last Modified: Tue, 25 Feb 2025 01:29:54 GMT  
		Size: 47.5 MB (47471282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a134b4fcf0acc50e44c8894b7b26096b90fd63d60da52f0e4447118964bbaa22`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b92e1bc78e68cd3a972e1930d3108907377a5d8e06d57d44baa2aea86af674b`  
		Last Modified: Tue, 25 Feb 2025 02:25:51 GMT  
		Size: 26.8 MB (26781831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1e7e88026e4c02ce9903067ca18c7e567adea841a9f4f7621538fe979a5e7d`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 866.7 KB (866745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3583e7ca6ec2db9ee7ae915c7ae1e3c438d933e3101513576a13ccd27b4f56b`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ce9742a15c11601098a5a7c9533c65aad7b4565d2c2a72310530de127e4308`  
		Last Modified: Tue, 25 Feb 2025 02:25:55 GMT  
		Size: 280.3 MB (280290644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:8b6f7d91859485958ef08983406785960e3ae48af10cbee96a5df487a824ecc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a262a8b118d52156737f48699f575ac04b78b64787e57adb2fc353802710fc`

```dockerfile
```

-	Layers:
	-	`sha256:b8bd42907f383e5fe14ac0cb260c5fc541cfd82d29820249a5b0f4cd07d410d0`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 12.6 MB (12577945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faba31f646dbb977363c3d5e8e15f6e9076b11d7890c8911cdeb38d77b9b0087`  
		Last Modified: Tue, 25 Feb 2025 02:25:50 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:feaff63863ff449976a4ba3935ef815b77236294f52c5e7749a179092772a456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343060806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2d7cb391a8ad97658e36d9e3ac3014ffe230acae3e71543bf476a955ac1d33`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1738540800'
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9b5d10d37c435444f1e303e9933bb6b72d4c5f46abb75cc41cb7eddc7a5c66f4`  
		Last Modified: Tue, 04 Feb 2025 01:40:18 GMT  
		Size: 48.7 MB (48735376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b561b12143d13a46709b42dfee0f2dbdc72bc271249f8817f0fada6909fcd757`  
		Last Modified: Tue, 04 Feb 2025 08:20:49 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb107f11593a94c6388a47ea22d62e66646da22745b67118bc36e08de37c19`  
		Last Modified: Tue, 04 Feb 2025 08:20:50 GMT  
		Size: 26.7 MB (26651466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f952a94ddc9838b2f68d14540c74283fad846a72a0f910c5c8c128e980e1854f`  
		Last Modified: Tue, 04 Feb 2025 08:20:49 GMT  
		Size: 866.7 KB (866747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7541110fc0c0befbfc08f682ab775e07fe5a9e041c548eecab7ff0ec82e01`  
		Last Modified: Tue, 04 Feb 2025 08:20:49 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ce0a50daa176f3e2b6cc79f429d3043da4584c3aab2113c817a42dbc37b62`  
		Last Modified: Tue, 04 Feb 2025 08:20:56 GMT  
		Size: 266.8 MB (266803559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:3149c5bb2907e3f4e5332181f6b657c30b8a450c54838667dc13a28771ea280f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12750597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516df7662c64ea4a8960670f3cef76593e2a46d224733df49da9e95d3e0513ca`

```dockerfile
```

-	Layers:
	-	`sha256:0d93949adee1a856b79d52c9c03efea0764ee7d95dc6cb3b60b7b6a76f3210c6`  
		Last Modified: Tue, 04 Feb 2025 08:20:50 GMT  
		Size: 12.7 MB (12732317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12d675d7cd4cb99b4db057362b6d34591e124f9e64f21c3fca0c50ded88face`  
		Last Modified: Tue, 04 Feb 2025 08:20:49 GMT  
		Size: 18.3 KB (18280 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:d4e0efd6df9bf5175ecb9ddcbcfeca849bf4eb3044cf093afbdb1e3994a32acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352734034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01743cc3c36eadb8a1e50bdb5452c8411fb0a3ccf6d9e2cafe24724142a49166`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1738540800'
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e6ea63efe3465a432aa2c59a14423e7ea72d35c4e4bd9e6d1285b38add0090d1`  
		Last Modified: Tue, 04 Feb 2025 01:40:28 GMT  
		Size: 52.1 MB (52139238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2392d0fb29c62a5444ad91164be4c73738dafcbd47114e388fdbbd0a7499e15`  
		Last Modified: Tue, 04 Feb 2025 07:00:09 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685699e5ec42b6cd57917202843ade41c6a8866d0fefc7bdee74bcc039ee9889`  
		Last Modified: Tue, 04 Feb 2025 07:00:10 GMT  
		Size: 27.0 MB (27017037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f68366bb05e28a7b9c764b21b27b6aa245aa9bf0f7c7a2baf058d9002c4018`  
		Last Modified: Tue, 04 Feb 2025 07:00:09 GMT  
		Size: 866.7 KB (866746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfdb00e49d847c4572d662226ebe8bd847b066188ec5b44e3df2e29a06eb550`  
		Last Modified: Tue, 04 Feb 2025 07:00:09 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce68c57f0e45f4304d77365c24c1defd4d0df59fece2a71fe266fef985ac414`  
		Last Modified: Tue, 04 Feb 2025 07:00:29 GMT  
		Size: 272.7 MB (272707352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:722344987c92956f4e94ff8e3ba45f9c0245fb2c55c72b765868272736ab0c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12650123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea891fb62b4c902eec1236c4e2fc6b80a81b7899b00f20d95d52f7acc5da7636`

```dockerfile
```

-	Layers:
	-	`sha256:62957fb136c5e7723c4b0bc2db20a711a37767a51383bc5698295a69e9bd0a2c`  
		Last Modified: Tue, 04 Feb 2025 07:00:10 GMT  
		Size: 12.6 MB (12631942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c327b1f2634e41c6ebcab128436b62194e7c1b4bba96693da5d3dde2abf4b4`  
		Last Modified: Tue, 04 Feb 2025 07:00:09 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:95c5f6404861c7bb12dc11c95c0b6e466619a3336056da5197fb90f580ed1b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325854810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a4ef5e96a192727c4cffc6fd62e5dec2b9d8818eda1fb290e6c0fa4337aa56`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1738540800'
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:27e3d5eecd9c93e60cd8a324bcd909d8591a2b8b1a3b865d569bcd832394b458`  
		Last Modified: Tue, 04 Feb 2025 01:40:46 GMT  
		Size: 48.4 MB (48414755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6838c9688637e1cf401883ffd7c776bf86fbe1998e0b2a83443ab6600f492704`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215196f92162946281eb3aa6e77e6a8360d89bcffc2e045c7861b312c60d616e`  
		Last Modified: Tue, 04 Feb 2025 07:09:37 GMT  
		Size: 26.7 MB (26724292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df95244a01085303551ed900643ce2d62094995194709615a44bf9ce78898bb`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 923.5 KB (923491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a19bbfb41d90ff010e2b206306155936798a6b2b3e2bde16fccd855537f057`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b997d676e67d6818ef054b7fdb19b3661c1d0f18dfc19053cc0595b6fb4289`  
		Last Modified: Tue, 04 Feb 2025 07:09:42 GMT  
		Size: 249.8 MB (249788613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:a51c20b2d943ff77b5027f7bf94d41e26a7abeceeb5946dc5bc8811996b91289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12457079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c64da36f4b391be4f086d75686cb85e297e2f55116d6d399965ac5845ff378e`

```dockerfile
```

-	Layers:
	-	`sha256:cb7d3faaa1a5cc8775ce3c701fb86467ed2eefcbbd43848e68f2685f1045228f`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 12.4 MB (12438938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eff428b08ef8a1cc71d6b8e4437840ce29e760ffe922c5c3801cfef6080dd4b`  
		Last Modified: Tue, 04 Feb 2025 07:09:36 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
