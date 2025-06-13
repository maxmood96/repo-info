## `r-base:latest`

```console
$ docker pull r-base@sha256:dbddaeff8acefd4b10b80f8962a9abc2d91452cf3aa754445460ba26c70af6ee
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
		Last Modified: Fri, 13 Jun 2025 19:49:49 GMT  
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
$ docker pull r-base@sha256:e192cec73e3e568249dcdeacbf9b0ea0754c0585e3d7f57800fb8f58a5d00c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.1 MB (354064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a3a4f527868852873c62d8a378026134cce4049bec654b96d1ea37a1881845`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Apr 2025 18:18:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1749513600'
# Fri, 11 Apr 2025 18:18:21 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Apr 2025 18:18:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV R_BASE_VERSION=4.5.0
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0c6457f694fbdaf02bab289aa278962ffe34817c6b1567f0311b7021b6a6ef4c`  
		Last Modified: Tue, 10 Jun 2025 22:51:18 GMT  
		Size: 53.1 MB (53090931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3947635601bf883f634241271031eaa6b5c530adf57db9bf73e0d5c0e885c43e`  
		Last Modified: Wed, 11 Jun 2025 04:22:38 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de752baa2c3d65c9553fc5c7f075a6c17181d2d9095bfe0a6f0418d75ea55446`  
		Last Modified: Wed, 11 Jun 2025 04:24:12 GMT  
		Size: 27.2 MB (27166721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66900eb6fa719ead84ec032a86085bd6d4cb386b4aee43563db349fdfc6561d`  
		Last Modified: Wed, 11 Jun 2025 04:22:42 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08f72c2f5a3dad2770273ca8558520621d14923fea76ba27aae294cb794548f`  
		Last Modified: Wed, 11 Jun 2025 04:22:46 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae56fe752eb4c09972a5ecb49974bf7c2bef36231aa6a86e381d540c46ee9ebd`  
		Last Modified: Wed, 11 Jun 2025 12:13:27 GMT  
		Size: 272.9 MB (272934797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:14c5c0e49f534faf2be304558682bf99ad78752142b570c1c95c17e4b3fccb47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12946826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573b53a881e528686652696a76fe56d2ee67159636af2b629ecd106b70b288f7`

```dockerfile
```

-	Layers:
	-	`sha256:4eb6f4bce566f9ea633c0236c6c78777f716b95a1555836bb3f86e308fb7512e`  
		Last Modified: Wed, 11 Jun 2025 06:13:39 GMT  
		Size: 12.9 MB (12928645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbe541baebc9aaff7d18638840b7aea94526ea4d09a0a04f80f6555184de86c`  
		Last Modified: Wed, 11 Jun 2025 06:13:40 GMT  
		Size: 18.2 KB (18181 bytes)  
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
		Last Modified: Fri, 13 Jun 2025 19:03:20 GMT  
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
