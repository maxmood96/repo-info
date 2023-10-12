<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.3.1`](#r-base431)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.3.1`

```console
$ docker pull r-base@sha256:3bc82794407d9d0667cf75e1d194f9f93b8d563227a29c32e17174c24ed4b070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.3.1` - linux; amd64

```console
$ docker pull r-base@sha256:06979524919e444f50cf01c8e37403a90c7d06daf988c206c3236049f75fe3bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339689239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64c713b3583c7003979857f85f2403af438d778f02022cf780e6f380ca1abcf`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 Oct 2023 18:37:09 GMT
ADD file:21d38a28e0614f04476d0dca2e0eb55defa5f216a30c05c084c97d6d1fa90e30 in / 
# Wed, 11 Oct 2023 18:37:10 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:12:02 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 12 Oct 2023 03:12:03 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 12 Oct 2023 03:12:14 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:12:16 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 12 Oct 2023 03:12:16 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 12 Oct 2023 03:12:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Oct 2023 03:12:17 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 12 Oct 2023 03:12:17 GMT
ENV R_BASE_VERSION=4.3.1
# Thu, 12 Oct 2023 03:13:17 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:13:19 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:4b9e93079e042882107af07d114a4c10a8202361c63fbdce4fc863cd7942e65e`  
		Last Modified: Wed, 11 Oct 2023 18:43:34 GMT  
		Size: 49.5 MB (49502114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3abc00097ca006fedf22776c231e2545fd41f2432d13fa20630f8066fb1b28`  
		Last Modified: Thu, 12 Oct 2023 03:13:31 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe8cc404d321c25adc422d19c121f41aa88609c90df0646e1d50661b0d45f64`  
		Last Modified: Thu, 12 Oct 2023 03:13:34 GMT  
		Size: 25.5 MB (25517750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefbc40b273a0602aaff7ebf3927d359b4b35b478a0404c6f875c0642e69a632`  
		Last Modified: Thu, 12 Oct 2023 03:13:32 GMT  
		Size: 866.3 KB (866326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de485d51833927eeffeba8297f3c9331260d41e2de8391fc3d0a37699701f3e`  
		Last Modified: Thu, 12 Oct 2023 03:13:31 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a08c976628a0a366eea2ab6923e995d675b63353914bbb811b55efbf0ea1a`  
		Last Modified: Thu, 12 Oct 2023 03:14:00 GMT  
		Size: 263.8 MB (263799339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.1` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:595a7cb5564e9f57ad854e5cf01226e09c5a24e9f6ba5161959c830a4890c5ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325347830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8ea1d6d7b698747b90d75600aabd31d4c4a4738cfd5e5787ac6fa4823f1fd7`
-	Default Command: `["R"]`

```dockerfile
# Wed, 20 Sep 2023 02:45:43 GMT
ADD file:f0c1d15ee705796bc58abf92f15b7a16aa341028b6e099383437710d3694d315 in / 
# Wed, 20 Sep 2023 02:45:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 12:39:06 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 20 Sep 2023 12:39:06 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 20 Sep 2023 12:39:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 12:39:17 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 20 Sep 2023 12:39:17 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 20 Sep 2023 12:39:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 20 Sep 2023 12:39:18 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 20 Sep 2023 12:39:18 GMT
ENV R_BASE_VERSION=4.3.1
# Wed, 20 Sep 2023 12:40:24 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 12:40:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c80309e0a5bbe8e3c8000103b383c6a60c58a6a84681e6aa5963d565eebe59a6`  
		Last Modified: Wed, 20 Sep 2023 02:51:00 GMT  
		Size: 49.4 MB (49404531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cbeb6beab250969d7a012bc457340f9616f734a70d5b3528c9ea0836cff737`  
		Last Modified: Wed, 20 Sep 2023 12:40:48 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7d63b8619e463d865c0fe84818c1100294ce19cc17e3a9c6c1afc141a949ba`  
		Last Modified: Wed, 20 Sep 2023 12:40:51 GMT  
		Size: 25.3 MB (25333710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d49c39ba288dc715fe7c732b83772de2a8362469d2de2984182ff219a2bbdd`  
		Last Modified: Wed, 20 Sep 2023 12:40:49 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cba2360fd37c6a0a4e49af374129c5d2c04fa6dc57617dd4ff8d379a001e37d`  
		Last Modified: Wed, 20 Sep 2023 12:40:48 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9c9354c3386447ea1123b43a83ec67cfc7dde48b7ba1300f678a4172e800f2`  
		Last Modified: Wed, 20 Sep 2023 12:41:09 GMT  
		Size: 249.7 MB (249739555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.1` - linux; ppc64le

```console
$ docker pull r-base@sha256:684f1fc33d6444796baa19843cee83842022f962004926c66723d9c5e299a3b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.0 MB (338001663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcfe919829dc5a2cb298b72ff4eed52f505ec170c305674b76cdb47f231a70c`
-	Default Command: `["R"]`

```dockerfile
# Wed, 20 Sep 2023 08:47:00 GMT
ADD file:3f9069bedf0a55742528dce12a4b55dbe06ecd03a163362a22ec262312f78e63 in / 
# Wed, 20 Sep 2023 08:47:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 20:58:19 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 20 Sep 2023 20:58:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 20 Sep 2023 20:58:41 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 20:58:45 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 20 Sep 2023 20:58:46 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 20 Sep 2023 20:58:46 GMT
ENV LANG=en_US.UTF-8
# Wed, 20 Sep 2023 20:58:47 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 20 Sep 2023 20:58:47 GMT
ENV R_BASE_VERSION=4.3.1
# Wed, 20 Sep 2023 21:00:34 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 21:00:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a30d0f3b9cb815b401d94b7504a260d701d1ceed70755bc25e7ad79803a36dbc`  
		Last Modified: Wed, 20 Sep 2023 08:53:19 GMT  
		Size: 53.4 MB (53395308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218edccd2dbb7c00606eac5d168804d394afa8461565f2cf2acc6dd454c11a13`  
		Last Modified: Wed, 20 Sep 2023 21:01:04 GMT  
		Size: 3.4 KB (3365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb28ec269e6fb71b4130b0b869c92ad5274b16ca5ad293cbacd01a6bc868282`  
		Last Modified: Wed, 20 Sep 2023 21:01:10 GMT  
		Size: 25.9 MB (25907347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ba1acc9c775a936d7c5ed1f267d709b8d4c410dd6bffdfa677ceb225658f8`  
		Last Modified: Wed, 20 Sep 2023 21:01:05 GMT  
		Size: 866.3 KB (866336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d2f71e8da69b69ec91368807fed3abfd45a64e4857e741cbb43e1bf0c78a23`  
		Last Modified: Wed, 20 Sep 2023 21:01:04 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8578201b94ad5fc0cd4844b64b16655e14374b4533fc4576bc393cba5f1aa3`  
		Last Modified: Wed, 20 Sep 2023 21:01:57 GMT  
		Size: 257.8 MB (257828958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.1` - linux; s390x

```console
$ docker pull r-base@sha256:d05da3551e4f08c2956c1ec1145c95aa4828601eea065461dff43bfdf02fdb75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304906936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a3f7fd1e35ed78bb3fe84e8a895a1f6a6bfd7e2504902bfc8536685454acfa`
-	Default Command: `["R"]`

```dockerfile
# Wed, 20 Sep 2023 02:56:53 GMT
ADD file:55adf3f3f6b9fa65711565f1c1946ce15e33e4fe2555b494fc36ac99ffa072ac in / 
# Wed, 20 Sep 2023 02:56:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:38:18 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 20 Sep 2023 09:38:19 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 20 Sep 2023 09:38:37 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:38:44 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 20 Sep 2023 09:38:45 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 20 Sep 2023 09:38:46 GMT
ENV LANG=en_US.UTF-8
# Wed, 20 Sep 2023 09:38:48 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 20 Sep 2023 09:38:48 GMT
ENV R_BASE_VERSION=4.3.1
# Wed, 20 Sep 2023 09:40:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:40:18 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9de78c172a0d9b73fefa46bf099a36fd6685a84a3d5085bc4bce9d9878f7f456`  
		Last Modified: Wed, 20 Sep 2023 03:01:52 GMT  
		Size: 48.8 MB (48760809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e59640c00685f0626d114efafdaa6a6308ce01a2269f9b4f125e847ddaaf96`  
		Last Modified: Wed, 20 Sep 2023 09:40:43 GMT  
		Size: 3.4 KB (3362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a81aed7fdfa5467fb51b917a6839d3d014803b019103b60663286669bf66e6`  
		Last Modified: Wed, 20 Sep 2023 09:40:46 GMT  
		Size: 25.4 MB (25359216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd77f58db8ae690ce4582b4df7b002060260e1eac5c18b477d030e881005a0a4`  
		Last Modified: Wed, 20 Sep 2023 09:40:43 GMT  
		Size: 922.3 KB (922274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bb1b7ba51b7cdb275902f6b05882e061af22b04d68aaa25a33a28160e694ea`  
		Last Modified: Wed, 20 Sep 2023 09:40:43 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ea360b6d0a5e8dad67d4839dae8881103bcec162a42b2260d64be916183052`  
		Last Modified: Wed, 20 Sep 2023 09:41:07 GMT  
		Size: 229.9 MB (229860924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:3bc82794407d9d0667cf75e1d194f9f93b8d563227a29c32e17174c24ed4b070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:06979524919e444f50cf01c8e37403a90c7d06daf988c206c3236049f75fe3bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339689239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64c713b3583c7003979857f85f2403af438d778f02022cf780e6f380ca1abcf`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 Oct 2023 18:37:09 GMT
ADD file:21d38a28e0614f04476d0dca2e0eb55defa5f216a30c05c084c97d6d1fa90e30 in / 
# Wed, 11 Oct 2023 18:37:10 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:12:02 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 12 Oct 2023 03:12:03 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 12 Oct 2023 03:12:14 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:12:16 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 12 Oct 2023 03:12:16 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 12 Oct 2023 03:12:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Oct 2023 03:12:17 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 12 Oct 2023 03:12:17 GMT
ENV R_BASE_VERSION=4.3.1
# Thu, 12 Oct 2023 03:13:17 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:13:19 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:4b9e93079e042882107af07d114a4c10a8202361c63fbdce4fc863cd7942e65e`  
		Last Modified: Wed, 11 Oct 2023 18:43:34 GMT  
		Size: 49.5 MB (49502114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3abc00097ca006fedf22776c231e2545fd41f2432d13fa20630f8066fb1b28`  
		Last Modified: Thu, 12 Oct 2023 03:13:31 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe8cc404d321c25adc422d19c121f41aa88609c90df0646e1d50661b0d45f64`  
		Last Modified: Thu, 12 Oct 2023 03:13:34 GMT  
		Size: 25.5 MB (25517750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefbc40b273a0602aaff7ebf3927d359b4b35b478a0404c6f875c0642e69a632`  
		Last Modified: Thu, 12 Oct 2023 03:13:32 GMT  
		Size: 866.3 KB (866326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de485d51833927eeffeba8297f3c9331260d41e2de8391fc3d0a37699701f3e`  
		Last Modified: Thu, 12 Oct 2023 03:13:31 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a08c976628a0a366eea2ab6923e995d675b63353914bbb811b55efbf0ea1a`  
		Last Modified: Thu, 12 Oct 2023 03:14:00 GMT  
		Size: 263.8 MB (263799339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:595a7cb5564e9f57ad854e5cf01226e09c5a24e9f6ba5161959c830a4890c5ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325347830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8ea1d6d7b698747b90d75600aabd31d4c4a4738cfd5e5787ac6fa4823f1fd7`
-	Default Command: `["R"]`

```dockerfile
# Wed, 20 Sep 2023 02:45:43 GMT
ADD file:f0c1d15ee705796bc58abf92f15b7a16aa341028b6e099383437710d3694d315 in / 
# Wed, 20 Sep 2023 02:45:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 12:39:06 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 20 Sep 2023 12:39:06 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 20 Sep 2023 12:39:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 12:39:17 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 20 Sep 2023 12:39:17 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 20 Sep 2023 12:39:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 20 Sep 2023 12:39:18 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 20 Sep 2023 12:39:18 GMT
ENV R_BASE_VERSION=4.3.1
# Wed, 20 Sep 2023 12:40:24 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 12:40:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c80309e0a5bbe8e3c8000103b383c6a60c58a6a84681e6aa5963d565eebe59a6`  
		Last Modified: Wed, 20 Sep 2023 02:51:00 GMT  
		Size: 49.4 MB (49404531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cbeb6beab250969d7a012bc457340f9616f734a70d5b3528c9ea0836cff737`  
		Last Modified: Wed, 20 Sep 2023 12:40:48 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7d63b8619e463d865c0fe84818c1100294ce19cc17e3a9c6c1afc141a949ba`  
		Last Modified: Wed, 20 Sep 2023 12:40:51 GMT  
		Size: 25.3 MB (25333710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d49c39ba288dc715fe7c732b83772de2a8362469d2de2984182ff219a2bbdd`  
		Last Modified: Wed, 20 Sep 2023 12:40:49 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cba2360fd37c6a0a4e49af374129c5d2c04fa6dc57617dd4ff8d379a001e37d`  
		Last Modified: Wed, 20 Sep 2023 12:40:48 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9c9354c3386447ea1123b43a83ec67cfc7dde48b7ba1300f678a4172e800f2`  
		Last Modified: Wed, 20 Sep 2023 12:41:09 GMT  
		Size: 249.7 MB (249739555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:684f1fc33d6444796baa19843cee83842022f962004926c66723d9c5e299a3b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.0 MB (338001663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcfe919829dc5a2cb298b72ff4eed52f505ec170c305674b76cdb47f231a70c`
-	Default Command: `["R"]`

```dockerfile
# Wed, 20 Sep 2023 08:47:00 GMT
ADD file:3f9069bedf0a55742528dce12a4b55dbe06ecd03a163362a22ec262312f78e63 in / 
# Wed, 20 Sep 2023 08:47:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 20:58:19 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 20 Sep 2023 20:58:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 20 Sep 2023 20:58:41 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 20:58:45 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 20 Sep 2023 20:58:46 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 20 Sep 2023 20:58:46 GMT
ENV LANG=en_US.UTF-8
# Wed, 20 Sep 2023 20:58:47 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 20 Sep 2023 20:58:47 GMT
ENV R_BASE_VERSION=4.3.1
# Wed, 20 Sep 2023 21:00:34 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 21:00:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a30d0f3b9cb815b401d94b7504a260d701d1ceed70755bc25e7ad79803a36dbc`  
		Last Modified: Wed, 20 Sep 2023 08:53:19 GMT  
		Size: 53.4 MB (53395308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218edccd2dbb7c00606eac5d168804d394afa8461565f2cf2acc6dd454c11a13`  
		Last Modified: Wed, 20 Sep 2023 21:01:04 GMT  
		Size: 3.4 KB (3365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb28ec269e6fb71b4130b0b869c92ad5274b16ca5ad293cbacd01a6bc868282`  
		Last Modified: Wed, 20 Sep 2023 21:01:10 GMT  
		Size: 25.9 MB (25907347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ba1acc9c775a936d7c5ed1f267d709b8d4c410dd6bffdfa677ceb225658f8`  
		Last Modified: Wed, 20 Sep 2023 21:01:05 GMT  
		Size: 866.3 KB (866336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d2f71e8da69b69ec91368807fed3abfd45a64e4857e741cbb43e1bf0c78a23`  
		Last Modified: Wed, 20 Sep 2023 21:01:04 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8578201b94ad5fc0cd4844b64b16655e14374b4533fc4576bc393cba5f1aa3`  
		Last Modified: Wed, 20 Sep 2023 21:01:57 GMT  
		Size: 257.8 MB (257828958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:d05da3551e4f08c2956c1ec1145c95aa4828601eea065461dff43bfdf02fdb75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304906936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a3f7fd1e35ed78bb3fe84e8a895a1f6a6bfd7e2504902bfc8536685454acfa`
-	Default Command: `["R"]`

```dockerfile
# Wed, 20 Sep 2023 02:56:53 GMT
ADD file:55adf3f3f6b9fa65711565f1c1946ce15e33e4fe2555b494fc36ac99ffa072ac in / 
# Wed, 20 Sep 2023 02:56:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:38:18 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 20 Sep 2023 09:38:19 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 20 Sep 2023 09:38:37 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:38:44 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 20 Sep 2023 09:38:45 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 20 Sep 2023 09:38:46 GMT
ENV LANG=en_US.UTF-8
# Wed, 20 Sep 2023 09:38:48 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 20 Sep 2023 09:38:48 GMT
ENV R_BASE_VERSION=4.3.1
# Wed, 20 Sep 2023 09:40:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:40:18 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9de78c172a0d9b73fefa46bf099a36fd6685a84a3d5085bc4bce9d9878f7f456`  
		Last Modified: Wed, 20 Sep 2023 03:01:52 GMT  
		Size: 48.8 MB (48760809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e59640c00685f0626d114efafdaa6a6308ce01a2269f9b4f125e847ddaaf96`  
		Last Modified: Wed, 20 Sep 2023 09:40:43 GMT  
		Size: 3.4 KB (3362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a81aed7fdfa5467fb51b917a6839d3d014803b019103b60663286669bf66e6`  
		Last Modified: Wed, 20 Sep 2023 09:40:46 GMT  
		Size: 25.4 MB (25359216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd77f58db8ae690ce4582b4df7b002060260e1eac5c18b477d030e881005a0a4`  
		Last Modified: Wed, 20 Sep 2023 09:40:43 GMT  
		Size: 922.3 KB (922274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bb1b7ba51b7cdb275902f6b05882e061af22b04d68aaa25a33a28160e694ea`  
		Last Modified: Wed, 20 Sep 2023 09:40:43 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ea360b6d0a5e8dad67d4839dae8881103bcec162a42b2260d64be916183052`  
		Last Modified: Wed, 20 Sep 2023 09:41:07 GMT  
		Size: 229.9 MB (229860924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
