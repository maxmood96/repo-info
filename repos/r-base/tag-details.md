<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.3`](#r-base443)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.3`

```console
$ docker pull r-base@sha256:847de88a7ad82936513d2b57e42150ddf64de4e5f5d5a81b32805d6d178b70f6
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

### `r-base:4.4.3` - linux; amd64

```console
$ docker pull r-base@sha256:8e18d98f191e5488f5aa6160c6b8070454049663177f500e6527b1304923ce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369262265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e063072dd9b06a5c42842dadfc0a8d3a58fbe21a1e383690f181f69ef14a4a1`
-	Default Command: `["R"]`

```dockerfile
# Fri, 28 Feb 2025 21:48:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1742169600'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:85b4ea79c9044a9663d0967fea182f2820065e34d4ba470c857d90ec0a29780d`  
		Last Modified: Mon, 17 Mar 2025 22:17:42 GMT  
		Size: 47.5 MB (47513469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78ae11910e4a1bad01c4efacde85bc70b64727dc56df68267f4203fa789d8f`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231fe637949b862388f99ab5253061570254fc8ffa204c151af0e4bd88610727`  
		Last Modified: Mon, 17 Mar 2025 23:14:35 GMT  
		Size: 26.8 MB (26793687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e55f773672e38f9df0da877d93607f403a1dbd67c63aa62698b08f9c446db0`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 868.5 KB (868485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed1c5c1eb39d2360d594a382540e3e4577e9bc14eb03787bac8bd74deb1546`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e068a6f1f3c5ec52f0ca37f64f5306ae00c16f85d75cf18d0ba61c41c19235ec`  
		Last Modified: Mon, 17 Mar 2025 23:14:58 GMT  
		Size: 294.1 MB (294082967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.3` - unknown; unknown

```console
$ docker pull r-base@sha256:349a0bb8c2152ea452863bbd4fea9f83dfff3c4e8b05d6c247b1c72e71a41858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12602199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff2b9d4b7581902e6c1d7eb46ccb1f56c2e8e7830678805fa2e442ec0cde82a`

```dockerfile
```

-	Layers:
	-	`sha256:cf1ae354abf4d8f3be020d26cdee1183187eeab5c0e5a911bbe8af7c133e2799`  
		Last Modified: Mon, 17 Mar 2025 23:14:35 GMT  
		Size: 12.6 MB (12584059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3a3d8b121310cf18eb2ea73f0edeb94ab8e53827a019a72c1c1e00781931ebd`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.3` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:3f619104ff15bdccd220d8d645156c109366e7bdce577afbe2db44db04230fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339886003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79745271bd78ba71b2a215eeae33ed8b94639e5ff00478ea5530285a45bf0aa`
-	Default Command: `["R"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1740355200'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1ba3f865dd56bb9dba3c2f6254549c558cbcbe483f2fc18dc07397512a8dcef7`  
		Last Modified: Tue, 25 Feb 2025 01:33:18 GMT  
		Size: 47.9 MB (47858534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4730b1fefb48cfd6ad0da4404d252d9ffca26dbddfd01afa95753745f6b82334`  
		Last Modified: Fri, 28 Feb 2025 22:09:22 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef3583ad134d464bcc3ef27c800d84b7bfd860a834917a7fb78fbee952147b2`  
		Last Modified: Fri, 28 Feb 2025 22:09:23 GMT  
		Size: 26.7 MB (26674973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338efe9d9ddedc28b8c2a5481b61bd53a1a3a28f488fe05110852df6dbda5d53`  
		Last Modified: Fri, 28 Feb 2025 22:09:23 GMT  
		Size: 866.7 KB (866740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253682ba7f10f8c62955deac167903c846bdafe3e00096f6c06f14c81e96374d`  
		Last Modified: Fri, 28 Feb 2025 22:09:22 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b337e8a0a01fd5bd17e05f4713f28327c8dff6ed151886a2697eef1339871a4`  
		Last Modified: Fri, 28 Feb 2025 22:09:30 GMT  
		Size: 264.5 MB (264482093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.3` - unknown; unknown

```console
$ docker pull r-base@sha256:8efec43b4ebe39f4ce973edbc59481ec17a0c9b08683348bf8d45c398db49a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12698133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1962a22ee9d4e1d0409b2a4462933ccc62d7101c412875566b0ae848a76411`

```dockerfile
```

-	Layers:
	-	`sha256:9b8d971469e62da530a6835c2df22afb7176506f21810999a6268e4b64b4d390`  
		Last Modified: Fri, 28 Feb 2025 22:09:23 GMT  
		Size: 12.7 MB (12679852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68e5e12642cc73c544d10257c7dcc438309f0affebd6f170e007c2d36111646`  
		Last Modified: Fri, 28 Feb 2025 22:09:22 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.3` - linux; ppc64le

```console
$ docker pull r-base@sha256:77ba1118aa606f9b26ca1cfda2d860d334575f901bbfefbd7c18fa0a83bd8440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364164979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a924d28610d4d7f1c82b68d78fb4391336ef10664b5a1c0653861190c553d82f`
-	Default Command: `["R"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1740355200'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2276a3a1acdb1d83dfa8fd7fcc9aab866253476e92fa90d5743936d20f8ff598`  
		Last Modified: Tue, 25 Feb 2025 01:33:08 GMT  
		Size: 51.1 MB (51131293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02084ecd8c4f862f63a884865f470874e0653ba6a16d6bacaec1176fc6b4e961`  
		Last Modified: Fri, 28 Feb 2025 22:11:00 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fb517d474d5314c42210729fe4fd675c88b968ecacba64bcb2d7c27c708f8f`  
		Last Modified: Fri, 28 Feb 2025 22:11:01 GMT  
		Size: 27.0 MB (27031836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552ba7f7e251b8f60926e2eb1bd72aa63592f1ef3a8c271e1407fc4eceec487`  
		Last Modified: Fri, 28 Feb 2025 22:11:00 GMT  
		Size: 866.7 KB (866748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6a6261182fb637e97eca3635967b2da55768894e32cbef5b0056f158cf5a5`  
		Last Modified: Fri, 28 Feb 2025 22:11:00 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efa12596ce84735925f3f8b2e2acb22a5e2c278c1362275c3c164cb3ce47b20`  
		Last Modified: Fri, 28 Feb 2025 22:11:13 GMT  
		Size: 285.1 MB (285131445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.3` - unknown; unknown

```console
$ docker pull r-base@sha256:6ce3c25548a967e457380e4eab49fdee4af10a7cd6212c43230ebcb5396ab4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12598449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6f0806f5923341d347cd2bd5beee3c46a2a30a28c98b411ef23b0061e5decd`

```dockerfile
```

-	Layers:
	-	`sha256:230fffdeec7e3f502925e5227d3dd3bd2b8188adc400f06123edfa4fa9772ce8`  
		Last Modified: Fri, 28 Feb 2025 22:11:01 GMT  
		Size: 12.6 MB (12580270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e552325ed11625ea19aa755efb17232d92af62ff009047bb15edc0dc69892d`  
		Last Modified: Fri, 28 Feb 2025 22:11:00 GMT  
		Size: 18.2 KB (18179 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.3` - linux; s390x

```console
$ docker pull r-base@sha256:9b0477f3b7369ae154e6f912dbe4eefbefe7489f01bdce34f3ddabf69c801a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322684562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25862d07f38bdcb30a87335f3b3fabd4321446c9b32e492526c46b23a10fc39f`
-	Default Command: `["R"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1740355200'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:dd378ad4dce685db0a75f42815a10d1e203fbf6600c696e54ca892740beee866`  
		Last Modified: Tue, 25 Feb 2025 01:33:20 GMT  
		Size: 47.5 MB (47508263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d2decaa67742df0a46e420bec2c28f09c42cabb5ff6a5ba706c7f87b1137cc`  
		Last Modified: Fri, 28 Feb 2025 22:10:54 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b1e4bcfd3cda77ebfabdb6472db315e61a9d5cf1c9287b14a48e28adb95718`  
		Last Modified: Fri, 28 Feb 2025 22:10:55 GMT  
		Size: 26.7 MB (26745581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5180ae153d5b0af3ff833531b7c7c343fbceb5130b6958a753fd5c33cce3c9`  
		Last Modified: Fri, 28 Feb 2025 22:10:54 GMT  
		Size: 923.5 KB (923483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253682ba7f10f8c62955deac167903c846bdafe3e00096f6c06f14c81e96374d`  
		Last Modified: Fri, 28 Feb 2025 22:09:22 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc31303283d63ad3748bde317923cc5d56f4b586018cfe5254dfe1738dd84f`  
		Last Modified: Fri, 28 Feb 2025 22:10:59 GMT  
		Size: 247.5 MB (247503572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.3` - unknown; unknown

```console
$ docker pull r-base@sha256:4808106cb2d992fad9eda1b051812eacac2c43d1985f76c7632e2c0af85b60fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12404616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b73c0ed6130310e42bc1ef66c53fbd0d632ca5205e63652732a7e140417574`

```dockerfile
```

-	Layers:
	-	`sha256:e2e1455bc48538c4b969e3ab71a954d3cded9ffc2f3715b01bc57d0d6606eb88`  
		Last Modified: Fri, 28 Feb 2025 22:10:54 GMT  
		Size: 12.4 MB (12386475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a677b261566420a5535541b42db44ca3070d5cf487c30004f30817add23ca0af`  
		Last Modified: Fri, 28 Feb 2025 22:10:54 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:847de88a7ad82936513d2b57e42150ddf64de4e5f5d5a81b32805d6d178b70f6
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
$ docker pull r-base@sha256:8e18d98f191e5488f5aa6160c6b8070454049663177f500e6527b1304923ce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369262265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e063072dd9b06a5c42842dadfc0a8d3a58fbe21a1e383690f181f69ef14a4a1`
-	Default Command: `["R"]`

```dockerfile
# Fri, 28 Feb 2025 21:48:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1742169600'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:85b4ea79c9044a9663d0967fea182f2820065e34d4ba470c857d90ec0a29780d`  
		Last Modified: Mon, 17 Mar 2025 22:17:42 GMT  
		Size: 47.5 MB (47513469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78ae11910e4a1bad01c4efacde85bc70b64727dc56df68267f4203fa789d8f`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231fe637949b862388f99ab5253061570254fc8ffa204c151af0e4bd88610727`  
		Last Modified: Mon, 17 Mar 2025 23:14:35 GMT  
		Size: 26.8 MB (26793687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e55f773672e38f9df0da877d93607f403a1dbd67c63aa62698b08f9c446db0`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 868.5 KB (868485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed1c5c1eb39d2360d594a382540e3e4577e9bc14eb03787bac8bd74deb1546`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e068a6f1f3c5ec52f0ca37f64f5306ae00c16f85d75cf18d0ba61c41c19235ec`  
		Last Modified: Mon, 17 Mar 2025 23:14:58 GMT  
		Size: 294.1 MB (294082967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:349a0bb8c2152ea452863bbd4fea9f83dfff3c4e8b05d6c247b1c72e71a41858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12602199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff2b9d4b7581902e6c1d7eb46ccb1f56c2e8e7830678805fa2e442ec0cde82a`

```dockerfile
```

-	Layers:
	-	`sha256:cf1ae354abf4d8f3be020d26cdee1183187eeab5c0e5a911bbe8af7c133e2799`  
		Last Modified: Mon, 17 Mar 2025 23:14:35 GMT  
		Size: 12.6 MB (12584059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3a3d8b121310cf18eb2ea73f0edeb94ab8e53827a019a72c1c1e00781931ebd`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:3f619104ff15bdccd220d8d645156c109366e7bdce577afbe2db44db04230fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339886003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79745271bd78ba71b2a215eeae33ed8b94639e5ff00478ea5530285a45bf0aa`
-	Default Command: `["R"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1740355200'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1ba3f865dd56bb9dba3c2f6254549c558cbcbe483f2fc18dc07397512a8dcef7`  
		Last Modified: Tue, 25 Feb 2025 01:33:18 GMT  
		Size: 47.9 MB (47858534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4730b1fefb48cfd6ad0da4404d252d9ffca26dbddfd01afa95753745f6b82334`  
		Last Modified: Fri, 28 Feb 2025 22:09:22 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef3583ad134d464bcc3ef27c800d84b7bfd860a834917a7fb78fbee952147b2`  
		Last Modified: Fri, 28 Feb 2025 22:09:23 GMT  
		Size: 26.7 MB (26674973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338efe9d9ddedc28b8c2a5481b61bd53a1a3a28f488fe05110852df6dbda5d53`  
		Last Modified: Fri, 28 Feb 2025 22:09:23 GMT  
		Size: 866.7 KB (866740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253682ba7f10f8c62955deac167903c846bdafe3e00096f6c06f14c81e96374d`  
		Last Modified: Fri, 28 Feb 2025 22:09:22 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b337e8a0a01fd5bd17e05f4713f28327c8dff6ed151886a2697eef1339871a4`  
		Last Modified: Fri, 28 Feb 2025 22:09:30 GMT  
		Size: 264.5 MB (264482093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:8efec43b4ebe39f4ce973edbc59481ec17a0c9b08683348bf8d45c398db49a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12698133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1962a22ee9d4e1d0409b2a4462933ccc62d7101c412875566b0ae848a76411`

```dockerfile
```

-	Layers:
	-	`sha256:9b8d971469e62da530a6835c2df22afb7176506f21810999a6268e4b64b4d390`  
		Last Modified: Fri, 28 Feb 2025 22:09:23 GMT  
		Size: 12.7 MB (12679852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68e5e12642cc73c544d10257c7dcc438309f0affebd6f170e007c2d36111646`  
		Last Modified: Fri, 28 Feb 2025 22:09:22 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:77ba1118aa606f9b26ca1cfda2d860d334575f901bbfefbd7c18fa0a83bd8440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364164979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a924d28610d4d7f1c82b68d78fb4391336ef10664b5a1c0653861190c553d82f`
-	Default Command: `["R"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1740355200'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2276a3a1acdb1d83dfa8fd7fcc9aab866253476e92fa90d5743936d20f8ff598`  
		Last Modified: Tue, 25 Feb 2025 01:33:08 GMT  
		Size: 51.1 MB (51131293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02084ecd8c4f862f63a884865f470874e0653ba6a16d6bacaec1176fc6b4e961`  
		Last Modified: Fri, 28 Feb 2025 22:11:00 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fb517d474d5314c42210729fe4fd675c88b968ecacba64bcb2d7c27c708f8f`  
		Last Modified: Fri, 28 Feb 2025 22:11:01 GMT  
		Size: 27.0 MB (27031836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552ba7f7e251b8f60926e2eb1bd72aa63592f1ef3a8c271e1407fc4eceec487`  
		Last Modified: Fri, 28 Feb 2025 22:11:00 GMT  
		Size: 866.7 KB (866748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6a6261182fb637e97eca3635967b2da55768894e32cbef5b0056f158cf5a5`  
		Last Modified: Fri, 28 Feb 2025 22:11:00 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efa12596ce84735925f3f8b2e2acb22a5e2c278c1362275c3c164cb3ce47b20`  
		Last Modified: Fri, 28 Feb 2025 22:11:13 GMT  
		Size: 285.1 MB (285131445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:6ce3c25548a967e457380e4eab49fdee4af10a7cd6212c43230ebcb5396ab4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12598449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6f0806f5923341d347cd2bd5beee3c46a2a30a28c98b411ef23b0061e5decd`

```dockerfile
```

-	Layers:
	-	`sha256:230fffdeec7e3f502925e5227d3dd3bd2b8188adc400f06123edfa4fa9772ce8`  
		Last Modified: Fri, 28 Feb 2025 22:11:01 GMT  
		Size: 12.6 MB (12580270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e552325ed11625ea19aa755efb17232d92af62ff009047bb15edc0dc69892d`  
		Last Modified: Fri, 28 Feb 2025 22:11:00 GMT  
		Size: 18.2 KB (18179 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:9b0477f3b7369ae154e6f912dbe4eefbefe7489f01bdce34f3ddabf69c801a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322684562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25862d07f38bdcb30a87335f3b3fabd4321446c9b32e492526c46b23a10fc39f`
-	Default Command: `["R"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1740355200'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:dd378ad4dce685db0a75f42815a10d1e203fbf6600c696e54ca892740beee866`  
		Last Modified: Tue, 25 Feb 2025 01:33:20 GMT  
		Size: 47.5 MB (47508263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d2decaa67742df0a46e420bec2c28f09c42cabb5ff6a5ba706c7f87b1137cc`  
		Last Modified: Fri, 28 Feb 2025 22:10:54 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b1e4bcfd3cda77ebfabdb6472db315e61a9d5cf1c9287b14a48e28adb95718`  
		Last Modified: Fri, 28 Feb 2025 22:10:55 GMT  
		Size: 26.7 MB (26745581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5180ae153d5b0af3ff833531b7c7c343fbceb5130b6958a753fd5c33cce3c9`  
		Last Modified: Fri, 28 Feb 2025 22:10:54 GMT  
		Size: 923.5 KB (923483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253682ba7f10f8c62955deac167903c846bdafe3e00096f6c06f14c81e96374d`  
		Last Modified: Fri, 28 Feb 2025 22:09:22 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc31303283d63ad3748bde317923cc5d56f4b586018cfe5254dfe1738dd84f`  
		Last Modified: Fri, 28 Feb 2025 22:10:59 GMT  
		Size: 247.5 MB (247503572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:4808106cb2d992fad9eda1b051812eacac2c43d1985f76c7632e2c0af85b60fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12404616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b73c0ed6130310e42bc1ef66c53fbd0d632ca5205e63652732a7e140417574`

```dockerfile
```

-	Layers:
	-	`sha256:e2e1455bc48538c4b969e3ab71a954d3cded9ffc2f3715b01bc57d0d6606eb88`  
		Last Modified: Fri, 28 Feb 2025 22:10:54 GMT  
		Size: 12.4 MB (12386475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a677b261566420a5535541b42db44ca3070d5cf487c30004f30817add23ca0af`  
		Last Modified: Fri, 28 Feb 2025 22:10:54 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
