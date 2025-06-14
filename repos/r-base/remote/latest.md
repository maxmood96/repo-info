## `r-base:latest`

```console
$ docker pull r-base@sha256:b453d0bb1e3251bc1599d16bb04cb2391ebe1b684153b09491b6506c214c4017
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
$ docker pull r-base@sha256:e7f74e401d5ffc72052486ccf1bbeb768c97c1480d4ddf8e1bead914718c3061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360059648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c7c6fb77c9b9925c3bac9b16096127a1e9c366163db44e5b91839c46fc7fd1`
-	Default Command: `["R"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1749513600'
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
	-	`sha256:4ff4bffc3f08cd1d95feabad784f3c375e82ea1205f7a5a16592da1233a7f424`  
		Last Modified: Tue, 10 Jun 2025 22:47:35 GMT  
		Size: 49.3 MB (49253857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc306264537cc16e0a095e957b67787b2c7c46eeb273532298ec9d1878281a5f`  
		Last Modified: Fri, 13 Jun 2025 17:24:56 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ea0743c79d2754d732b042aa421360691ab72b042ebadc4fa0bd53d1557c52`  
		Last Modified: Fri, 13 Jun 2025 17:24:49 GMT  
		Size: 26.9 MB (26899150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fe902e5436f241543922dfa26df601c0011c23ca5f4c81356c04243b9ac07f`  
		Last Modified: Fri, 13 Jun 2025 17:24:54 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2516f5f41bcb69f069dcc34e764d41bc475ccea2bcfcccba58e2688e41ec42`  
		Last Modified: Fri, 13 Jun 2025 17:24:48 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575ee34798689154f4ad28c764703ab240a6ffabfb95aef40518a2a2abd3bb0`  
		Last Modified: Fri, 13 Jun 2025 18:14:39 GMT  
		Size: 283.0 MB (283034487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:086efb99ce4901b3400050a2c4f42b44c6d792aa5a1a1bfaf395219e0896af9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12941137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9ba0ba776f0bacb0d809f922d8ba23577a730a9efe6efe704c9cf3d4119783`

```dockerfile
```

-	Layers:
	-	`sha256:6682d02073c8687e1b183699a9adb32c7be303c8cc38046d65bf542cd431ba90`  
		Last Modified: Fri, 13 Jun 2025 18:13:19 GMT  
		Size: 12.9 MB (12922998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a99a5c6f0044fb9c6d96030956a847f3cfa3a35b3a66e4b565a22492523a7c3`  
		Last Modified: Fri, 13 Jun 2025 18:13:20 GMT  
		Size: 18.1 KB (18139 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:0d29725b3a78d483a111ddb579279373cace43a5801fc7cdcd161defda8de189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344490156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19ff8d12c5ead0a9a2c5a47ea9791ee8d76128753bef019153e86c2795556cf`
-	Default Command: `["R"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1749513600'
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
	-	`sha256:2584ee33622825de68aac8f6321753e02da0f3221630beb0c925bab76ac076f1`  
		Last Modified: Tue, 10 Jun 2025 22:52:06 GMT  
		Size: 49.6 MB (49621526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9123f61ecfd11f8267d0e9fe82accaa3d09b4e765833e45f6f56605fe4194393`  
		Last Modified: Fri, 13 Jun 2025 19:50:08 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba869059508fe73d836c0a8de37f007ed2a8440a77d9d46c8d92096bc3b8a58e`  
		Last Modified: Fri, 13 Jun 2025 19:50:12 GMT  
		Size: 26.8 MB (26801076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eb9fb7a00277c1c775aec74e446bb433101ad1529ba30cdfb840b43f72f074`  
		Last Modified: Fri, 13 Jun 2025 19:50:10 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541854bf33a3ba388d77c3aba2f06751d705f4831a2cc4911ab2f937b276d0e5`  
		Last Modified: Fri, 13 Jun 2025 19:50:10 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2e0c728d04fe27c5a82b63454343c93a0861b4244ecd49c78dfe3421aec6fb`  
		Last Modified: Sat, 14 Jun 2025 01:27:55 GMT  
		Size: 267.2 MB (267195408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:c3194c532a4f6ea138cca008d95902a3808484305e1436b47026736094ee7064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13039996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730b00c70bf4e075d9eb0e096580f9c9e7ce9a33f9711a131412a61365182dc4`

```dockerfile
```

-	Layers:
	-	`sha256:6229fe6abd50955f0a27a19f350c7cf1eab6162692fa9065798e246647335af4`  
		Last Modified: Fri, 13 Jun 2025 21:13:30 GMT  
		Size: 13.0 MB (13021715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ced8295d3a32e3cb84c449abbfe699ee2d7fb0181776c02f9bc24a0db8a2e03`  
		Last Modified: Fri, 13 Jun 2025 21:13:31 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:9c41ac583c8715fd20405e7991a0d74ea4242fb693969459fa7973b09c6d0403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.1 MB (354136787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289b2c2260bfcc13a5a5075921e72524f63c15260ed4a2f237b2df093ada2581`
-	Default Command: `["R"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1749513600'
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
	-	`sha256:0c6457f694fbdaf02bab289aa278962ffe34817c6b1567f0311b7021b6a6ef4c`  
		Last Modified: Tue, 10 Jun 2025 22:51:18 GMT  
		Size: 53.1 MB (53090931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4364dae8f25219e5ea6e2925be8c14758e71270ac09e3047471ab31b516cdde6`  
		Last Modified: Fri, 13 Jun 2025 22:17:06 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115f0966d820a5c0237d746d5224671e29963e4eae75fd7823f68d584194da61`  
		Last Modified: Fri, 13 Jun 2025 22:17:09 GMT  
		Size: 27.2 MB (27166954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29bc10da56808f50646f265b440d49166615e1e11b4e01e6d5ae5870d4f8aae`  
		Last Modified: Fri, 13 Jun 2025 22:17:07 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dce0ecb4341068ba80ed3658d20ee3e3e98248a5adaf1e8f4def26e248bdde`  
		Last Modified: Fri, 13 Jun 2025 22:17:06 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d0c2a36487e44ff9fdec44dfb416fc550810561d405ce447141b3d86bfbdf3`  
		Last Modified: Sat, 14 Jun 2025 01:33:02 GMT  
		Size: 273.0 MB (273006748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:7155e1631094d73267cc47deff2efb0e91d81cb203927023f4d97200438b0da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12946825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f72105c06745b0cf94c5f4d8a529733a77b03e00b9abc57c766274fbcb65ad7`

```dockerfile
```

-	Layers:
	-	`sha256:850e7081af705af67d2a944c8f5c31bc44b9b548f3fd42e02cb70bd407261be3`  
		Last Modified: Sat, 14 Jun 2025 00:13:35 GMT  
		Size: 12.9 MB (12928645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1f996160df1aa8907cf92827fa7971eabff2bd66179f9fd316ddda58831f6f`  
		Last Modified: Sat, 14 Jun 2025 00:13:36 GMT  
		Size: 18.2 KB (18180 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:65268f7e4a6876b88f3d4477266ff2d0fb14d7722bb79b6c24c076b5ea4dda79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327236236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52e13b52df8ef2d9502958ff282e3e7379a499f1dcb5785db29bf8c9d3ff081`
-	Default Command: `["R"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1749513600'
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
	-	`sha256:d36874750d91bcfb68b6278bc4ac7b65b49eaa71d557564fe1954853bbbd7588`  
		Last Modified: Wed, 11 Jun 2025 02:05:42 GMT  
		Size: 49.3 MB (49329766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8b3943aa7b61449175d647e85b601e36ded18690038a0aedcb70b969ec4425`  
		Last Modified: Fri, 13 Jun 2025 19:03:45 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7613ae8a3978acbbcc21e7c87249d1034e8e7903914c70661f1fbb6840a594`  
		Last Modified: Fri, 13 Jun 2025 19:03:48 GMT  
		Size: 26.9 MB (26866903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dca0bcc42eea01895e316157baff3af6b479286fdb40815f2d3c1df3fe88256`  
		Last Modified: Fri, 13 Jun 2025 19:03:45 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcc1ce51ccbf01a75395d0e53746d2a5f524cd867cc3900cf534d3f37acec3f`  
		Last Modified: Fri, 13 Jun 2025 19:03:44 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e829993c913bb92f6697ec5f3235838a4ce5fee4f10056c9560667d677fa5378`  
		Last Modified: Sat, 14 Jun 2025 01:38:39 GMT  
		Size: 250.1 MB (250111357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f7b363df829e3573ed5aa064af356d6c72e346aa41bc6ff59f18940b9217c5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12752280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd67e253dd81ffcfd08d9bd49cfe1fbf0e1f2dca70a6127397e400ba348b0d9`

```dockerfile
```

-	Layers:
	-	`sha256:d3cad624eaafbcc5fdb58510f86829d78de39b289a04946e9fb03b264f241b59`  
		Last Modified: Fri, 13 Jun 2025 21:13:44 GMT  
		Size: 12.7 MB (12734139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be479d625bcb411faf269a99b1d45d956a058100e1a30ea960289ae109692222`  
		Last Modified: Fri, 13 Jun 2025 21:13:44 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
