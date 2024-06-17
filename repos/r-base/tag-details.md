<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.1`](#r-base441)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.1`

```console
$ docker pull r-base@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `r-base:latest`

```console
$ docker pull r-base@sha256:2a29b5ba91a84dd60f5706546e6165b292c7e8f4da6c07153c1a0a3a4a01e429
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
$ docker pull r-base@sha256:5dbdbc57c503e3d1488b757e27020857ad286de4e77aa5f44bb7c72c3b825698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359945038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1626bec51d3b177e576f0f5f4caa65ecb7a676a6e50a9b104a4147545259c93c`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 17:36:33 GMT
ADD file:641543c898704e70b2f0fdc6960cf28865c10fff8d9e502bca973f3032f48ee5 in / 
# Wed, 24 Apr 2024 17:36:33 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 17:36:33 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 17:36:33 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 17:36:33 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 17:36:33 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 17:36:33 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:86f6cd73387be605d114f6a6b93a5a5db028ff60a33da4e42acb4d10aa73746f`  
		Last Modified: Thu, 13 Jun 2024 01:29:06 GMT  
		Size: 52.3 MB (52277771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52033ed3730d6af01990a6e4966a9ec6d59cbdf57e190b258015087c305d5575`  
		Last Modified: Thu, 13 Jun 2024 18:31:03 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d0e5723b117f9e8832bdde445e3821fc7792bda7ca8fafdd87fe58860b0f7f`  
		Last Modified: Thu, 13 Jun 2024 18:31:03 GMT  
		Size: 23.1 MB (23104107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82100ceefafdf10600a12614cf5ccab63f77f1e02212d75d66b6008a1bc1348`  
		Last Modified: Thu, 13 Jun 2024 18:31:03 GMT  
		Size: 866.3 KB (866326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359377d70b3b45e3c018837e81ed007a021f09d08642f2498f12569c84de1a90`  
		Last Modified: Thu, 13 Jun 2024 18:31:04 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84c3854da39ab5b8b8051ac2989ce391f327e03399cc19e1b4b2519d90634f`  
		Last Modified: Thu, 13 Jun 2024 18:31:08 GMT  
		Size: 283.7 MB (283693174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:dba0d0bcb2c3c2b4ed4b1c17357d2639f29523e73fdfefdc44bebceefd18d050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12363970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acefaa46e8a81ef5bf1d9566dc94758bc4580e553685a495b182a28f5db97029`

```dockerfile
```

-	Layers:
	-	`sha256:81147e34c84b495924643c7fbb87870de1afc881f7f18e7784191a513f5641e4`  
		Last Modified: Thu, 13 Jun 2024 18:31:03 GMT  
		Size: 12.3 MB (12346042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e775ccf4197ffaa127155d30781bcdc4de83a2db103f6e0516b6cb79289be63`  
		Last Modified: Thu, 13 Jun 2024 18:31:03 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:462f6785d870ef2cee6d1c5ba15be28c2d14bb7c783174a4976373f987bd43cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345445029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c62538679b081642d3a86330700074b081bb965f668e6d0550ddd3791a8fef`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 17:36:33 GMT
ADD file:01c0f4d76bf24fca2751abe72efa9c7df45d0b92b1a1e4ec04166ae4f86e0e5e in / 
# Wed, 24 Apr 2024 17:36:33 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 17:36:33 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 17:36:33 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 17:36:33 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 17:36:33 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 17:36:33 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bf8309700f9bbb327bede604070aa78243b4af661147b0f82fa09c9fee807790`  
		Last Modified: Thu, 13 Jun 2024 00:46:35 GMT  
		Size: 52.5 MB (52514403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600a4a7abde0d128b958ada7041967bf0bc7e8d1c421fd211cd3dea7299f6de1`  
		Last Modified: Fri, 14 Jun 2024 01:15:31 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2c2a2f75707bb2fecc7c06b17c1926d2f32a79b0dcd205287589b1dbf042c`  
		Last Modified: Fri, 14 Jun 2024 01:15:32 GMT  
		Size: 23.1 MB (23088718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b41e3af61026d979c57a33df77d062b4c047302f92a0c9360f95da0219ffc5`  
		Last Modified: Fri, 14 Jun 2024 01:15:32 GMT  
		Size: 866.3 KB (866328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a285d402501daaa7ff64921613e8190d86dd9a3b4541ccc9d2034cbc8778d25`  
		Last Modified: Fri, 14 Jun 2024 01:15:32 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fca8d61768f450d4521f0499b759ee3fd797327cf43d810a33f176298eba67`  
		Last Modified: Fri, 14 Jun 2024 01:15:39 GMT  
		Size: 269.0 MB (268971922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:bcb4beccc1c15d077bd238fdcf37302bf7010bd935d4334808b9c881163bbce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12409781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcd02ebe1e913b266e793ae8f0b3150efbcb5ffae6f6676d72940f09349a939`

```dockerfile
```

-	Layers:
	-	`sha256:43f6fe0ecfdb4f13464cccbd8a9b7838c176240d2a5162f7938dd16ea21af613`  
		Last Modified: Fri, 14 Jun 2024 01:15:32 GMT  
		Size: 12.4 MB (12391573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136f73c450bd7ebdb4de1658c6250509f40f6f4dd2b520f50c5355dd1e9b0a12`  
		Last Modified: Fri, 14 Jun 2024 01:15:31 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:5eb94373d943c17f9e3a7d339331514888093bdf5f680377ca7626089bbbac30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351062133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b52a64f5a4c7e09f23dc2c0ed23f62ef0caa20e52a3ba16cc6cfeef5be71c08`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 17:36:33 GMT
ADD file:a0c25580162c011cc186a00ff527d3dccd6ebde9583f49d925d9c4a0bcf07470 in / 
# Wed, 24 Apr 2024 17:36:33 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 17:36:33 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 17:36:33 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 17:36:33 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 17:36:33 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 17:36:33 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c17ef498846c0b5766aa996aaf6ece599537a2132a98b21abc95e98de5797774`  
		Last Modified: Thu, 13 Jun 2024 01:24:41 GMT  
		Size: 56.1 MB (56146522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf17d59ea2618f21d2f6298f4aca59b482668c00c5d8bbe1dceb4b36e69c1915`  
		Last Modified: Fri, 14 Jun 2024 05:13:56 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01df415577231747e399a2a9caed4e453cbe90669562e40f9759aa093ab1c91b`  
		Last Modified: Fri, 14 Jun 2024 05:13:58 GMT  
		Size: 30.1 MB (30124447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64daafafffbe5fa554b9e80872335f55389dc28cfed0c0e847418168d0d8602a`  
		Last Modified: Fri, 14 Jun 2024 05:13:56 GMT  
		Size: 866.3 KB (866329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb17b4b8171d4c9f61cc4b9980f01fddd81af5521c304a6a19a8e1d73aed689d`  
		Last Modified: Fri, 14 Jun 2024 05:13:57 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c351e500a48d692d73c1ca4c00b38fa8801f9851c664fa4473e01042f3458a9`  
		Last Modified: Fri, 14 Jun 2024 05:14:04 GMT  
		Size: 263.9 MB (263921175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:66a60cfe494de9867821eaae12c22ce743094a1371bdb9d278eb17b35ea6b01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12336819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ebff7ddaf4b3aef6384389889467824254f155d8523288054d495653e166c2`

```dockerfile
```

-	Layers:
	-	`sha256:e366efc7c12922f21aab11504141816d3444ddfb0f2dd089b1d8f248f62943ce`  
		Last Modified: Fri, 14 Jun 2024 05:13:57 GMT  
		Size: 12.3 MB (12318856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6786b4ba5b8bbf3fa22185a8955cd6fa4fc0c306f7de1d0ac0b006270937be`  
		Last Modified: Fri, 14 Jun 2024 05:13:56 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:021c4ef3a185d805dd63295d4fc5405ce1b2946dd819088883f43233cc8a7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329787814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1744a709eaaddb3f20d2ea7022c9f547dbb44b22cb10020e5818f92fff53aa6a`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 17:36:33 GMT
ADD file:10228c4b34e8ce576af7bd79fcb17c133b1ea50ced4c4e3086c0d133e54eb0a8 in / 
# Wed, 24 Apr 2024 17:36:33 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 17:36:33 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 24 Apr 2024 17:36:33 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 24 Apr 2024 17:36:33 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Apr 2024 17:36:33 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
ENV R_BASE_VERSION=4.4.0
# Wed, 24 Apr 2024 17:36:33 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 17:36:33 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6eb6b57af9d4e65be8055ff33f3b560adcb2c0d5f354553283f30c55e9a081f3`  
		Last Modified: Thu, 13 Jun 2024 00:49:43 GMT  
		Size: 51.9 MB (51895345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04249ea9dcc36fa3a64d73b3a3e537928ba8beedf83c762f849918174eef64e`  
		Last Modified: Thu, 13 Jun 2024 12:39:44 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042f7cfa1e706dc9a7aec15a7f890607019b188d0268dd6f4a34459c215bac80`  
		Last Modified: Thu, 13 Jun 2024 12:39:47 GMT  
		Size: 23.2 MB (23211640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6d562641d54f66850fc3f64b72e825e7c26d99173106df91f138fb1f636027`  
		Last Modified: Thu, 13 Jun 2024 12:39:45 GMT  
		Size: 922.3 KB (922278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301375afdecf9c6913b104cdf8175803f5ab96beb88c38bac0ee3f72a59c5ac0`  
		Last Modified: Thu, 13 Jun 2024 12:39:46 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18bba2c794dd03a6252507ea45b7dbb2664c607f3a02bd87c823eb307c9b20`  
		Last Modified: Thu, 13 Jun 2024 12:39:50 GMT  
		Size: 253.8 MB (253754894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:054167353d1cba1b73c27d07a908cb3063462f93c1afaa401e37169995fb2113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12183854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36ac2680b27b5de7ba7792d0af19a21141170144a6df4038801a9b6f706b13b`

```dockerfile
```

-	Layers:
	-	`sha256:261451f205b5477fc46be0c86b99c0e14144ba1664913e0f64d2b151867f14da`  
		Last Modified: Thu, 13 Jun 2024 12:39:45 GMT  
		Size: 12.2 MB (12165926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2855e73d08b272152ac1678fc7c5856b302243e3e9165bade21a35faf2e321`  
		Last Modified: Thu, 13 Jun 2024 12:39:44 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json
