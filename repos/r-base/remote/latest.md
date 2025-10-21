## `r-base:latest`

```console
$ docker pull r-base@sha256:fa1972f31def171b83e0911e947ab8b57db143f0fc8a67af4c0d5ac329041646
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
$ docker pull r-base@sha256:a5845a19dbe67a49284a328ad2505cf8688aecaf22e4bbbac581044bbbd11c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.8 MB (906793790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ae9d30c37e27b1356e9c214136e538d5a350216a05898eb91b651d8877cf78`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1760918400'
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
	-	`sha256:4a5c7cbd3a941ab0c02b6508acfe1e36538433539b8d0d1b5fd34bdb9f52ad60`  
		Last Modified: Tue, 21 Oct 2025 00:20:25 GMT  
		Size: 49.8 MB (49759134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f807ca5580e26dd423ba811dc3cd10874294c7d53bd59cadee489efe8af2f0f0`  
		Last Modified: Tue, 21 Oct 2025 01:42:20 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb751f1a3c574d232af4930be1ab5722e79453e0d736d8eb1263708e0eeb646`  
		Last Modified: Tue, 21 Oct 2025 01:42:22 GMT  
		Size: 27.0 MB (26954569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafba1d3190b6953d36d66372309237a598779e9309cc61256a3abe3b3d67545`  
		Last Modified: Tue, 21 Oct 2025 01:42:20 GMT  
		Size: 868.5 KB (868478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340ee36ead8b4f8acf469ad350188ef08afbcab3975a3cffbfe485a66844ed7b`  
		Last Modified: Tue, 21 Oct 2025 01:42:20 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb66856b0312f97fb4f36f0418572d970715774614d7394d7e6dc211857dfc6`  
		Last Modified: Tue, 21 Oct 2025 08:58:57 GMT  
		Size: 829.2 MB (829207948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:afc2ae3d73274957376944a0aff6ae5ecc55fa80baa4b4d51a97e1d119e3cd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12993491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7d20993d0f8b8d0c05660ef991961a078ca2f3d1add2f948cad488b39d1a2e`

```dockerfile
```

-	Layers:
	-	`sha256:690b412d2e2d1f8587ce2b45bff374da4fad441be2d3c7c0e5c0298747d1e31c`  
		Last Modified: Tue, 21 Oct 2025 09:13:25 GMT  
		Size: 13.0 MB (12975350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d365036e453b121145f3207e78f44be8b7c44432bb6860889fecf006af61528d`  
		Last Modified: Tue, 21 Oct 2025 09:13:26 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:591fb54c981957a2bce056f8f6be212bc7250596d6fcdf1de4c38062b05eabd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.5 MB (907500520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab448b6bc7f7eaa392e5f62ba67fcab51cd81f70e618b234825fed0fd3b1833`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1760918400'
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
	-	`sha256:e6d3cb0e5bff2ab511722bdfb0d01ad86b98208ac1234c63856d04921ea955fa`  
		Last Modified: Tue, 21 Oct 2025 00:22:22 GMT  
		Size: 49.9 MB (49888480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77482bc733d7381c63bc2707d12c4d7ec3554c33a3faca7d07baadf78e039e`  
		Last Modified: Tue, 21 Oct 2025 02:31:44 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4e4b6c1e93b6eaa11c4c0da6a6eba1a9d394a5184b500803ed2776bae88cde`  
		Last Modified: Tue, 21 Oct 2025 10:24:24 GMT  
		Size: 26.8 MB (26839661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853c5faf0330335c12341146ca95b20a4ecde771c1a6551a136fc8f4601ed5f`  
		Last Modified: Tue, 21 Oct 2025 02:31:45 GMT  
		Size: 868.5 KB (868482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c5b54d539c2470297efb788ee0ef3b6a73a70239950af0a9d812d20a100431`  
		Last Modified: Tue, 21 Oct 2025 02:31:44 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6d3b16e1704470db91c8ed07ef50204aa7c1a68ea747535b5c83119b8ea720`  
		Last Modified: Tue, 21 Oct 2025 10:24:51 GMT  
		Size: 829.9 MB (829900237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:feedccdadead44bf6b28e5a5f7e513d535c7b41fce24924b297ec445eb5ee760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13082739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d47b09b05dfd8d66b49d80947890d03bf8ecec6eed3b1d3d13f47de411981f6`

```dockerfile
```

-	Layers:
	-	`sha256:7581bf22336c48c64ad4ef82e3d5d1372667252a4ced2f6144aead2793d45438`  
		Last Modified: Tue, 21 Oct 2025 09:13:38 GMT  
		Size: 13.1 MB (13064458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a157e0e38bef743ef34603aed8acdcb5e18075c691c01577b2687c8f1f9c20`  
		Last Modified: Tue, 21 Oct 2025 09:13:38 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:b6cf10b516ce6c868a1a71ceb9e516d6ae402b06cdbc1934ba846a6aa8a18690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.4 MB (826424596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0300295acc2b6529b0b093693be5af445621932b7d2677a791fd0c65f57969`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1760918400'
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
	-	`sha256:36d0226101dd4d1467e5db6271afb57e987afc3f5bae52044471b8b5521e9b0f`  
		Last Modified: Tue, 21 Oct 2025 00:25:25 GMT  
		Size: 54.9 MB (54875795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85646ea74bf38169f2b9d17182cd4eab987c862b4d4e07664f8e8990e56a2c85`  
		Last Modified: Tue, 21 Oct 2025 07:11:51 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d125e1d918ff2a09fef3fb58b3a67138fc205a0e54e2c8469dd7ea702bee33`  
		Last Modified: Tue, 21 Oct 2025 07:11:55 GMT  
		Size: 27.2 MB (27213186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415966122a650a0bf87ec9a0569a98817f0c7a22d9869ee9354d978f16660f17`  
		Last Modified: Tue, 21 Oct 2025 07:11:52 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b745a59851063c1c18058b6c12d093d528171099e660c8e44ffdfc17e52f2d14`  
		Last Modified: Tue, 21 Oct 2025 07:11:52 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac5e37feca903a44b4b2628d57646209cae4504f3e93d422bc15e53ab413bd9`  
		Last Modified: Tue, 21 Oct 2025 10:30:00 GMT  
		Size: 743.5 MB (743463461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:d029bf1d8ba2f864bf4bf11aa2166c8490da0c62b930e05739432ccac5e15779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12979334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fce9f3a27b961e81c6ed6a89d9478250a2e190d774f7b28bde73976e8696a2f`

```dockerfile
```

-	Layers:
	-	`sha256:586a2ea968504ad5b995e15045f1ec26ac08a18f147e31e7a0c409c3ffa8d921`  
		Last Modified: Tue, 21 Oct 2025 09:13:49 GMT  
		Size: 13.0 MB (12961153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1e42759477ea10983043b787d372cddb3ebb3e926402a88cd74fcf32f10a19`  
		Last Modified: Tue, 21 Oct 2025 09:13:50 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:9ef0644a70df708a82b4424c0f33b7e124432ba58a718cb4e1741e1eccf22284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.4 MB (779372790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccf9e2dc3df957952a46a01aa9a8105efbdac2dfd64bc32ba5fe8b44dc5da4`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1760918400'
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
	-	`sha256:51fdd12f65670bad766fd6f57cffa9e3640464411e76b2dce4dba9c4c4c01438`  
		Last Modified: Tue, 21 Oct 2025 00:26:48 GMT  
		Size: 49.6 MB (49620786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ffd483098a2ae8d97868f3c212e492290cdb452b4e76bc07fa2db8d79cd121`  
		Last Modified: Tue, 21 Oct 2025 11:41:25 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73c7278129f0efc4442260f21e3f275858b19a591ea9d1ab2d1a0580d49bc49`  
		Last Modified: Tue, 21 Oct 2025 11:41:26 GMT  
		Size: 26.9 MB (26908971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e451d816f825973a87233febcba7a5f493fc21b78e24da3d15a013684c680f65`  
		Last Modified: Tue, 21 Oct 2025 11:41:25 GMT  
		Size: 924.5 KB (924548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041365f0f3ac7a5a39568a1f5b8b9293b61bd98498243022fcd50c8bf3f4c837`  
		Last Modified: Tue, 21 Oct 2025 11:41:25 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357b1194500fefbd0f9741edcd2f749dead2b071e84da68afc36a1d4189117bc`  
		Last Modified: Tue, 21 Oct 2025 11:41:17 GMT  
		Size: 701.9 MB (701914825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:ee05fe9d979cf1df8ec9f4543283c9527fff7ad79e60d6c67d6654cff4766586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12784700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18cee4b52dce171bff83679fb6eb33cbdfd7f54f565361caaaae548bddc96ec`

```dockerfile
```

-	Layers:
	-	`sha256:8378c7d4f396c938998bd2ec1e302c8a2a703e1571d82d25ffdb9d3187f56590`  
		Last Modified: Tue, 21 Oct 2025 12:13:44 GMT  
		Size: 12.8 MB (12766560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8855430796d006c4df81c77db921862f2d6c149c342f1af2ec8649838ee9358`  
		Last Modified: Tue, 21 Oct 2025 12:13:45 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json
