## `r-base:latest`

```console
$ docker pull r-base@sha256:a71740f8a406c48b889cfc55e8e7990e9da42cfd606c960718b73e690ebfabe7
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
$ docker pull r-base@sha256:8312d5369c1f022bccabf707ca3e9f097dc6a6e88aa3ff9a59a94cf8ac7a6614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368947502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c871b07caac8e49ab54ac8b2388ff16f1bc586e975e8b67e0fb0f957ab846485`
-	Default Command: `["R"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1773619200'
# Mon, 16 Mar 2026 22:35:02 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Mon, 16 Mar 2026 22:35:02 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Mon, 16 Mar 2026 22:35:09 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:10 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Mon, 16 Mar 2026 22:35:10 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 16 Mar 2026 22:35:10 GMT
ENV LANG=en_US.UTF-8
# Mon, 16 Mar 2026 22:35:10 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Mon, 16 Mar 2026 22:35:10 GMT
ENV R_BASE_VERSION=4.5.3
# Mon, 16 Mar 2026 22:35:51 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:51 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:7bdf93a2879f2008840b5f624f2c4c1f23c3eff5c5c1ecf008ac6cbe78630f3b`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 48.6 MB (48625090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287988b33731d7a80a73f885ee328af47da653ff75ff855aaad767e194d7d4d5`  
		Last Modified: Mon, 16 Mar 2026 22:36:31 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926e752f577f3abddc7a512a05df7bc6b43744d471ee3128b1a758bec971c758`  
		Last Modified: Mon, 16 Mar 2026 22:36:32 GMT  
		Size: 27.2 MB (27231163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba69e337bf960a37a5e19a206f86914646b2b506c2473ea97392715744e87dc4`  
		Last Modified: Mon, 16 Mar 2026 22:36:31 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a551d534f109d98b54206291dee2af76a50db1f43f23a80b97305890780cd`  
		Last Modified: Mon, 16 Mar 2026 22:36:31 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62b34504ad1c5deeec7cae90f292174017d6f18f64ff24e08a7e9b1be3a1414`  
		Last Modified: Mon, 16 Mar 2026 22:36:38 GMT  
		Size: 292.2 MB (292219027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:5f521c40b53890a6035e898a9cd13226bd90356f4321ab9c43b9e4299c507d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13052813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feb53075203e84779ceb717643f1124265b9e8ed0747d49ec6bd2429c676de6`

```dockerfile
```

-	Layers:
	-	`sha256:21fcb6c9fa115adc0b23ee38a67a4285399e657e531b4f17087949d4db9d085e`  
		Last Modified: Mon, 16 Mar 2026 22:36:31 GMT  
		Size: 13.0 MB (13033652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10085566285c5dd411c105481f6abd6c73056b5ce8210b044848d5bba3fdc420`  
		Last Modified: Mon, 16 Mar 2026 22:36:31 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:7db6b2491844028cdc5daadbaa0954ada304dac706f94bd6108cc0d95c645bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352089862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5292dc998cec93fbcaf68b5f0b1ac5ab789ab43bf86960c2428bbc60d0b6bf5`
-	Default Command: `["R"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1773619200'
# Mon, 16 Mar 2026 22:36:48 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Mon, 16 Mar 2026 22:36:48 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Mon, 16 Mar 2026 22:36:55 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:56 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Mon, 16 Mar 2026 22:36:56 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 16 Mar 2026 22:36:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 16 Mar 2026 22:36:56 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Mon, 16 Mar 2026 22:36:56 GMT
ENV R_BASE_VERSION=4.5.3
# Mon, 16 Mar 2026 22:37:39 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:37:39 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:12fcadc230f71b86971148dec79ff06c30c49aa5439d1eb5f527c324c9b378da`  
		Last Modified: Mon, 16 Mar 2026 21:52:52 GMT  
		Size: 48.7 MB (48659056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dc18d0d7912f45cf76fa0872368c41bc96ec6d7c64a4d1518c48fff3c7556`  
		Last Modified: Mon, 16 Mar 2026 22:38:16 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e5a935cc0f9be541335cd92f405b97da6c3e018d029453478d8c0f81764d1f`  
		Last Modified: Mon, 16 Mar 2026 22:38:17 GMT  
		Size: 27.1 MB (27081410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7f1f8b3565b12465ead218b591cfc643461db22e413bba91cc509e9e59546c`  
		Last Modified: Mon, 16 Mar 2026 22:38:16 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ed8bfc1a41f760ec0aa390653e2b7225fef395da74a58b9c158e8e1865a657`  
		Last Modified: Mon, 16 Mar 2026 22:38:16 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f90e5e5184cc0264eba397669c027caf68a7db653ef199ea7308b430bb363e`  
		Last Modified: Mon, 16 Mar 2026 22:38:22 GMT  
		Size: 275.5 MB (275477182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:60699dabf33beb64f850975b8b25ed0d0b4cb93d822b3fea25489077ed76218c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13157640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3788e5522864558b0e1f05c458ee21580e1a815de473ce3deec1c4351c8839fc`

```dockerfile
```

-	Layers:
	-	`sha256:1af78df7ac5849f9d0c707a859261ca3df64329adc30936b7358370559e422a8`  
		Last Modified: Mon, 16 Mar 2026 22:38:17 GMT  
		Size: 13.1 MB (13138341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b23ac8751367393f3d61bf56554d24b2ce673cd22f5e25c272a009d681f8e4`  
		Last Modified: Mon, 16 Mar 2026 22:38:16 GMT  
		Size: 19.3 KB (19299 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:3d3047b091d65298ee8cfe1403154d9fc1c8f5d4e6515fabf1fa2af59582a1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.8 MB (364841801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0724d0909c91c441c11e15b4bd5c2708c124992af8b007490b71bffe36c383e`
-	Default Command: `["R"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1773619200'
# Tue, 17 Mar 2026 01:36:57 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 17 Mar 2026 01:36:57 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 17 Mar 2026 01:37:14 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:37:16 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:37:16 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:37:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:37:16 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 17 Mar 2026 01:37:16 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 17 Mar 2026 01:38:59 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:38:59 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:7d2a89cc09cc8fe5da27040e11d563b97eb6a593d465fda24b4d65de6eac9269`  
		Last Modified: Mon, 16 Mar 2026 21:54:36 GMT  
		Size: 53.9 MB (53863313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea0de53a5639b498029a80ae91947ca74e5ac626fa0a7c194672dbfd6de9cb8`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8b551f810b76cbe15fd8b273b5b1125473ab4687bb46317fcf6931ba97039a`  
		Last Modified: Tue, 17 Mar 2026 01:40:15 GMT  
		Size: 27.5 MB (27534886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997f0ac5bee6617add414a018030488818aa22e7c2f996e8028accb4dd4eab95`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f262b36c183b99fa980f6eee5b7175dc525dfeb804487a02b3c436c326c4c22`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3237d4f0046c14e08ce09a1bf341c777b1faffe4a3146130f81f52cf2b8d0fd`  
		Last Modified: Tue, 17 Mar 2026 01:40:21 GMT  
		Size: 282.6 MB (282571377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:265cd3469661bbdfb76a647e021a8e79e7a5ab1c2101652ea7baecf21e00fcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13036665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba00dd67643fd0e1563c038e842cb8527d809b3a1e4d596c07e051d676262e8`

```dockerfile
```

-	Layers:
	-	`sha256:d394e0b9748c01810a1e78150f738829d456e1bc10e1439e79f0a06c1dc74aeb`  
		Last Modified: Tue, 17 Mar 2026 01:40:15 GMT  
		Size: 13.0 MB (13017464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6209873a9abf3bf2165d2c5e2c6d8d045cd704a0d6978bc8815de02501708f2`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 19.2 KB (19201 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:ce745ad31650784434f28918fdd791e3125a863219387f41d099613aff1878e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337586709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d6b299114ec3d13fd0d0c885afcee17abe1b7807bb0fbb56b18054d966cbc3`
-	Default Command: `["R"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1773619200'
# Mon, 16 Mar 2026 23:33:50 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Mon, 16 Mar 2026 23:33:50 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Mon, 16 Mar 2026 23:34:01 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:34:02 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Mon, 16 Mar 2026 23:34:02 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 16 Mar 2026 23:34:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 16 Mar 2026 23:34:02 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Mon, 16 Mar 2026 23:34:02 GMT
ENV R_BASE_VERSION=4.5.3
# Mon, 16 Mar 2026 23:34:56 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:34:56 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:86061245e560c9a63c0fbedc08ed9a258a537380494ebcd35a7a03910bcfbd2d`  
		Last Modified: Mon, 16 Mar 2026 21:52:35 GMT  
		Size: 48.3 MB (48334621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae56a295fc6d984a51dff9a6c247fe0e4a3326f02fefd87977abec30a08a227`  
		Last Modified: Mon, 16 Mar 2026 23:35:55 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bf0b2512a862a09d55c20514d9062d16b7db7b67b6c2034a69c847419e7bb2`  
		Last Modified: Mon, 16 Mar 2026 23:35:55 GMT  
		Size: 27.2 MB (27166038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6564f13441d0057f4fe0e0abe87441e5e1468ab705e4f53039e5469bbebab6ed`  
		Last Modified: Mon, 16 Mar 2026 23:35:55 GMT  
		Size: 924.5 KB (924549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcb6cbb7fd4ac600d4571af302b281b521c1508416daf2279668ff0deb8220f`  
		Last Modified: Mon, 16 Mar 2026 23:35:55 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0962ab6fc51233abcc1b9bd117d6d2a99ffe1b75055b5beb0f428a3375daf79`  
		Last Modified: Mon, 16 Mar 2026 23:36:00 GMT  
		Size: 261.2 MB (261157770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:aa64db7d2cb98ac169e7d77cd1852da3bfbf3cfdac58527c0cb95da9db735f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12852918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d359855b7085fbbe67b6fd2e5019bbbbced2748adfc08d0a94f0ea69fe85a26c`

```dockerfile
```

-	Layers:
	-	`sha256:53e0a3ff2f8b777618b542ac108ff5d024b57d2a6e6135ef00b889cab6e98e4e`  
		Last Modified: Mon, 16 Mar 2026 23:35:55 GMT  
		Size: 12.8 MB (12833757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f858dcfc24127bd16a2d43666cb217d34039fa9c49267808cd1cc468a3097f2`  
		Last Modified: Mon, 16 Mar 2026 23:35:55 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.in-toto+json
