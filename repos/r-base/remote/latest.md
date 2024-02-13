## `r-base:latest`

```console
$ docker pull r-base@sha256:4bdf68161b2ed65fa6ca8285d1dc445ceb8100e94f503c56f59d2cfc453c7cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:047334e11cedf798682a4402e54d5a0832979aa1cf4df3bb1264be111392cf0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349255075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcd3973c46d5d18c5da58714a8574cceb7c1e2a0424ef20c0a6e2b49a5a0239`
-	Default Command: `["R"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:42 GMT
ADD file:60accd0e24f9359f285bdb996cc23936f5277a33b0c08d9e01c25b16f02e03cf in / 
# Tue, 13 Feb 2024 00:39:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:58:41 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Feb 2024 07:58:42 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 13 Feb 2024 07:58:52 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:58:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:58:54 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 07:58:54 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:58:55 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 13 Feb 2024 07:58:55 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 13 Feb 2024 07:59:52 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:59:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0b1f27ef3dce030fde69c2689259679ae6e799a473bd1aaf174fea653de5b1d6`  
		Last Modified: Tue, 13 Feb 2024 00:45:59 GMT  
		Size: 52.3 MB (52331573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d3e9c4848f501db8468a34003e05e41859720acfbca8870cdbf2f0a540abb`  
		Last Modified: Tue, 13 Feb 2024 08:00:16 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231db3b0cffcf678da53090c6dba04799f064614ad615cb1b07374d5182fb033`  
		Last Modified: Tue, 13 Feb 2024 08:00:19 GMT  
		Size: 25.5 MB (25540031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f88cacec3b94a5c3680566276556a1ad0c4582626daace78e62a4d26d2caa0`  
		Last Modified: Tue, 13 Feb 2024 08:00:16 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9ef2e707da945e16168ba5e4cef9448815e27a43667ce556a729d97b5ad2a3`  
		Last Modified: Tue, 13 Feb 2024 08:00:16 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53938125944ad7a21226f4a1afd13a1473758d0d1e3f0d4b756e1424c9207d80`  
		Last Modified: Tue, 13 Feb 2024 08:00:46 GMT  
		Size: 270.5 MB (270513442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:379b9a6f3bde64681fa64505c0b2906417feead8c19ad6bcd973bdbd91f2ad30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (337026349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5802d72c477916925ee61aaeb49608e7763f477011214d5f2d328dae0bab22`
-	Default Command: `["R"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:53 GMT
ADD file:84a74589525ee8c23c5f03b46e981779c3a844eb1650ace0c0f608d665f71690 in / 
# Tue, 13 Feb 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:33:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Feb 2024 07:33:04 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 13 Feb 2024 07:33:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:33:16 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:33:17 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 07:33:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:33:17 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 13 Feb 2024 07:33:17 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 13 Feb 2024 07:34:21 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:34:26 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1dd8c22b346593e149ade1aa99ea3d35442a7aa0f7d3e32abb41db5e4ff20379`  
		Last Modified: Tue, 13 Feb 2024 00:48:35 GMT  
		Size: 52.2 MB (52194113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d56ebea94b2a04482bb5e0b668deb9677812b98cc51928aa266ab558fd7fb`  
		Last Modified: Tue, 13 Feb 2024 07:34:47 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5666500bb0e142ac423bbd25d4a3e3ddaa5187e1d126570958064081b8c21e96`  
		Last Modified: Tue, 13 Feb 2024 07:34:49 GMT  
		Size: 25.3 MB (25330316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55a0e1551eaf53744747f1e40cde0a99598382047683211bb69b4bbcd7bebc0`  
		Last Modified: Tue, 13 Feb 2024 07:34:47 GMT  
		Size: 866.3 KB (866324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40da1c2ff00f634d6818de07b40d839045cba1a4e17dd7f138c1c7fe0bb99a50`  
		Last Modified: Tue, 13 Feb 2024 07:34:47 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a981d8ca7d2843652ffcda06f1295891b1566957892abb88376a0e1004ea27c`  
		Last Modified: Tue, 13 Feb 2024 07:35:08 GMT  
		Size: 258.6 MB (258631893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:554834dc7fac8c3d4e87e908af3f2824692b9c6e1e2db0b701b196988d750131
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350481650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc7a4b821fb39fb6d75f7c21c9aa7c569e734c5865eaa19653c63112167e833`
-	Default Command: `["R"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:09 GMT
ADD file:fb513218e649a1afb3e363333714c9f9699093574358ac0b47cd3046f1eb5186 in / 
# Tue, 13 Feb 2024 00:41:12 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:41:37 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 13 Feb 2024 07:41:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 13 Feb 2024 07:41:57 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:42:00 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:42:01 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 07:42:01 GMT
ENV LANG=en_US.UTF-8
# Tue, 13 Feb 2024 07:42:02 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 13 Feb 2024 07:42:03 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 13 Feb 2024 07:43:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:43:59 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:26cad4a1d56e1b4700207ff4bc765a669dfe6bc2d3fc942e890febbeec77c519`  
		Last Modified: Tue, 13 Feb 2024 00:47:17 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd9bbffa1d774c9166592815a0e576368265a592d044b5c1bbb75f2191580`  
		Last Modified: Tue, 13 Feb 2024 07:44:07 GMT  
		Size: 3.4 KB (3358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a3a9cb161be3007849862bd630cc904e4bbe2b7f0b39f3c06d6997fbfa89a6`  
		Last Modified: Tue, 13 Feb 2024 07:44:11 GMT  
		Size: 25.9 MB (25860108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627fa6d14c62e04f5d17bba4581773ba388912eefbf32b6268257d1eb52d3106`  
		Last Modified: Tue, 13 Feb 2024 07:44:08 GMT  
		Size: 866.3 KB (866339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141427271f0a75234f3cc23f329380f76a19dc3937bc7b500da9d54f0c5810e4`  
		Last Modified: Tue, 13 Feb 2024 07:44:07 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1b101b265a5096daad7c12ae6be73e2dee7144ca9cebd4e352328972c4e0c3`  
		Last Modified: Tue, 13 Feb 2024 07:44:43 GMT  
		Size: 267.5 MB (267516656 bytes)  
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
