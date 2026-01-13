<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.5.2`](#r-base452)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.5.2`

```console
$ docker pull r-base@sha256:eaba45edfa19b2f912075116c88cee1ec6fc31399a57eeabe6f3ce8105e4ba3a
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
$ docker pull r-base@sha256:7e00453b9880c0ae07d1db71a2721b18f43f3596c003e5e84581bab222a40d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.5 MB (369455734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76afb0f2d1ac31e5267ca28c3351ec276f1be177a846113eebc70fbebf7e402`
-	Default Command: `["R"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:56:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Jan 2026 01:56:11 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 13 Jan 2026 01:56:18 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:56:19 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 13 Jan 2026 01:56:19 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 01:56:19 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Jan 2026 01:56:19 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 13 Jan 2026 01:56:19 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 13 Jan 2026 01:56:57 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:56:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:5abf542d95a9328e19a36e1d742dd98dd9f67b38be29da7b849a1c9e274c1583`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 48.8 MB (48836502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9e25747c37407f20b8fcfa3240e9980f40a8e3b4409b1275ecdb9cd5eae2e9`  
		Last Modified: Tue, 13 Jan 2026 01:57:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f41690588de60eeaa52eeaadd25b82cd90950a93d488067ed2323b88ef3acd`  
		Last Modified: Tue, 13 Jan 2026 01:57:52 GMT  
		Size: 27.0 MB (27035616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82f3632ae8bc7cce7f58f958fe20eb72f54c99735f525859a52103c1f66adbc`  
		Last Modified: Tue, 13 Jan 2026 01:57:49 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c76a267ae2d1122586611a3101b3b6999566a61e340222db6058ee237b59e1`  
		Last Modified: Tue, 13 Jan 2026 01:57:49 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cee5ef84ab81afd841a3aafa27240a4ff96e361bd6e5535192f3b8a60b03d2`  
		Last Modified: Tue, 13 Jan 2026 01:58:09 GMT  
		Size: 292.7 MB (292711467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:f8e04f26209fb27983853b1d18214e537205d60ffba8ce39cd1d4513a2f802a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12990917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdd2eab1ce506418a0cb9379dc845a136a46234b674568f9dfb623f15bd4fec`

```dockerfile
```

-	Layers:
	-	`sha256:2c8a5ff41b262d1f47de7959e581400c076adbbc1ddfa237f99e84ae4b54be73`  
		Last Modified: Tue, 13 Jan 2026 04:14:28 GMT  
		Size: 13.0 MB (12972819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f302d4294848b50ab8b432ff13875cad73b86d05c26bca90e6f37a6b057f4fc`  
		Last Modified: Tue, 13 Jan 2026 04:14:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:11 GMT  
		Size: 48.8 MB (48820814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb28f762553349deb6532eea027cff1be2677b7b652c5a961caf34646579f8d`  
		Last Modified: Tue, 13 Jan 2026 02:01:30 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76734e972ab3837229f3cc63100cc580d7f3188305ed6240a1d651c69e0a36`  
		Last Modified: Tue, 13 Jan 2026 02:01:32 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4981255760d73d5b0d192b763648c61e43362dc442ab75f3537008a4f1801e82`  
		Last Modified: Tue, 13 Jan 2026 02:01:30 GMT  
		Size: 868.5 KB (868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdc6ee7cddd3db841a5004871713036f2dc66d7b2dce24f271bc2e958bd92e5`  
		Last Modified: Tue, 13 Jan 2026 02:01:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d4aea4f4f21716b2e41e48b81137112752e200efa0740c1662523b64a5a0b`  
		Last Modified: Tue, 13 Jan 2026 02:02:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:14:40 GMT  
		Size: 13.1 MB (13061924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91448c165d0b22ae0e931fd21274cbcea247da4e62d05511f996b191d7ab1b9e`  
		Last Modified: Tue, 13 Jan 2026 04:14:41 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:ebfe5c57edc99a7e0b7e3a0ecdff8851fef32fab45470409c031e9d4b392d7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361436264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f6bb4fd5cea8e8222e6dc263216bad7abee6fd8c70fb1ffc567bedb3e56660`
-	Default Command: `["R"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1766966400'
# Tue, 30 Dec 2025 17:27:57 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 30 Dec 2025 17:27:57 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 30 Dec 2025 17:28:29 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:28:33 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 30 Dec 2025 17:28:33 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 30 Dec 2025 17:28:33 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Dec 2025 17:28:34 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 30 Dec 2025 17:28:34 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 30 Dec 2025 17:30:30 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:30:30 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:5a75c60b8a87177661c6b4e6d045cd20aa06dba288dc0ccace27182fc9ab2ac7`  
		Last Modified: Tue, 30 Dec 2025 15:10:00 GMT  
		Size: 53.5 MB (53522114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7cb81c778008bf715119911d5b8ddb3e1810313ff62be2208f77411d8b56a3`  
		Last Modified: Tue, 30 Dec 2025 17:32:12 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d5c046096af019231304bf88f00effc86ea07629b701646b0c058ff6ee4040`  
		Last Modified: Tue, 30 Dec 2025 17:32:16 GMT  
		Size: 27.3 MB (27318543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c63712eedbd249f5a4dc81723c4625f8c38da4741bc0efb8f147af9553b6c8b`  
		Last Modified: Tue, 30 Dec 2025 17:32:13 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8c8795ffe0f1d5330f8f35b80cb4778743aea6effb77593eab8557a7d4f96`  
		Last Modified: Tue, 30 Dec 2025 17:32:13 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d06e3dcd31306faf0a9ff22f2f20746dac372d95ade24ce1e305ba5f6e68ea`  
		Last Modified: Tue, 30 Dec 2025 17:32:18 GMT  
		Size: 279.7 MB (279723456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:f6fca1473bcc6c4bdc7f900c9f93ebb0c19c1064e4e13e85c2b378d70aaf7aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12952263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164ec1de1db95c3014520b5b5e91ebef8d92865e7e2f6131bf07ed6301b31d19`

```dockerfile
```

-	Layers:
	-	`sha256:31fe2a5a9133d493f289627fcfb77782175048fcf2821f1756085b2a0928e2c1`  
		Last Modified: Tue, 30 Dec 2025 19:13:44 GMT  
		Size: 12.9 MB (12934125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d597700fca5fa1b5b98bbae228d8d92320e59cb8ac837d755047b5094b5ba48d`  
		Last Modified: Tue, 30 Dec 2025 19:13:45 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 48.4 MB (48389301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa6770a934822895ad765c0a3a209a8eb7a23affeaaed47839b86c74ac92ac7`  
		Last Modified: Tue, 13 Jan 2026 02:04:33 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70b1a288c469fe1bfc9978b5e3bfe0ea53a4a618d477bf227f017b9a2eda736`  
		Last Modified: Tue, 13 Jan 2026 02:04:37 GMT  
		Size: 27.0 MB (26975279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712ffe52fcee3360e3813c0531cf9d52daefc570489d5899a6c0794aa6bbd106`  
		Last Modified: Tue, 13 Jan 2026 02:04:33 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8276b45126cb168fdde0fb4251f61d98ab7ef83de43a054c8bd09cd071a3eda`  
		Last Modified: Tue, 13 Jan 2026 02:04:33 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7929aee6952bd67e672421a0ba8626ce6010272f975e715f4ff8a48766eb3f4`  
		Last Modified: Tue, 13 Jan 2026 02:04:39 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:00 GMT  
		Size: 12.8 MB (12774540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb126a4ac648a913be2b361f91a0947243e43ee55cb7997efe7f3954f19fe3bb`  
		Last Modified: Tue, 13 Jan 2026 04:15:01 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:eaba45edfa19b2f912075116c88cee1ec6fc31399a57eeabe6f3ce8105e4ba3a
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
$ docker pull r-base@sha256:7e00453b9880c0ae07d1db71a2721b18f43f3596c003e5e84581bab222a40d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.5 MB (369455734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76afb0f2d1ac31e5267ca28c3351ec276f1be177a846113eebc70fbebf7e402`
-	Default Command: `["R"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1768176000'
# Tue, 13 Jan 2026 01:56:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Jan 2026 01:56:11 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 13 Jan 2026 01:56:18 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:56:19 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 13 Jan 2026 01:56:19 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Jan 2026 01:56:19 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Jan 2026 01:56:19 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 13 Jan 2026 01:56:19 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 13 Jan 2026 01:56:57 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:56:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:5abf542d95a9328e19a36e1d742dd98dd9f67b38be29da7b849a1c9e274c1583`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 48.8 MB (48836502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9e25747c37407f20b8fcfa3240e9980f40a8e3b4409b1275ecdb9cd5eae2e9`  
		Last Modified: Tue, 13 Jan 2026 01:57:48 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f41690588de60eeaa52eeaadd25b82cd90950a93d488067ed2323b88ef3acd`  
		Last Modified: Tue, 13 Jan 2026 01:57:52 GMT  
		Size: 27.0 MB (27035616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82f3632ae8bc7cce7f58f958fe20eb72f54c99735f525859a52103c1f66adbc`  
		Last Modified: Tue, 13 Jan 2026 01:57:49 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c76a267ae2d1122586611a3101b3b6999566a61e340222db6058ee237b59e1`  
		Last Modified: Tue, 13 Jan 2026 01:57:49 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cee5ef84ab81afd841a3aafa27240a4ff96e361bd6e5535192f3b8a60b03d2`  
		Last Modified: Tue, 13 Jan 2026 01:58:09 GMT  
		Size: 292.7 MB (292711467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f8e04f26209fb27983853b1d18214e537205d60ffba8ce39cd1d4513a2f802a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12990917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdd2eab1ce506418a0cb9379dc845a136a46234b674568f9dfb623f15bd4fec`

```dockerfile
```

-	Layers:
	-	`sha256:2c8a5ff41b262d1f47de7959e581400c076adbbc1ddfa237f99e84ae4b54be73`  
		Last Modified: Tue, 13 Jan 2026 04:14:28 GMT  
		Size: 13.0 MB (12972819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f302d4294848b50ab8b432ff13875cad73b86d05c26bca90e6f37a6b057f4fc`  
		Last Modified: Tue, 13 Jan 2026 04:14:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:11 GMT  
		Size: 48.8 MB (48820814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb28f762553349deb6532eea027cff1be2677b7b652c5a961caf34646579f8d`  
		Last Modified: Tue, 13 Jan 2026 02:01:30 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76734e972ab3837229f3cc63100cc580d7f3188305ed6240a1d651c69e0a36`  
		Last Modified: Tue, 13 Jan 2026 02:01:32 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4981255760d73d5b0d192b763648c61e43362dc442ab75f3537008a4f1801e82`  
		Last Modified: Tue, 13 Jan 2026 02:01:30 GMT  
		Size: 868.5 KB (868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdc6ee7cddd3db841a5004871713036f2dc66d7b2dce24f271bc2e958bd92e5`  
		Last Modified: Tue, 13 Jan 2026 02:01:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d4aea4f4f21716b2e41e48b81137112752e200efa0740c1662523b64a5a0b`  
		Last Modified: Tue, 13 Jan 2026 02:02:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:14:40 GMT  
		Size: 13.1 MB (13061924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91448c165d0b22ae0e931fd21274cbcea247da4e62d05511f996b191d7ab1b9e`  
		Last Modified: Tue, 13 Jan 2026 04:14:41 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:ebfe5c57edc99a7e0b7e3a0ecdff8851fef32fab45470409c031e9d4b392d7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361436264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f6bb4fd5cea8e8222e6dc263216bad7abee6fd8c70fb1ffc567bedb3e56660`
-	Default Command: `["R"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1766966400'
# Tue, 30 Dec 2025 17:27:57 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 30 Dec 2025 17:27:57 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 30 Dec 2025 17:28:29 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:28:33 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 30 Dec 2025 17:28:33 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 30 Dec 2025 17:28:33 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Dec 2025 17:28:34 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 30 Dec 2025 17:28:34 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 30 Dec 2025 17:30:30 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:30:30 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:5a75c60b8a87177661c6b4e6d045cd20aa06dba288dc0ccace27182fc9ab2ac7`  
		Last Modified: Tue, 30 Dec 2025 15:10:00 GMT  
		Size: 53.5 MB (53522114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7cb81c778008bf715119911d5b8ddb3e1810313ff62be2208f77411d8b56a3`  
		Last Modified: Tue, 30 Dec 2025 17:32:12 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d5c046096af019231304bf88f00effc86ea07629b701646b0c058ff6ee4040`  
		Last Modified: Tue, 30 Dec 2025 17:32:16 GMT  
		Size: 27.3 MB (27318543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c63712eedbd249f5a4dc81723c4625f8c38da4741bc0efb8f147af9553b6c8b`  
		Last Modified: Tue, 30 Dec 2025 17:32:13 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8c8795ffe0f1d5330f8f35b80cb4778743aea6effb77593eab8557a7d4f96`  
		Last Modified: Tue, 30 Dec 2025 17:32:13 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d06e3dcd31306faf0a9ff22f2f20746dac372d95ade24ce1e305ba5f6e68ea`  
		Last Modified: Tue, 30 Dec 2025 17:32:18 GMT  
		Size: 279.7 MB (279723456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f6fca1473bcc6c4bdc7f900c9f93ebb0c19c1064e4e13e85c2b378d70aaf7aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12952263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164ec1de1db95c3014520b5b5e91ebef8d92865e7e2f6131bf07ed6301b31d19`

```dockerfile
```

-	Layers:
	-	`sha256:31fe2a5a9133d493f289627fcfb77782175048fcf2821f1756085b2a0928e2c1`  
		Last Modified: Tue, 30 Dec 2025 19:13:44 GMT  
		Size: 12.9 MB (12934125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d597700fca5fa1b5b98bbae228d8d92320e59cb8ac837d755047b5094b5ba48d`  
		Last Modified: Tue, 30 Dec 2025 19:13:45 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 48.4 MB (48389301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa6770a934822895ad765c0a3a209a8eb7a23affeaaed47839b86c74ac92ac7`  
		Last Modified: Tue, 13 Jan 2026 02:04:33 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70b1a288c469fe1bfc9978b5e3bfe0ea53a4a618d477bf227f017b9a2eda736`  
		Last Modified: Tue, 13 Jan 2026 02:04:37 GMT  
		Size: 27.0 MB (26975279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712ffe52fcee3360e3813c0531cf9d52daefc570489d5899a6c0794aa6bbd106`  
		Last Modified: Tue, 13 Jan 2026 02:04:33 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8276b45126cb168fdde0fb4251f61d98ab7ef83de43a054c8bd09cd071a3eda`  
		Last Modified: Tue, 13 Jan 2026 02:04:33 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7929aee6952bd67e672421a0ba8626ce6010272f975e715f4ff8a48766eb3f4`  
		Last Modified: Tue, 13 Jan 2026 02:04:39 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:15:00 GMT  
		Size: 12.8 MB (12774540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb126a4ac648a913be2b361f91a0947243e43ee55cb7997efe7f3954f19fe3bb`  
		Last Modified: Tue, 13 Jan 2026 04:15:01 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json
