<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.3.2`](#r-base432)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.3.2`

```console
$ docker pull r-base@sha256:54241dc5a461f473a27d92b73a86fb5d391da7bf34926eb08f08768d8942a46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.3.2` - linux; amd64

```console
$ docker pull r-base@sha256:6c7491030f6078f0013919651f72c812fd555a0e0cdbd8d5f3469c6eaff58b5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340308096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d7f781b1d50983a824e4f9e317249ab7236d1e63ea512e1123fc10d71ae4d0`
-	Default Command: `["R"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:36 GMT
ADD file:603237810768dd1380a911bc8974893a077b7a5906fa11d5bd7013e62e2aa352 in / 
# Wed, 31 Jan 2024 22:37:37 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 01 Feb 2024 06:20:55 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 01 Feb 2024 06:21:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:21:08 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 01 Feb 2024 06:21:08 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 06:21:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 01 Feb 2024 06:21:08 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 01 Feb 2024 06:21:08 GMT
ENV R_BASE_VERSION=4.3.2
# Thu, 01 Feb 2024 06:22:03 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:22:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:10c69e045d41e730cfa46d159956d856795f06d2d429a76925ed787b9cb1b442`  
		Last Modified: Wed, 31 Jan 2024 22:44:03 GMT  
		Size: 52.3 MB (52283193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd695353bb02e42f4fa93eb17ab3c6bd94ccd89e6ce0afb4ed4da381c8a8462a`  
		Last Modified: Thu, 01 Feb 2024 06:22:22 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32070770751adc04a1ebd286a20e8e56c32eb73dbbeb6a9bf32bb8872b13966a`  
		Last Modified: Thu, 01 Feb 2024 06:22:25 GMT  
		Size: 23.0 MB (23036975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd50c4dc03f0ad6cd15022df06c20f99b96ceb14a4bbb5e6c3dacae3016d89d1`  
		Last Modified: Thu, 01 Feb 2024 06:22:23 GMT  
		Size: 866.3 KB (866334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f09dd8d76bca6e0102b76fedaea1e45559b31306a15b8adfb01c8318b944c6`  
		Last Modified: Thu, 01 Feb 2024 06:22:22 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3067bf23d2bb0ffcc64951c99703398c5919c367f0623c102a6017cfec40b577`  
		Last Modified: Thu, 01 Feb 2024 06:22:51 GMT  
		Size: 264.1 MB (264117882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:ec20a6944d7c5deb387b4c6af1aef601ac2f21e5277780e88ff3c577e5f4e1a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326631658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e53f2bc735c860f93a69bb23e145d4689b090eb959aa1d1bef0786a51ea938a`
-	Default Command: `["R"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:03 GMT
ADD file:7ee3c0539d396e0792ed68269fa710165c0457a7534e01b5c22cabc84cdafcfb in / 
# Wed, 31 Jan 2024 22:46:04 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:53:39 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 01 Feb 2024 05:53:39 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 01 Feb 2024 05:53:49 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:53:51 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 01 Feb 2024 05:53:51 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 05:53:51 GMT
ENV LANG=en_US.UTF-8
# Thu, 01 Feb 2024 05:53:52 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 01 Feb 2024 05:53:52 GMT
ENV R_BASE_VERSION=4.3.2
# Thu, 01 Feb 2024 05:54:49 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:54:50 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:76832b4a5d197ea5c080862484bac9955c3fb1c4bab0098cf33a245ed7bfd72e`  
		Last Modified: Wed, 31 Jan 2024 22:51:59 GMT  
		Size: 52.2 MB (52161380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2384fb2e9c544367cefb483a3c010ff43931c05fc44daf257b4d87176a11354`  
		Last Modified: Thu, 01 Feb 2024 05:55:08 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc26c48f5c6c2420b9e0913ba8dab6863456182d144e26d7e919868cc8389ef`  
		Last Modified: Thu, 01 Feb 2024 05:55:10 GMT  
		Size: 23.0 MB (23032340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bac7a79ea1fc88a335bfd0f60087c727b0eca82108a7a2e7cb9f200d2a1bba`  
		Last Modified: Thu, 01 Feb 2024 05:55:08 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c94eaccdf15ee148dd9f6b0bf3ba7e3e9d75fbd0cc18fa4ca8517fc141f1a2`  
		Last Modified: Thu, 01 Feb 2024 05:55:08 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a62c2f3dcf1c1f03ca01d021ba51083ed415c15ca01cd8255cc522810d8814`  
		Last Modified: Thu, 01 Feb 2024 05:55:29 GMT  
		Size: 250.6 MB (250567908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:a26659a8205eb0bc94d40cd900d0b0ec828ffb8b4d984f386c1806042d9186b6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338760207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b082201f42e72b3ac11ee47bb1ee17c69811e631348013efc315937242b6e8f`
-	Default Command: `["R"]`

```dockerfile
# Wed, 31 Jan 2024 22:31:45 GMT
ADD file:250d605af8ffae8b389f7325ab9d0e69d953ea56c80a4aff820652c5a4fe0ada in / 
# Wed, 31 Jan 2024 22:31:49 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 08:03:30 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 01 Feb 2024 08:03:32 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 01 Feb 2024 08:03:51 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 08:03:55 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 01 Feb 2024 08:03:56 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 08:03:57 GMT
ENV LANG=en_US.UTF-8
# Thu, 01 Feb 2024 08:03:59 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 01 Feb 2024 08:03:59 GMT
ENV R_BASE_VERSION=4.3.2
# Thu, 01 Feb 2024 08:06:43 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 08:06:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e31582b2e6d39845d4311bbd81ac584a8bcc2c9e6e745892afb34a275a20d4b2`  
		Last Modified: Wed, 31 Jan 2024 22:37:37 GMT  
		Size: 56.2 MB (56198847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955e13d07656a51983fff317bee59cf96d7d2804d55eb0323737ff5a4b5e721b`  
		Last Modified: Thu, 01 Feb 2024 08:07:15 GMT  
		Size: 3.4 KB (3359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a66e00681143ba020d926179d2e111b3f3fb77e31bd4c45f11a0f9c38659c56`  
		Last Modified: Thu, 01 Feb 2024 08:07:18 GMT  
		Size: 23.3 MB (23258605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd02c648a8cf1f459155e3e796e168a40c2fa2ee01e9d484f770be5136ad9e5`  
		Last Modified: Thu, 01 Feb 2024 08:07:15 GMT  
		Size: 866.3 KB (866335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe5fbbed95b750f6e53591d5d480274d339d43bda4aa76002cbabfdc0f0088`  
		Last Modified: Thu, 01 Feb 2024 08:07:14 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318808960cfa371efe87b15847858bdc05c0c4e67a009a0506a32082d16f2c3f`  
		Last Modified: Thu, 01 Feb 2024 08:07:48 GMT  
		Size: 258.4 MB (258432711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.2` - linux; s390x

```console
$ docker pull r-base@sha256:d80fecc4a6eeaf8bdf0fe5be05181ad6dff7d58714fb335452da8af7349f8e02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323476218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceef6a2c15eb9978c1220083741ff1c6b4f45683d010c8bee6d837c222d2f81`
-	Default Command: `["R"]`

```dockerfile
# Tue, 13 Feb 2024 01:17:18 GMT
ADD file:9e08f22ce952afa84f6e81b5e9b67fb56721966677cb1078f32490a0caa1fe78 in / 
# Tue, 13 Feb 2024 01:17:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:57:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Feb 2024 04:57:12 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 13 Feb 2024 04:57:20 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:57:23 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 13 Feb 2024 04:57:23 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 04:57:23 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Feb 2024 04:57:23 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 13 Feb 2024 04:57:23 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 13 Feb 2024 04:58:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:58:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2ee5e82c8f402fc32ba854108be67fb942736c23baf589298d4f94671ddaac35`  
		Last Modified: Tue, 13 Feb 2024 01:32:20 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2c3de9ad6e528e3d1254fc0bba25f4fc91bd39216fc9728cb9c756bbb974f7`  
		Last Modified: Tue, 13 Feb 2024 04:59:25 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18668ab2396e889c788bf12bf3d947bcee323f954ce94776d81ff6636d655b3`  
		Last Modified: Tue, 13 Feb 2024 04:59:27 GMT  
		Size: 25.3 MB (25306283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f451d92a8b4253e5b3ffacefdc0ad797f673d6abb538adebe07f1ceffd26f03`  
		Last Modified: Tue, 13 Feb 2024 04:59:25 GMT  
		Size: 922.3 KB (922276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28aa0e95e1e8e18ac08264dcc3acc9519254a2fd5fc145082b1e3a0e767f9777`  
		Last Modified: Tue, 13 Feb 2024 04:59:24 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d844d0ed068b232257eddbb7a0e33d39b9949b70b882e125282efabcaa36ca`  
		Last Modified: Tue, 13 Feb 2024 04:59:50 GMT  
		Size: 245.5 MB (245501631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:54241dc5a461f473a27d92b73a86fb5d391da7bf34926eb08f08768d8942a46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:6c7491030f6078f0013919651f72c812fd555a0e0cdbd8d5f3469c6eaff58b5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340308096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d7f781b1d50983a824e4f9e317249ab7236d1e63ea512e1123fc10d71ae4d0`
-	Default Command: `["R"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:36 GMT
ADD file:603237810768dd1380a911bc8974893a077b7a5906fa11d5bd7013e62e2aa352 in / 
# Wed, 31 Jan 2024 22:37:37 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 01 Feb 2024 06:20:55 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 01 Feb 2024 06:21:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:21:08 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 01 Feb 2024 06:21:08 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 06:21:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 01 Feb 2024 06:21:08 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 01 Feb 2024 06:21:08 GMT
ENV R_BASE_VERSION=4.3.2
# Thu, 01 Feb 2024 06:22:03 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:22:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:10c69e045d41e730cfa46d159956d856795f06d2d429a76925ed787b9cb1b442`  
		Last Modified: Wed, 31 Jan 2024 22:44:03 GMT  
		Size: 52.3 MB (52283193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd695353bb02e42f4fa93eb17ab3c6bd94ccd89e6ce0afb4ed4da381c8a8462a`  
		Last Modified: Thu, 01 Feb 2024 06:22:22 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32070770751adc04a1ebd286a20e8e56c32eb73dbbeb6a9bf32bb8872b13966a`  
		Last Modified: Thu, 01 Feb 2024 06:22:25 GMT  
		Size: 23.0 MB (23036975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd50c4dc03f0ad6cd15022df06c20f99b96ceb14a4bbb5e6c3dacae3016d89d1`  
		Last Modified: Thu, 01 Feb 2024 06:22:23 GMT  
		Size: 866.3 KB (866334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f09dd8d76bca6e0102b76fedaea1e45559b31306a15b8adfb01c8318b944c6`  
		Last Modified: Thu, 01 Feb 2024 06:22:22 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3067bf23d2bb0ffcc64951c99703398c5919c367f0623c102a6017cfec40b577`  
		Last Modified: Thu, 01 Feb 2024 06:22:51 GMT  
		Size: 264.1 MB (264117882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:ec20a6944d7c5deb387b4c6af1aef601ac2f21e5277780e88ff3c577e5f4e1a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326631658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e53f2bc735c860f93a69bb23e145d4689b090eb959aa1d1bef0786a51ea938a`
-	Default Command: `["R"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:03 GMT
ADD file:7ee3c0539d396e0792ed68269fa710165c0457a7534e01b5c22cabc84cdafcfb in / 
# Wed, 31 Jan 2024 22:46:04 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:53:39 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 01 Feb 2024 05:53:39 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 01 Feb 2024 05:53:49 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:53:51 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 01 Feb 2024 05:53:51 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 05:53:51 GMT
ENV LANG=en_US.UTF-8
# Thu, 01 Feb 2024 05:53:52 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 01 Feb 2024 05:53:52 GMT
ENV R_BASE_VERSION=4.3.2
# Thu, 01 Feb 2024 05:54:49 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:54:50 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:76832b4a5d197ea5c080862484bac9955c3fb1c4bab0098cf33a245ed7bfd72e`  
		Last Modified: Wed, 31 Jan 2024 22:51:59 GMT  
		Size: 52.2 MB (52161380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2384fb2e9c544367cefb483a3c010ff43931c05fc44daf257b4d87176a11354`  
		Last Modified: Thu, 01 Feb 2024 05:55:08 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc26c48f5c6c2420b9e0913ba8dab6863456182d144e26d7e919868cc8389ef`  
		Last Modified: Thu, 01 Feb 2024 05:55:10 GMT  
		Size: 23.0 MB (23032340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bac7a79ea1fc88a335bfd0f60087c727b0eca82108a7a2e7cb9f200d2a1bba`  
		Last Modified: Thu, 01 Feb 2024 05:55:08 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c94eaccdf15ee148dd9f6b0bf3ba7e3e9d75fbd0cc18fa4ca8517fc141f1a2`  
		Last Modified: Thu, 01 Feb 2024 05:55:08 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a62c2f3dcf1c1f03ca01d021ba51083ed415c15ca01cd8255cc522810d8814`  
		Last Modified: Thu, 01 Feb 2024 05:55:29 GMT  
		Size: 250.6 MB (250567908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:a26659a8205eb0bc94d40cd900d0b0ec828ffb8b4d984f386c1806042d9186b6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338760207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b082201f42e72b3ac11ee47bb1ee17c69811e631348013efc315937242b6e8f`
-	Default Command: `["R"]`

```dockerfile
# Wed, 31 Jan 2024 22:31:45 GMT
ADD file:250d605af8ffae8b389f7325ab9d0e69d953ea56c80a4aff820652c5a4fe0ada in / 
# Wed, 31 Jan 2024 22:31:49 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 08:03:30 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 01 Feb 2024 08:03:32 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 01 Feb 2024 08:03:51 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 08:03:55 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 01 Feb 2024 08:03:56 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 08:03:57 GMT
ENV LANG=en_US.UTF-8
# Thu, 01 Feb 2024 08:03:59 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 01 Feb 2024 08:03:59 GMT
ENV R_BASE_VERSION=4.3.2
# Thu, 01 Feb 2024 08:06:43 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 08:06:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e31582b2e6d39845d4311bbd81ac584a8bcc2c9e6e745892afb34a275a20d4b2`  
		Last Modified: Wed, 31 Jan 2024 22:37:37 GMT  
		Size: 56.2 MB (56198847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955e13d07656a51983fff317bee59cf96d7d2804d55eb0323737ff5a4b5e721b`  
		Last Modified: Thu, 01 Feb 2024 08:07:15 GMT  
		Size: 3.4 KB (3359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a66e00681143ba020d926179d2e111b3f3fb77e31bd4c45f11a0f9c38659c56`  
		Last Modified: Thu, 01 Feb 2024 08:07:18 GMT  
		Size: 23.3 MB (23258605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd02c648a8cf1f459155e3e796e168a40c2fa2ee01e9d484f770be5136ad9e5`  
		Last Modified: Thu, 01 Feb 2024 08:07:15 GMT  
		Size: 866.3 KB (866335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe5fbbed95b750f6e53591d5d480274d339d43bda4aa76002cbabfdc0f0088`  
		Last Modified: Thu, 01 Feb 2024 08:07:14 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318808960cfa371efe87b15847858bdc05c0c4e67a009a0506a32082d16f2c3f`  
		Last Modified: Thu, 01 Feb 2024 08:07:48 GMT  
		Size: 258.4 MB (258432711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:d80fecc4a6eeaf8bdf0fe5be05181ad6dff7d58714fb335452da8af7349f8e02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323476218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceef6a2c15eb9978c1220083741ff1c6b4f45683d010c8bee6d837c222d2f81`
-	Default Command: `["R"]`

```dockerfile
# Tue, 13 Feb 2024 01:17:18 GMT
ADD file:9e08f22ce952afa84f6e81b5e9b67fb56721966677cb1078f32490a0caa1fe78 in / 
# Tue, 13 Feb 2024 01:17:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:57:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Feb 2024 04:57:12 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 13 Feb 2024 04:57:20 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:57:23 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 13 Feb 2024 04:57:23 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 04:57:23 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Feb 2024 04:57:23 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 13 Feb 2024 04:57:23 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 13 Feb 2024 04:58:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:58:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2ee5e82c8f402fc32ba854108be67fb942736c23baf589298d4f94671ddaac35`  
		Last Modified: Tue, 13 Feb 2024 01:32:20 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2c3de9ad6e528e3d1254fc0bba25f4fc91bd39216fc9728cb9c756bbb974f7`  
		Last Modified: Tue, 13 Feb 2024 04:59:25 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18668ab2396e889c788bf12bf3d947bcee323f954ce94776d81ff6636d655b3`  
		Last Modified: Tue, 13 Feb 2024 04:59:27 GMT  
		Size: 25.3 MB (25306283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f451d92a8b4253e5b3ffacefdc0ad797f673d6abb538adebe07f1ceffd26f03`  
		Last Modified: Tue, 13 Feb 2024 04:59:25 GMT  
		Size: 922.3 KB (922276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28aa0e95e1e8e18ac08264dcc3acc9519254a2fd5fc145082b1e3a0e767f9777`  
		Last Modified: Tue, 13 Feb 2024 04:59:24 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d844d0ed068b232257eddbb7a0e33d39b9949b70b882e125282efabcaa36ca`  
		Last Modified: Tue, 13 Feb 2024 04:59:50 GMT  
		Size: 245.5 MB (245501631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
