## `r-base:latest`

```console
$ docker pull r-base@sha256:f18ee88640038e896a9508bc672cb799312041b243ad5a917b4e7ad454b3ed21
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
$ docker pull r-base@sha256:54b034ad9f044968de3d5cdd9ef04b11efaae1f2c8a11b2b108410c502dc8f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368574405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782b91bb26cafdba17fa83e4422562c6fc97bd5614e639c7a5fe5ed04f4f6b01`
-	Default Command: `["R"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 00:26:43 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 04 Nov 2025 00:26:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 04 Nov 2025 00:26:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:26:49 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 04 Nov 2025 00:26:49 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 04 Nov 2025 00:26:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 04 Nov 2025 00:26:49 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 04 Nov 2025 00:26:49 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 04 Nov 2025 00:27:27 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:27:27 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:90f44b176643572e0370d1172f54e2db1950b1b69536cab5f222f4cf55cff73c`  
		Last Modified: Tue, 04 Nov 2025 00:13:16 GMT  
		Size: 48.5 MB (48481362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9b122020bb73b6c313329c72f33e298c1318bb85a6a8441c9ba79520cdd7cc`  
		Last Modified: Tue, 04 Nov 2025 00:28:25 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ccee98e0c5342b211aeddeb7b160649c278569d830f4fc4dfdcf62b471eb0f`  
		Last Modified: Tue, 04 Nov 2025 00:28:29 GMT  
		Size: 27.0 MB (26965582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40a3af05dc2e715fd926c41976d4ae3265c6745c5d9ae42a7755bfd23747f28`  
		Last Modified: Tue, 04 Nov 2025 00:28:26 GMT  
		Size: 868.5 KB (868475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9673056c13e29d01ba7d9b13957dde8d4b899365fa4bf8bb16315c8245c7e04a`  
		Last Modified: Tue, 04 Nov 2025 00:28:25 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1870cc1c5b60ff51a184044f3993cc90eef9ba271d3952374fc20f98a5cf30`  
		Last Modified: Tue, 04 Nov 2025 09:10:13 GMT  
		Size: 292.3 MB (292255326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:ad8ed0bd6e2e9dd2e88b7c3fefdf043ea712ab24e9c786e21865372b984d03a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12961209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10cfe4eebcb372133d500f002e06a6099a96e5c410cbccfa36cfc9124effb8e`

```dockerfile
```

-	Layers:
	-	`sha256:918444515da411e70baed0980345eb2919077307a8e2581674967d7f624826f6`  
		Last Modified: Tue, 04 Nov 2025 10:13:29 GMT  
		Size: 12.9 MB (12943111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8899878d02ce93f259900fc5d013b8a40a0dd59b495865b3826b14d7f97b139e`  
		Last Modified: Tue, 04 Nov 2025 10:13:30 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:cc8d405442367204e524c366a9cbdcfa68b33002565fbd985606406bbc34ad6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349839868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9436d8bcb07218ca45fd9d6bf57674b1fdad41bbed30e439f1069006b210f484`
-	Default Command: `["R"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 01:28:46 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 04 Nov 2025 01:28:46 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 04 Nov 2025 01:28:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:28:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 04 Nov 2025 01:28:54 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 04 Nov 2025 01:28:54 GMT
ENV LANG=en_US.UTF-8
# Tue, 04 Nov 2025 01:28:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 04 Nov 2025 01:28:54 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 04 Nov 2025 01:29:36 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:36 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:8fe74ebf733f4a2b673fce2a29ff282e87d98a36ff2897bc5c237fab3f805191`  
		Last Modified: Tue, 04 Nov 2025 00:14:31 GMT  
		Size: 48.6 MB (48583636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48056523e294cdbfe53b3157e7f79995b746d12c7450b2aad3c89e7e734f09e`  
		Last Modified: Tue, 04 Nov 2025 01:30:27 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2368c5fb3cfe9f4ed0104415135f66ba4a7211d26e6c624b07292dc467ee25a`  
		Last Modified: Tue, 04 Nov 2025 01:30:35 GMT  
		Size: 26.8 MB (26827462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4978d5739d34be12c1238cc60ea1e4ae77b7957990bee4a01933b8d92b5602b5`  
		Last Modified: Tue, 04 Nov 2025 01:30:27 GMT  
		Size: 868.5 KB (868484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208ed69fdb4c0625750ecb66bafa24829ae750bf7234413c334ded1c285dd4dd`  
		Last Modified: Tue, 04 Nov 2025 01:30:27 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33277d925e54cb497fe8f8e9755dc94683e9d171a62c61b650821cd33f44485a`  
		Last Modified: Tue, 04 Nov 2025 10:33:30 GMT  
		Size: 273.6 MB (273556626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:ec4d688cabb310e3a24be792200879e10b4ac6f1789ad5ea8f18573e1bc91d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13050455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d99df1fe470038fc2cdf2dcc20db9e3dbb4afde4fc2715156695df8166b575`

```dockerfile
```

-	Layers:
	-	`sha256:0c24220a7c3f8461a40ea1e05b2cfc5115431669b4d5ebe5ea185317c4ba428c`  
		Last Modified: Tue, 04 Nov 2025 10:13:40 GMT  
		Size: 13.0 MB (13032217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2599b222e782cceae8b53d21f04a51090d702f9e2ff623a8d30d8559338d072`  
		Last Modified: Tue, 04 Nov 2025 10:13:41 GMT  
		Size: 18.2 KB (18238 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:79213ec3fdc89b237a87d44351730fcbd3d00c247ea5e9eeda6b2690a801db0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360239245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34982a8173860e848dc1269f00d061e177b443198527dc617c514f26ebff712d`
-	Default Command: `["R"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 05:52:27 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 04 Nov 2025 05:52:27 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 04 Nov 2025 05:52:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:52:46 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 04 Nov 2025 05:52:46 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 04 Nov 2025 05:52:46 GMT
ENV LANG=en_US.UTF-8
# Tue, 04 Nov 2025 05:52:46 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 04 Nov 2025 05:52:46 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 04 Nov 2025 05:54:16 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:54:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:174727ec3d50f4bd692245f2ee33064dc9c22375cca6dc7eda65e345ac6d4927`  
		Last Modified: Tue, 04 Nov 2025 00:19:09 GMT  
		Size: 53.3 MB (53315238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71379cbab8dfe04257ba14ee7b34b1789839d081788bf6c4f946366a46f7bcc1`  
		Last Modified: Tue, 04 Nov 2025 05:55:59 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614065e0ed25dced713c4e6f42f356a7f2ffe93aca5e599798476f0740b651a3`  
		Last Modified: Tue, 04 Nov 2025 05:56:01 GMT  
		Size: 27.2 MB (27229662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd18e4118fe702c209d9b7beadd0c46723298e8ccff6672ee05536a711de4e`  
		Last Modified: Tue, 04 Nov 2025 05:56:00 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4362509f82cab9fcb569c9f14340f347857099c6d5dffacdaec463b0eab03c31`  
		Last Modified: Tue, 04 Nov 2025 05:55:59 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cadb423dae841f78cba8d96caa956ec9ad283722fa33144c01697441febb130`  
		Last Modified: Tue, 04 Nov 2025 10:35:50 GMT  
		Size: 278.8 MB (278822194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:49dfb02c84b535f920ece166e7ae0b1acc97dfe886401ddc58bc4f6e1e9904a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12947037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1f603513abfdc2e9ffd008d64a9d2ff6e25ea2b59b1659fc5c7730b06952fa`

```dockerfile
```

-	Layers:
	-	`sha256:471e73932e5fb7c3729cb67f6dc83676fd7ec48e6786ad924e3eb915c656ccfd`  
		Last Modified: Tue, 04 Nov 2025 10:13:50 GMT  
		Size: 12.9 MB (12928900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:218c8b855f291ff8be472c55e01430775a3a9455d32513e8fa9ca292b28ad45a`  
		Last Modified: Tue, 04 Nov 2025 10:13:51 GMT  
		Size: 18.1 KB (18137 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:e348364f6b7b4bfd52f770b1160ccf15358366f1b7367371d7e46344bad60caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328527525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1879512e14d41f3e48600614b9eb28d1571dda1407721864ce2ca079992ad7`
-	Default Command: `["R"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 09:41:56 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 04 Nov 2025 09:41:56 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 04 Nov 2025 09:42:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:42:06 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 04 Nov 2025 09:42:06 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 04 Nov 2025 09:42:06 GMT
ENV LANG=en_US.UTF-8
# Tue, 04 Nov 2025 09:42:07 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 04 Nov 2025 09:42:07 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 04 Nov 2025 09:42:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:42:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e99c0da2e97fc60ed941b2b64ad1209d58000b6a2e554be98962ab3f543525bf`  
		Last Modified: Tue, 04 Nov 2025 00:18:40 GMT  
		Size: 48.3 MB (48343060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcad3425f2c21d2ed77186dd47813d539b27a283698d8c249401e4d3eca25e8`  
		Last Modified: Tue, 04 Nov 2025 09:44:04 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715f8d43e18aefb7383de55633cb62c0aa24d32791b8fb47432f11b8f66e3366`  
		Last Modified: Tue, 04 Nov 2025 09:44:07 GMT  
		Size: 26.9 MB (26908544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70b8ae7ee892be56cd50cd3f55119fe0dd230a81838f9096b97ecf77cadb951`  
		Last Modified: Tue, 04 Nov 2025 09:44:04 GMT  
		Size: 924.5 KB (924544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f423087300b16864b36a824864d055f4be75c81c1b24da3c470e9bb303c562f1`  
		Last Modified: Tue, 04 Nov 2025 09:44:04 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4473a5d6c60fa1ab91fd29b48827608f6c3da1130bf39e32a324b0068cd2f02`  
		Last Modified: Tue, 04 Nov 2025 10:36:49 GMT  
		Size: 252.3 MB (252347719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:c668304a4db629f8c5e52e3183c21467610ad2613da709eed6ae92d9297ebf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12752421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecf0ca1bc124745dac3f096a766b2eb572511df2169cdc122ef042b53cb0587`

```dockerfile
```

-	Layers:
	-	`sha256:5c6e4a660f16bb398870dab3b48123de84007ac004de23efe2883bf5d470ec73`  
		Last Modified: Tue, 04 Nov 2025 10:14:01 GMT  
		Size: 12.7 MB (12734323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17aeb5ad1c9c3231ccd442045efd12091dc4973e101463a2e178018cc6526398`  
		Last Modified: Tue, 04 Nov 2025 10:14:01 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json
