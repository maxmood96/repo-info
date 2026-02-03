<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.5.2`](#r-base452)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.5.2`

```console
$ docker pull r-base@sha256:3126c2d28e627a806e38e6cada7929c37987780c6eb13a380bdc29339bf2cf71
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
$ docker pull r-base@sha256:0f451fb3308a4961b4c0177f9c86850bc4dd5d7d233e6fee3385541301c515f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365841261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c522375070e91d31658ecf2055e085da378852e009ea29696269e511f34e5449`
-	Default Command: `["R"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:39:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 03 Feb 2026 02:39:24 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 03 Feb 2026 02:39:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:39:34 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 03 Feb 2026 02:39:34 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 03 Feb 2026 02:39:34 GMT
ENV LANG=en_US.UTF-8
# Tue, 03 Feb 2026 02:39:34 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 03 Feb 2026 02:39:34 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 03 Feb 2026 02:40:16 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:5195bf09170e6f427c63401408925ebdcc18df14385049cc0921fa4e070abc9b`  
		Last Modified: Tue, 03 Feb 2026 01:15:55 GMT  
		Size: 48.7 MB (48655738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9975f51a91bcb0bbfee61eac34ede0cca253f737ba0566723dd7f86ae0f3b2`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d0af0dafd2a6a59a3c08d7eaa697841bccb7e519f46352b989882d26c752e8`  
		Last Modified: Tue, 03 Feb 2026 02:40:57 GMT  
		Size: 27.0 MB (27048830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e1a149de68203e25b1c5bf1c33411bb24c42f3bfb0cb66f1805e2392ec9a74`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8c7ab08d5a8df0f02955f8b8bfea31235ce2b138e8c6fe26a83be8b55c8549`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8ad8a9d0773b2b4ab448eae44558037e3b2bb1f0f50646ce68aa86b03e7ff1`  
		Last Modified: Tue, 03 Feb 2026 02:41:03 GMT  
		Size: 289.3 MB (289264540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:286fffee8f22c7456cc5b6ba88105c61b26d35be481434c1514a47d3440afa0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13039397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d13b40a7c8c0110d09603c91aa4713701c2d6615fca0e54c1952be6489233f5`

```dockerfile
```

-	Layers:
	-	`sha256:24366fc9dca2cd157b6f9af2caf62806f530b0b0bcc935d6ca0887ba2402a00b`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 13.0 MB (13021299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60cf19584ef7a268b8ed01cfb136f1e1bae337c3cf26ecf86c2a0a07ad43d825`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:cfbfcb4bcfc617b343f0d09153bcc90fe483f29e8b76164d2b890f49bda4c589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350468650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7b2d1704adf4510947779ab61f07cbb3552b7032c4419089e991d7e4eacd33`
-	Default Command: `["R"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:59:51 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Jan 2026 01:59:51 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 13 Jan 2026 01:59:58 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:59:59 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 13 Jan 2026 01:59:59 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 01:59:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Jan 2026 01:59:59 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 13 Jan 2026 01:59:59 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 13 Jan 2026 02:00:40 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:00:40 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:7bff1ad60177e8dd221d8df5866b0e7967fbd97f4eb69a5eb672bd24b7ffc9ba`  
		Last Modified: Tue, 13 Jan 2026 00:43:00 GMT  
		Size: 48.8 MB (48820814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb28f762553349deb6532eea027cff1be2677b7b652c5a961caf34646579f8d`  
		Last Modified: Tue, 13 Jan 2026 02:01:17 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76734e972ab3837229f3cc63100cc580d7f3188305ed6240a1d651c69e0a36`  
		Last Modified: Tue, 13 Jan 2026 02:01:18 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4981255760d73d5b0d192b763648c61e43362dc442ab75f3537008a4f1801e82`  
		Last Modified: Tue, 13 Jan 2026 02:01:17 GMT  
		Size: 868.5 KB (868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdc6ee7cddd3db841a5004871713036f2dc66d7b2dce24f271bc2e958bd92e5`  
		Last Modified: Tue, 13 Jan 2026 02:01:17 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d4aea4f4f21716b2e41e48b81137112752e200efa0740c1662523b64a5a0b`  
		Last Modified: Tue, 13 Jan 2026 02:01:24 GMT  
		Size: 273.9 MB (273882182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:f25b88ea610d938b0a05cac633994426f5b0113472721555815be5e8d9314d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13080161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772ce558dc40eafa6e4007b54ae97b959c452d1fc293a5333fdc01e0c31c2ca6`

```dockerfile
```

-	Layers:
	-	`sha256:37e958df6e2cd932b11d5c7566758ce6d694e725b3659d5b76e2fc2209079bc9`  
		Last Modified: Tue, 13 Jan 2026 02:01:18 GMT  
		Size: 13.1 MB (13061924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91448c165d0b22ae0e931fd21274cbcea247da4e62d05511f996b191d7ab1b9e`  
		Last Modified: Tue, 13 Jan 2026 02:01:17 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:cbdf0e7028148662181edb74eb0b2a3934bde72da8b362c0ae269938460849f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360077132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284942420ad85f79f5c24ce843da13e1baee4fa7f37d1302c9ccb724b78fb713`
-	Default Command: `["R"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 03:23:23 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Jan 2026 03:23:23 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 13 Jan 2026 03:23:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:23:47 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 13 Jan 2026 03:23:47 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 03:23:47 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Jan 2026 03:23:48 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 13 Jan 2026 03:23:48 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 13 Jan 2026 03:26:11 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:26:11 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3c09db137a92dd478d776e54d49034b249ad15299a714fc28f5e13f7c59c6f6e`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 53.5 MB (53516189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fac3ed4db2cf72c14847e32d7af576ab1f7c2f437314b175d607d2a6083402`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15a1c252d0ff17d821ffd9e6e90364cd6e041eb6bb40859b9d2de91e104f3d6`  
		Last Modified: Tue, 13 Jan 2026 03:27:34 GMT  
		Size: 27.3 MB (27320673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902220f22138a27c0cab0f87efc29e189f5681d92986c9d41d4392d9267c39e1`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f248072615edd85e070a943f29a2a27c33fd0e0f42f05d05a2f86ca060752d`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340b3824935c2bbb0c85b45e931ac4a146e9de3ea0512201ce6b6e63b247c323`  
		Last Modified: Tue, 13 Jan 2026 03:27:44 GMT  
		Size: 278.4 MB (278368115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:743808ba78a06686734f11269fb7710436f84cf838c90cfc04ccf72b07756600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12974070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d803176f3dc44ae45bf554e004ff83ce7ac210a53e570e6f5fd32cce3ba7d1`

```dockerfile
```

-	Layers:
	-	`sha256:f3196c63d3a077f6ee56d63f76dcd778cb88def5274b6b8cb27e6898c28a660b`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 13.0 MB (12955932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d2fcfa67a549856149423e031279d7cd1e067a95989923bafd5acee82c79ad`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 18.1 KB (18138 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; s390x

```console
$ docker pull r-base@sha256:e3cd11038b186c280f675e95b31836ff8a6069450be399fd4d6b223ac7185b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335060149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e46c338d750962e2fee8ce1d975a9f153ca89bb6ce0331e09318a6b96e79193`
-	Default Command: `["R"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 02:02:41 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Jan 2026 02:02:41 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 13 Jan 2026 02:02:49 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:02:50 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 13 Jan 2026 02:02:50 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 02:02:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Jan 2026 02:02:50 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 13 Jan 2026 02:02:50 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 13 Jan 2026 02:03:33 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:03:33 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:62ffa4c0309d07ab05b7709095497112179f2c729363c4d63136ece116e95e0d`  
		Last Modified: Tue, 13 Jan 2026 00:41:33 GMT  
		Size: 48.4 MB (48389301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa6770a934822895ad765c0a3a209a8eb7a23affeaaed47839b86c74ac92ac7`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70b1a288c469fe1bfc9978b5e3bfe0ea53a4a618d477bf227f017b9a2eda736`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 27.0 MB (26975279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712ffe52fcee3360e3813c0531cf9d52daefc570489d5899a6c0794aa6bbd106`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8276b45126cb168fdde0fb4251f61d98ab7ef83de43a054c8bd09cd071a3eda`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7929aee6952bd67e672421a0ba8626ce6010272f975e715f4ff8a48766eb3f4`  
		Last Modified: Tue, 13 Jan 2026 02:04:27 GMT  
		Size: 258.8 MB (258767358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:7c246d3f24fb29a239657ec985b04f90b1e43c4a766dbd60c0783ad7a706148e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12792637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5e3b387b7ce6e93be8671ba9ad9f499f36b7dcf261a160224ad70828845591`

```dockerfile
```

-	Layers:
	-	`sha256:363528e1842b841ef940850b864b17248b532c38279690a4b4e8687fa4a3bab7`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 12.8 MB (12774540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb126a4ac648a913be2b361f91a0947243e43ee55cb7997efe7f3954f19fe3bb`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:3126c2d28e627a806e38e6cada7929c37987780c6eb13a380bdc29339bf2cf71
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
$ docker pull r-base@sha256:0f451fb3308a4961b4c0177f9c86850bc4dd5d7d233e6fee3385541301c515f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365841261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c522375070e91d31658ecf2055e085da378852e009ea29696269e511f34e5449`
-	Default Command: `["R"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:39:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 03 Feb 2026 02:39:24 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 03 Feb 2026 02:39:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:39:34 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 03 Feb 2026 02:39:34 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 03 Feb 2026 02:39:34 GMT
ENV LANG=en_US.UTF-8
# Tue, 03 Feb 2026 02:39:34 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 03 Feb 2026 02:39:34 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 03 Feb 2026 02:40:16 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:40:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:5195bf09170e6f427c63401408925ebdcc18df14385049cc0921fa4e070abc9b`  
		Last Modified: Tue, 03 Feb 2026 01:15:55 GMT  
		Size: 48.7 MB (48655738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9975f51a91bcb0bbfee61eac34ede0cca253f737ba0566723dd7f86ae0f3b2`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d0af0dafd2a6a59a3c08d7eaa697841bccb7e519f46352b989882d26c752e8`  
		Last Modified: Tue, 03 Feb 2026 02:40:57 GMT  
		Size: 27.0 MB (27048830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e1a149de68203e25b1c5bf1c33411bb24c42f3bfb0cb66f1805e2392ec9a74`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8c7ab08d5a8df0f02955f8b8bfea31235ce2b138e8c6fe26a83be8b55c8549`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8ad8a9d0773b2b4ab448eae44558037e3b2bb1f0f50646ce68aa86b03e7ff1`  
		Last Modified: Tue, 03 Feb 2026 02:41:03 GMT  
		Size: 289.3 MB (289264540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:286fffee8f22c7456cc5b6ba88105c61b26d35be481434c1514a47d3440afa0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13039397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d13b40a7c8c0110d09603c91aa4713701c2d6615fca0e54c1952be6489233f5`

```dockerfile
```

-	Layers:
	-	`sha256:24366fc9dca2cd157b6f9af2caf62806f530b0b0bcc935d6ca0887ba2402a00b`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 13.0 MB (13021299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60cf19584ef7a268b8ed01cfb136f1e1bae337c3cf26ecf86c2a0a07ad43d825`  
		Last Modified: Tue, 03 Feb 2026 02:40:56 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:cfbfcb4bcfc617b343f0d09153bcc90fe483f29e8b76164d2b890f49bda4c589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350468650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7b2d1704adf4510947779ab61f07cbb3552b7032c4419089e991d7e4eacd33`
-	Default Command: `["R"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:59:51 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Jan 2026 01:59:51 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 13 Jan 2026 01:59:58 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:59:59 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 13 Jan 2026 01:59:59 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 01:59:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Jan 2026 01:59:59 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 13 Jan 2026 01:59:59 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 13 Jan 2026 02:00:40 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:00:40 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:7bff1ad60177e8dd221d8df5866b0e7967fbd97f4eb69a5eb672bd24b7ffc9ba`  
		Last Modified: Tue, 13 Jan 2026 00:43:00 GMT  
		Size: 48.8 MB (48820814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb28f762553349deb6532eea027cff1be2677b7b652c5a961caf34646579f8d`  
		Last Modified: Tue, 13 Jan 2026 02:01:17 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76734e972ab3837229f3cc63100cc580d7f3188305ed6240a1d651c69e0a36`  
		Last Modified: Tue, 13 Jan 2026 02:01:18 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4981255760d73d5b0d192b763648c61e43362dc442ab75f3537008a4f1801e82`  
		Last Modified: Tue, 13 Jan 2026 02:01:17 GMT  
		Size: 868.5 KB (868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdc6ee7cddd3db841a5004871713036f2dc66d7b2dce24f271bc2e958bd92e5`  
		Last Modified: Tue, 13 Jan 2026 02:01:17 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d4aea4f4f21716b2e41e48b81137112752e200efa0740c1662523b64a5a0b`  
		Last Modified: Tue, 13 Jan 2026 02:01:24 GMT  
		Size: 273.9 MB (273882182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f25b88ea610d938b0a05cac633994426f5b0113472721555815be5e8d9314d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13080161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772ce558dc40eafa6e4007b54ae97b959c452d1fc293a5333fdc01e0c31c2ca6`

```dockerfile
```

-	Layers:
	-	`sha256:37e958df6e2cd932b11d5c7566758ce6d694e725b3659d5b76e2fc2209079bc9`  
		Last Modified: Tue, 13 Jan 2026 02:01:18 GMT  
		Size: 13.1 MB (13061924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91448c165d0b22ae0e931fd21274cbcea247da4e62d05511f996b191d7ab1b9e`  
		Last Modified: Tue, 13 Jan 2026 02:01:17 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:cbdf0e7028148662181edb74eb0b2a3934bde72da8b362c0ae269938460849f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360077132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284942420ad85f79f5c24ce843da13e1baee4fa7f37d1302c9ccb724b78fb713`
-	Default Command: `["R"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 03:23:23 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Jan 2026 03:23:23 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 13 Jan 2026 03:23:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:23:47 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 13 Jan 2026 03:23:47 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 03:23:47 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Jan 2026 03:23:48 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 13 Jan 2026 03:23:48 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 13 Jan 2026 03:26:11 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:26:11 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3c09db137a92dd478d776e54d49034b249ad15299a714fc28f5e13f7c59c6f6e`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 53.5 MB (53516189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fac3ed4db2cf72c14847e32d7af576ab1f7c2f437314b175d607d2a6083402`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15a1c252d0ff17d821ffd9e6e90364cd6e041eb6bb40859b9d2de91e104f3d6`  
		Last Modified: Tue, 13 Jan 2026 03:27:34 GMT  
		Size: 27.3 MB (27320673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902220f22138a27c0cab0f87efc29e189f5681d92986c9d41d4392d9267c39e1`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f248072615edd85e070a943f29a2a27c33fd0e0f42f05d05a2f86ca060752d`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340b3824935c2bbb0c85b45e931ac4a146e9de3ea0512201ce6b6e63b247c323`  
		Last Modified: Tue, 13 Jan 2026 03:27:44 GMT  
		Size: 278.4 MB (278368115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:743808ba78a06686734f11269fb7710436f84cf838c90cfc04ccf72b07756600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12974070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d803176f3dc44ae45bf554e004ff83ce7ac210a53e570e6f5fd32cce3ba7d1`

```dockerfile
```

-	Layers:
	-	`sha256:f3196c63d3a077f6ee56d63f76dcd778cb88def5274b6b8cb27e6898c28a660b`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 13.0 MB (12955932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d2fcfa67a549856149423e031279d7cd1e067a95989923bafd5acee82c79ad`  
		Last Modified: Tue, 13 Jan 2026 03:27:33 GMT  
		Size: 18.1 KB (18138 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:e3cd11038b186c280f675e95b31836ff8a6069450be399fd4d6b223ac7185b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335060149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e46c338d750962e2fee8ce1d975a9f153ca89bb6ce0331e09318a6b96e79193`
-	Default Command: `["R"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 02:02:41 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Jan 2026 02:02:41 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 13 Jan 2026 02:02:49 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:02:50 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 13 Jan 2026 02:02:50 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 02:02:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Jan 2026 02:02:50 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 13 Jan 2026 02:02:50 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 13 Jan 2026 02:03:33 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:03:33 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:62ffa4c0309d07ab05b7709095497112179f2c729363c4d63136ece116e95e0d`  
		Last Modified: Tue, 13 Jan 2026 00:41:33 GMT  
		Size: 48.4 MB (48389301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa6770a934822895ad765c0a3a209a8eb7a23affeaaed47839b86c74ac92ac7`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70b1a288c469fe1bfc9978b5e3bfe0ea53a4a618d477bf227f017b9a2eda736`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 27.0 MB (26975279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712ffe52fcee3360e3813c0531cf9d52daefc570489d5899a6c0794aa6bbd106`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8276b45126cb168fdde0fb4251f61d98ab7ef83de43a054c8bd09cd071a3eda`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7929aee6952bd67e672421a0ba8626ce6010272f975e715f4ff8a48766eb3f4`  
		Last Modified: Tue, 13 Jan 2026 02:04:27 GMT  
		Size: 258.8 MB (258767358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:7c246d3f24fb29a239657ec985b04f90b1e43c4a766dbd60c0783ad7a706148e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12792637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5e3b387b7ce6e93be8671ba9ad9f499f36b7dcf261a160224ad70828845591`

```dockerfile
```

-	Layers:
	-	`sha256:363528e1842b841ef940850b864b17248b532c38279690a4b4e8687fa4a3bab7`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 12.8 MB (12774540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb126a4ac648a913be2b361f91a0947243e43ee55cb7997efe7f3954f19fe3bb`  
		Last Modified: Tue, 13 Jan 2026 02:04:22 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json
