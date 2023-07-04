## `r-base:latest`

```console
$ docker pull r-base@sha256:f2d5d20b9832ee81239c15a12aec29b590b8244cc59e69e3b95d219f444eb2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:649a9bb859a9eed1c5ec7afb015faba12924cbc0eadfa039828a4418c1e329d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338596469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5441619af0c00724ee7bc64395ce504ee368b23cde615d72b25df1a300db0a26`
-	Default Command: `["R"]`

```dockerfile
# Tue, 04 Jul 2023 01:22:36 GMT
ADD file:de5374a9ef9a0a868df3aca8ce7b7d50abbcf762f41fef9c58012f36d97f78ad in / 
# Tue, 04 Jul 2023 01:22:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 07:09:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 04 Jul 2023 07:09:12 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 04 Jul 2023 07:09:24 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 07:09:26 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 04 Jul 2023 07:09:27 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 07:09:27 GMT
ENV LANG=en_US.UTF-8
# Tue, 04 Jul 2023 07:09:27 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 04 Jul 2023 07:09:27 GMT
ENV R_BASE_VERSION=4.3.1
# Tue, 04 Jul 2023 07:10:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 07:10:53 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:dfc7daecfaf18ac4d0f8113f6edff692b509a3dfec300e2dc347fc813f7fd887`  
		Last Modified: Tue, 04 Jul 2023 01:28:45 GMT  
		Size: 49.5 MB (49523824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724d9d5a54683c65388b07995a649f6df0b22cac8901836d3ce0029ecd7de185`  
		Last Modified: Tue, 04 Jul 2023 07:11:11 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7d454ec983caa297e5b5a95b98faa11038e1d9ce9600d32d3ce35cc6a814`  
		Last Modified: Tue, 04 Jul 2023 07:11:14 GMT  
		Size: 25.2 MB (25178309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c065bd9257e8106bcd249c68ab9c583e09c52a897c3ee556a285230778e052`  
		Last Modified: Tue, 04 Jul 2023 07:11:11 GMT  
		Size: 865.8 KB (865846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f388f2fe8b68155bac332b7e8a14b2cbe70791fb653bb18734bb097e2377f0c2`  
		Last Modified: Tue, 04 Jul 2023 07:11:11 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c31e2e824ca5623dafd5caf30d34a1e758be709b9421e5308d5e5ba01bba509`  
		Last Modified: Tue, 04 Jul 2023 07:11:40 GMT  
		Size: 263.0 MB (263024782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:6cd021882325eac207a33aaf0e24d31d4591faf55eed97136086ae9ce5e7f451
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324240509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d9164d48a1b349114116eec1fbe6f5a2f3fb39f215aad1b534973764dcf3a0`
-	Default Command: `["R"]`

```dockerfile
# Tue, 04 Jul 2023 01:59:20 GMT
ADD file:7c88bfb3f20f1d350105594d828661ca616d541d9efd2337a981f3da607d714a in / 
# Tue, 04 Jul 2023 01:59:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 09:50:59 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 04 Jul 2023 09:51:00 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 04 Jul 2023 09:51:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 09:51:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 04 Jul 2023 09:51:12 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 09:51:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 04 Jul 2023 09:51:13 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 04 Jul 2023 09:51:13 GMT
ENV R_BASE_VERSION=4.3.1
# Tue, 04 Jul 2023 09:52:41 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 09:52:45 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6c47644f3190914c8cddc6aa8fbe2992624219125ffe676d8186f7a2492ede06`  
		Last Modified: Tue, 04 Jul 2023 02:04:55 GMT  
		Size: 49.5 MB (49524494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f815751959c538cc987a3a3a7aa391ed5a6ace996b7c8615c5143b6589fa6bf1`  
		Last Modified: Tue, 04 Jul 2023 09:52:58 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b4f64f4112c559c4febefce24b7180654c18c681f03f5eeb21394c829e6aed`  
		Last Modified: Tue, 04 Jul 2023 09:53:00 GMT  
		Size: 25.0 MB (25000972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379e41c949787b5bdedb78b91810250a0e5082a638490d0ab685a01feee5c917`  
		Last Modified: Tue, 04 Jul 2023 09:52:58 GMT  
		Size: 865.9 KB (865851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee9b4801a66e67daf317855a0dbdae94324acd90f57e4a1ed69d85000fc355a`  
		Last Modified: Tue, 04 Jul 2023 09:52:58 GMT  
		Size: 346.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa24baee642d00544a32191346e28385115ca4c60e8b4069416bdb1e6d8dcbb`  
		Last Modified: Tue, 04 Jul 2023 09:53:19 GMT  
		Size: 248.8 MB (248845488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:20b9ee3f6ca171833cb3f181e13c3bd8e9d9e1217fb97383fe4fed335fdd52c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339627090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c7dac40d82e0dfec54b074f580f0dea9a0f84357b48e893a81f5ffdf3a7329`
-	Default Command: `["R"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:50 GMT
ADD file:c800eebe5b5256d5f3eb9d436f7401634618c397b30f31d8beee6daa24772dee in / 
# Mon, 12 Jun 2023 23:20:54 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:01:26 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Jun 2023 07:01:27 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 13 Jun 2023 07:01:47 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:01:51 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 13 Jun 2023 07:01:52 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Jun 2023 07:01:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Jun 2023 07:01:53 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 20 Jun 2023 22:17:36 GMT
ENV R_BASE_VERSION=4.3.1
# Tue, 20 Jun 2023 22:21:59 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Jun 2023 22:22:12 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:da363b5a528e02b2ccc2452bd956ac683fa34d495ffdfd1407ffd0bd41cb001a`  
		Last Modified: Mon, 12 Jun 2023 23:27:36 GMT  
		Size: 53.5 MB (53536756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c48b63dbc8203e931d84f41ad09099a3028f74e0de284398a50d4212b5a1b2b`  
		Last Modified: Tue, 13 Jun 2023 07:05:13 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ccb7cfd103d968b0337507ee49bb5171fe8b8c5c74adb5af8cb3dcc6e568fe`  
		Last Modified: Tue, 13 Jun 2023 07:05:16 GMT  
		Size: 25.6 MB (25578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b8cc93cc8be20745d9070e877ae867c2b15547fa7160e151bff57c3417b557`  
		Last Modified: Tue, 13 Jun 2023 07:05:12 GMT  
		Size: 865.9 KB (865852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c8bc99811dbe6a83892b6b4f56a01256b59b9dc439bc7d8342767b3f3795dc`  
		Last Modified: Tue, 13 Jun 2023 07:05:11 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440ef8655cf83730c53a4341be03a450079d6625702dcad71a6019fa253f3433`  
		Last Modified: Tue, 20 Jun 2023 22:23:15 GMT  
		Size: 259.6 MB (259642305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:9671f2981f451f741b75cdff8c91456590707eaa976684fa7ebd44e3532a0620
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299192994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7b500faf2365b996142f27ed52be5a12f04fb4eed6e80f752d6de4b40a18fd`
-	Default Command: `["R"]`

```dockerfile
# Tue, 04 Jul 2023 01:34:19 GMT
ADD file:905d0d0e6d4f57fc2258b13e088f9d03967c81aa9affec0d939ac1dc063668f4 in / 
# Tue, 04 Jul 2023 01:34:22 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 12:38:01 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 04 Jul 2023 12:38:01 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 04 Jul 2023 12:38:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 12:38:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 04 Jul 2023 12:38:13 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 12:38:13 GMT
ENV LANG=en_US.UTF-8
# Tue, 04 Jul 2023 12:38:13 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 04 Jul 2023 12:38:13 GMT
ENV R_BASE_VERSION=4.3.1
# Tue, 04 Jul 2023 12:39:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 12:39:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:91571ef190c1d77037a9711c8341236d7f9955149bcb264c8c332f20daf0519e`  
		Last Modified: Tue, 04 Jul 2023 01:39:01 GMT  
		Size: 47.9 MB (47949790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60736f5d3a305414ae07cde2b2659f8a530634bd7fdbd5f0f49d9341ad43497`  
		Last Modified: Tue, 04 Jul 2023 12:39:55 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87719a401bab5106b48cc77baab5b99f57689c60d4870df46f19e9b77701ae30`  
		Last Modified: Tue, 04 Jul 2023 12:39:58 GMT  
		Size: 24.8 MB (24846509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d1237dfbcd790e563df112aee3fad857c9bd8675356163cd8d29242a16a49f`  
		Last Modified: Tue, 04 Jul 2023 12:39:55 GMT  
		Size: 921.0 KB (921007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681465620c7383793d1cc757b7a97fa1180dc669601791ad65e8b90f43554c62`  
		Last Modified: Tue, 04 Jul 2023 12:39:55 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee9f29b54c8e3cbfba99f6c498aebf4e447e79cdfd98a30974431dbb980929a`  
		Last Modified: Tue, 04 Jul 2023 12:40:19 GMT  
		Size: 225.5 MB (225471979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
