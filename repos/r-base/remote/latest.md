## `r-base:latest`

```console
$ docker pull r-base@sha256:c74336dbf65bbe6f81aa5cfffe2fb107faebdbd9e517fd5f0b121192cbfc4cfe
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
$ docker pull r-base@sha256:8b6e194a0b39b8d8fd6588a9ff0b03cc409e1e64e26ac2deb428d08eaa0801d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (354000930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860231d4935ab2a5122471500b603f7608986d9b1bd12e458a45db409d1a9a85`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:dfa41c5a8e1c4511359423b532cb30507d2ec0cb9ef2412143a4d4a2752d2d0a in / 
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
	-	`sha256:be8a7f4a2cec45419ae4d29243820f77c134b84630752f45d42a7725f62db14f`  
		Last Modified: Fri, 27 Sep 2024 04:43:03 GMT  
		Size: 53.6 MB (53616589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d9661c099ef330077e90bc400671543300a1c30b436cb33b5e64861b0ac46`  
		Last Modified: Fri, 27 Sep 2024 22:22:45 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e571c2121ab5d9d1f56e30b27b9976709c92f72f6859ef4cb8d04e4b396401c`  
		Last Modified: Fri, 27 Sep 2024 22:22:46 GMT  
		Size: 23.1 MB (23149429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b110e8737974804701b4f0cf0569e426a6b2cafb4d779f229a96a51dfa757d`  
		Last Modified: Fri, 27 Sep 2024 22:22:45 GMT  
		Size: 866.7 KB (866741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50763ffd1bad10cde7609ba9036ef3111f9a385e93c10498e9abce3fbc65fddb`  
		Last Modified: Fri, 27 Sep 2024 22:22:46 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77674851e7e2bf4b1dd6c134860b2ae0799f560a0c91e8e8e26851b4423cb6b`  
		Last Modified: Fri, 27 Sep 2024 22:22:52 GMT  
		Size: 276.4 MB (276364512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:13b63f9aa75800a3773c352a9f975ea4e26194cfce34336ead0423bbd8a04e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12526879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3fe2c79a5e895cfeab09be2500528e3758beae7bb5eed7659c672fb1f984a3`

```dockerfile
```

-	Layers:
	-	`sha256:c1c2a006273f2095c5e72277c582fc4089b70bc6d533916dca3496b0345d1a6c`  
		Last Modified: Fri, 27 Sep 2024 22:22:46 GMT  
		Size: 12.5 MB (12508671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e7ad11c5c4089c8fc88593c726cbe11d1427e7562bc8bd8b1e5138ac68bd29`  
		Last Modified: Fri, 27 Sep 2024 22:22:45 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:69b133609790f11087cf6785d47242b9495a7e2aa90fc82d364837ce3370d2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364062540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c196318021da76b23dbf726779cd2af32d6f3e33e938cdf4b0c72b43b0f3673`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:1cabb289a72ffeb44fe38a5ebdb31c8f6a7bb3e5fd5c46b1b4132b34443c5811 in / 
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
	-	`sha256:4fe1b2916866944b77c438d068d2b8fa4c195832fc93b9c0068bfa8310f21499`  
		Last Modified: Fri, 27 Sep 2024 05:37:42 GMT  
		Size: 57.1 MB (57100382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba218fe68ebd0d7f69d627c7fce135693731243bcb923b19ef119e27419415b2`  
		Last Modified: Sat, 28 Sep 2024 00:37:00 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3068638ac49643d6041c45e8a6fa27c6e7dc1b33d24a0d89df4309f4672ff3f`  
		Last Modified: Sat, 28 Sep 2024 00:37:03 GMT  
		Size: 23.4 MB (23388977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63c2fc529fcc4b2e9574aa1cdbb4134d802c60e7090e348abb2db92bcd59b33`  
		Last Modified: Sat, 28 Sep 2024 00:37:00 GMT  
		Size: 866.7 KB (866739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80501242161fe4814e3ac5c57aa16f3fd7d0110efbd63b2ec824a69d26f60ce`  
		Last Modified: Sat, 28 Sep 2024 00:37:01 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f067a43ffc1cae8646b40328bf96662bc95878e7feff8528a154bdffdcfb660b`  
		Last Modified: Sat, 28 Sep 2024 00:37:10 GMT  
		Size: 282.7 MB (282702784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:1aec9b3a2dc0d628b3be7030d12376a1ceda1712afdd09262cc95acf0250fcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12425477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3b5f76568136219ffc9d307c7d7f7e210776eee9580d80dcbfe9d53a50d043`

```dockerfile
```

-	Layers:
	-	`sha256:82067597a6c485a353a4ad4d3373e0e75e2c1e7f7334a77b7f568b30a7a91dac`  
		Last Modified: Sat, 28 Sep 2024 00:37:02 GMT  
		Size: 12.4 MB (12407514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21d5df45ed58f706580880d7c7e0cdab4a40445b31adf5b3125ea192ab17b09`  
		Last Modified: Sat, 28 Sep 2024 00:37:00 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:908d10f013c6d99c2ebaa9dd179cb07dcd46a150eb867e85bc15ddcf2b249e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334693552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48aade0bcbb0bc1bacce1b84177a6b082176acae6c82089c1d6f6715b20cf63`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:3e39c625eaf60953d8cee79d51e2111b241d054227598d815a080b9fe676b690 in / 
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
	-	`sha256:6254903b6edc85d1dc106a3e9025a77bf951ee477df6401427b61d5e2f6ccc3a`  
		Last Modified: Fri, 27 Sep 2024 02:48:24 GMT  
		Size: 52.8 MB (52771071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943f2b224fce1f40ab1cddd6049c0ac1afcc891c0dabd939eb9f8edb31bd8808`  
		Last Modified: Fri, 27 Sep 2024 17:07:44 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508a3d8711517c72d656fc1fe63b1a2c98a7a9180454425c82bd05d46e99e5d9`  
		Last Modified: Fri, 27 Sep 2024 17:07:46 GMT  
		Size: 23.1 MB (23118257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d78006081c4114633b3e155f66827561d457677bceac7c28059b8d5ee07fef`  
		Last Modified: Fri, 27 Sep 2024 17:07:44 GMT  
		Size: 923.5 KB (923491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c982f8adc6ef361a5c0b2ae14baaee0476a4d3016c09dc14ee113bb0d855c`  
		Last Modified: Fri, 27 Sep 2024 17:07:45 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c18bd7fc7d58d45b73127b2ed122053cc466495dcefac630673b57626af4f4`  
		Last Modified: Fri, 27 Sep 2024 17:07:48 GMT  
		Size: 257.9 MB (257877077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:78879ce3abe4638fa65248a80fa689dd6c8e2e22cec679c4380e0553d531af2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12232675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84c5187d911a72e0f54fd940f0152f39e202fc85996a13096f73bce4b653d37`

```dockerfile
```

-	Layers:
	-	`sha256:5ebb9a42f6843adef5550b165500a4cd294db1cb35adbdcd19170c48c8c73a45`  
		Last Modified: Fri, 27 Sep 2024 17:07:45 GMT  
		Size: 12.2 MB (12214746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4096daa85eef065603a7905ad68764e971cd3d929abf72a698bd745aba432d63`  
		Last Modified: Fri, 27 Sep 2024 17:07:44 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json
