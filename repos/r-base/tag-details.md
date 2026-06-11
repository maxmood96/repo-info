<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.6.0`](#r-base460)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.6.0`

```console
$ docker pull r-base@sha256:56a973276c744069e532927807b1f83648c21f818b4be8550306477b2d556a9a
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

### `r-base:4.6.0` - linux; amd64

```console
$ docker pull r-base@sha256:a94dc2b5a5db9e6aa415f6ea4f8b39255c3eaa6db14b34d4567df986216bd586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371406943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6845d53159ab7f45d9fcb70073269a818b38f4144f99a30c4472673e46a267c7`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 00:35:39 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 11 Jun 2026 00:35:39 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Thu, 11 Jun 2026 00:35:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:46 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Thu, 11 Jun 2026 00:35:46 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 11 Jun 2026 00:35:46 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jun 2026 00:35:46 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://deb.debian.org/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Thu, 11 Jun 2026 00:35:46 GMT
ENV R_BASE_VERSION=4.6.0
# Thu, 11 Jun 2026 00:36:27 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:36:27 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9fcbe81726325315e419e96d2d3462a068d809512f102a51a6a2a820988cae49`  
		Last Modified: Wed, 10 Jun 2026 23:40:23 GMT  
		Size: 48.8 MB (48779277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd361b707110a5d39706fa260bbce0c7402c266c2ca0b7cdcb3dadd10c8d08a`  
		Last Modified: Thu, 11 Jun 2026 00:37:03 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d761d9736809cd592cf2bc768f25320f348bb49b32bf40d7aa43be27e5b6ebeb`  
		Last Modified: Thu, 11 Jun 2026 00:37:04 GMT  
		Size: 27.1 MB (27098195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f105444db1ca2bc83e33214ea2099fa64103ee695f6d8ebf7174cba31d9c0c`  
		Last Modified: Thu, 11 Jun 2026 00:37:03 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413b63891d2202311f7d8287b826327078032bddf795992aa296e10b6c5fd736`  
		Last Modified: Thu, 11 Jun 2026 00:37:03 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b03687e6b80ceb8bd4a501952bac289ff13aebab8fa239f3df7f27da95c8fde`  
		Last Modified: Thu, 11 Jun 2026 00:37:12 GMT  
		Size: 294.7 MB (294657249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.6.0` - unknown; unknown

```console
$ docker pull r-base@sha256:31a19ec1f4983179c17cacc68106c8314e3e52000852f3de1c13aeb19daef2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13015417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529ba39e0522f2d10fbfe5219bf7b0a485eb564194aa697f4484e8f0f1eeb762`

```dockerfile
```

-	Layers:
	-	`sha256:ac08093058e2d9ac278a9fe8af38a7a567c65ff58f50eb8ac362c2131f9210c7`  
		Last Modified: Thu, 11 Jun 2026 00:37:04 GMT  
		Size: 13.0 MB (12996257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70f69a26ed4a7046c252473f67d64bcfb9c153e60f325c508eee2f6d8235502`  
		Last Modified: Thu, 11 Jun 2026 00:37:03 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.6.0` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:92e3c2b8533b644fb205b93dfe1e35c26ce2192bd64a58fdf1c0e425a3e34435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.0 MB (354950773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22677c6e0238db0d360bd754d31abc6259aaf0c792fecf1e2e5c22da33962ef5`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 00:37:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 11 Jun 2026 00:37:11 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Thu, 11 Jun 2026 00:37:20 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:37:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Thu, 11 Jun 2026 00:37:21 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 11 Jun 2026 00:37:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jun 2026 00:37:21 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://deb.debian.org/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Thu, 11 Jun 2026 00:37:21 GMT
ENV R_BASE_VERSION=4.6.0
# Thu, 11 Jun 2026 00:38:03 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:38:03 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0ac2de9040ad910c5f209871a68d1fc648dea0542b3e6b1dad4c36549fff6879`  
		Last Modified: Wed, 10 Jun 2026 23:40:15 GMT  
		Size: 48.8 MB (48795609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059ceaf202c8e61c77714bd03ed9b98dbccaf41188c49c6cce11bd4686cf0ece`  
		Last Modified: Thu, 11 Jun 2026 00:38:39 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc7486387a92c79f8412bfb3a261f52ff745912eb0587de48015528c69e874f`  
		Last Modified: Thu, 11 Jun 2026 00:38:41 GMT  
		Size: 26.9 MB (26949542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594c92c31faede6d67047578d13b4f331158c46b9eacf9756cb1a64305d82e64`  
		Last Modified: Thu, 11 Jun 2026 00:38:40 GMT  
		Size: 868.5 KB (868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16b5e343efd2b0c340a88b0f4522f4ff6c49242bd7d45e56a6a5097525c2cb`  
		Last Modified: Thu, 11 Jun 2026 00:38:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365f6fcd8d4204ee0aa1b88ed66cd0507fdf767e3e02fbf1a912a8484fd95edf`  
		Last Modified: Thu, 11 Jun 2026 00:38:47 GMT  
		Size: 278.3 MB (278333411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.6.0` - unknown; unknown

```console
$ docker pull r-base@sha256:ae6a1b593c1904cc1a60d247b576d7c8efbbceaf14560d75b71d5cdaf4438053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb7f5e5f361c804064a4d496c74edaa55bb0275badd89c00746c91e86734ee`

```dockerfile
```

-	Layers:
	-	`sha256:077bb1c1d943200f856c33690a2f06b9e06bfd35a5c6760a3b80cb779ab4c9dd`  
		Last Modified: Thu, 11 Jun 2026 00:38:40 GMT  
		Size: 13.1 MB (13121457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0be3712af1764cab106bcd1db2c27db7fa848a2670e51fbbd10bdbbcd3e139`  
		Last Modified: Thu, 11 Jun 2026 00:38:39 GMT  
		Size: 19.3 KB (19300 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.6.0` - linux; ppc64le

```console
$ docker pull r-base@sha256:0586766e68044dd4e5c9e68ca71eba9a377ceb6d32baff04fcefe5b2f3473bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.3 MB (366270772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316fd923c68de895b4f47962717d3843d9dca44cb5176875f9c1c2416bd0c61e`
-	Default Command: `["R"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1779062400'
# Wed, 20 May 2026 01:02:56 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 20 May 2026 01:02:56 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 20 May 2026 01:03:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:03:18 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 20 May 2026 01:03:18 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 20 May 2026 01:03:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 20 May 2026 01:03:19 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://deb.debian.org/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 20 May 2026 01:03:19 GMT
ENV R_BASE_VERSION=4.6.0
# Wed, 20 May 2026 01:05:14 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:05:14 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a896bf8623032a9b4075e6319b6f84fd18fb93674032660f124004714d68a5b6`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 54.0 MB (54021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba977f5eaab329d9a7591ecb7586fa2daed69b07997a03c6e24c9fa38235882`  
		Last Modified: Wed, 20 May 2026 01:06:31 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df805e40bcf0f6efdc6eb3ffa493d96400e331d6ace06aeb38f658e966df8308`  
		Last Modified: Wed, 20 May 2026 01:06:33 GMT  
		Size: 27.5 MB (27474540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6485a413d11cbafc61ea650f0825f36abc30cd62f51c502b2ddade425e52e5a`  
		Last Modified: Wed, 20 May 2026 01:06:31 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6249c35f973cd8190c018269911f7a32c11b8902c403ae15f374d439553002d4`  
		Last Modified: Wed, 20 May 2026 01:06:31 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d30c32906f0d3c3bd12ca7269ae9952ea38e7eb72f2a7718d6f1fd29d1304f`  
		Last Modified: Wed, 20 May 2026 01:06:43 GMT  
		Size: 283.9 MB (283902729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.6.0` - unknown; unknown

```console
$ docker pull r-base@sha256:2c65b659054253fad84e897befebd3f0b485a1f2083c65cbde7f8d9a56f745cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13045532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743296bd766271c83229f65b82264b93a606eacb661fc1ecf9c73162d1a3524b`

```dockerfile
```

-	Layers:
	-	`sha256:2f2f45140608f50fd27a154c1dccac529180ccde73e63080321596db748b478a`  
		Last Modified: Wed, 20 May 2026 01:06:32 GMT  
		Size: 13.0 MB (13026332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528993b4377ba2e504c279e07713a0f07d9ab8bfcd4a900300c36b481352987e`  
		Last Modified: Wed, 20 May 2026 01:06:31 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.6.0` - linux; s390x

```console
$ docker pull r-base@sha256:76467b0d2fae189a364381d8bcbb9663683cfa4e8e3a9ab8b70eec0d51b814bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340267660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a196def21c411379c7fdd8e8578aa7574281d453e3286917eddd1b3deac514da`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 01:39:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 11 Jun 2026 01:39:24 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Thu, 11 Jun 2026 01:39:35 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:39:36 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Thu, 11 Jun 2026 01:39:36 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 11 Jun 2026 01:39:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jun 2026 01:39:36 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://deb.debian.org/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Thu, 11 Jun 2026 01:39:36 GMT
ENV R_BASE_VERSION=4.6.0
# Thu, 11 Jun 2026 01:40:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:40:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d7126aef2aebb51829b0047dfcdb7ebc424e9fa253eef97b8d7aaa7471f6f16c`  
		Last Modified: Wed, 10 Jun 2026 23:42:13 GMT  
		Size: 48.5 MB (48513111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c985a3b70bcf5f9cd5a68ca6d6f0a70aa068a90face21dbb3ea0d3f9cffecb`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62c5ae5fe1701644c273f3051e8c2d9bf3e37dde1703bd770015f6e2d892d92`  
		Last Modified: Thu, 11 Jun 2026 01:41:29 GMT  
		Size: 27.0 MB (27046788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc1a4a04824267ffcacd2d542fda3ae31a6489762fbcfb101b234913487f278`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 924.5 KB (924544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c3db3c8fe73edb639445224079a480e6d11e4a6473856686b48b1a6793a56f`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916908bc4730aec7b9bcd20da85037aaddcd2535d1179015c3129a78e31fab02`  
		Last Modified: Thu, 11 Jun 2026 01:41:34 GMT  
		Size: 263.8 MB (263779491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.6.0` - unknown; unknown

```console
$ docker pull r-base@sha256:b989420b653bfdfa87f48a2067c0522c8502a4b4a25e63aa8b79d174bd0a2208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12841203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2996ac2945ff5cd19661579f946b31f48bf933f426ee6b005ee3825ac54e9e`

```dockerfile
```

-	Layers:
	-	`sha256:3e2a4ac4b2125047f1eca78f6c53d3d19b4576e3f6a150d44f9816fcd9f818f8`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 12.8 MB (12822043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8167897362f8e6d8c0a1697dffec4e6184f7814c51e02bf8a5943d79654af432`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:56a973276c744069e532927807b1f83648c21f818b4be8550306477b2d556a9a
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
$ docker pull r-base@sha256:a94dc2b5a5db9e6aa415f6ea4f8b39255c3eaa6db14b34d4567df986216bd586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371406943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6845d53159ab7f45d9fcb70073269a818b38f4144f99a30c4472673e46a267c7`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 00:35:39 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 11 Jun 2026 00:35:39 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Thu, 11 Jun 2026 00:35:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:46 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Thu, 11 Jun 2026 00:35:46 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 11 Jun 2026 00:35:46 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jun 2026 00:35:46 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://deb.debian.org/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Thu, 11 Jun 2026 00:35:46 GMT
ENV R_BASE_VERSION=4.6.0
# Thu, 11 Jun 2026 00:36:27 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:36:27 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9fcbe81726325315e419e96d2d3462a068d809512f102a51a6a2a820988cae49`  
		Last Modified: Wed, 10 Jun 2026 23:40:23 GMT  
		Size: 48.8 MB (48779277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd361b707110a5d39706fa260bbce0c7402c266c2ca0b7cdcb3dadd10c8d08a`  
		Last Modified: Thu, 11 Jun 2026 00:37:03 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d761d9736809cd592cf2bc768f25320f348bb49b32bf40d7aa43be27e5b6ebeb`  
		Last Modified: Thu, 11 Jun 2026 00:37:04 GMT  
		Size: 27.1 MB (27098195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f105444db1ca2bc83e33214ea2099fa64103ee695f6d8ebf7174cba31d9c0c`  
		Last Modified: Thu, 11 Jun 2026 00:37:03 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413b63891d2202311f7d8287b826327078032bddf795992aa296e10b6c5fd736`  
		Last Modified: Thu, 11 Jun 2026 00:37:03 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b03687e6b80ceb8bd4a501952bac289ff13aebab8fa239f3df7f27da95c8fde`  
		Last Modified: Thu, 11 Jun 2026 00:37:12 GMT  
		Size: 294.7 MB (294657249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:31a19ec1f4983179c17cacc68106c8314e3e52000852f3de1c13aeb19daef2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13015417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529ba39e0522f2d10fbfe5219bf7b0a485eb564194aa697f4484e8f0f1eeb762`

```dockerfile
```

-	Layers:
	-	`sha256:ac08093058e2d9ac278a9fe8af38a7a567c65ff58f50eb8ac362c2131f9210c7`  
		Last Modified: Thu, 11 Jun 2026 00:37:04 GMT  
		Size: 13.0 MB (12996257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70f69a26ed4a7046c252473f67d64bcfb9c153e60f325c508eee2f6d8235502`  
		Last Modified: Thu, 11 Jun 2026 00:37:03 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:92e3c2b8533b644fb205b93dfe1e35c26ce2192bd64a58fdf1c0e425a3e34435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.0 MB (354950773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22677c6e0238db0d360bd754d31abc6259aaf0c792fecf1e2e5c22da33962ef5`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 00:37:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 11 Jun 2026 00:37:11 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Thu, 11 Jun 2026 00:37:20 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:37:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Thu, 11 Jun 2026 00:37:21 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 11 Jun 2026 00:37:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jun 2026 00:37:21 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://deb.debian.org/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Thu, 11 Jun 2026 00:37:21 GMT
ENV R_BASE_VERSION=4.6.0
# Thu, 11 Jun 2026 00:38:03 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:38:03 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0ac2de9040ad910c5f209871a68d1fc648dea0542b3e6b1dad4c36549fff6879`  
		Last Modified: Wed, 10 Jun 2026 23:40:15 GMT  
		Size: 48.8 MB (48795609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059ceaf202c8e61c77714bd03ed9b98dbccaf41188c49c6cce11bd4686cf0ece`  
		Last Modified: Thu, 11 Jun 2026 00:38:39 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc7486387a92c79f8412bfb3a261f52ff745912eb0587de48015528c69e874f`  
		Last Modified: Thu, 11 Jun 2026 00:38:41 GMT  
		Size: 26.9 MB (26949542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594c92c31faede6d67047578d13b4f331158c46b9eacf9756cb1a64305d82e64`  
		Last Modified: Thu, 11 Jun 2026 00:38:40 GMT  
		Size: 868.5 KB (868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16b5e343efd2b0c340a88b0f4522f4ff6c49242bd7d45e56a6a5097525c2cb`  
		Last Modified: Thu, 11 Jun 2026 00:38:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365f6fcd8d4204ee0aa1b88ed66cd0507fdf767e3e02fbf1a912a8484fd95edf`  
		Last Modified: Thu, 11 Jun 2026 00:38:47 GMT  
		Size: 278.3 MB (278333411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:ae6a1b593c1904cc1a60d247b576d7c8efbbceaf14560d75b71d5cdaf4438053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb7f5e5f361c804064a4d496c74edaa55bb0275badd89c00746c91e86734ee`

```dockerfile
```

-	Layers:
	-	`sha256:077bb1c1d943200f856c33690a2f06b9e06bfd35a5c6760a3b80cb779ab4c9dd`  
		Last Modified: Thu, 11 Jun 2026 00:38:40 GMT  
		Size: 13.1 MB (13121457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0be3712af1764cab106bcd1db2c27db7fa848a2670e51fbbd10bdbbcd3e139`  
		Last Modified: Thu, 11 Jun 2026 00:38:39 GMT  
		Size: 19.3 KB (19300 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:0586766e68044dd4e5c9e68ca71eba9a377ceb6d32baff04fcefe5b2f3473bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.3 MB (366270772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316fd923c68de895b4f47962717d3843d9dca44cb5176875f9c1c2416bd0c61e`
-	Default Command: `["R"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1779062400'
# Wed, 20 May 2026 01:02:56 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 20 May 2026 01:02:56 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 20 May 2026 01:03:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:03:18 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 20 May 2026 01:03:18 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 20 May 2026 01:03:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 20 May 2026 01:03:19 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://deb.debian.org/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 20 May 2026 01:03:19 GMT
ENV R_BASE_VERSION=4.6.0
# Wed, 20 May 2026 01:05:14 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:05:14 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a896bf8623032a9b4075e6319b6f84fd18fb93674032660f124004714d68a5b6`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 54.0 MB (54021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba977f5eaab329d9a7591ecb7586fa2daed69b07997a03c6e24c9fa38235882`  
		Last Modified: Wed, 20 May 2026 01:06:31 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df805e40bcf0f6efdc6eb3ffa493d96400e331d6ace06aeb38f658e966df8308`  
		Last Modified: Wed, 20 May 2026 01:06:33 GMT  
		Size: 27.5 MB (27474540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6485a413d11cbafc61ea650f0825f36abc30cd62f51c502b2ddade425e52e5a`  
		Last Modified: Wed, 20 May 2026 01:06:31 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6249c35f973cd8190c018269911f7a32c11b8902c403ae15f374d439553002d4`  
		Last Modified: Wed, 20 May 2026 01:06:31 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d30c32906f0d3c3bd12ca7269ae9952ea38e7eb72f2a7718d6f1fd29d1304f`  
		Last Modified: Wed, 20 May 2026 01:06:43 GMT  
		Size: 283.9 MB (283902729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:2c65b659054253fad84e897befebd3f0b485a1f2083c65cbde7f8d9a56f745cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13045532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743296bd766271c83229f65b82264b93a606eacb661fc1ecf9c73162d1a3524b`

```dockerfile
```

-	Layers:
	-	`sha256:2f2f45140608f50fd27a154c1dccac529180ccde73e63080321596db748b478a`  
		Last Modified: Wed, 20 May 2026 01:06:32 GMT  
		Size: 13.0 MB (13026332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528993b4377ba2e504c279e07713a0f07d9ab8bfcd4a900300c36b481352987e`  
		Last Modified: Wed, 20 May 2026 01:06:31 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:76467b0d2fae189a364381d8bcbb9663683cfa4e8e3a9ab8b70eec0d51b814bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340267660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a196def21c411379c7fdd8e8578aa7574281d453e3286917eddd1b3deac514da`
-	Default Command: `["R"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1781049600'
# Thu, 11 Jun 2026 01:39:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 11 Jun 2026 01:39:24 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Thu, 11 Jun 2026 01:39:35 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:39:36 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Thu, 11 Jun 2026 01:39:36 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 11 Jun 2026 01:39:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jun 2026 01:39:36 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://deb.debian.org/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Thu, 11 Jun 2026 01:39:36 GMT
ENV R_BASE_VERSION=4.6.0
# Thu, 11 Jun 2026 01:40:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:40:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d7126aef2aebb51829b0047dfcdb7ebc424e9fa253eef97b8d7aaa7471f6f16c`  
		Last Modified: Wed, 10 Jun 2026 23:42:13 GMT  
		Size: 48.5 MB (48513111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c985a3b70bcf5f9cd5a68ca6d6f0a70aa068a90face21dbb3ea0d3f9cffecb`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62c5ae5fe1701644c273f3051e8c2d9bf3e37dde1703bd770015f6e2d892d92`  
		Last Modified: Thu, 11 Jun 2026 01:41:29 GMT  
		Size: 27.0 MB (27046788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc1a4a04824267ffcacd2d542fda3ae31a6489762fbcfb101b234913487f278`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 924.5 KB (924544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c3db3c8fe73edb639445224079a480e6d11e4a6473856686b48b1a6793a56f`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916908bc4730aec7b9bcd20da85037aaddcd2535d1179015c3129a78e31fab02`  
		Last Modified: Thu, 11 Jun 2026 01:41:34 GMT  
		Size: 263.8 MB (263779491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:b989420b653bfdfa87f48a2067c0522c8502a4b4a25e63aa8b79d174bd0a2208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12841203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2996ac2945ff5cd19661579f946b31f48bf933f426ee6b005ee3825ac54e9e`

```dockerfile
```

-	Layers:
	-	`sha256:3e2a4ac4b2125047f1eca78f6c53d3d19b4576e3f6a150d44f9816fcd9f818f8`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 12.8 MB (12822043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8167897362f8e6d8c0a1697dffec4e6184f7814c51e02bf8a5943d79654af432`  
		Last Modified: Thu, 11 Jun 2026 01:41:28 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.in-toto+json
