<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.1`](#r-base441)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.1`

```console
$ docker pull r-base@sha256:619ae385ea3d449433add6247b682f6f5a36a787a5deb57d1b323d4c4856805d
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

### `r-base:4.4.1` - linux; amd64

```console
$ docker pull r-base@sha256:d4a6c9d9bd4f60958392bb619d3fac438342ec3a68a5fac1bd18f82ab47a550f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.2 MB (369217450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42279fff3881e232cd62b4404e798e200351e178a3c28d51dc7ec14323c1e2d`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:619723247570b0124cdbdcd330640fb9768a7a0580fcd6674fc64a59361d9b61 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:082e67d038aa34d78979422af7626a1fa8594a4afa81d6465c09f9626234451e`  
		Last Modified: Tue, 23 Jul 2024 05:30:14 GMT  
		Size: 52.8 MB (52821221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63019cb4f70083a8f6d226b3cb6b35e512b6d9bc9f21c75b4b09706b8b2e6e04`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ca2ee447c3a44bbea026d515e3b4159734b453198ca151245de106d6c224f`  
		Last Modified: Tue, 23 Jul 2024 06:21:05 GMT  
		Size: 29.1 MB (29061492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a5cc0c1d108990afeb7e8cbd404eaa149bbc727ccaf00edbc4c5c2f9ca28de`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 866.7 KB (866721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783363ecf354c92210593d9bd224ea37737492a6de08f85de1891f440f47ebd6`  
		Last Modified: Tue, 23 Jul 2024 06:21:05 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaf50c4513920e5b062b36cb655b72263b9ae9faf08f0a6ed807800351647a3`  
		Last Modified: Tue, 23 Jul 2024 06:21:09 GMT  
		Size: 286.5 MB (286464356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.1` - unknown; unknown

```console
$ docker pull r-base@sha256:5aebc8fc541776daafb37895b17217cbe27ea19afd59370da2076cca5074f8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12436910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bf82f5e866d43a4d058a685f7ab6080e20d6927ebaf0120c0474c6b4279e5d`

```dockerfile
```

-	Layers:
	-	`sha256:5e013cf08cf1d927c7aadc5ff98b5776545df40c7b8a80fa939d0ef94627c5bd`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 12.4 MB (12418981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d9310389ff18be48145aed662eb549780762ae472fe3eaabb403a27ed2ed30`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.1` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:15dad49f06e363746472f322c284da57f99120b67ce3080e34907fc84382fb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362557881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f208ea591430c5f950d0d9152cf5eadd7dee63a2b25cf117635943a082c8c00`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:191eea951292a448fdf8391f23851acc883220c3612e40314b0a5264d37462a3 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:8178889186a4cf7f663eadfa45ade24cd1b46b0ef61e6ea2ad08abad38cc802b`  
		Last Modified: Tue, 23 Jul 2024 04:22:35 GMT  
		Size: 53.0 MB (53026332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ee50d947abc4b4591bea23448370e6887d3def243a37cfe38170e33dceb8d`  
		Last Modified: Wed, 24 Jul 2024 06:57:47 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1317302adf352a1eeb1529d1cc9e66709d557b3cc1f0b491894e0ce809caf6b`  
		Last Modified: Wed, 24 Jul 2024 06:57:49 GMT  
		Size: 29.1 MB (29059072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa57c2c2165836ce9961cd30da2f59c669c6a7ac04e3be0d0754bb61c12e94a`  
		Last Modified: Wed, 24 Jul 2024 06:57:48 GMT  
		Size: 866.7 KB (866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2179cb94ab79e80c3c05d7b647d50e589c48c532a2581d64e55cc5992b98ef8e`  
		Last Modified: Wed, 24 Jul 2024 06:57:48 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0996070b1994fe170579aa2ddb1d7f5769902690ced628ee1234361261c03ba`  
		Last Modified: Wed, 24 Jul 2024 06:57:56 GMT  
		Size: 279.6 MB (279602084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.1` - unknown; unknown

```console
$ docker pull r-base@sha256:3185eaa57870bfe82abe9b7fa0daba49421ad0f71fec8c1e1ee0b5a12f338049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12540966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10fc1c9ec2dee2629f413416907208000c33f353d36db36bd720cd03949a150`

```dockerfile
```

-	Layers:
	-	`sha256:42b7b89e3b2d94719089858d95d1ca5e4f38813bac8ab1e4fe6e26a92bfc4b43`  
		Last Modified: Wed, 24 Jul 2024 06:57:48 GMT  
		Size: 12.5 MB (12522758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ddd3077fa079a1501cfcc50040b25813454586e88ad8ed92eb7ef7c14e1d306`  
		Last Modified: Wed, 24 Jul 2024 06:57:47 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.1` - linux; ppc64le

```console
$ docker pull r-base@sha256:96eb6287ac901e1edc0dfda8d55dc37c3a5e63ca8d21134ed863913c39131490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.4 MB (374395940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05289fc54873bb0113be1b57a1bc3eef91ac31613b9100d45d1e8ee5b155b245`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:a2a9ed566b597667e2ca2f80c13e7f6156ef9de7770cd85f3275359c96ec5da5 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:720dc0d16caf9c5de466cdb031bdddbf8af5b09238053dbfe371c831d5114ecf`  
		Last Modified: Tue, 23 Jul 2024 01:33:54 GMT  
		Size: 56.7 MB (56722063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5280d9f54347399d284737f05fbb83a203b60b09a62a45e451741008c54e23b`  
		Last Modified: Wed, 24 Jul 2024 09:57:24 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9d80167bed71b30612af104dbed72011e4d094cfd9ad542c943e56c3d28c73`  
		Last Modified: Wed, 24 Jul 2024 09:57:26 GMT  
		Size: 30.1 MB (30143456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fb9c6ae754d8e74257c39045553f9a1c8dcb0602bba31ebb06675caafa4e2d`  
		Last Modified: Wed, 24 Jul 2024 09:57:24 GMT  
		Size: 866.7 KB (866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2813a22799aaa6729bedd595f219a418cb2e46b6cef29d35d3513c974c2258c`  
		Last Modified: Wed, 24 Jul 2024 09:57:25 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8055919e5f844b33c2129d0dfd94f5d9e0a98d791bd5aa0c095706d0466c31`  
		Last Modified: Wed, 24 Jul 2024 09:57:38 GMT  
		Size: 286.7 MB (286660028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.1` - unknown; unknown

```console
$ docker pull r-base@sha256:f2643eb1082cc5bf50bf235af99d42b5a19777df674737071eb045a626d36ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12437263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ae47a7a92d259a7f25663d01ffe113e5bab496de6a80cda1dddf371bbf4e5d`

```dockerfile
```

-	Layers:
	-	`sha256:3fbe8f41089d0fedd71822966e008d0b59718a5b799a2420fa15c9b61af35865`  
		Last Modified: Wed, 24 Jul 2024 09:57:25 GMT  
		Size: 12.4 MB (12419300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ffa7d9ebc0aa5cde1bbf5750f6b78f72adccf5ba74ae9da5f3803dfe7a6373`  
		Last Modified: Wed, 24 Jul 2024 09:57:24 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.1` - linux; s390x

```console
$ docker pull r-base@sha256:ba647584b44eed9ea0f67d559e5bf5dc36682bc0b551978350953be37ef935ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343564614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10334b300ebc2d946c5989e2ac467c8719804c7e5ff89d3a3854524ffd3e8cc4`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:c24c5de69f78a6ef3e0df2856d26ea708ca0ebdee3694d47c33faaf3b5a060ff in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:79d588d68b7011912ab3b5fa8c08ba9b146dab2ef01b4ce5b083d84fffa630d7`  
		Last Modified: Tue, 23 Jul 2024 02:34:36 GMT  
		Size: 52.4 MB (52414249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59282ce1e2f75f5effa8d9bb61e4fe84d553eda0a395212e289acc59fc4b2601`  
		Last Modified: Wed, 24 Jul 2024 08:33:52 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312e4836a3104bf291ac121457ae865e7e0ed0f226008a234a3b2fe47e53da75`  
		Last Modified: Wed, 24 Jul 2024 08:33:53 GMT  
		Size: 28.5 MB (28508009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c408f87d2cfcc0a976518fc57bf6d655fe679a63c49a31bc26a5e3660ba4fc`  
		Last Modified: Wed, 24 Jul 2024 08:33:52 GMT  
		Size: 923.5 KB (923485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37780c874ac6f2d2b614a1ee55ac7cac331926afdc12f36bd8be21e6167cfba9`  
		Last Modified: Wed, 24 Jul 2024 08:33:53 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb62a429814508bf37d45ea72e2d088dd153e6812abeb70554a77b0d75bb1a9`  
		Last Modified: Wed, 24 Jul 2024 08:33:58 GMT  
		Size: 261.7 MB (261715210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.1` - unknown; unknown

```console
$ docker pull r-base@sha256:c3efe5651d350de11fe1dce73b99bc5564d9df322a59ecb29c52bbcab165a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12244484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4be4a990ffb3bb6c25b6e8406d5f4ba74d8e4abf790f9f5351fa9ce82d23cb`

```dockerfile
```

-	Layers:
	-	`sha256:8c30b15ef47d47bda1e1d7b83c364bc627a7478df0b5f25d565503c09c6757fb`  
		Last Modified: Wed, 24 Jul 2024 08:33:53 GMT  
		Size: 12.2 MB (12226556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496cfacde5aabdc09bf5e5745e3f1f1277600065f47e1a3b3cfaff25899fa5ad`  
		Last Modified: Wed, 24 Jul 2024 08:33:52 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:619ae385ea3d449433add6247b682f6f5a36a787a5deb57d1b323d4c4856805d
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
$ docker pull r-base@sha256:d4a6c9d9bd4f60958392bb619d3fac438342ec3a68a5fac1bd18f82ab47a550f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.2 MB (369217450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42279fff3881e232cd62b4404e798e200351e178a3c28d51dc7ec14323c1e2d`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:619723247570b0124cdbdcd330640fb9768a7a0580fcd6674fc64a59361d9b61 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:082e67d038aa34d78979422af7626a1fa8594a4afa81d6465c09f9626234451e`  
		Last Modified: Tue, 23 Jul 2024 05:30:14 GMT  
		Size: 52.8 MB (52821221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63019cb4f70083a8f6d226b3cb6b35e512b6d9bc9f21c75b4b09706b8b2e6e04`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ca2ee447c3a44bbea026d515e3b4159734b453198ca151245de106d6c224f`  
		Last Modified: Tue, 23 Jul 2024 06:21:05 GMT  
		Size: 29.1 MB (29061492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a5cc0c1d108990afeb7e8cbd404eaa149bbc727ccaf00edbc4c5c2f9ca28de`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 866.7 KB (866721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783363ecf354c92210593d9bd224ea37737492a6de08f85de1891f440f47ebd6`  
		Last Modified: Tue, 23 Jul 2024 06:21:05 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaf50c4513920e5b062b36cb655b72263b9ae9faf08f0a6ed807800351647a3`  
		Last Modified: Tue, 23 Jul 2024 06:21:09 GMT  
		Size: 286.5 MB (286464356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:5aebc8fc541776daafb37895b17217cbe27ea19afd59370da2076cca5074f8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12436910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bf82f5e866d43a4d058a685f7ab6080e20d6927ebaf0120c0474c6b4279e5d`

```dockerfile
```

-	Layers:
	-	`sha256:5e013cf08cf1d927c7aadc5ff98b5776545df40c7b8a80fa939d0ef94627c5bd`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 12.4 MB (12418981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d9310389ff18be48145aed662eb549780762ae472fe3eaabb403a27ed2ed30`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:15dad49f06e363746472f322c284da57f99120b67ce3080e34907fc84382fb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362557881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f208ea591430c5f950d0d9152cf5eadd7dee63a2b25cf117635943a082c8c00`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:191eea951292a448fdf8391f23851acc883220c3612e40314b0a5264d37462a3 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:8178889186a4cf7f663eadfa45ade24cd1b46b0ef61e6ea2ad08abad38cc802b`  
		Last Modified: Tue, 23 Jul 2024 04:22:35 GMT  
		Size: 53.0 MB (53026332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ee50d947abc4b4591bea23448370e6887d3def243a37cfe38170e33dceb8d`  
		Last Modified: Wed, 24 Jul 2024 06:57:47 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1317302adf352a1eeb1529d1cc9e66709d557b3cc1f0b491894e0ce809caf6b`  
		Last Modified: Wed, 24 Jul 2024 06:57:49 GMT  
		Size: 29.1 MB (29059072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa57c2c2165836ce9961cd30da2f59c669c6a7ac04e3be0d0754bb61c12e94a`  
		Last Modified: Wed, 24 Jul 2024 06:57:48 GMT  
		Size: 866.7 KB (866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2179cb94ab79e80c3c05d7b647d50e589c48c532a2581d64e55cc5992b98ef8e`  
		Last Modified: Wed, 24 Jul 2024 06:57:48 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0996070b1994fe170579aa2ddb1d7f5769902690ced628ee1234361261c03ba`  
		Last Modified: Wed, 24 Jul 2024 06:57:56 GMT  
		Size: 279.6 MB (279602084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:3185eaa57870bfe82abe9b7fa0daba49421ad0f71fec8c1e1ee0b5a12f338049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12540966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10fc1c9ec2dee2629f413416907208000c33f353d36db36bd720cd03949a150`

```dockerfile
```

-	Layers:
	-	`sha256:42b7b89e3b2d94719089858d95d1ca5e4f38813bac8ab1e4fe6e26a92bfc4b43`  
		Last Modified: Wed, 24 Jul 2024 06:57:48 GMT  
		Size: 12.5 MB (12522758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ddd3077fa079a1501cfcc50040b25813454586e88ad8ed92eb7ef7c14e1d306`  
		Last Modified: Wed, 24 Jul 2024 06:57:47 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:96eb6287ac901e1edc0dfda8d55dc37c3a5e63ca8d21134ed863913c39131490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.4 MB (374395940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05289fc54873bb0113be1b57a1bc3eef91ac31613b9100d45d1e8ee5b155b245`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:a2a9ed566b597667e2ca2f80c13e7f6156ef9de7770cd85f3275359c96ec5da5 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:720dc0d16caf9c5de466cdb031bdddbf8af5b09238053dbfe371c831d5114ecf`  
		Last Modified: Tue, 23 Jul 2024 01:33:54 GMT  
		Size: 56.7 MB (56722063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5280d9f54347399d284737f05fbb83a203b60b09a62a45e451741008c54e23b`  
		Last Modified: Wed, 24 Jul 2024 09:57:24 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9d80167bed71b30612af104dbed72011e4d094cfd9ad542c943e56c3d28c73`  
		Last Modified: Wed, 24 Jul 2024 09:57:26 GMT  
		Size: 30.1 MB (30143456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fb9c6ae754d8e74257c39045553f9a1c8dcb0602bba31ebb06675caafa4e2d`  
		Last Modified: Wed, 24 Jul 2024 09:57:24 GMT  
		Size: 866.7 KB (866729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2813a22799aaa6729bedd595f219a418cb2e46b6cef29d35d3513c974c2258c`  
		Last Modified: Wed, 24 Jul 2024 09:57:25 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8055919e5f844b33c2129d0dfd94f5d9e0a98d791bd5aa0c095706d0466c31`  
		Last Modified: Wed, 24 Jul 2024 09:57:38 GMT  
		Size: 286.7 MB (286660028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f2643eb1082cc5bf50bf235af99d42b5a19777df674737071eb045a626d36ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12437263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ae47a7a92d259a7f25663d01ffe113e5bab496de6a80cda1dddf371bbf4e5d`

```dockerfile
```

-	Layers:
	-	`sha256:3fbe8f41089d0fedd71822966e008d0b59718a5b799a2420fa15c9b61af35865`  
		Last Modified: Wed, 24 Jul 2024 09:57:25 GMT  
		Size: 12.4 MB (12419300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ffa7d9ebc0aa5cde1bbf5750f6b78f72adccf5ba74ae9da5f3803dfe7a6373`  
		Last Modified: Wed, 24 Jul 2024 09:57:24 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:ba647584b44eed9ea0f67d559e5bf5dc36682bc0b551978350953be37ef935ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343564614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10334b300ebc2d946c5989e2ac467c8719804c7e5ff89d3a3854524ffd3e8cc4`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:c24c5de69f78a6ef3e0df2856d26ea708ca0ebdee3694d47c33faaf3b5a060ff in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:79d588d68b7011912ab3b5fa8c08ba9b146dab2ef01b4ce5b083d84fffa630d7`  
		Last Modified: Tue, 23 Jul 2024 02:34:36 GMT  
		Size: 52.4 MB (52414249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59282ce1e2f75f5effa8d9bb61e4fe84d553eda0a395212e289acc59fc4b2601`  
		Last Modified: Wed, 24 Jul 2024 08:33:52 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312e4836a3104bf291ac121457ae865e7e0ed0f226008a234a3b2fe47e53da75`  
		Last Modified: Wed, 24 Jul 2024 08:33:53 GMT  
		Size: 28.5 MB (28508009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c408f87d2cfcc0a976518fc57bf6d655fe679a63c49a31bc26a5e3660ba4fc`  
		Last Modified: Wed, 24 Jul 2024 08:33:52 GMT  
		Size: 923.5 KB (923485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37780c874ac6f2d2b614a1ee55ac7cac331926afdc12f36bd8be21e6167cfba9`  
		Last Modified: Wed, 24 Jul 2024 08:33:53 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb62a429814508bf37d45ea72e2d088dd153e6812abeb70554a77b0d75bb1a9`  
		Last Modified: Wed, 24 Jul 2024 08:33:58 GMT  
		Size: 261.7 MB (261715210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:c3efe5651d350de11fe1dce73b99bc5564d9df322a59ecb29c52bbcab165a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12244484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4be4a990ffb3bb6c25b6e8406d5f4ba74d8e4abf790f9f5351fa9ce82d23cb`

```dockerfile
```

-	Layers:
	-	`sha256:8c30b15ef47d47bda1e1d7b83c364bc627a7478df0b5f25d565503c09c6757fb`  
		Last Modified: Wed, 24 Jul 2024 08:33:53 GMT  
		Size: 12.2 MB (12226556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496cfacde5aabdc09bf5e5745e3f1f1277600065f47e1a3b3cfaff25899fa5ad`  
		Last Modified: Wed, 24 Jul 2024 08:33:52 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json
