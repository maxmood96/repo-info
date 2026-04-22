## `r-base:latest`

```console
$ docker pull r-base@sha256:71bfeae94ede8d2d3a8fef56a3170e6f83d7c82adb353b194871c766f2eab932
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
$ docker pull r-base@sha256:f2b2c6b849c1b725b690b09c3ddeb1f1ceead00c5c968545af14f4ecbd98a861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381914870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72523386981be59b6ba561dcb6a690ef6981944b7d5206739720a09ee5c183f`
-	Default Command: `["R"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:33:19 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 22 Apr 2026 01:33:19 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 22 Apr 2026 01:33:26 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:33:27 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 22 Apr 2026 01:33:27 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 01:33:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Apr 2026 01:33:27 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 22 Apr 2026 01:33:27 GMT
ENV R_BASE_VERSION=4.5.3
# Wed, 22 Apr 2026 01:34:11 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:11 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:abac6300560e52d30e8863740fd61dd35f371fafec8988cf290ccbea4887753e`  
		Last Modified: Wed, 22 Apr 2026 00:16:46 GMT  
		Size: 48.7 MB (48697649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fb346d2b3d7dc513346f49ebd0818faba07f14d3fb19430d99af2241d0d47d`  
		Last Modified: Wed, 22 Apr 2026 01:34:50 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02458232b605b81125f359f4676dee41381ea2e0ac9dd3bb1582373a67535c1b`  
		Last Modified: Wed, 22 Apr 2026 01:34:51 GMT  
		Size: 27.1 MB (27111655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d683b3f801e49b08eca4fd1189bc6b8c47017c370d0415150d49914788a009f`  
		Last Modified: Wed, 22 Apr 2026 01:34:50 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12694d1e53ab25dd3c0a3bc54a3d823e65440e2c323f78562ce36e1e32e57d4`  
		Last Modified: Wed, 22 Apr 2026 01:34:50 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3515c09a6a712b8cca62c8b165ebab19372633bcde69201a01f497ba07996df5`  
		Last Modified: Wed, 22 Apr 2026 01:34:58 GMT  
		Size: 305.2 MB (305233347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:5305e47a6bc4318dc84c1bf96608458dfb71b9253a857e546de144b60029f4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13041629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670c0fb158d4e5086bd8fb4c92ecab9ed3305a2df60df6990450c27a5c030581`

```dockerfile
```

-	Layers:
	-	`sha256:1492255ad3bbd0533bc49ba4c22ee3ffb9c04174765e444010d60efa1d92f2f0`  
		Last Modified: Wed, 22 Apr 2026 01:34:51 GMT  
		Size: 13.0 MB (13022468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ad7234c2ed5884ec41220474a376f193b1bb136d38c40c1da9c55af50d669c`  
		Last Modified: Wed, 22 Apr 2026 01:34:50 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:de0262a8cfd26f79605a7a8f9a35a4a684e29aad1eedb32e306c76f1322c192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365258620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad713c0b7679114b63788adc38dec7b183b60d394bdac26b4058df42615d9f76`
-	Default Command: `["R"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:36:06 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 22 Apr 2026 01:36:06 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 22 Apr 2026 01:36:14 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:36:15 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 22 Apr 2026 01:36:15 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 01:36:15 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Apr 2026 01:36:16 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 22 Apr 2026 01:36:16 GMT
ENV R_BASE_VERSION=4.5.3
# Wed, 22 Apr 2026 01:37:00 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:37:00 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bf17e2bd9d2bffe1d04cffd7317dcbb7a2a4c186c9dfb9d304256a390be3e654`  
		Last Modified: Wed, 22 Apr 2026 00:16:36 GMT  
		Size: 48.7 MB (48726110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af78eed9ee669be8379364cae59bb860eb631551c4ea19471dc1b1ab4dfd50b`  
		Last Modified: Wed, 22 Apr 2026 01:37:38 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b084fdb42e75e6a3a52489f41bea5d65a303415124f34d771e0cb5ae56462edc`  
		Last Modified: Wed, 22 Apr 2026 01:37:39 GMT  
		Size: 27.0 MB (26958744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b896c22962cca3ae262830de6c0ee83821b1f1c12d3abf86c7fedb6a68f8f88b`  
		Last Modified: Wed, 22 Apr 2026 01:37:38 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d861698fe5f6fd1bdc54d3c58220bc3a8cb26bfe8138b195b202b9639780e5`  
		Last Modified: Wed, 22 Apr 2026 01:37:38 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bb82e72ad6ccfde5e78661de47f00b25867c33aba899b728c0e3a320eb9cd3`  
		Last Modified: Wed, 22 Apr 2026 01:37:45 GMT  
		Size: 288.7 MB (288701549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:0d5ca8f811e2754988006c99f9388b1f02e36cdf1c2a9eab5f177f0dec9b6111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13144015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aa58bd9adc19a5480a6b31d6766b61fcdcd23110b4998461df7c8cb45c8043`

```dockerfile
```

-	Layers:
	-	`sha256:d97cff7acae59e2d4e0fa7565de15661aa848c2d2abcb1d6f3e407aeb192b3bc`  
		Last Modified: Wed, 22 Apr 2026 01:37:39 GMT  
		Size: 13.1 MB (13124714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa966d7db90f76f23f3ee4c528d75eed5442620cd4b54708d6a3a87e1548a7f8`  
		Last Modified: Wed, 22 Apr 2026 01:37:38 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:aee895497ad35581a322e2400fabc86029af7f96042e850cfaa6f2da711d38b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363942457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56571e3c80320b8f8e91c8fd3f26c1a732d7d0422fbab4ffaeef8b13aa5aa788`
-	Default Command: `["R"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 04:08:41 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 07 Apr 2026 04:08:41 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 07 Apr 2026 04:09:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:09:09 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 07 Apr 2026 04:09:09 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 04:09:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 04:09:09 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 07 Apr 2026 04:09:09 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 07 Apr 2026 04:11:49 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:11:49 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d2fff16aab3eb8d89b3bdbae0814c0146f162ecacdf526ba2f4a1dfd7b082ae6`  
		Last Modified: Tue, 07 Apr 2026 00:12:16 GMT  
		Size: 53.9 MB (53851239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d244606985c8fba1ab58a562bf3b577b999e2fbb4661310361d28c409a577ab`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f79bf7373af22c1f1d4b77a5e9becb01bc664a3ebf74af1cdb4795e1db927b`  
		Last Modified: Tue, 07 Apr 2026 04:13:04 GMT  
		Size: 27.4 MB (27416201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebddcba1cadd3bf56f1f2fee24ee7524f0504234985824803b5cb26474698b65`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8a2a77cde68fcbea97bb8f109506629e7af424cc643780e7ae507a8658840a`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2544b72dd9dc8236201dfdeece6f90a786590df70ef05effb90c542e6e4daf0d`  
		Last Modified: Tue, 07 Apr 2026 04:13:11 GMT  
		Size: 281.8 MB (281802797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:d74dba730e372cb2e0a56538901a42ba231b99b74ef7e395d115b7dba423d1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13029399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd63f08bead5e9c9a360559d1f19ec5a8ed926385cc6138daac35a40be9b61b5`

```dockerfile
```

-	Layers:
	-	`sha256:8ed8aa891a6804cafb2ae079b93007dfc65eb08bc615d2bac74a9060d7840953`  
		Last Modified: Tue, 07 Apr 2026 04:13:04 GMT  
		Size: 13.0 MB (13010198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5c2934c18501ce1ef132738f28204db1a5911837fcf013a27a891524643476`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 19.2 KB (19201 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:09365544e2bdc9dd868804d20319793dff9998bd3963b1a4ce7f46e6b26e1bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349822009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5e97f3e45c6b51e7d93e06a10abe9a4610adce813622ebc943c5f94d7c1e68`
-	Default Command: `["R"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 02:25:22 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 22 Apr 2026 02:25:22 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 22 Apr 2026 02:25:32 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:25:33 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 22 Apr 2026 02:25:33 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 02:25:33 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Apr 2026 02:25:33 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 22 Apr 2026 02:25:33 GMT
ENV R_BASE_VERSION=4.5.3
# Wed, 22 Apr 2026 02:26:37 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:26:37 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:7d15de2b1a4fc4a6aaea8920bf366a7c0eeaaf95efaa5bf45810c4f134cefa77`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.4 MB (48407605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d79f56165217f07e7b2906ac4ecfeaa3f1f2e3891d43de3254fff465a7c73`  
		Last Modified: Wed, 22 Apr 2026 02:27:29 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5807e15ef5343d25e72c672ef7c38874cc860263a6d13ba2b8f966ece7c6975`  
		Last Modified: Wed, 22 Apr 2026 02:27:30 GMT  
		Size: 27.1 MB (27062364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9ef5da4863b04839649bca7fc0dc229d0ce89d8027a68c72b737b2b061e0fb`  
		Last Modified: Wed, 22 Apr 2026 02:27:29 GMT  
		Size: 924.5 KB (924543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35734131a0eecb60a5b715fd91797159d3ec922c58334e53cb60e338741d4cc`  
		Last Modified: Wed, 22 Apr 2026 02:27:29 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a47bd112084e2d7167cf071c5203fb29625ebcdc8327de9f1dab54831a21dc`  
		Last Modified: Wed, 22 Apr 2026 02:27:35 GMT  
		Size: 273.4 MB (273423770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:d8f66cc77f30f3fcc191e9b9c553db266e4f92f06c34024c592938648cabc178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12842553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5233c4937f64c5811efc5d1bca14d303c87fd74f774c366ccd8e4755ee4b956`

```dockerfile
```

-	Layers:
	-	`sha256:50541aaccb19a4a3ad17df57ec4f66198ddedc5ab76a2705aead3e92b60789fa`  
		Last Modified: Wed, 22 Apr 2026 02:27:29 GMT  
		Size: 12.8 MB (12823392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d0376ccdf0045753fccd194155751ebd0d125b75f80d53d9e192c246bbdc98`  
		Last Modified: Wed, 22 Apr 2026 02:27:30 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.in-toto+json
