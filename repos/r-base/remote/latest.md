## `r-base:latest`

```console
$ docker pull r-base@sha256:a567e31b6afcd2376f001a56e6e87577529aa7f3cbef81b1696552ef662e1671
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
$ docker pull r-base@sha256:8d0da7f57ef01b23924495af8fcec5f6e45691cc5e49e8d539a8af9cc0377c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.5 MB (915465911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0256e008dd6d09015cf3a5a433023e7bc4650ad60ca10bb66ed36de20e227ff8`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1757289600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6ab7b67a197cbaabd3b9625fc408e9e525cb4827257b84c6dffb4f74f04d2b05`  
		Last Modified: Mon, 08 Sep 2025 21:13:07 GMT  
		Size: 49.6 MB (49575039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd034a73e2a938cd5ed53f061468c1f9d8818a690efa4e56a93bbb8bed26bdf`  
		Last Modified: Mon, 08 Sep 2025 21:41:00 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0570d39cd4c6e026922992c176fef8f0af1810c197eae5148a5bf11901f45c1b`  
		Last Modified: Mon, 08 Sep 2025 21:40:57 GMT  
		Size: 26.9 MB (26899757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ad8ac5129aa65574373755dc4a0fb4ac17194501674dc72b4ef4ad72c9de0`  
		Last Modified: Mon, 08 Sep 2025 21:41:01 GMT  
		Size: 868.5 KB (868485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55ef87fbead67d1c6062caba4eba4efdf0b144eeefaa5a2061fb88374bb5f64`  
		Last Modified: Mon, 08 Sep 2025 21:40:53 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4375d1a240ea6013c734c91d303492fbbc0a05fbad2652ef8c66cd3d1dfb4f34`  
		Last Modified: Mon, 08 Sep 2025 21:42:27 GMT  
		Size: 838.1 MB (838118975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:002baaafe3f7af5ad7494c6f95aa57d3c8ba119deb7deacf4df6ca197380d057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12984417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b9e29dfe4a2df8e8a03a90f3cf32f365bce93ffc411bd20ceecf42dd76834`

```dockerfile
```

-	Layers:
	-	`sha256:3c7321a4c39f71ec8657cb0e7d61086aa22a178a9baef6cb2af29a82faf5b041`  
		Last Modified: Tue, 09 Sep 2025 00:13:22 GMT  
		Size: 13.0 MB (12966276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6418213639affcf9db570c2e668067d6e08843922ef57050e337efb7a3b53219`  
		Last Modified: Tue, 09 Sep 2025 00:13:24 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:c9662a49a2d0c52cbb28522199c28fdee302645422958eece0df65669275133b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **912.3 MB (912320082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6fce9dff098fb6caa1b09b6cc06586bdd4fd506a0a157f3d4c9235082d17bc`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1757289600'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:008c1ca0cb19a0a582dad95007bc30c33500300de3bb8e851eb4f56693a697c6`  
		Last Modified: Mon, 08 Sep 2025 21:15:15 GMT  
		Size: 49.9 MB (49863490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1c9f0bffcc2ce1a9d7848d2bc2ab31cfe47c60b85ce40b104688ba405077e8`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a9db2df6741f2c1fde5c41446a296527b2146517dfda847ace6bfd995ba8c8`  
		Last Modified: Mon, 08 Sep 2025 22:32:50 GMT  
		Size: 26.8 MB (26803828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb3278d861be01190e0708ab97b5a65622d11cf58782ace6a9467dad2158a0c`  
		Last Modified: Mon, 08 Sep 2025 22:08:13 GMT  
		Size: 868.5 KB (868485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb9c5c292fe9349f663b7a916ffc5ee6a6069718aef284beef8d44ae5dd3dbc`  
		Last Modified: Mon, 08 Sep 2025 22:08:18 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4effa052c00765fd9710f4f339d3f492a6907195abe373d31621fa55c0f80c8`  
		Last Modified: Mon, 08 Sep 2025 22:33:00 GMT  
		Size: 834.8 MB (834780622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:bda3e702f6cb60d57a4d6773cefb82511ef95ec927f7e577607d1c4109801615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13074301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7b6188a387e39bca514c8e0c41c36e8a33efbfd918b25c5fd8a797d6fce2a0`

```dockerfile
```

-	Layers:
	-	`sha256:c2b8a269ca60c619da8002770de70e45dbf4707b43ff15a202b0a27f39cc3c89`  
		Last Modified: Tue, 09 Sep 2025 00:13:33 GMT  
		Size: 13.1 MB (13056020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3cc14b504a79e032d906ba56e97a6d42c6914aaf95ab50644aa2a6b9910919e`  
		Last Modified: Tue, 09 Sep 2025 00:13:34 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:6a1cbe072806c729821e5e69e06787d7eeb8c687be0a1fd887b3bd3323449ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357883903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c88bc36e84decd6e527c48c2f4a2c62e0d343d7a31dfbc41dc50d95b044da9`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1754870400'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e0e720fbbf7674e3333bf57c0ffa5840d5f88cd640f2eef04ae4e830fee84e14`  
		Last Modified: Wed, 13 Aug 2025 12:02:08 GMT  
		Size: 53.1 MB (53103377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7d8e77520ea8a45c2aad2f094ad41b5ce1d5d5ca6783a750099a468d6b21f8`  
		Last Modified: Wed, 13 Aug 2025 11:43:31 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9528393b852edc3a972cb7825f447fadc27a9da8d64d553a326173efb740c72`  
		Last Modified: Wed, 13 Aug 2025 11:43:36 GMT  
		Size: 27.2 MB (27160787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a32704cacbbcce377241f76d838661e82a52708b7f3dcae0f9aaeb8da9fc11`  
		Last Modified: Wed, 13 Aug 2025 11:43:31 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b6f37d953ef3b0181e59e5b6f3813fdad13adbc2cc89b0d6692b84b74630fe`  
		Last Modified: Wed, 13 Aug 2025 11:43:31 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dcd10608e90c523fbbabf09b0a76f2ed43f36547e32afe72a1b72a7a5fff13`  
		Last Modified: Wed, 13 Aug 2025 12:59:08 GMT  
		Size: 276.7 MB (276747589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:8c9b45617efb384cfce665d0499d4fee063b5f60c8a8ed30274031ea66a0f47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12968334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d9c958020c131728474e34050fdb27fe9ff56bc8a55b9f5505c314b86e77a`

```dockerfile
```

-	Layers:
	-	`sha256:e0c333f190321f80303f0af17f8ce9f8676505aa020b68b3957faa0c5bf523e8`  
		Last Modified: Wed, 13 Aug 2025 12:13:38 GMT  
		Size: 13.0 MB (12950153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41a725bcaece3f9c8d57dc4752ac96e1a0dd46fafdf783fd0102f9a7b850f38`  
		Last Modified: Wed, 13 Aug 2025 12:13:39 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:28fda5ae475a671adf61657b64142060bf5a20e3db29902e15858fc7fbb7ebca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330126234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe2bf8327ff4b34da25385ca424a93e2688e1462f789f8a47bb99289fcb67f`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1754870400'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e3fba30a53b175f7d81ae2ba7c6194799d01dd14bf5dc4efae9e8516a4d5579c`  
		Last Modified: Tue, 12 Aug 2025 20:58:13 GMT  
		Size: 49.3 MB (49345158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73096ba58ebe7acba25a81caa785ab1a07d746096a98e11cc6b105390a25d3ba`  
		Last Modified: Wed, 13 Aug 2025 03:11:33 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab15386c181b6abe446474ded6534ba2d2fd5ba1eeb151bf2bb503d6fd3e8b4`  
		Last Modified: Wed, 13 Aug 2025 03:11:38 GMT  
		Size: 26.9 MB (26872471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4f23a2bd52bc028f9e08639c49cfa7b8d825ce213c3c7c8db56ac151b7587f`  
		Last Modified: Wed, 13 Aug 2025 03:11:34 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88604f1678d9f591709a02d1fde719fc0546c70ce4ac9d3a0be1fa2ab74720c`  
		Last Modified: Wed, 13 Aug 2025 03:11:32 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ca4d9b8d49902879a3319d63a0d37084c3a72d12e055ed1afff14d1201897`  
		Last Modified: Wed, 13 Aug 2025 06:19:51 GMT  
		Size: 253.0 MB (252980400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:8fed68ebe6c7f85cd1713bc1bda9951cf804217ce24f93ed9b58e9b826921b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12773666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c84751a9957a13352776464d0c9e16dbbc3b8083b1ae1506158846c43ce1c3`

```dockerfile
```

-	Layers:
	-	`sha256:82f6170a31e76b05bc4a18824e913b9540963d14a0554c5996c5e697e425e4a0`  
		Last Modified: Wed, 13 Aug 2025 06:13:47 GMT  
		Size: 12.8 MB (12755527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56bfb6a5ceaa90ab23d8fb694424d6400fd56680848145b1ba96ae645a50b116`  
		Last Modified: Wed, 13 Aug 2025 06:13:48 GMT  
		Size: 18.1 KB (18139 bytes)  
		MIME: application/vnd.in-toto+json
