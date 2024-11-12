<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.2`](#r-base442)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.2`

```console
$ docker pull r-base@sha256:3eb44ff41a1e6e428fd95eb26cac4fdc6a3473df41265280da7aa2ea01780fb3
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

### `r-base:4.4.2` - linux; amd64

```console
$ docker pull r-base@sha256:3a5226a4070a7ff76ee6b50d6ccc668e41cf0be28205d98177d044553a73e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.1 MB (354145749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16d19479021f579c790a1b5e216cd778622d17fd18ef420efc895b937bb1ef9`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c1f3f669a92f4b53dd069b7da2ebc504d2fdec161442dba2fc3ea1f47ff18b14`  
		Last Modified: Tue, 12 Nov 2024 00:55:03 GMT  
		Size: 53.2 MB (53226783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da929976e0644c860ff89c01bf3bf90d08ca8eebe045546aa155e460086ecac`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ff877eea58514c5274f4922d83865e610aae93f32f586d40af40310176e82e`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 23.2 MB (23170263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0581e5b835f0ac2291d2db5a88f801e7a1ae5dfca206e2b95d332790ef9d861e`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 866.7 KB (866744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd925e584ee927e31a8ca9b2eb681fa1b42e26646dbde6385cd4ac5b1e72ae8`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896d66f6f118fe8dea2be4acf5e965f74a53919a7256f733c14d224da1794a16`  
		Last Modified: Tue, 12 Nov 2024 02:37:36 GMT  
		Size: 276.9 MB (276878301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.2` - unknown; unknown

```console
$ docker pull r-base@sha256:b2e92e852ff804041179573915be8863a3aa84693ae40688957f952d75892369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12602728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc3d142309ad2c5215d7a422b10fbcba55e82c80ebd43571c88e86019ad068`

```dockerfile
```

-	Layers:
	-	`sha256:f5d10ba5db55a7b685b4f9226a77617e7eb981553a1ad731df9b1400a3d25aab`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 12.6 MB (12584587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a11ef98bcce8fbc308dc5eaa10c61e4ba5981d6f07bc101b764a470df1b9b67`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:79bd1bb12c1465d0d34b07255925b11f899b90d144945fc41f0823e474d664e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347500585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f25e01f7cfa0f153e8d4caaad435b0ade4fd1362c59ebd7f8ad1c5bb70129c`
-	Default Command: `["R"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:03 GMT
ADD file:e3e9f477c791fc688010cc87eaedfcd80ede2cdd070c953518b515ed1b668a55 in / 
# Thu, 17 Oct 2024 01:13:04 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a6d8e57ff3309f685dd823e43fca05a8da4dba501d2eae9451a046edaeaca8d2`  
		Last Modified: Thu, 17 Oct 2024 01:16:49 GMT  
		Size: 53.6 MB (53599758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a263d1f16674c467fe5be6fbe7b0469abcfd8b97c0a1ae6c4b99a6d60338acb5`  
		Last Modified: Mon, 04 Nov 2024 20:59:37 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394e0750c7872c810ae0a6d64633587d9a201af101b7c0e4d569c4512a458cfc`  
		Last Modified: Mon, 04 Nov 2024 20:59:38 GMT  
		Size: 26.3 MB (26267574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d351ce24c3bc2473504445a640a970742ab193a05b63c3d867edfd016f78a7c`  
		Last Modified: Mon, 04 Nov 2024 20:59:37 GMT  
		Size: 866.7 KB (866744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9372e99721d44e2ce69dcd75aaf083eb13ea034c41e200568de5f111da00f65d`  
		Last Modified: Mon, 04 Nov 2024 20:59:37 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667a0546e4d95cdb2ad6ae449ed72f31dd4201e98797c389a4c86dfbf602d804`  
		Last Modified: Mon, 04 Nov 2024 20:59:44 GMT  
		Size: 266.8 MB (266762844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.2` - unknown; unknown

```console
$ docker pull r-base@sha256:fd07acd2efefdd14a73ae5f5840988115e46dd932c00062ccf3eba673e0605df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12704220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3c917ebafe3dd35f1ade72013f2c4b8c6c71c13a9fe1c9f706afd88f1aba93`

```dockerfile
```

-	Layers:
	-	`sha256:c7273e499f65f6d4981deaeefadd29808bc0493318c0d79b038c05fe3b20f0bf`  
		Last Modified: Mon, 04 Nov 2024 20:59:38 GMT  
		Size: 12.7 MB (12686123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d350dc63b2f23c2f56e5a3d3f4caf78d0714c623d6a4534ca08f3a1fba4c22cb`  
		Last Modified: Mon, 04 Nov 2024 20:59:37 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:cc56be8bceabf5a4975372c2d94c82b403ccb16349f5e3a54700bf623821dec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.8 MB (356769738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed970da681e9ebec446f6c438ca746b1f488fa38351d1a6770b651be29b9da5e`
-	Default Command: `["R"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:50 GMT
ADD file:5c4544ac0d27b357afba9feb379224b111f7149e7b3f21fe35317eef03b8bcea in / 
# Thu, 17 Oct 2024 01:19:53 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:311042d460227ad120f24056ab56c7fe2202f03f09ec22ed4f93b2ffc0adb201`  
		Last Modified: Thu, 17 Oct 2024 01:23:20 GMT  
		Size: 57.1 MB (57126660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165425e5ba9726db340382dcdd65e7f6063d196dbfbb4ede5bc70c9273e235ae`  
		Last Modified: Mon, 04 Nov 2024 21:01:19 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1440abf71f194d24d416a09c3575470cf8c130babaaa8700ca1e704ed0dc2e4d`  
		Last Modified: Mon, 04 Nov 2024 21:01:21 GMT  
		Size: 26.3 MB (26339262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f66ad4dc4c9da0a66fb30a8935201f5957187b4034fc125c2a7f667da6cc66`  
		Last Modified: Mon, 04 Nov 2024 21:01:20 GMT  
		Size: 866.7 KB (866746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48220684a6dc6af2e2348239845d9efc86df8bfa2828e488ef096f376c9953e9`  
		Last Modified: Mon, 04 Nov 2024 21:01:19 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bcd18d81b31db2fcfe5527ff57bd373fc7120c67e70d809a03ac798f0d7eae`  
		Last Modified: Mon, 04 Nov 2024 21:01:28 GMT  
		Size: 272.4 MB (272433410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.2` - unknown; unknown

```console
$ docker pull r-base@sha256:9314c79d8921b21cdd12d01b3c6a4b34effff24ac46ce0b53b753ac068008bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12589014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a89d0c346de1045ad13d0235025f4a554e06f923a407ea9d922796f61a39b8`

```dockerfile
```

-	Layers:
	-	`sha256:31fb984e5274065424bc821d06b8c5f5b76ffbfa8775a6a5b443a6c0bfdfb572`  
		Last Modified: Mon, 04 Nov 2024 21:01:20 GMT  
		Size: 12.6 MB (12571017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee449623febf48ae921330b99186c0010a6e13ba140d20df0e4cf4d10361f8d`  
		Last Modified: Mon, 04 Nov 2024 21:01:19 GMT  
		Size: 18.0 KB (17997 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.2` - linux; s390x

```console
$ docker pull r-base@sha256:05c188dc01c2e4ffe23c5449ca7a12695eca1a19b983aecfca199c220a3fce18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328301288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30041231370ca64204e33544a77d7d2e506daae0ab55c50b4a0b52b28153df0e`
-	Default Command: `["R"]`

```dockerfile
# Thu, 17 Oct 2024 01:47:36 GMT
ADD file:61f096f81ed7cfc876be4edad4438e9e9e439382507d192f09f51c428e99a482 in / 
# Thu, 17 Oct 2024 01:47:38 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f66a11769d6242f4b78b255eed3607d4c3b4b3fa3e8fb47724dd3586e9a6da4f`  
		Last Modified: Thu, 17 Oct 2024 01:51:31 GMT  
		Size: 52.8 MB (52808853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdf454b2b350177821807d4fe1f38cbaf90c2bb2e2aaa6671f250f6e3f03a7`  
		Last Modified: Mon, 04 Nov 2024 20:59:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431629a16002b3b5958490ef9a97dcf467aa58a20f712628335108333b155e41`  
		Last Modified: Mon, 04 Nov 2024 20:59:56 GMT  
		Size: 25.5 MB (25503496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1a6af4d81e4f3f08c67cb10ef1a51237f6afa68abdcd72c34ef7e562dd89dd`  
		Last Modified: Mon, 04 Nov 2024 20:59:55 GMT  
		Size: 923.5 KB (923487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792e79b292cde90e3a3ad156eea2a6928999d2cc9c9ed126b58f24fe7f4b689b`  
		Last Modified: Mon, 04 Nov 2024 20:59:56 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931d726549aff2598bae7374a1db4234e6c252b6924c66e527ed80400acc183c`  
		Last Modified: Mon, 04 Nov 2024 21:00:00 GMT  
		Size: 249.1 MB (249061792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.2` - unknown; unknown

```console
$ docker pull r-base@sha256:937300e4710146c4fb252b833f1f2d9dfa53627e375b3809090c88771d8baf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12395746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df84afe09aa8541a7cdeb91e652c0eec2d87bb91f66de15d08233c1c6204535`

```dockerfile
```

-	Layers:
	-	`sha256:2101aece3cc25e9c38ea808b34d89371d189d981aef567bc28404fab6b71c96a`  
		Last Modified: Mon, 04 Nov 2024 20:59:55 GMT  
		Size: 12.4 MB (12377783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4011111be779e0a7adf9918abad7e38fd773fb6436cd70adbdfca4cff227de2e`  
		Last Modified: Mon, 04 Nov 2024 20:59:55 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:3eb44ff41a1e6e428fd95eb26cac4fdc6a3473df41265280da7aa2ea01780fb3
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
$ docker pull r-base@sha256:3a5226a4070a7ff76ee6b50d6ccc668e41cf0be28205d98177d044553a73e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.1 MB (354145749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16d19479021f579c790a1b5e216cd778622d17fd18ef420efc895b937bb1ef9`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c1f3f669a92f4b53dd069b7da2ebc504d2fdec161442dba2fc3ea1f47ff18b14`  
		Last Modified: Tue, 12 Nov 2024 00:55:03 GMT  
		Size: 53.2 MB (53226783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da929976e0644c860ff89c01bf3bf90d08ca8eebe045546aa155e460086ecac`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ff877eea58514c5274f4922d83865e610aae93f32f586d40af40310176e82e`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 23.2 MB (23170263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0581e5b835f0ac2291d2db5a88f801e7a1ae5dfca206e2b95d332790ef9d861e`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 866.7 KB (866744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd925e584ee927e31a8ca9b2eb681fa1b42e26646dbde6385cd4ac5b1e72ae8`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896d66f6f118fe8dea2be4acf5e965f74a53919a7256f733c14d224da1794a16`  
		Last Modified: Tue, 12 Nov 2024 02:37:36 GMT  
		Size: 276.9 MB (276878301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:b2e92e852ff804041179573915be8863a3aa84693ae40688957f952d75892369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12602728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc3d142309ad2c5215d7a422b10fbcba55e82c80ebd43571c88e86019ad068`

```dockerfile
```

-	Layers:
	-	`sha256:f5d10ba5db55a7b685b4f9226a77617e7eb981553a1ad731df9b1400a3d25aab`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 12.6 MB (12584587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a11ef98bcce8fbc308dc5eaa10c61e4ba5981d6f07bc101b764a470df1b9b67`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:79bd1bb12c1465d0d34b07255925b11f899b90d144945fc41f0823e474d664e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347500585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f25e01f7cfa0f153e8d4caaad435b0ade4fd1362c59ebd7f8ad1c5bb70129c`
-	Default Command: `["R"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:03 GMT
ADD file:e3e9f477c791fc688010cc87eaedfcd80ede2cdd070c953518b515ed1b668a55 in / 
# Thu, 17 Oct 2024 01:13:04 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a6d8e57ff3309f685dd823e43fca05a8da4dba501d2eae9451a046edaeaca8d2`  
		Last Modified: Thu, 17 Oct 2024 01:16:49 GMT  
		Size: 53.6 MB (53599758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a263d1f16674c467fe5be6fbe7b0469abcfd8b97c0a1ae6c4b99a6d60338acb5`  
		Last Modified: Mon, 04 Nov 2024 20:59:37 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394e0750c7872c810ae0a6d64633587d9a201af101b7c0e4d569c4512a458cfc`  
		Last Modified: Mon, 04 Nov 2024 20:59:38 GMT  
		Size: 26.3 MB (26267574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d351ce24c3bc2473504445a640a970742ab193a05b63c3d867edfd016f78a7c`  
		Last Modified: Mon, 04 Nov 2024 20:59:37 GMT  
		Size: 866.7 KB (866744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9372e99721d44e2ce69dcd75aaf083eb13ea034c41e200568de5f111da00f65d`  
		Last Modified: Mon, 04 Nov 2024 20:59:37 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667a0546e4d95cdb2ad6ae449ed72f31dd4201e98797c389a4c86dfbf602d804`  
		Last Modified: Mon, 04 Nov 2024 20:59:44 GMT  
		Size: 266.8 MB (266762844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:fd07acd2efefdd14a73ae5f5840988115e46dd932c00062ccf3eba673e0605df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12704220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3c917ebafe3dd35f1ade72013f2c4b8c6c71c13a9fe1c9f706afd88f1aba93`

```dockerfile
```

-	Layers:
	-	`sha256:c7273e499f65f6d4981deaeefadd29808bc0493318c0d79b038c05fe3b20f0bf`  
		Last Modified: Mon, 04 Nov 2024 20:59:38 GMT  
		Size: 12.7 MB (12686123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d350dc63b2f23c2f56e5a3d3f4caf78d0714c623d6a4534ca08f3a1fba4c22cb`  
		Last Modified: Mon, 04 Nov 2024 20:59:37 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:cc56be8bceabf5a4975372c2d94c82b403ccb16349f5e3a54700bf623821dec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.8 MB (356769738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed970da681e9ebec446f6c438ca746b1f488fa38351d1a6770b651be29b9da5e`
-	Default Command: `["R"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:50 GMT
ADD file:5c4544ac0d27b357afba9feb379224b111f7149e7b3f21fe35317eef03b8bcea in / 
# Thu, 17 Oct 2024 01:19:53 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:311042d460227ad120f24056ab56c7fe2202f03f09ec22ed4f93b2ffc0adb201`  
		Last Modified: Thu, 17 Oct 2024 01:23:20 GMT  
		Size: 57.1 MB (57126660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165425e5ba9726db340382dcdd65e7f6063d196dbfbb4ede5bc70c9273e235ae`  
		Last Modified: Mon, 04 Nov 2024 21:01:19 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1440abf71f194d24d416a09c3575470cf8c130babaaa8700ca1e704ed0dc2e4d`  
		Last Modified: Mon, 04 Nov 2024 21:01:21 GMT  
		Size: 26.3 MB (26339262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f66ad4dc4c9da0a66fb30a8935201f5957187b4034fc125c2a7f667da6cc66`  
		Last Modified: Mon, 04 Nov 2024 21:01:20 GMT  
		Size: 866.7 KB (866746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48220684a6dc6af2e2348239845d9efc86df8bfa2828e488ef096f376c9953e9`  
		Last Modified: Mon, 04 Nov 2024 21:01:19 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bcd18d81b31db2fcfe5527ff57bd373fc7120c67e70d809a03ac798f0d7eae`  
		Last Modified: Mon, 04 Nov 2024 21:01:28 GMT  
		Size: 272.4 MB (272433410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:9314c79d8921b21cdd12d01b3c6a4b34effff24ac46ce0b53b753ac068008bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12589014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a89d0c346de1045ad13d0235025f4a554e06f923a407ea9d922796f61a39b8`

```dockerfile
```

-	Layers:
	-	`sha256:31fb984e5274065424bc821d06b8c5f5b76ffbfa8775a6a5b443a6c0bfdfb572`  
		Last Modified: Mon, 04 Nov 2024 21:01:20 GMT  
		Size: 12.6 MB (12571017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee449623febf48ae921330b99186c0010a6e13ba140d20df0e4cf4d10361f8d`  
		Last Modified: Mon, 04 Nov 2024 21:01:19 GMT  
		Size: 18.0 KB (17997 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:05c188dc01c2e4ffe23c5449ca7a12695eca1a19b983aecfca199c220a3fce18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328301288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30041231370ca64204e33544a77d7d2e506daae0ab55c50b4a0b52b28153df0e`
-	Default Command: `["R"]`

```dockerfile
# Thu, 17 Oct 2024 01:47:36 GMT
ADD file:61f096f81ed7cfc876be4edad4438e9e9e439382507d192f09f51c428e99a482 in / 
# Thu, 17 Oct 2024 01:47:38 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f66a11769d6242f4b78b255eed3607d4c3b4b3fa3e8fb47724dd3586e9a6da4f`  
		Last Modified: Thu, 17 Oct 2024 01:51:31 GMT  
		Size: 52.8 MB (52808853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdf454b2b350177821807d4fe1f38cbaf90c2bb2e2aaa6671f250f6e3f03a7`  
		Last Modified: Mon, 04 Nov 2024 20:59:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431629a16002b3b5958490ef9a97dcf467aa58a20f712628335108333b155e41`  
		Last Modified: Mon, 04 Nov 2024 20:59:56 GMT  
		Size: 25.5 MB (25503496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1a6af4d81e4f3f08c67cb10ef1a51237f6afa68abdcd72c34ef7e562dd89dd`  
		Last Modified: Mon, 04 Nov 2024 20:59:55 GMT  
		Size: 923.5 KB (923487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792e79b292cde90e3a3ad156eea2a6928999d2cc9c9ed126b58f24fe7f4b689b`  
		Last Modified: Mon, 04 Nov 2024 20:59:56 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931d726549aff2598bae7374a1db4234e6c252b6924c66e527ed80400acc183c`  
		Last Modified: Mon, 04 Nov 2024 21:00:00 GMT  
		Size: 249.1 MB (249061792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:937300e4710146c4fb252b833f1f2d9dfa53627e375b3809090c88771d8baf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12395746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df84afe09aa8541a7cdeb91e652c0eec2d87bb91f66de15d08233c1c6204535`

```dockerfile
```

-	Layers:
	-	`sha256:2101aece3cc25e9c38ea808b34d89371d189d981aef567bc28404fab6b71c96a`  
		Last Modified: Mon, 04 Nov 2024 20:59:55 GMT  
		Size: 12.4 MB (12377783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4011111be779e0a7adf9918abad7e38fd773fb6436cd70adbdfca4cff227de2e`  
		Last Modified: Mon, 04 Nov 2024 20:59:55 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json
