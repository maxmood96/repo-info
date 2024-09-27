<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.1`](#r-base441)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.1`

```console
$ docker pull r-base@sha256:70bab059e37f59e7d1ac5ee770501794593314d1c190f24b684fdd10898c6232
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

### `r-base:4.4.1` - linux; amd64

```console
$ docker pull r-base@sha256:32307ec88f3d29d30b4185f195d1dd9cf25ad79e044329fdd4c0b3892afca49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.5 MB (368487491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182b915af64703cd5ae7dc81ac03cbe6727051d05a5cfee40d67f10906b3acf6`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:d124f58a75824fb48cc5bc8f7954157ace87dcf80be8ba17fd0bb3fac8f6d19a in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:082d57a12cea884a5f3c544769a8e5aa73570907b945a48991f31218efa6a3af`  
		Last Modified: Fri, 27 Sep 2024 04:35:32 GMT  
		Size: 53.2 MB (53178053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb180473087c6a17021ec0249e4bb3563ec98a11ae9667364a10d77c4e94ecdd`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54969262ece898682002be7d2eb1a279de293ddf48831f617ae7ca76a2b4d52`  
		Last Modified: Fri, 27 Sep 2024 06:04:26 GMT  
		Size: 23.1 MB (23136215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f03b5d0e428edf5aa2202b6581f4fb79cb47f1e1748c6f5a9a8514fe729e25`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 866.7 KB (866742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8526c62f29b5eb6cb994891f718510e3de28de4ce253fc06dd05ef9e2c0a267c`  
		Last Modified: Fri, 27 Sep 2024 06:04:26 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f4edb453d58c253f0c0c82ab607f502d92236088ef45120d73470864abcb7c`  
		Last Modified: Fri, 27 Sep 2024 06:04:30 GMT  
		Size: 291.3 MB (291302827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.1` - unknown; unknown

```console
$ docker pull r-base@sha256:f8f0ffaa8214ec779d8a325eeec0014fd1a0c316d68f222d148089b69a26f283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12431539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087de72f4471f51bad51bae2083833ba810eda20f9d64757e786232809610a9e`

```dockerfile
```

-	Layers:
	-	`sha256:7aae09a3ef380eaa190424b91e687cc2f22ba70d71100eccd4d0a1392c06f011`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 12.4 MB (12413611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339073a790c65d995a712728a2c46b660bcc24c6cccefe0709e9f08786526d44`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.1` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:0e97b4a6f6bb9960d8eb42177b7ae95259cac3c064a7f1bb03243c1463f701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340093357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d60923d7881cc077e0d84ea93eb89e6791509367c60ec06ecb0c0dda4c283c0`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:394779f4486ebaf8490ab95548a898d31798f528981c6abde9a64ae9541ad916 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1d833a2b98580c8c6fbc93eec4d1f948a740704ada36d9bfe4881cc92113a70f`  
		Last Modified: Wed, 04 Sep 2024 21:44:46 GMT  
		Size: 53.6 MB (53594358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04779dca231fa8a1beca354a3edcd2abb13fbcce1cf1c82e91e00b00fcc54a5`  
		Last Modified: Thu, 05 Sep 2024 19:17:19 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d67177ad9145469b6a009fa47242c3b8c0b3763e6c7de311864313891b0c7f`  
		Last Modified: Thu, 05 Sep 2024 19:17:20 GMT  
		Size: 23.1 MB (23125537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8c4381a2c48680c73629366ba287de8729f95cd922761a5ff44fac52a62748`  
		Last Modified: Thu, 05 Sep 2024 19:17:19 GMT  
		Size: 866.7 KB (866742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfecfa476833a0c79899a1e60ad384d9da2ac39cf84ea8680dcc6a4a05d89ba`  
		Last Modified: Thu, 05 Sep 2024 19:17:20 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5066773a4b36fd82ba103416ed00dab0365476609145be5c8b3d6adc01273ed`  
		Last Modified: Thu, 05 Sep 2024 19:17:26 GMT  
		Size: 262.5 MB (262503060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.1` - unknown; unknown

```console
$ docker pull r-base@sha256:fd564ed74212666a7f667c5ce6f0465390f8115166dd5d4c6c033ff9c203c649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12515083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354e21cb72ec4148b40ec8d4ccdb8a548978f2d2bffbdf46ca105c03608cac45`

```dockerfile
```

-	Layers:
	-	`sha256:20b0695573da518b3a4937a64cd570a9a700d34f466017bb3b34ab626f6bb7bb`  
		Last Modified: Thu, 05 Sep 2024 19:17:19 GMT  
		Size: 12.5 MB (12496875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd37149c0810c5501b2f1126a299fa22691a9fde24bbe8e4ebe93584b8addba4`  
		Last Modified: Thu, 05 Sep 2024 19:17:19 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.1` - linux; ppc64le

```console
$ docker pull r-base@sha256:daae24d5d397ea371924e0e30d2a9e03fe28b47e23323b5cdb8c3edd9847319d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349347468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68017f4c62ce974eb135b4c646cb21bd0d623bbebc32140bc27259a9b26fab5c`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:e76ca2322a73a59209e43148c51a8c79f7c3e572eff94a2519628b16edb02b11 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3b2659f6b1aa74a9122222e29d09e5d1b06a1b6eadfed4e19fd744c16754d022`  
		Last Modified: Wed, 04 Sep 2024 22:32:58 GMT  
		Size: 57.1 MB (57077769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a8dc601b282bcde7e450b843eecd0cd9f604ee0fa97ed6c62cbe51267a84e8`  
		Last Modified: Thu, 05 Sep 2024 05:41:15 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e97d4e527da3286a677193b21649ae0ff212c4c8a3b0d321d1f62e70a9a3c1a`  
		Last Modified: Thu, 05 Sep 2024 05:41:16 GMT  
		Size: 23.4 MB (23358742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ea0f13859f55ec4c4c687603cc8f0e35280a962614e6dd01d0a64c8905d691`  
		Last Modified: Thu, 05 Sep 2024 05:41:15 GMT  
		Size: 866.7 KB (866746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec3708b97d79c442471f9fe4656fa4871fde00afeb9a5c18425ab25c4badfef`  
		Last Modified: Thu, 05 Sep 2024 05:41:16 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735e3c72d451c857446c7052cc33a173e6e27bcc8abe79641da24e84302e64bc`  
		Last Modified: Thu, 05 Sep 2024 05:41:33 GMT  
		Size: 268.0 MB (268040550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.1` - unknown; unknown

```console
$ docker pull r-base@sha256:e1817bff7152b301cccef838712b9cd3d8114eaa623e730d26d4c9964625a9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12414474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea42a3817e3810af4a020cdf1c60c18dfc4985e7e733aada0b84fc7ad00ea06c`

```dockerfile
```

-	Layers:
	-	`sha256:a4f056abdb4e8cdeafce107e03b32ef30e34362844258c3e761f3c67f5f19e1e`  
		Last Modified: Thu, 05 Sep 2024 05:41:16 GMT  
		Size: 12.4 MB (12396511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d7b1d445f7a4268b9620d241a5047ee4e523ec664275418b067abca958c8176`  
		Last Modified: Thu, 05 Sep 2024 05:41:15 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.1` - linux; s390x

```console
$ docker pull r-base@sha256:67ff8f2d7b26542a6830d2bcf23a435a18bdf1307587d193e79a4a670e726267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321602486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ef3df98703d101c690e2d53df9179f43dc223b1b8c3e2948eb8fd56624cedb`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:59e982fbd6b5364ff9e3c3a4656bf6cb6795d637a02c788e4db61959964e2b65 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ff4f98e3072ebdb612b0732715fb700fbfdf55f51351132742a0b343fd7fbfc8`  
		Last Modified: Wed, 04 Sep 2024 21:49:29 GMT  
		Size: 52.7 MB (52746481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e90a9355cf91cb09a280cbcf072956d96d4202fe9245935d3707e75093d8cbd`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8435ceb8d71e22ab12f773cd5e47f46729571d4740e7e663b502935e61dcb0e`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 23.2 MB (23247315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42211844e7ef040cb7b3ab22d83de1d919276069da6cf5e4ded9e92046b59e7c`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 923.5 KB (923490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d3b5af296e22b8c3d91ddc3c318ef48fabf4eeaaab40c624373833ef8a7af6`  
		Last Modified: Thu, 05 Sep 2024 06:40:23 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3074d9857a3d16036dc8a09935da0352f6189d5c9f8baa81155afdeb4708af`  
		Last Modified: Thu, 05 Sep 2024 06:40:29 GMT  
		Size: 244.7 MB (244681541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.1` - unknown; unknown

```console
$ docker pull r-base@sha256:1687d016b22dd19921e2470802c6150e4de567be390c83c7e4fb9195435d340e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12221705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe1ae2cb892bce6023634745db5fdf3c209a1c56b30cdf9956d678a9be1ec74`

```dockerfile
```

-	Layers:
	-	`sha256:453b03948f69315d58e377d98e3e074db0a908675aec36e2aa7959e875a1f657`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 12.2 MB (12203777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a366c370004305d8f75dcd2320aec5947363dc80f34c8e45059bd227fff32276`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:70bab059e37f59e7d1ac5ee770501794593314d1c190f24b684fdd10898c6232
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
$ docker pull r-base@sha256:32307ec88f3d29d30b4185f195d1dd9cf25ad79e044329fdd4c0b3892afca49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.5 MB (368487491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182b915af64703cd5ae7dc81ac03cbe6727051d05a5cfee40d67f10906b3acf6`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:d124f58a75824fb48cc5bc8f7954157ace87dcf80be8ba17fd0bb3fac8f6d19a in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:082d57a12cea884a5f3c544769a8e5aa73570907b945a48991f31218efa6a3af`  
		Last Modified: Fri, 27 Sep 2024 04:35:32 GMT  
		Size: 53.2 MB (53178053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb180473087c6a17021ec0249e4bb3563ec98a11ae9667364a10d77c4e94ecdd`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54969262ece898682002be7d2eb1a279de293ddf48831f617ae7ca76a2b4d52`  
		Last Modified: Fri, 27 Sep 2024 06:04:26 GMT  
		Size: 23.1 MB (23136215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f03b5d0e428edf5aa2202b6581f4fb79cb47f1e1748c6f5a9a8514fe729e25`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 866.7 KB (866742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8526c62f29b5eb6cb994891f718510e3de28de4ce253fc06dd05ef9e2c0a267c`  
		Last Modified: Fri, 27 Sep 2024 06:04:26 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f4edb453d58c253f0c0c82ab607f502d92236088ef45120d73470864abcb7c`  
		Last Modified: Fri, 27 Sep 2024 06:04:30 GMT  
		Size: 291.3 MB (291302827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f8f0ffaa8214ec779d8a325eeec0014fd1a0c316d68f222d148089b69a26f283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12431539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087de72f4471f51bad51bae2083833ba810eda20f9d64757e786232809610a9e`

```dockerfile
```

-	Layers:
	-	`sha256:7aae09a3ef380eaa190424b91e687cc2f22ba70d71100eccd4d0a1392c06f011`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 12.4 MB (12413611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339073a790c65d995a712728a2c46b660bcc24c6cccefe0709e9f08786526d44`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:0e97b4a6f6bb9960d8eb42177b7ae95259cac3c064a7f1bb03243c1463f701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340093357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d60923d7881cc077e0d84ea93eb89e6791509367c60ec06ecb0c0dda4c283c0`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:394779f4486ebaf8490ab95548a898d31798f528981c6abde9a64ae9541ad916 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1d833a2b98580c8c6fbc93eec4d1f948a740704ada36d9bfe4881cc92113a70f`  
		Last Modified: Wed, 04 Sep 2024 21:44:46 GMT  
		Size: 53.6 MB (53594358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04779dca231fa8a1beca354a3edcd2abb13fbcce1cf1c82e91e00b00fcc54a5`  
		Last Modified: Thu, 05 Sep 2024 19:17:19 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d67177ad9145469b6a009fa47242c3b8c0b3763e6c7de311864313891b0c7f`  
		Last Modified: Thu, 05 Sep 2024 19:17:20 GMT  
		Size: 23.1 MB (23125537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8c4381a2c48680c73629366ba287de8729f95cd922761a5ff44fac52a62748`  
		Last Modified: Thu, 05 Sep 2024 19:17:19 GMT  
		Size: 866.7 KB (866742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfecfa476833a0c79899a1e60ad384d9da2ac39cf84ea8680dcc6a4a05d89ba`  
		Last Modified: Thu, 05 Sep 2024 19:17:20 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5066773a4b36fd82ba103416ed00dab0365476609145be5c8b3d6adc01273ed`  
		Last Modified: Thu, 05 Sep 2024 19:17:26 GMT  
		Size: 262.5 MB (262503060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:fd564ed74212666a7f667c5ce6f0465390f8115166dd5d4c6c033ff9c203c649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12515083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354e21cb72ec4148b40ec8d4ccdb8a548978f2d2bffbdf46ca105c03608cac45`

```dockerfile
```

-	Layers:
	-	`sha256:20b0695573da518b3a4937a64cd570a9a700d34f466017bb3b34ab626f6bb7bb`  
		Last Modified: Thu, 05 Sep 2024 19:17:19 GMT  
		Size: 12.5 MB (12496875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd37149c0810c5501b2f1126a299fa22691a9fde24bbe8e4ebe93584b8addba4`  
		Last Modified: Thu, 05 Sep 2024 19:17:19 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:daae24d5d397ea371924e0e30d2a9e03fe28b47e23323b5cdb8c3edd9847319d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349347468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68017f4c62ce974eb135b4c646cb21bd0d623bbebc32140bc27259a9b26fab5c`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:e76ca2322a73a59209e43148c51a8c79f7c3e572eff94a2519628b16edb02b11 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3b2659f6b1aa74a9122222e29d09e5d1b06a1b6eadfed4e19fd744c16754d022`  
		Last Modified: Wed, 04 Sep 2024 22:32:58 GMT  
		Size: 57.1 MB (57077769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a8dc601b282bcde7e450b843eecd0cd9f604ee0fa97ed6c62cbe51267a84e8`  
		Last Modified: Thu, 05 Sep 2024 05:41:15 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e97d4e527da3286a677193b21649ae0ff212c4c8a3b0d321d1f62e70a9a3c1a`  
		Last Modified: Thu, 05 Sep 2024 05:41:16 GMT  
		Size: 23.4 MB (23358742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ea0f13859f55ec4c4c687603cc8f0e35280a962614e6dd01d0a64c8905d691`  
		Last Modified: Thu, 05 Sep 2024 05:41:15 GMT  
		Size: 866.7 KB (866746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec3708b97d79c442471f9fe4656fa4871fde00afeb9a5c18425ab25c4badfef`  
		Last Modified: Thu, 05 Sep 2024 05:41:16 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735e3c72d451c857446c7052cc33a173e6e27bcc8abe79641da24e84302e64bc`  
		Last Modified: Thu, 05 Sep 2024 05:41:33 GMT  
		Size: 268.0 MB (268040550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:e1817bff7152b301cccef838712b9cd3d8114eaa623e730d26d4c9964625a9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12414474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea42a3817e3810af4a020cdf1c60c18dfc4985e7e733aada0b84fc7ad00ea06c`

```dockerfile
```

-	Layers:
	-	`sha256:a4f056abdb4e8cdeafce107e03b32ef30e34362844258c3e761f3c67f5f19e1e`  
		Last Modified: Thu, 05 Sep 2024 05:41:16 GMT  
		Size: 12.4 MB (12396511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d7b1d445f7a4268b9620d241a5047ee4e523ec664275418b067abca958c8176`  
		Last Modified: Thu, 05 Sep 2024 05:41:15 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:67ff8f2d7b26542a6830d2bcf23a435a18bdf1307587d193e79a4a670e726267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321602486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ef3df98703d101c690e2d53df9179f43dc223b1b8c3e2948eb8fd56624cedb`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:59e982fbd6b5364ff9e3c3a4656bf6cb6795d637a02c788e4db61959964e2b65 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ff4f98e3072ebdb612b0732715fb700fbfdf55f51351132742a0b343fd7fbfc8`  
		Last Modified: Wed, 04 Sep 2024 21:49:29 GMT  
		Size: 52.7 MB (52746481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e90a9355cf91cb09a280cbcf072956d96d4202fe9245935d3707e75093d8cbd`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8435ceb8d71e22ab12f773cd5e47f46729571d4740e7e663b502935e61dcb0e`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 23.2 MB (23247315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42211844e7ef040cb7b3ab22d83de1d919276069da6cf5e4ded9e92046b59e7c`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 923.5 KB (923490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d3b5af296e22b8c3d91ddc3c318ef48fabf4eeaaab40c624373833ef8a7af6`  
		Last Modified: Thu, 05 Sep 2024 06:40:23 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3074d9857a3d16036dc8a09935da0352f6189d5c9f8baa81155afdeb4708af`  
		Last Modified: Thu, 05 Sep 2024 06:40:29 GMT  
		Size: 244.7 MB (244681541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:1687d016b22dd19921e2470802c6150e4de567be390c83c7e4fb9195435d340e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12221705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe1ae2cb892bce6023634745db5fdf3c209a1c56b30cdf9956d678a9be1ec74`

```dockerfile
```

-	Layers:
	-	`sha256:453b03948f69315d58e377d98e3e074db0a908675aec36e2aa7959e875a1f657`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 12.2 MB (12203777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a366c370004305d8f75dcd2320aec5947363dc80f34c8e45059bd227fff32276`  
		Last Modified: Thu, 05 Sep 2024 06:40:22 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json
