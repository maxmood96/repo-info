<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.0.3`](#r-base403)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.0.3`

```console
$ docker pull r-base@sha256:bad540dfcf3cc1fa799c28c384f50dbd3f82075291df92fc6028ec53816ffbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `r-base:4.0.3` - linux; amd64

```console
$ docker pull r-base@sha256:6eaf4b405bbb6538cead9219221c66a68a52c0718e38745a59a233e14c26a967
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.1 MB (644140148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d505b1b24a98083901eb7a50ddaf8bfdf296bbf7b81a1407b837cdff799c611`
-	Default Command: `["R"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:45 GMT
ADD file:b6d9d03d246917cd8a499e26b7dafcdd42ca61c3cbb6e60b78c888a349814210 in / 
# Tue, 17 Nov 2020 20:24:45 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:21:07 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 18 Nov 2020 08:21:08 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 18 Nov 2020 08:21:22 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:21:25 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 18 Nov 2020 08:21:25 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 18 Nov 2020 08:21:25 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Nov 2020 08:21:26 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 18 Nov 2020 08:21:26 GMT
ENV R_BASE_VERSION=4.0.3
# Wed, 18 Nov 2020 08:24:05 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:24:06 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a919358b170f991da872d2c4a5b2210ce45783166a93d65c90ee3cad6b86dbc8`  
		Last Modified: Tue, 17 Nov 2020 20:30:58 GMT  
		Size: 55.6 MB (55577988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1a676142d9f8d956a73ebf191e49d0cfe6a8062c92c85c1c1e0ef01a7d9bc4`  
		Last Modified: Wed, 18 Nov 2020 08:24:29 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbe917a25f5b0973636460470a97c3ed05959d992ef5414c7138c59613a622e`  
		Last Modified: Wed, 18 Nov 2020 08:24:36 GMT  
		Size: 25.6 MB (25558198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fdbdc08d5003898a1569e91ec7ba5568d84ea4806d34187f7e8c670f11e8ae`  
		Last Modified: Wed, 18 Nov 2020 08:24:29 GMT  
		Size: 863.6 KB (863578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7e3fa43e357767fd578d1b7a1a6c4f88193a7c91f87ad8549c09e884dc7fca`  
		Last Modified: Wed, 18 Nov 2020 08:24:28 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0808418726cfd4b10b2a7b0bbccd1d55c65f100364aa5ef49baf1b0d766a2f`  
		Last Modified: Wed, 18 Nov 2020 08:26:37 GMT  
		Size: 562.1 MB (562138189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.3` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:6ba94de9e7adb0f7cd759594a90b025a8782dbd032c72dabc9bd8d33c6f2f648
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.1 MB (507072736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad039ec4a4b4b25d8b7955589ea37ca166ad971f2fb85bd0a3c1dfa576dc3d20`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Dec 2020 02:49:00 GMT
ADD file:68734186568fd3a803d44d4f42065373a0200929b1ff39d104a24dfe14316ae0 in / 
# Fri, 11 Dec 2020 02:49:04 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:02:39 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Dec 2020 17:02:41 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Fri, 11 Dec 2020 17:03:04 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:03:10 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Fri, 11 Dec 2020 17:03:13 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Dec 2020 17:03:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Dec 2020 17:03:18 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 11 Dec 2020 17:03:20 GMT
ENV R_BASE_VERSION=4.0.3
# Fri, 11 Dec 2020 17:05:40 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:37ba54a7ad02aab7f88ab28bf1de79bd2861de26af6a6998d9b8dab9cc58b2f9`  
		Last Modified: Fri, 11 Dec 2020 02:56:23 GMT  
		Size: 52.0 MB (51961789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc484ab337728ab0a3c81b0016c1b7d0042e4dc5881e2bee0f37111cc38000`  
		Last Modified: Fri, 11 Dec 2020 17:06:04 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1353e5265e09e606d78cfdd681b7dc846953a304e13bf818911949895b3b9353`  
		Last Modified: Fri, 11 Dec 2020 17:06:12 GMT  
		Size: 27.3 MB (27309206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617418dda951dc7cf53cd4c56893d986d78219ef8422a487fbf414e3dfd6a4a2`  
		Last Modified: Fri, 11 Dec 2020 17:06:05 GMT  
		Size: 863.6 KB (863571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073a1e61d66d2451b5f7149251cdbf6de1483ea3bceded8d786dfb5f9bd85bf`  
		Last Modified: Fri, 11 Dec 2020 17:06:04 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab79f74827b044a430446d69c7439babb4bfb3a8e2c11a19ac582bf4f230849a`  
		Last Modified: Fri, 11 Dec 2020 17:07:39 GMT  
		Size: 426.9 MB (426935945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.3` - linux; ppc64le

```console
$ docker pull r-base@sha256:f14e1662edbeebb2c9e6b1cc38af4ae90de52e058dead44566d96ffba0c679af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.3 MB (613313880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcc0e2c50ee03625ade975c2ec10ee2812c8dcced8aab7b381881d571b5e7c1`
-	Default Command: `["R"]`

```dockerfile
# Tue, 17 Nov 2020 23:25:16 GMT
ADD file:74e3f9199d8973f4d6859f7dfad98ea11e79e7829d5756710a16351f8c033596 in / 
# Tue, 17 Nov 2020 23:25:24 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 10:06:53 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 18 Nov 2020 10:07:06 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 18 Nov 2020 10:08:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 10:08:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 18 Nov 2020 10:08:24 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 18 Nov 2020 10:08:26 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Nov 2020 10:08:30 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 18 Nov 2020 10:08:35 GMT
ENV R_BASE_VERSION=4.0.3
# Wed, 18 Nov 2020 10:16:52 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 10:16:58 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ac668230de37b88984090c102d2d7b0848c85b72d33b9fe4aff709b7ef0074ed`  
		Last Modified: Tue, 17 Nov 2020 23:38:25 GMT  
		Size: 59.8 MB (59761435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c05719ec613e5ce07a8a32f835dfaa5162ad8acc7f2c619ba4c90b06806e656`  
		Last Modified: Wed, 18 Nov 2020 10:17:13 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de98d65e9efa65b4ea55a70f08f8d43802a3dafd91caa1ad7a77c57d20f1e07`  
		Last Modified: Wed, 18 Nov 2020 10:17:18 GMT  
		Size: 25.8 MB (25773500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5028154bc4993e2607ff85963e6013c3f2ea51581c8cecc9b94a1e3f59e3dc`  
		Last Modified: Wed, 18 Nov 2020 10:17:14 GMT  
		Size: 863.6 KB (863578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e82a370224d81e617bf9bb64eb08c9939808ccbc5833aefa935b1b4bfdd87`  
		Last Modified: Wed, 18 Nov 2020 10:17:14 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2a2b677d0eff30f3c0a002e31fbd62f9fa36b0f5db799a8fa9e5540963b0e9`  
		Last Modified: Wed, 18 Nov 2020 10:18:54 GMT  
		Size: 526.9 MB (526913130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:bad540dfcf3cc1fa799c28c384f50dbd3f82075291df92fc6028ec53816ffbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:6eaf4b405bbb6538cead9219221c66a68a52c0718e38745a59a233e14c26a967
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.1 MB (644140148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d505b1b24a98083901eb7a50ddaf8bfdf296bbf7b81a1407b837cdff799c611`
-	Default Command: `["R"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:45 GMT
ADD file:b6d9d03d246917cd8a499e26b7dafcdd42ca61c3cbb6e60b78c888a349814210 in / 
# Tue, 17 Nov 2020 20:24:45 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:21:07 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 18 Nov 2020 08:21:08 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 18 Nov 2020 08:21:22 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:21:25 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 18 Nov 2020 08:21:25 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 18 Nov 2020 08:21:25 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Nov 2020 08:21:26 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 18 Nov 2020 08:21:26 GMT
ENV R_BASE_VERSION=4.0.3
# Wed, 18 Nov 2020 08:24:05 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:24:06 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a919358b170f991da872d2c4a5b2210ce45783166a93d65c90ee3cad6b86dbc8`  
		Last Modified: Tue, 17 Nov 2020 20:30:58 GMT  
		Size: 55.6 MB (55577988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1a676142d9f8d956a73ebf191e49d0cfe6a8062c92c85c1c1e0ef01a7d9bc4`  
		Last Modified: Wed, 18 Nov 2020 08:24:29 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbe917a25f5b0973636460470a97c3ed05959d992ef5414c7138c59613a622e`  
		Last Modified: Wed, 18 Nov 2020 08:24:36 GMT  
		Size: 25.6 MB (25558198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fdbdc08d5003898a1569e91ec7ba5568d84ea4806d34187f7e8c670f11e8ae`  
		Last Modified: Wed, 18 Nov 2020 08:24:29 GMT  
		Size: 863.6 KB (863578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7e3fa43e357767fd578d1b7a1a6c4f88193a7c91f87ad8549c09e884dc7fca`  
		Last Modified: Wed, 18 Nov 2020 08:24:28 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0808418726cfd4b10b2a7b0bbccd1d55c65f100364aa5ef49baf1b0d766a2f`  
		Last Modified: Wed, 18 Nov 2020 08:26:37 GMT  
		Size: 562.1 MB (562138189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:6ba94de9e7adb0f7cd759594a90b025a8782dbd032c72dabc9bd8d33c6f2f648
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.1 MB (507072736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad039ec4a4b4b25d8b7955589ea37ca166ad971f2fb85bd0a3c1dfa576dc3d20`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Dec 2020 02:49:00 GMT
ADD file:68734186568fd3a803d44d4f42065373a0200929b1ff39d104a24dfe14316ae0 in / 
# Fri, 11 Dec 2020 02:49:04 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:02:39 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Dec 2020 17:02:41 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Fri, 11 Dec 2020 17:03:04 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:03:10 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Fri, 11 Dec 2020 17:03:13 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Dec 2020 17:03:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Dec 2020 17:03:18 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Fri, 11 Dec 2020 17:03:20 GMT
ENV R_BASE_VERSION=4.0.3
# Fri, 11 Dec 2020 17:05:40 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:05:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:37ba54a7ad02aab7f88ab28bf1de79bd2861de26af6a6998d9b8dab9cc58b2f9`  
		Last Modified: Fri, 11 Dec 2020 02:56:23 GMT  
		Size: 52.0 MB (51961789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc484ab337728ab0a3c81b0016c1b7d0042e4dc5881e2bee0f37111cc38000`  
		Last Modified: Fri, 11 Dec 2020 17:06:04 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1353e5265e09e606d78cfdd681b7dc846953a304e13bf818911949895b3b9353`  
		Last Modified: Fri, 11 Dec 2020 17:06:12 GMT  
		Size: 27.3 MB (27309206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617418dda951dc7cf53cd4c56893d986d78219ef8422a487fbf414e3dfd6a4a2`  
		Last Modified: Fri, 11 Dec 2020 17:06:05 GMT  
		Size: 863.6 KB (863571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073a1e61d66d2451b5f7149251cdbf6de1483ea3bceded8d786dfb5f9bd85bf`  
		Last Modified: Fri, 11 Dec 2020 17:06:04 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab79f74827b044a430446d69c7439babb4bfb3a8e2c11a19ac582bf4f230849a`  
		Last Modified: Fri, 11 Dec 2020 17:07:39 GMT  
		Size: 426.9 MB (426935945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:f14e1662edbeebb2c9e6b1cc38af4ae90de52e058dead44566d96ffba0c679af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.3 MB (613313880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcc0e2c50ee03625ade975c2ec10ee2812c8dcced8aab7b381881d571b5e7c1`
-	Default Command: `["R"]`

```dockerfile
# Tue, 17 Nov 2020 23:25:16 GMT
ADD file:74e3f9199d8973f4d6859f7dfad98ea11e79e7829d5756710a16351f8c033596 in / 
# Tue, 17 Nov 2020 23:25:24 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 10:06:53 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 18 Nov 2020 10:07:06 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 18 Nov 2020 10:08:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 10:08:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 18 Nov 2020 10:08:24 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 18 Nov 2020 10:08:26 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Nov 2020 10:08:30 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 18 Nov 2020 10:08:35 GMT
ENV R_BASE_VERSION=4.0.3
# Wed, 18 Nov 2020 10:16:52 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 10:16:58 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ac668230de37b88984090c102d2d7b0848c85b72d33b9fe4aff709b7ef0074ed`  
		Last Modified: Tue, 17 Nov 2020 23:38:25 GMT  
		Size: 59.8 MB (59761435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c05719ec613e5ce07a8a32f835dfaa5162ad8acc7f2c619ba4c90b06806e656`  
		Last Modified: Wed, 18 Nov 2020 10:17:13 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de98d65e9efa65b4ea55a70f08f8d43802a3dafd91caa1ad7a77c57d20f1e07`  
		Last Modified: Wed, 18 Nov 2020 10:17:18 GMT  
		Size: 25.8 MB (25773500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5028154bc4993e2607ff85963e6013c3f2ea51581c8cecc9b94a1e3f59e3dc`  
		Last Modified: Wed, 18 Nov 2020 10:17:14 GMT  
		Size: 863.6 KB (863578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e82a370224d81e617bf9bb64eb08c9939808ccbc5833aefa935b1b4bfdd87`  
		Last Modified: Wed, 18 Nov 2020 10:17:14 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2a2b677d0eff30f3c0a002e31fbd62f9fa36b0f5db799a8fa9e5540963b0e9`  
		Last Modified: Wed, 18 Nov 2020 10:18:54 GMT  
		Size: 526.9 MB (526913130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
