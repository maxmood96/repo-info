## `r-base:latest`

```console
$ docker pull r-base@sha256:7ec92d23bd38500feb9c6afa1c371f107d24c8e091884ffb061fc6800894a8e6
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
$ docker pull r-base@sha256:7f4833ef846a07404d4cc7267f1c6c8797eb1f939af1c2859e7b4608084d4655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 MB (373886494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce23df3be293490117f46ea07e392635baa48dd2c6cc8545c21cdab9c6735e3`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Apr 2025 18:18:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1747699200'
# Fri, 11 Apr 2025 18:18:21 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Apr 2025 18:18:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV R_BASE_VERSION=4.5.0
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:df56d2e10300383b653c76122e6b5696d7113980a59e9e16cfad3e99742758e3`  
		Last Modified: Tue, 03 Jun 2025 13:33:02 GMT  
		Size: 49.2 MB (49246909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e4c4b4b12907e909d1b154c321cf30206ace4a3354afc8639a53c931fedf2e`  
		Last Modified: Tue, 03 Jun 2025 13:39:13 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40450e585eb9c615f111400420b9f5de11ed02719f96900623f75f9961c90e29`  
		Last Modified: Tue, 03 Jun 2025 13:39:16 GMT  
		Size: 26.9 MB (26898512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a24b0ca57ca3e74c1c121bb6e64eb2928e6ab1768cd776166f1006f9908aa0`  
		Last Modified: Tue, 03 Jun 2025 13:39:15 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768eb9dfc708ba26d5ad78436301637de2805fe1f23bcb9f258132bb9a24facb`  
		Last Modified: Tue, 03 Jun 2025 13:39:15 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5b98d313448c218e6c16ae140b98cce2c4f662cb32ed291ce3e1a438e2d19a`  
		Last Modified: Tue, 03 Jun 2025 13:39:30 GMT  
		Size: 296.9 MB (296868926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:e9ae94703ef317a13556ef65806accf2b8279b57defc4049f6ad92fc2aa1e0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12732833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0050b0e8aa5d356c8102f207edbb77e48065ab4048bea836abc7de66a83eb854`

```dockerfile
```

-	Layers:
	-	`sha256:20cd57d5db06005dd291364144ea49a06c6fbc6dbab265547edcc823b914fc6e`  
		Last Modified: Tue, 10 Jun 2025 01:23:21 GMT  
		Size: 12.7 MB (12714692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604155a008cd0801643987b7f004c8ce97cdadee3c6d73cae78639d3921dfb17`  
		Last Modified: Tue, 10 Jun 2025 01:23:22 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:8f622845f4e9a7e9e4d30d53ff3e082b479298e67758105acfa8a6454d9fcc8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.3 MB (358348097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90adb491f5e7f587c37ceba90f9397199d1e56411e9210610828a687253c6dd6`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Apr 2025 18:18:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1747699200'
# Fri, 11 Apr 2025 18:18:21 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Apr 2025 18:18:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV R_BASE_VERSION=4.5.0
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3f6b3f3a36e322107da5dfb855c52cd71df93c73a06d6a82855f69268b41d80f`  
		Last Modified: Tue, 03 Jun 2025 13:47:32 GMT  
		Size: 49.6 MB (49618291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5edf3a78a9d41b952d672d8b1b6fb41d1df8bba6673afc8d982d66a030be55`  
		Last Modified: Tue, 03 Jun 2025 13:47:27 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5e8f8f70c19a37c754af2af25cb1b7b85e4c46094fe925a7f1b57c55ef1b82`  
		Last Modified: Tue, 03 Jun 2025 13:47:31 GMT  
		Size: 26.8 MB (26798772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1753d25fda0059d0d674127cf8a10eb7c1df53bf2d668cb9396a409c6dd46ba`  
		Last Modified: Tue, 03 Jun 2025 13:47:29 GMT  
		Size: 868.5 KB (868484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193f4c5614d1cd81ac9d7fcbe31b29e125174e9980288f26c14d827f96075d4b`  
		Last Modified: Tue, 03 Jun 2025 13:47:31 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9188e7cf4bceceeae7839b52df4a7761487e8da6b5b0b23a72d592986a33ad3`  
		Last Modified: Tue, 03 Jun 2025 13:47:49 GMT  
		Size: 281.1 MB (281058887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f2d90d6c1f2e445dd1237a9d136fe6649f1f73c80752103e3cd8580c4320c6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12831681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b7a7975e9dccee9010f9720801102a2aa7f99f0358a4575742a6025020798e`

```dockerfile
```

-	Layers:
	-	`sha256:cda099e36c67ae117e5464c4f66f744b6afde5956b0f8b320d068ce71001b816`  
		Last Modified: Tue, 10 Jun 2025 01:23:31 GMT  
		Size: 12.8 MB (12813400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa74459b14a341a80d64e1e15bfbdd13e0dba2d62065bc0fc97ad440189164b4`  
		Last Modified: Tue, 10 Jun 2025 01:23:32 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:6febf8acb18d6df46468a7910740ef8c15607528a30d268ae727c289ff20664d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368746393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7849cc2e8f0cafd13afec567c819f8e5f309475fcfadea827430143e578a68d0`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Apr 2025 18:18:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1747699200'
# Fri, 11 Apr 2025 18:18:21 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Apr 2025 18:18:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV R_BASE_VERSION=4.5.0
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6a533743cd8d66e1407986affbdb4273987e0e3aa7905a4809596a56ecaf2568`  
		Last Modified: Tue, 03 Jun 2025 21:24:01 GMT  
		Size: 53.1 MB (53080541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c217be23c8dc27881068855f24dae1d8271709202e4196c4063649913f43f4c9`  
		Last Modified: Thu, 22 May 2025 07:07:25 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f213e2f0c9e64380b0e36a339d808108205d861ef7acfa11337d13e22de2de`  
		Last Modified: Thu, 22 May 2025 07:07:26 GMT  
		Size: 27.2 MB (27164555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5015b665a8b6cf5491866b986465f30ee516176ac4ed1ffcff7194ea4e7a5185`  
		Last Modified: Thu, 22 May 2025 07:07:25 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1ac6f8f683e6733eed24ac56ae9181ba36af2b4d0aa179d8162191956110c1`  
		Last Modified: Thu, 22 May 2025 07:07:25 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96690a978809bcbeae3f6742a4657b33876634b0b867b89fa3ec848adb2b2c91`  
		Last Modified: Thu, 22 May 2025 07:07:55 GMT  
		Size: 287.6 MB (287629144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:19734d36275b6055b2e3bf34e761dfdc8b97fd01e9efe6f19d83190e28f9f29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12735596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e686a4e9f45103a96b7d039469db69e7cbebd1c0e25e47a51f461ba8af746a1`

```dockerfile
```

-	Layers:
	-	`sha256:cd4cf0c8594f81ce95d98ab28de8d033a976d6b7516b1f9ab4cdbc24393541df`  
		Last Modified: Tue, 10 Jun 2025 01:23:40 GMT  
		Size: 12.7 MB (12717415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620476c6ddb40f221a0f04fbbc458a629eb848b87bbf20e401d1d68ea0b8d72d`  
		Last Modified: Tue, 10 Jun 2025 01:23:41 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:003d38110d87a92bbcc280106271d0a02d1e75fc25f40d3d2f66f42c68829fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.4 MB (340416747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc7364a6db22c251f469ccbe4c71cb83fa4942eb8c0d844002b35d2e8d94215`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Apr 2025 18:18:21 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1747699200'
# Fri, 11 Apr 2025 18:18:21 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 11 Apr 2025 18:18:21 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 18:18:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
ENV R_BASE_VERSION=4.5.0
# Fri, 11 Apr 2025 18:18:21 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Apr 2025 18:18:21 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:8c7c5c720e3ebad3a2e1fa96d133e48b73226c9ee75449abcbd73a5d7a88ef3e`  
		Last Modified: Wed, 04 Jun 2025 22:26:45 GMT  
		Size: 49.3 MB (49322225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6743a885668e775252237c53eb38600d52f7a1446cebd3219196d48ac193e2`  
		Last Modified: Thu, 22 May 2025 00:36:38 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f45afaa31e6ac545b598a360fb34b65d009c8742906a55f6b575bd8ee627dc`  
		Last Modified: Thu, 22 May 2025 00:36:39 GMT  
		Size: 26.9 MB (26866331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c85ff86267f02ad2ae03ab6db9716d9583b77d00fba7c7e3e45bb51fce1f1`  
		Last Modified: Thu, 22 May 2025 00:36:38 GMT  
		Size: 924.5 KB (924543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ecc69e9eb00ccb3847f96874601493167a8f16b443f2a27ff0119a0a9e41f4`  
		Last Modified: Thu, 22 May 2025 00:36:38 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1bcb70aa3add52ad0345fb5b68f963e17bc61a24dbe53e31cbb9103115dbff`  
		Last Modified: Thu, 22 May 2025 00:36:44 GMT  
		Size: 263.3 MB (263299989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:6f902732eea181aaee01e8884cbad1b1d683bb17d1799f8c395818b30a902221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12541102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d059e503f4096a9986b098bae3fbefab52e257f67bb408b6521988baf61135d`

```dockerfile
```

-	Layers:
	-	`sha256:37959b8e1100dcf5ab52c0c7cdb658f88d895a191b9296d5daae1612ea6ee4ed`  
		Last Modified: Tue, 10 Jun 2025 01:23:51 GMT  
		Size: 12.5 MB (12522961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c0bce93dd43cb1959c53b0598c619cfdeacfadee2de15ed3822d1909348018`  
		Last Modified: Tue, 10 Jun 2025 01:24:04 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
