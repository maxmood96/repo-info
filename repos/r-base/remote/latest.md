## `r-base:latest`

```console
$ docker pull r-base@sha256:0aab7f28dafb1b36e3aeafb88ad2792bd71b7eb452a907b2e251dcc9e05b5176
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
$ docker pull r-base@sha256:8e18d98f191e5488f5aa6160c6b8070454049663177f500e6527b1304923ce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369262265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e063072dd9b06a5c42842dadfc0a8d3a58fbe21a1e383690f181f69ef14a4a1`
-	Default Command: `["R"]`

```dockerfile
# Fri, 28 Feb 2025 21:48:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1742169600'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:85b4ea79c9044a9663d0967fea182f2820065e34d4ba470c857d90ec0a29780d`  
		Last Modified: Mon, 17 Mar 2025 22:17:42 GMT  
		Size: 47.5 MB (47513469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78ae11910e4a1bad01c4efacde85bc70b64727dc56df68267f4203fa789d8f`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231fe637949b862388f99ab5253061570254fc8ffa204c151af0e4bd88610727`  
		Last Modified: Mon, 17 Mar 2025 23:14:35 GMT  
		Size: 26.8 MB (26793687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e55f773672e38f9df0da877d93607f403a1dbd67c63aa62698b08f9c446db0`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 868.5 KB (868485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed1c5c1eb39d2360d594a382540e3e4577e9bc14eb03787bac8bd74deb1546`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e068a6f1f3c5ec52f0ca37f64f5306ae00c16f85d75cf18d0ba61c41c19235ec`  
		Last Modified: Mon, 17 Mar 2025 23:14:58 GMT  
		Size: 294.1 MB (294082967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:349a0bb8c2152ea452863bbd4fea9f83dfff3c4e8b05d6c247b1c72e71a41858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12602199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff2b9d4b7581902e6c1d7eb46ccb1f56c2e8e7830678805fa2e442ec0cde82a`

```dockerfile
```

-	Layers:
	-	`sha256:cf1ae354abf4d8f3be020d26cdee1183187eeab5c0e5a911bbe8af7c133e2799`  
		Last Modified: Mon, 17 Mar 2025 23:14:35 GMT  
		Size: 12.6 MB (12584059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3a3d8b121310cf18eb2ea73f0edeb94ab8e53827a019a72c1c1e00781931ebd`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:bf4c913af573be314c0f154648de0048ec35a12f68ce5e461f1f586ea28a6d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.7 MB (353697978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13f997dafe42952732e53935c0ac4273294a953f29be583a717c00335a80ec4`
-	Default Command: `["R"]`

```dockerfile
# Fri, 28 Feb 2025 21:48:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1742169600'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a87e40d063d94bca6cee4060371898336a27e03db357917f8f5132975c91cf52`  
		Last Modified: Mon, 17 Mar 2025 22:21:22 GMT  
		Size: 47.9 MB (47886356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e6f17ac23195db9ba9ed8bc5033f998587080432f8b405e4441991691b4b7`  
		Last Modified: Tue, 18 Mar 2025 05:17:01 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a676be49a9178e9d1ec6ccb9703fbf9ce5979d7e3fdac5239338c56f04e79e5`  
		Last Modified: Tue, 18 Mar 2025 05:17:02 GMT  
		Size: 26.7 MB (26690668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b741e82d0ed6dc1c5462149ea872b4f4ab4f6f8134e07f1341682f59e66f17ca`  
		Last Modified: Tue, 18 Mar 2025 05:17:02 GMT  
		Size: 868.5 KB (868478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441fb2c55aab9f2df212fd1aa6827e5d6bf8a61b6d4beca176a7d1e2f9640e68`  
		Last Modified: Tue, 18 Mar 2025 05:17:01 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efec05038212add7a2231637fea78485919e6c0dda2efc03a8e0504ee849eb9f`  
		Last Modified: Tue, 18 Mar 2025 05:17:10 GMT  
		Size: 278.2 MB (278248816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:08212641a2922fdcd7bd2913339403b62ab5d40a1fa8bec4f06d93ee1abd5add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12702603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa815e12e8d27a87ef60e508c2a6e321c814016b1a37ab40c6a055a0dd54956`

```dockerfile
```

-	Layers:
	-	`sha256:a0d86fef0ad97c9854f9f3fb20e2c1bb7a586b22c3915122c20322c238b91e08`  
		Last Modified: Tue, 18 Mar 2025 05:17:02 GMT  
		Size: 12.7 MB (12684322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c295992573902907f7598a33eb2c1af0ca1a707561366d2f628c8052958f5904`  
		Last Modified: Tue, 18 Mar 2025 05:17:01 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:e44d7a60b5ab519a48ee4bbb4288e1909dc83a6ed023e52ea1d9d72b175c2119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (363982898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2840df82aabb787cb6a2f65142a3e0efbdff779f403da918776c5255c2d36013`
-	Default Command: `["R"]`

```dockerfile
# Fri, 28 Feb 2025 21:48:43 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1742169600'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:93b4cf80d4f0aa11fc61d4952c10ab920f3dabbc5c9d761611276b2e062e32e8`  
		Last Modified: Mon, 17 Mar 2025 22:21:27 GMT  
		Size: 51.2 MB (51162726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b9ca4737e993bba79f6cf72d5bf552570335de3322bbbc3c0095383f7c11e0`  
		Last Modified: Tue, 18 Mar 2025 02:18:30 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c90ec3bb6476682fd3f18fa20abed7257210ab2a9e86486fa904344a8950326`  
		Last Modified: Tue, 18 Mar 2025 02:18:31 GMT  
		Size: 27.1 MB (27050807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dbb395738750a47a2340842e5e02fefa1755af0a6cdc6e24f46b6b889824a9`  
		Last Modified: Tue, 18 Mar 2025 02:18:30 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8995313fb9209dda30ce9eabb9693298bc9ffb89b3e10112c316538fcc2d85`  
		Last Modified: Tue, 18 Mar 2025 02:18:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc0fd116c3c541ffa6d128007b60048893663428b7289e1baad6fb7389c19cf`  
		Last Modified: Tue, 18 Mar 2025 02:18:52 GMT  
		Size: 284.9 MB (284897216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:da57ed3f2a1b35f53077344c0507e288cf4f54e27b2264278c9d263ffa5b5838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12604395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287e5f3bdadeaa2a48a11711e847898a8ab35b957b42e110e922cce1839e3b76`

```dockerfile
```

-	Layers:
	-	`sha256:086f3180596b7f714aef99af29351bb3aee59f303ba9948a8eb8ff2772fcc85c`  
		Last Modified: Tue, 18 Mar 2025 02:18:31 GMT  
		Size: 12.6 MB (12586214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07caf5d2df2a2c8ad532be3bc563880e49816a2fdb836ca6862ba9be43d8ddac`  
		Last Modified: Tue, 18 Mar 2025 02:18:30 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:db9b1411aa6673aed0ba8a9693c82748349488c4aa1c2261e15e8d229e2670b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335798195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d51872583d15460e6d8762834d0420caf07d9a5a98a2c6b57ff8bd490b9069d`
-	Default Command: `["R"]`

```dockerfile
# Fri, 28 Feb 2025 21:48:43 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1742169600'
# Fri, 28 Feb 2025 21:48:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 28 Feb 2025 21:48:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Feb 2025 21:48:43 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
ENV R_BASE_VERSION=4.4.3
# Fri, 28 Feb 2025 21:48:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 21:48:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f380e797293e157c2e1f2e1362f5706c0b4f711bdc4d4b7354a7465f3791bb1f`  
		Last Modified: Mon, 17 Mar 2025 22:47:22 GMT  
		Size: 47.5 MB (47548827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b55828dd878c6cb2acaa31b05a84915de0d62c7ac0eff4062afdc201d0af8dd`  
		Last Modified: Tue, 18 Mar 2025 03:31:18 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfbd9d585291b07af691596bd289aca2ed333fc8a4b6cd42392e472a4f6d2bb`  
		Last Modified: Tue, 18 Mar 2025 03:31:19 GMT  
		Size: 26.8 MB (26765097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b1c697d405357f93ab9f2f53cd9e2050efd746066c4d804f271f2d4b4e1b13`  
		Last Modified: Tue, 18 Mar 2025 03:31:18 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3ea81f53c0866eaa8b14fcfda9fdd259b8a094d23bcc4071880aa07f307bac`  
		Last Modified: Tue, 18 Mar 2025 03:31:19 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c1c598dec11aec56c88daf34f45005352ba9bea16991f7bad1a5dbd124b204`  
		Last Modified: Tue, 18 Mar 2025 03:31:24 GMT  
		Size: 260.6 MB (260556060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:3b769b64f7c855e11045c50b11ed981cba4b6d58c27fcbcceee9188088741f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12410540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da3b0adcc44b5ef28937bb70b38518ad42128c1900e8d248eef97c73d8e0b51`

```dockerfile
```

-	Layers:
	-	`sha256:4c80784befa697df3020c4cf1813873ba9e9082be463d03856542f822fdd4cf5`  
		Last Modified: Tue, 18 Mar 2025 03:31:19 GMT  
		Size: 12.4 MB (12392399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cafc585e91d532f659911c0305a15d74ea02d535df4d3bec2249af7ca717fdc`  
		Last Modified: Tue, 18 Mar 2025 03:31:18 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
