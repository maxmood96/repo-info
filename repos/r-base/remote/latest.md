## `r-base:latest`

```console
$ docker pull r-base@sha256:b697beb724eb36afc82b41f9af950c258e82348201861ec63bddcadcb928c1be
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
$ docker pull r-base@sha256:a8e0ccd233c479c60c20c51b62e868ec1478c0113caaae4c9717540451bd3e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371578225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63504eeaa419c3e10c2a8695c6225619f13d90d1e14ee4ae6b3af5a2a61ee98c`
-	Default Command: `["R"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1771804800'
# Wed, 11 Mar 2026 20:54:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 Mar 2026 20:54:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 11 Mar 2026 20:55:01 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 20:55:02 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 11 Mar 2026 20:55:02 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 20:55:02 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 Mar 2026 20:55:02 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 11 Mar 2026 20:55:02 GMT
ENV R_BASE_VERSION=4.5.3
# Wed, 11 Mar 2026 20:55:44 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 20:55:44 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:34be0fb38bdb10b6efea64895d8af767ee0135f3467c8cbf6b2a7ad809ff66f7`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430ada9548868d4d3eb784e7e53789c22a5cd4b0702d57720db38b34ca47ee39`  
		Last Modified: Wed, 11 Mar 2026 20:56:23 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66b6654d979a87a8b95630a26fe1996b0b84904dc2f4bcd3f17e58fbbd04c2`  
		Last Modified: Wed, 11 Mar 2026 20:56:24 GMT  
		Size: 27.2 MB (27226264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45155cd655c9591681e63b9dd142a8e321a005c94c3347a29469c1abfd99382e`  
		Last Modified: Wed, 11 Mar 2026 20:56:23 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e746b5604f5ec0a1c412384a368bfa95acc667d3f517a3416c4063bce6c6bed`  
		Last Modified: Wed, 11 Mar 2026 20:56:24 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e51c67c2052ad005f9a9855ba20b9c817d4d0ce96b5332821400af5d400715`  
		Last Modified: Wed, 11 Mar 2026 20:56:30 GMT  
		Size: 294.8 MB (294802553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:06c8ef44fb79e89938b50902769a55ca477a00842fcc7b24457775089f2f4fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13057837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74393a8ad88ada4ec81097640d0e7230936d3e972b6a5c04e1d4b4ab2ed62226`

```dockerfile
```

-	Layers:
	-	`sha256:5327e75a445fe87ae928a228f3ec2b0556f86452a93ce883e25fc1ff6fe9ecbb`  
		Last Modified: Wed, 11 Mar 2026 20:56:24 GMT  
		Size: 13.0 MB (13038677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbe1ada19b6e7bc12bc132f58bd47845625467f10fa9a1c5c7810e863cfad423`  
		Last Modified: Wed, 11 Mar 2026 20:56:23 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:683ed0564664bbc7d435d4dc77adbcdc6302aada12014a590c5b8ff938189169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354703175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f64222396766d010c5e57e271d4e0d3ae3bb17957c615830649f79f761b161c`
-	Default Command: `["R"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1771804800'
# Wed, 11 Mar 2026 20:53:44 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 Mar 2026 20:53:44 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 11 Mar 2026 20:53:51 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 20:53:53 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 11 Mar 2026 20:53:53 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 20:53:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 Mar 2026 20:53:53 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 11 Mar 2026 20:53:53 GMT
ENV R_BASE_VERSION=4.5.3
# Wed, 11 Mar 2026 20:54:35 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 20:54:35 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c8a993150206adc8ed6d5444bc6073fe1f1f2401037e10aa375ccb6fbef8932e`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b00c85e84960839a1af3f23b42ea748d463c7c3ffef6151f51843ef92f0dbc`  
		Last Modified: Wed, 11 Mar 2026 20:55:12 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a80cdb9fb1a245b33c3ca89cc8366d116503d98f417e8f1c671cab72b4b0286`  
		Last Modified: Wed, 11 Mar 2026 20:55:13 GMT  
		Size: 27.1 MB (27060547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66fa48bdbad819223c7b4476b32a67b7231956a0d1ebfcc708cfc247de202d5`  
		Last Modified: Wed, 11 Mar 2026 20:55:12 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efac05fe4a01e99f273b3213726bad486b02b436951f80b76bdf27850153198`  
		Last Modified: Wed, 11 Mar 2026 20:55:12 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225753ec71ed4e3d955d943cb2d9067cddb00c2b645aa8ab719fbc3c1ede386c`  
		Last Modified: Wed, 11 Mar 2026 20:55:18 GMT  
		Size: 278.1 MB (278065376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:c0712f893ef8cac54819460d9da79faac9b6c42d3ae6c2d0a6466ea416dcc3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13163949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4c19d42e0aa02341e4172870688df12eea3a953311be74e448b0ddec863578`

```dockerfile
```

-	Layers:
	-	`sha256:c91cba8af85236bc185eb2340559e1ebde2535786bf3b766c273d50071e0822d`  
		Last Modified: Wed, 11 Mar 2026 20:55:12 GMT  
		Size: 13.1 MB (13144648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63f1dc8bc9ea8e9f2c3fce2edb446ce6bd2677b608dfe63649038e0c38ede78`  
		Last Modified: Wed, 11 Mar 2026 20:55:12 GMT  
		Size: 19.3 KB (19301 bytes)  
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
