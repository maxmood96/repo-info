<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.5.2`](#r-base452)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.5.2`

```console
$ docker pull r-base@sha256:d87597e48514a3a2cb822321b6e755110e2ce2562e4a56340c7b6ba88a87fe09
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
$ docker pull r-base@sha256:fe0a52868f4f0eef7808fd8ea226368c556a6af1357867dec355682e279b716b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367407258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cdab98616ac2ca81313d6adb8b38fc3ab89a44e6e3b425e9e6aed981069a4d`
-	Default Command: `["R"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 19:16:47 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 24 Feb 2026 19:16:47 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 24 Feb 2026 19:16:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:16:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 24 Feb 2026 19:16:54 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 24 Feb 2026 19:16:54 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Feb 2026 19:16:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 24 Feb 2026 19:16:54 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 24 Feb 2026 19:17:34 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:17:34 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:34be0fb38bdb10b6efea64895d8af767ee0135f3467c8cbf6b2a7ad809ff66f7`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a3e4d41ac08127f084914f46ca7b89b6fdc3f4135c9a893c0b0804c9aa163`  
		Last Modified: Tue, 24 Feb 2026 19:18:11 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b0817fbd3b27538f04f7ffc54b2a1350d508c9293e2279481d269d0da701aa`  
		Last Modified: Tue, 24 Feb 2026 19:18:12 GMT  
		Size: 27.2 MB (27185628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b506feb40b987fc7a1ba5b8dedeb980bbf58e66baf23eb80f0846aae4167f3e`  
		Last Modified: Tue, 24 Feb 2026 19:18:11 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240aebf5aedd5592967725cf55d004773b1bf6cc7b7c6473161100f2d127e876`  
		Last Modified: Tue, 24 Feb 2026 19:18:11 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a61a7d01545dd0f7b1e3e042860c5be90d3bc4fe5fa52248d14d25a65be4457`  
		Last Modified: Tue, 24 Feb 2026 19:18:18 GMT  
		Size: 290.7 MB (290672300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:f5d3bca8b428aadc7a241ad89cb7532fe4f8442b61085ab04c1e4e1deb07ccac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13043125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119a4ae93124f8dbcce21edea1e32a0c9270bb45d20f7824ac8f94e4d895a5c3`

```dockerfile
```

-	Layers:
	-	`sha256:54422e88fa2a4608ec1623f0d4233cc065175805e518820ec4c9912f2f6d62a4`  
		Last Modified: Tue, 24 Feb 2026 19:18:12 GMT  
		Size: 13.0 MB (13025028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc36a0c7f5e4155f806aec9580e41ff7f5de515e6d23c3b275d4a5a14ac5226`  
		Last Modified: Tue, 24 Feb 2026 19:18:11 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:7a3839d56e712718883edda43ad7e0349f82f33c942d1b9efb31450489e4e5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350860814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9929dfcb31a05667cb24e26ec389d17b3d3a07279478eaa23595eb5006a6ed3a`
-	Default Command: `["R"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 19:21:44 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 24 Feb 2026 19:21:44 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 24 Feb 2026 19:21:51 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:53 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 24 Feb 2026 19:21:53 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 24 Feb 2026 19:21:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Feb 2026 19:21:53 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 24 Feb 2026 19:21:53 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 24 Feb 2026 19:22:35 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:22:35 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c8a993150206adc8ed6d5444bc6073fe1f1f2401037e10aa375ccb6fbef8932e`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946399acf8fdbe7d29ab7bc1ad53cda8107dccf9f0e1dda58fa133e2bfc9933d`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d15b773937636fd63bf05eaf9273fff9845dd4b1e1d526e9bb131184998b7a`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 27.0 MB (27038086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b676b1954861e4e4a35d6f58dbe78f6ae5297a634632126c6bc922c7649f91`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860fd7b110fe11a960c8321d5ad87a367b7e325526866d047edd167d10f44f8`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296032745e08c0b390659b295700ca6dacfa37f9ff2c6129394a4a84f99636a5`  
		Last Modified: Tue, 24 Feb 2026 19:23:18 GMT  
		Size: 274.2 MB (274245553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:9631e920ae328badad6b6348d3f94f6b6e108fb1b5ea4bf46ce268675d557108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13149244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac7f39c6e87290d628ec040f4b6a2a4340ed0499305ab3697ac3377fb4c39d1`

```dockerfile
```

-	Layers:
	-	`sha256:439a891fa0b366299260a2784c364ee47e41396c5674c0a6af7ff9dc61687976`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 13.1 MB (13131006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd38b4c950a2a744b06ef988c1581c50343dcdbe9f75e55a89549b5a0a436699`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 18.2 KB (18238 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:7a1cd56ff8d723ef2af872a7d41777af08dadd5f16aadc102e80ae3e75ef4d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367253839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9519597fc590390066249c261fb3dba98296ae166044eed3701de1f043ecb0c`
-	Default Command: `["R"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 05:10:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 03 Feb 2026 05:10:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 03 Feb 2026 05:11:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:11:17 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 03 Feb 2026 05:11:17 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 03 Feb 2026 05:11:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 03 Feb 2026 05:11:18 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 03 Feb 2026 05:11:18 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 03 Feb 2026 05:13:09 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:13:09 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1a1783231c3dd75846ddfd4277f3f207d78dec75ee1f53161099a048c12db614`  
		Last Modified: Tue, 03 Feb 2026 01:15:51 GMT  
		Size: 53.6 MB (53582668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0625a2564c855f62bbf0417716a72e176254a006d3159c62e389ff2888779d9`  
		Last Modified: Tue, 03 Feb 2026 05:14:28 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e6966b03f6273d9e4172071c443fdd6fc0e74e195f9a99ab8f663b2774a1c7`  
		Last Modified: Tue, 03 Feb 2026 05:14:30 GMT  
		Size: 27.4 MB (27366614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6546012197874db72e5c61d5539c5aaab39d976a4a535540c26113f82ee6841`  
		Last Modified: Tue, 03 Feb 2026 05:14:29 GMT  
		Size: 868.5 KB (868491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc7bcefc910e8d9b9847606b0ab8d57c1b2dca922f8e2812990ab0ec5df1a`  
		Last Modified: Tue, 03 Feb 2026 05:14:29 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68afe17928a564b3d8cbf9d61881d2395d6c4356ea48196a7f8f395d9f8b06f`  
		Last Modified: Tue, 03 Feb 2026 05:14:36 GMT  
		Size: 285.4 MB (285432394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:d02ba6a07bebc56718e4b61759fbd120ba6b19437785c0f7e4a13668baa1ce29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13026528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76d2a5efb8f0e62b478f73fe6dd2ed000dccc1b7b48665f12b98fdeffb96221`

```dockerfile
```

-	Layers:
	-	`sha256:384732b55bfe5b82dee9b9e735e9b46789e55fc6ea8400c90a40a1b06a5fc345`  
		Last Modified: Tue, 03 Feb 2026 05:14:29 GMT  
		Size: 13.0 MB (13008390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8fd36869774b15376fcef701921b44883ed5eff1abe9dcc8a4bf47bdc52185`  
		Last Modified: Tue, 03 Feb 2026 05:14:29 GMT  
		Size: 18.1 KB (18138 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; s390x

```console
$ docker pull r-base@sha256:183b61756208a2dc8eb4996df07a531ff6554949df9b0c1bd613ca0422f49573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334487010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9c2e8c75f31b36f1b9b2a4d9593dd7b003729c157985461173cf8175ce601e`
-	Default Command: `["R"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 03:37:15 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 03 Feb 2026 03:37:15 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 03 Feb 2026 03:37:25 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:37:26 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 03 Feb 2026 03:37:26 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 03 Feb 2026 03:37:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 03 Feb 2026 03:37:26 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 03 Feb 2026 03:37:26 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 03 Feb 2026 03:38:09 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:38:09 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:307dd5b030418664167d57cabfead401f56d4230a8297dc01ed7acc18877867e`  
		Last Modified: Tue, 03 Feb 2026 01:13:49 GMT  
		Size: 48.4 MB (48429333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e4c46afca789e6207d27bfa4144d0720600fbf22dedbd74cb9223812897d56`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d53285f623023c7d2a77972d0ee0d10fc71de3da48c5cf0e81f1ee147cbbbfa`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 27.0 MB (26986526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10eb8e41b63e9a6746e1eeba778db4cc1c8570c0280f850eaa0c165204eb104`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 924.5 KB (924548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a7a94f16eab376f7fb5a048636f3faf02161591b1f36829279d58f555d32c9`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e98dd44fe9dce58945b39fee5982b70a5701c83ba5934523d57aec817c89a2`  
		Last Modified: Tue, 03 Feb 2026 03:39:04 GMT  
		Size: 258.1 MB (258142942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:6b019e41ee39beb41b9d81102d7e4bf40994cffceea342be1e24a205883ecc5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12839493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad7a5337c04b96f2453c42843ed1c47dcba5e73391e1889985fd93d96f005e7`

```dockerfile
```

-	Layers:
	-	`sha256:386dc120db44b974e2865744ccfddda4a4cbca7c93df9c760fcb46ffc35baa14`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 12.8 MB (12821395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703c631fea67ff406b7aaa3a7b9472ee48b6c3cc6f147a23a24378a7e33ab321`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:d87597e48514a3a2cb822321b6e755110e2ce2562e4a56340c7b6ba88a87fe09
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
$ docker pull r-base@sha256:fe0a52868f4f0eef7808fd8ea226368c556a6af1357867dec355682e279b716b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367407258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cdab98616ac2ca81313d6adb8b38fc3ab89a44e6e3b425e9e6aed981069a4d`
-	Default Command: `["R"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 19:16:47 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 24 Feb 2026 19:16:47 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 24 Feb 2026 19:16:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:16:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 24 Feb 2026 19:16:54 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 24 Feb 2026 19:16:54 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Feb 2026 19:16:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 24 Feb 2026 19:16:54 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 24 Feb 2026 19:17:34 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:17:34 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:34be0fb38bdb10b6efea64895d8af767ee0135f3467c8cbf6b2a7ad809ff66f7`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a3e4d41ac08127f084914f46ca7b89b6fdc3f4135c9a893c0b0804c9aa163`  
		Last Modified: Tue, 24 Feb 2026 19:18:11 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b0817fbd3b27538f04f7ffc54b2a1350d508c9293e2279481d269d0da701aa`  
		Last Modified: Tue, 24 Feb 2026 19:18:12 GMT  
		Size: 27.2 MB (27185628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b506feb40b987fc7a1ba5b8dedeb980bbf58e66baf23eb80f0846aae4167f3e`  
		Last Modified: Tue, 24 Feb 2026 19:18:11 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240aebf5aedd5592967725cf55d004773b1bf6cc7b7c6473161100f2d127e876`  
		Last Modified: Tue, 24 Feb 2026 19:18:11 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a61a7d01545dd0f7b1e3e042860c5be90d3bc4fe5fa52248d14d25a65be4457`  
		Last Modified: Tue, 24 Feb 2026 19:18:18 GMT  
		Size: 290.7 MB (290672300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f5d3bca8b428aadc7a241ad89cb7532fe4f8442b61085ab04c1e4e1deb07ccac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13043125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119a4ae93124f8dbcce21edea1e32a0c9270bb45d20f7824ac8f94e4d895a5c3`

```dockerfile
```

-	Layers:
	-	`sha256:54422e88fa2a4608ec1623f0d4233cc065175805e518820ec4c9912f2f6d62a4`  
		Last Modified: Tue, 24 Feb 2026 19:18:12 GMT  
		Size: 13.0 MB (13025028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc36a0c7f5e4155f806aec9580e41ff7f5de515e6d23c3b275d4a5a14ac5226`  
		Last Modified: Tue, 24 Feb 2026 19:18:11 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:7a3839d56e712718883edda43ad7e0349f82f33c942d1b9efb31450489e4e5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350860814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9929dfcb31a05667cb24e26ec389d17b3d3a07279478eaa23595eb5006a6ed3a`
-	Default Command: `["R"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 19:21:44 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 24 Feb 2026 19:21:44 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 24 Feb 2026 19:21:51 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:53 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 24 Feb 2026 19:21:53 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 24 Feb 2026 19:21:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Feb 2026 19:21:53 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 24 Feb 2026 19:21:53 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 24 Feb 2026 19:22:35 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:22:35 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c8a993150206adc8ed6d5444bc6073fe1f1f2401037e10aa375ccb6fbef8932e`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946399acf8fdbe7d29ab7bc1ad53cda8107dccf9f0e1dda58fa133e2bfc9933d`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d15b773937636fd63bf05eaf9273fff9845dd4b1e1d526e9bb131184998b7a`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 27.0 MB (27038086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b676b1954861e4e4a35d6f58dbe78f6ae5297a634632126c6bc922c7649f91`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860fd7b110fe11a960c8321d5ad87a367b7e325526866d047edd167d10f44f8`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296032745e08c0b390659b295700ca6dacfa37f9ff2c6129394a4a84f99636a5`  
		Last Modified: Tue, 24 Feb 2026 19:23:18 GMT  
		Size: 274.2 MB (274245553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:9631e920ae328badad6b6348d3f94f6b6e108fb1b5ea4bf46ce268675d557108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13149244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac7f39c6e87290d628ec040f4b6a2a4340ed0499305ab3697ac3377fb4c39d1`

```dockerfile
```

-	Layers:
	-	`sha256:439a891fa0b366299260a2784c364ee47e41396c5674c0a6af7ff9dc61687976`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 13.1 MB (13131006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd38b4c950a2a744b06ef988c1581c50343dcdbe9f75e55a89549b5a0a436699`  
		Last Modified: Tue, 24 Feb 2026 19:23:12 GMT  
		Size: 18.2 KB (18238 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:7a1cd56ff8d723ef2af872a7d41777af08dadd5f16aadc102e80ae3e75ef4d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367253839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9519597fc590390066249c261fb3dba98296ae166044eed3701de1f043ecb0c`
-	Default Command: `["R"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 05:10:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 03 Feb 2026 05:10:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 03 Feb 2026 05:11:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:11:17 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 03 Feb 2026 05:11:17 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 03 Feb 2026 05:11:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 03 Feb 2026 05:11:18 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 03 Feb 2026 05:11:18 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 03 Feb 2026 05:13:09 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:13:09 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1a1783231c3dd75846ddfd4277f3f207d78dec75ee1f53161099a048c12db614`  
		Last Modified: Tue, 03 Feb 2026 01:15:51 GMT  
		Size: 53.6 MB (53582668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0625a2564c855f62bbf0417716a72e176254a006d3159c62e389ff2888779d9`  
		Last Modified: Tue, 03 Feb 2026 05:14:28 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e6966b03f6273d9e4172071c443fdd6fc0e74e195f9a99ab8f663b2774a1c7`  
		Last Modified: Tue, 03 Feb 2026 05:14:30 GMT  
		Size: 27.4 MB (27366614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6546012197874db72e5c61d5539c5aaab39d976a4a535540c26113f82ee6841`  
		Last Modified: Tue, 03 Feb 2026 05:14:29 GMT  
		Size: 868.5 KB (868491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc7bcefc910e8d9b9847606b0ab8d57c1b2dca922f8e2812990ab0ec5df1a`  
		Last Modified: Tue, 03 Feb 2026 05:14:29 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68afe17928a564b3d8cbf9d61881d2395d6c4356ea48196a7f8f395d9f8b06f`  
		Last Modified: Tue, 03 Feb 2026 05:14:36 GMT  
		Size: 285.4 MB (285432394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:d02ba6a07bebc56718e4b61759fbd120ba6b19437785c0f7e4a13668baa1ce29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13026528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76d2a5efb8f0e62b478f73fe6dd2ed000dccc1b7b48665f12b98fdeffb96221`

```dockerfile
```

-	Layers:
	-	`sha256:384732b55bfe5b82dee9b9e735e9b46789e55fc6ea8400c90a40a1b06a5fc345`  
		Last Modified: Tue, 03 Feb 2026 05:14:29 GMT  
		Size: 13.0 MB (13008390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8fd36869774b15376fcef701921b44883ed5eff1abe9dcc8a4bf47bdc52185`  
		Last Modified: Tue, 03 Feb 2026 05:14:29 GMT  
		Size: 18.1 KB (18138 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:183b61756208a2dc8eb4996df07a531ff6554949df9b0c1bd613ca0422f49573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334487010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9c2e8c75f31b36f1b9b2a4d9593dd7b003729c157985461173cf8175ce601e`
-	Default Command: `["R"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 03:37:15 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 03 Feb 2026 03:37:15 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 03 Feb 2026 03:37:25 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:37:26 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 03 Feb 2026 03:37:26 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 03 Feb 2026 03:37:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 03 Feb 2026 03:37:26 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 03 Feb 2026 03:37:26 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 03 Feb 2026 03:38:09 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:38:09 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:307dd5b030418664167d57cabfead401f56d4230a8297dc01ed7acc18877867e`  
		Last Modified: Tue, 03 Feb 2026 01:13:49 GMT  
		Size: 48.4 MB (48429333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e4c46afca789e6207d27bfa4144d0720600fbf22dedbd74cb9223812897d56`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d53285f623023c7d2a77972d0ee0d10fc71de3da48c5cf0e81f1ee147cbbbfa`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 27.0 MB (26986526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10eb8e41b63e9a6746e1eeba778db4cc1c8570c0280f850eaa0c165204eb104`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 924.5 KB (924548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a7a94f16eab376f7fb5a048636f3faf02161591b1f36829279d58f555d32c9`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e98dd44fe9dce58945b39fee5982b70a5701c83ba5934523d57aec817c89a2`  
		Last Modified: Tue, 03 Feb 2026 03:39:04 GMT  
		Size: 258.1 MB (258142942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:6b019e41ee39beb41b9d81102d7e4bf40994cffceea342be1e24a205883ecc5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12839493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad7a5337c04b96f2453c42843ed1c47dcba5e73391e1889985fd93d96f005e7`

```dockerfile
```

-	Layers:
	-	`sha256:386dc120db44b974e2865744ccfddda4a4cbca7c93df9c760fcb46ffc35baa14`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 12.8 MB (12821395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703c631fea67ff406b7aaa3a7b9472ee48b6c3cc6f147a23a24378a7e33ab321`  
		Last Modified: Tue, 03 Feb 2026 03:38:59 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json
