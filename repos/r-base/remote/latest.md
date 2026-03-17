## `r-base:latest`

```console
$ docker pull r-base@sha256:0987965d97f0cd870f16790f637b860e5b8731baff9410f997da80c6be013d7b
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
$ docker pull r-base@sha256:1e0be99cb268329538a875469d997f57414c324600b6fd8e232d08f25bb2b0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367313546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26256a5a53c5b6a7bde6ef1cdf56e8632598e98445c5cb501294037e2751bc6`
-	Default Command: `["R"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1771804800'
# Wed, 11 Mar 2026 20:54:15 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 Mar 2026 20:54:15 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 11 Mar 2026 20:54:34 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 20:54:36 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 11 Mar 2026 20:54:36 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 20:54:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 Mar 2026 20:54:37 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 11 Mar 2026 20:54:37 GMT
ENV R_BASE_VERSION=4.5.3
# Wed, 11 Mar 2026 20:56:12 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 20:56:12 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a9c7d7625b810d130976f4d65172bc2e59635199240180b43a17644df8a7c067`  
		Last Modified: Tue, 24 Feb 2026 18:44:39 GMT  
		Size: 53.6 MB (53641787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9f777dfea30663ba82ecb730ddfea8b1725ca12f2a2d1f14f1cbe1754f6b29`  
		Last Modified: Wed, 11 Mar 2026 20:57:25 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6016ffa7107b2ccbc57744ddd4522e9ffaa7459b70733ad852389720ab5fe9eb`  
		Last Modified: Wed, 11 Mar 2026 20:57:26 GMT  
		Size: 27.5 MB (27537705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f659853fe8774d3822e7fdaebf8c669431414f96e2e65daada06a99815ee7be`  
		Last Modified: Wed, 11 Mar 2026 20:57:25 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aa95ef99801cd66c993451763265deea02dc6f37cd33c22ec4d18884aef4a3`  
		Last Modified: Wed, 11 Mar 2026 20:57:25 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fbbf438006aad41783cdd3bcc9276b7ca8741af9fe0045e6c8cd75eb31647e`  
		Last Modified: Wed, 11 Mar 2026 20:57:32 GMT  
		Size: 285.3 MB (285261829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:9adbd1a4b77f5bf13e3fbe4f08798868a2aa2df3421c1f76a14da37b3c2ff1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13041708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032af2802af2c6eb17320c2b822908fbe8b2c191be9366295c1046a62d7226b3`

```dockerfile
```

-	Layers:
	-	`sha256:090d39d44dbc697e200739baaaf987cda4e857e45695eb521ab8e5adf9262da2`  
		Last Modified: Wed, 11 Mar 2026 20:57:26 GMT  
		Size: 13.0 MB (13022507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8712c04e40c575e01182bb1139825e263207a7e1f3a1ddea17d01ce350e3295c`  
		Last Modified: Wed, 11 Mar 2026 20:57:25 GMT  
		Size: 19.2 KB (19201 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:5f779db218615433dbf68353659d233681e6885aa02abb154a21a35e2e9841c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340281419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed533e3e7f517b99e73b8e91fa0d8e30181f125ae9a4179a67c62da3bc64bb3`
-	Default Command: `["R"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1771804800'
# Wed, 11 Mar 2026 20:54:48 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 Mar 2026 20:54:48 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 11 Mar 2026 20:54:56 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 20:54:57 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 11 Mar 2026 20:54:57 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 20:54:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 Mar 2026 20:54:57 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 11 Mar 2026 20:54:57 GMT
ENV R_BASE_VERSION=4.5.3
# Wed, 11 Mar 2026 20:55:43 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 20:55:43 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:fc75b039b41eab51d245e601a0ca918f28836808b7ae484f3d0e33c4db6b6ceb`  
		Last Modified: Tue, 24 Feb 2026 18:43:05 GMT  
		Size: 48.4 MB (48448352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef5182530c16092ab2da280b9e4b229cc86925800dfedf483643bad1bb62609`  
		Last Modified: Wed, 11 Mar 2026 20:56:33 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9937d54c325bc3a40c10171309e4099ec40b65b0e6f10ce71b0c28f895594`  
		Last Modified: Wed, 11 Mar 2026 20:56:33 GMT  
		Size: 27.2 MB (27167496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8eb7213754501e3846ecc6537d1cfa359362638bb6fa7dc97cfabb03406920`  
		Last Modified: Wed, 11 Mar 2026 20:56:33 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a779b6db3aee0a87f0ea0ea183f77906c0d2e6c85d4b6550094e588cc77f52`  
		Last Modified: Wed, 11 Mar 2026 20:56:33 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cd0b3a3ffbb50d01e37c2e14e4b6a0cfc17d3dfc57e0422bc98354904e4a4`  
		Last Modified: Wed, 11 Mar 2026 20:56:38 GMT  
		Size: 263.7 MB (263737286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:97b5b2183b0dfe5628fb33b27163212f415d8d32d23c674f986b8c13dfaceff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12857941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e304a5a7dede3058b7f96b32782a4c63b315d4b929bde16d6a870d6b77bdd78`

```dockerfile
```

-	Layers:
	-	`sha256:846f77db24942cc36259768a30d8d2084e55d4af8e8307e6a67d88e455b523a2`  
		Last Modified: Wed, 11 Mar 2026 20:56:33 GMT  
		Size: 12.8 MB (12838780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7410dc18d40d1f5fb44d0c26aa738eeec386f95ced8c59f9bd6954e0a6b72503`  
		Last Modified: Wed, 11 Mar 2026 20:56:33 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.in-toto+json
