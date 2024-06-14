<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.0`](#r-base440)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.0`

```console
$ docker pull r-base@sha256:2b69d053a78071fc4060e232c386b1063301235fe1d11e7c9c4bff93f82fd376
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

### `r-base:4.4.0` - linux; amd64

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

### `r-base:4.4.0` - unknown; unknown

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

### `r-base:4.4.0` - linux; arm64 variant v8

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

### `r-base:4.4.0` - unknown; unknown

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

### `r-base:4.4.0` - linux; ppc64le

```console
$ docker pull r-base@sha256:0073f73fa25a47a4256c0bed644c3790dd03f8b2de02b634cc4e43b04df408a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352638613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c672094bc74c6b890e0db4e35641934b18212819bad9be221b89f0710c8764f8`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 17:36:33 GMT
ADD file:1e419951dadece1f9151a37e9ad50f8131769e122c138fa53d258e388386961d in / 
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
	-	`sha256:d17c53859f4c9ab9a4d5fad8696f2c0eb323a7e2f067d4d131095bd5ef2b0f91`  
		Last Modified: Tue, 14 May 2024 01:27:03 GMT  
		Size: 56.5 MB (56531498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472c754b83de2021038320e36a2f932bda403b5974277febbfb18abc3145e02a`  
		Last Modified: Thu, 30 May 2024 23:46:38 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a508419ee720887bcaa95b5828dae50b5c21c7d8c285ae945d07bb2e2f8d00f`  
		Last Modified: Thu, 30 May 2024 23:46:40 GMT  
		Size: 30.1 MB (30120620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ecfba06fb5c7b56acc15430368e9efd942e4c98a927882c251c548830ad9c6`  
		Last Modified: Thu, 30 May 2024 23:46:38 GMT  
		Size: 866.3 KB (866327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a525e9a8e4c0c700c0d24fc79517b39708e7371c602819f2563efa478808f1`  
		Last Modified: Thu, 30 May 2024 23:46:39 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce402012255b5f46d0ca5bf7238bbc10844b66b13d06497a1785aaf1924a62e`  
		Last Modified: Thu, 30 May 2024 23:46:46 GMT  
		Size: 265.1 MB (265116510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.0` - unknown; unknown

```console
$ docker pull r-base@sha256:80617873458a452afb5544536be42aaef98c2f00babf97a5378b9039f44894ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12349638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b878829c398a0c85890dc085c64cd7454cc4ba4f0e344b390e68791296e77d0`

```dockerfile
```

-	Layers:
	-	`sha256:cef09f23063d5b592e09beaa56d0f6e64cf845b751eba6fb3545e7f1354472a7`  
		Last Modified: Thu, 30 May 2024 23:46:39 GMT  
		Size: 12.3 MB (12331724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b5d1b8f9e372a29befc838d86b597406543eeaa8e80ad18bf0e85ef0d2e593`  
		Last Modified: Thu, 30 May 2024 23:46:38 GMT  
		Size: 17.9 KB (17914 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.0` - linux; s390x

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

### `r-base:4.4.0` - unknown; unknown

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

## `r-base:latest`

```console
$ docker pull r-base@sha256:2b69d053a78071fc4060e232c386b1063301235fe1d11e7c9c4bff93f82fd376
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
$ docker pull r-base@sha256:0073f73fa25a47a4256c0bed644c3790dd03f8b2de02b634cc4e43b04df408a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352638613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c672094bc74c6b890e0db4e35641934b18212819bad9be221b89f0710c8764f8`
-	Default Command: `["R"]`

```dockerfile
# Wed, 24 Apr 2024 17:36:33 GMT
ADD file:1e419951dadece1f9151a37e9ad50f8131769e122c138fa53d258e388386961d in / 
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
	-	`sha256:d17c53859f4c9ab9a4d5fad8696f2c0eb323a7e2f067d4d131095bd5ef2b0f91`  
		Last Modified: Tue, 14 May 2024 01:27:03 GMT  
		Size: 56.5 MB (56531498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472c754b83de2021038320e36a2f932bda403b5974277febbfb18abc3145e02a`  
		Last Modified: Thu, 30 May 2024 23:46:38 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a508419ee720887bcaa95b5828dae50b5c21c7d8c285ae945d07bb2e2f8d00f`  
		Last Modified: Thu, 30 May 2024 23:46:40 GMT  
		Size: 30.1 MB (30120620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ecfba06fb5c7b56acc15430368e9efd942e4c98a927882c251c548830ad9c6`  
		Last Modified: Thu, 30 May 2024 23:46:38 GMT  
		Size: 866.3 KB (866327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a525e9a8e4c0c700c0d24fc79517b39708e7371c602819f2563efa478808f1`  
		Last Modified: Thu, 30 May 2024 23:46:39 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce402012255b5f46d0ca5bf7238bbc10844b66b13d06497a1785aaf1924a62e`  
		Last Modified: Thu, 30 May 2024 23:46:46 GMT  
		Size: 265.1 MB (265116510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:80617873458a452afb5544536be42aaef98c2f00babf97a5378b9039f44894ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12349638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b878829c398a0c85890dc085c64cd7454cc4ba4f0e344b390e68791296e77d0`

```dockerfile
```

-	Layers:
	-	`sha256:cef09f23063d5b592e09beaa56d0f6e64cf845b751eba6fb3545e7f1354472a7`  
		Last Modified: Thu, 30 May 2024 23:46:39 GMT  
		Size: 12.3 MB (12331724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b5d1b8f9e372a29befc838d86b597406543eeaa8e80ad18bf0e85ef0d2e593`  
		Last Modified: Thu, 30 May 2024 23:46:38 GMT  
		Size: 17.9 KB (17914 bytes)  
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
