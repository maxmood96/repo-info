<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.5.1`](#r-base451)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.5.1`

```console
$ docker pull r-base@sha256:c143ac223eff70f437c56f980ed582b4960dbb460a499b1d5119ff461a9f051b
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

### `r-base:4.5.1` - linux; amd64

```console
$ docker pull r-base@sha256:b2b37f9498b8cbd17575433e29973e328207fe2c7143f9566fb0946f72dcce45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362573721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36f1751796c4153eed549688a5bd015a3068327e826d3b06fff182ffe55fff5`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1754870400'
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
	-	`sha256:183c6c07933c216179cd1e895ff01916eb3110e79f0745835a0f37a59a4e1217`  
		Last Modified: Tue, 12 Aug 2025 20:45:06 GMT  
		Size: 49.3 MB (49278276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129329f8cd84788f34d219df69be2a8a8a0406dfe989636963489cf574f1653`  
		Last Modified: Tue, 12 Aug 2025 22:32:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fade62e54a43e42ff0a820f3639e06a3d02c06c00a0d7bb25aaddb8cc161cc0`  
		Last Modified: Wed, 13 Aug 2025 00:13:28 GMT  
		Size: 26.9 MB (26892700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc636a5d2c78a74aae357edbe79bad8ee543de84bdef92929fbea7833fe3ea`  
		Last Modified: Tue, 12 Aug 2025 22:32:59 GMT  
		Size: 868.5 KB (868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef1a384753c8d712c7ec3891f80d80ebf9babcfb770b57ecf6fa6beba12986`  
		Last Modified: Tue, 12 Aug 2025 22:33:06 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedcaa4cb84db435f0f1ce17860efa781271af7317a64d1288bf5848a4f4b197`  
		Last Modified: Wed, 13 Aug 2025 00:13:35 GMT  
		Size: 285.5 MB (285530604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.1` - unknown; unknown

```console
$ docker pull r-base@sha256:865b4b0455e9c28bafe59b219d800f9b2df3a346ab951132cb1098bb27addcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12971841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efacaaf3f3903cc6acdf524863815ed54e0f0d8ce15e7cec597d17c1fcf7b92a`

```dockerfile
```

-	Layers:
	-	`sha256:5ba08e31cf6efd001e8fb8de3b78c90e84f28c8c2a99bfb07f24bcc1d8b52f4b`  
		Last Modified: Wed, 13 Aug 2025 00:13:21 GMT  
		Size: 13.0 MB (12953700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6cb15ddd945c2a146fefa5c04100cd5d1de3c12e8bbb0f44cc6f0f044dd936c`  
		Last Modified: Wed, 13 Aug 2025 00:13:22 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.1` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:28f07fb0a454a4bf6af3c1fa3e8003af73b9e3f45fbb64d53cce285405e01425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347748032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9223a47ad29bd8748ca4faf8f83e6cb47152b80d7b29ed131726d9aee735a07a`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1754870400'
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
	-	`sha256:7906ceaece39d18b2e7c69126723c225ce46b2550c6e388f597fd687b30b7ffc`  
		Last Modified: Tue, 12 Aug 2025 22:11:59 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a950a1b0f5b321d981b402ed7a62d8068d07ab3a586682496e5cda6eab15c8`  
		Last Modified: Wed, 13 Aug 2025 06:05:04 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4ce97460937cde2c5ef9f73912d73bdf3d66706b93d4bd72597bb29c14c811`  
		Last Modified: Wed, 13 Aug 2025 06:05:06 GMT  
		Size: 26.8 MB (26797623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda1a0128251ec19b4c19c35a156b0bcca6f4fa3a069891a57f5a7c786fd77f2`  
		Last Modified: Wed, 13 Aug 2025 06:05:06 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425d9c4283e4dc5079fe487f3c8ed2cde3d56a0a0e355bd9e3339a422d1e6cb6`  
		Last Modified: Wed, 13 Aug 2025 06:05:06 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93d5493b5049ee822900742b8ba53f0ec77d0165512ce9113239eefdc7fac0c`  
		Last Modified: Wed, 13 Aug 2025 07:32:03 GMT  
		Size: 270.4 MB (270436656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.1` - unknown; unknown

```console
$ docker pull r-base@sha256:a16de4207bddeb6e1a27b0693af4a518995773bcadf4281c5d29b06eb848714b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13070699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe8d7bceb126b5d4a655ee4f7cdc4717e5cf3c525bb49ba0a6a13a2409593c3`

```dockerfile
```

-	Layers:
	-	`sha256:eb0c953494ed72497c6f140b967a52cf1ddc94f2e93715a934027cc3a926979a`  
		Last Modified: Wed, 13 Aug 2025 06:13:29 GMT  
		Size: 13.1 MB (13052418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19a25f60e186186a5d18ac9b0f9e14f097f35df5bc4a4bed4e182dfd47cca97f`  
		Last Modified: Wed, 13 Aug 2025 06:13:30 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.1` - linux; ppc64le

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

### `r-base:4.5.1` - unknown; unknown

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

### `r-base:4.5.1` - linux; s390x

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

### `r-base:4.5.1` - unknown; unknown

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

## `r-base:latest`

```console
$ docker pull r-base@sha256:c143ac223eff70f437c56f980ed582b4960dbb460a499b1d5119ff461a9f051b
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
$ docker pull r-base@sha256:b2b37f9498b8cbd17575433e29973e328207fe2c7143f9566fb0946f72dcce45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362573721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36f1751796c4153eed549688a5bd015a3068327e826d3b06fff182ffe55fff5`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1754870400'
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
	-	`sha256:183c6c07933c216179cd1e895ff01916eb3110e79f0745835a0f37a59a4e1217`  
		Last Modified: Tue, 12 Aug 2025 20:45:06 GMT  
		Size: 49.3 MB (49278276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129329f8cd84788f34d219df69be2a8a8a0406dfe989636963489cf574f1653`  
		Last Modified: Tue, 12 Aug 2025 22:32:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fade62e54a43e42ff0a820f3639e06a3d02c06c00a0d7bb25aaddb8cc161cc0`  
		Last Modified: Wed, 13 Aug 2025 00:13:28 GMT  
		Size: 26.9 MB (26892700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc636a5d2c78a74aae357edbe79bad8ee543de84bdef92929fbea7833fe3ea`  
		Last Modified: Tue, 12 Aug 2025 22:32:59 GMT  
		Size: 868.5 KB (868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef1a384753c8d712c7ec3891f80d80ebf9babcfb770b57ecf6fa6beba12986`  
		Last Modified: Tue, 12 Aug 2025 22:33:06 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedcaa4cb84db435f0f1ce17860efa781271af7317a64d1288bf5848a4f4b197`  
		Last Modified: Wed, 13 Aug 2025 00:13:35 GMT  
		Size: 285.5 MB (285530604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:865b4b0455e9c28bafe59b219d800f9b2df3a346ab951132cb1098bb27addcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12971841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efacaaf3f3903cc6acdf524863815ed54e0f0d8ce15e7cec597d17c1fcf7b92a`

```dockerfile
```

-	Layers:
	-	`sha256:5ba08e31cf6efd001e8fb8de3b78c90e84f28c8c2a99bfb07f24bcc1d8b52f4b`  
		Last Modified: Wed, 13 Aug 2025 00:13:21 GMT  
		Size: 13.0 MB (12953700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6cb15ddd945c2a146fefa5c04100cd5d1de3c12e8bbb0f44cc6f0f044dd936c`  
		Last Modified: Wed, 13 Aug 2025 00:13:22 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:28f07fb0a454a4bf6af3c1fa3e8003af73b9e3f45fbb64d53cce285405e01425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347748032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9223a47ad29bd8748ca4faf8f83e6cb47152b80d7b29ed131726d9aee735a07a`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1754870400'
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
	-	`sha256:7906ceaece39d18b2e7c69126723c225ce46b2550c6e388f597fd687b30b7ffc`  
		Last Modified: Tue, 12 Aug 2025 22:11:59 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a950a1b0f5b321d981b402ed7a62d8068d07ab3a586682496e5cda6eab15c8`  
		Last Modified: Wed, 13 Aug 2025 06:05:04 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4ce97460937cde2c5ef9f73912d73bdf3d66706b93d4bd72597bb29c14c811`  
		Last Modified: Wed, 13 Aug 2025 06:05:06 GMT  
		Size: 26.8 MB (26797623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda1a0128251ec19b4c19c35a156b0bcca6f4fa3a069891a57f5a7c786fd77f2`  
		Last Modified: Wed, 13 Aug 2025 06:05:06 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425d9c4283e4dc5079fe487f3c8ed2cde3d56a0a0e355bd9e3339a422d1e6cb6`  
		Last Modified: Wed, 13 Aug 2025 06:05:06 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93d5493b5049ee822900742b8ba53f0ec77d0165512ce9113239eefdc7fac0c`  
		Last Modified: Wed, 13 Aug 2025 07:32:03 GMT  
		Size: 270.4 MB (270436656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:a16de4207bddeb6e1a27b0693af4a518995773bcadf4281c5d29b06eb848714b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13070699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe8d7bceb126b5d4a655ee4f7cdc4717e5cf3c525bb49ba0a6a13a2409593c3`

```dockerfile
```

-	Layers:
	-	`sha256:eb0c953494ed72497c6f140b967a52cf1ddc94f2e93715a934027cc3a926979a`  
		Last Modified: Wed, 13 Aug 2025 06:13:29 GMT  
		Size: 13.1 MB (13052418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19a25f60e186186a5d18ac9b0f9e14f097f35df5bc4a4bed4e182dfd47cca97f`  
		Last Modified: Wed, 13 Aug 2025 06:13:30 GMT  
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
