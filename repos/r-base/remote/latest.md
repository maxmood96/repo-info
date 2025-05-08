## `r-base:latest`

```console
$ docker pull r-base@sha256:c8a0e25cc45f084ae2d9d48aabd6b70bf4d1e0b89417bd21b60af3a6d2fe454e
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
$ docker pull r-base@sha256:44297207cac3465f7f3b7246a1467adeeced0f09b26c8c0dc5d0c012982ae0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.3 MB (357322194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188ab841510528d39ce8b9440751516b04e7ba2df62ce4a10e8e796029b9b8a2`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Apr 2025 18:18:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1745798400'
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
	-	`sha256:81a2166de1b8a6c47ca8fc42d672902bef240be053c9679962c5c82612b430b6`  
		Last Modified: Thu, 08 May 2025 17:07:13 GMT  
		Size: 49.2 MB (49248241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24a0c0353042563a8461a2e88770df812545be5bf865cfe4b438b450e04a1e6`  
		Last Modified: Thu, 08 May 2025 17:18:28 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f7cf404813c9a8a5dd85f839b610121ff2e54b52d1c87036d2b051a686d54`  
		Last Modified: Thu, 08 May 2025 17:18:30 GMT  
		Size: 26.9 MB (26888780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8b192ea797887c620f901aeabb49ff3aa52c9eb1be5515ee1a8b58a8df5363`  
		Last Modified: Thu, 08 May 2025 17:18:29 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48707abf8354c01ce5f82f8fdbddd730c0cadf92b91979724c8b886b9f873436`  
		Last Modified: Thu, 08 May 2025 17:18:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391b2048fd61f0a0aa2ce9ad974cb1f99afc5e19ef7a56b1db9b17f7dfebc54`  
		Last Modified: Thu, 08 May 2025 17:41:34 GMT  
		Size: 280.3 MB (280313027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:33dcf3fc5bd346c3b3abece0e4ff5852c61b4fc88bdf1e885021ff2ea41ee272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12665419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91e2ee15689608d02fb9b118623fdcfd991a7cc398a03f29513c8af43d84e0f`

```dockerfile
```

-	Layers:
	-	`sha256:bcc46d85c8ff6de41db1477b3651974cdb2fbb81df2994b8b9d40cff081fb211`  
		Last Modified: Mon, 28 Apr 2025 21:55:19 GMT  
		Size: 12.6 MB (12647278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b23345aa21e86c4c093b12a2695f8b24196898819b2d51581fe1a942f96a1ec`  
		Last Modified: Mon, 28 Apr 2025 21:55:18 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:2c1acd9aad1a9ed499d3006dbd28986d84bf54966efedc376f365ab54c1e4d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341718748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef81b5670aeed8ce304ccb44cfc33c6c0845dc6091d7a999e6f6558e928379b`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Apr 2025 18:18:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1745798400'
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
	-	`sha256:cd585a598f86b68ebbf8a5d4b616e008cafabe62249915f4d4b2cd795c5bda4e`  
		Last Modified: Thu, 08 May 2025 19:52:23 GMT  
		Size: 49.6 MB (49624120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7423dae0847149681fcd11f6653ee74ab2c03483490f55b08103d1e80c1b1867`  
		Last Modified: Tue, 29 Apr 2025 01:16:21 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa1a9a2e56a7924c6aedfcbc164396106679af348ad7befa3e25f01895e93e4`  
		Last Modified: Tue, 29 Apr 2025 01:16:22 GMT  
		Size: 26.8 MB (26794989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177143745666aca5b94ee9cbd9cc9a768e5b914dd49f101213079fb19fdc5871`  
		Last Modified: Tue, 29 Apr 2025 01:16:21 GMT  
		Size: 868.5 KB (868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f717357bf9cdc841874d3d9626087998776996639d9337e1b1ddd1dbd0a949b7`  
		Last Modified: Tue, 29 Apr 2025 01:16:21 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b12fdf1b2864d6e0db552c3c98fcda24afbd110b3fd49746153d2568c6d1b`  
		Last Modified: Tue, 29 Apr 2025 01:16:32 GMT  
		Size: 264.4 MB (264427490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f70f5c0eb1356e2bc7fc6cc7650f46f9a8d61eeea49d90cc3e66efa57451007a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12764547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c002e6328b7e21f44a921df424c539e80c9fe6bcbf67d21d631716bf9dc4e5da`

```dockerfile
```

-	Layers:
	-	`sha256:7e5329b78679b14c88292907c5ca62cfac22241606d19c9d2d687dc77d23475e`  
		Last Modified: Tue, 29 Apr 2025 01:16:21 GMT  
		Size: 12.7 MB (12746270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43394e2a1cacf11e2ac187ffa1b106756ab4ec54cfc88577ad402988732a5067`  
		Last Modified: Tue, 29 Apr 2025 01:16:21 GMT  
		Size: 18.3 KB (18277 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:af1563f3826abb5543679daebcbe928977cda30ad752af93d10e7c3b84b7597a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351270293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8fa92e4df445280272f99cdbbbc3b9fa291e30362130e70ae7a01d210ca83f`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Apr 2025 18:18:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1745798400'
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
	-	`sha256:67711a213cd6db21e47edc66a3f7a3e47bfcfbbdf5795cd3cc86d651bbd88e22`  
		Last Modified: Mon, 28 Apr 2025 21:24:32 GMT  
		Size: 53.1 MB (53072554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bf17c78a31fe7464c93c6f8b3f5f920b6f6cfa03ce843542ffe718095be4de`  
		Last Modified: Tue, 29 Apr 2025 00:14:13 GMT  
		Size: 3.3 KB (3317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbce094fb3a86f6bf6e613bfe6e3412fc7e540f07c6be8182c5adebdd508702b`  
		Last Modified: Tue, 29 Apr 2025 00:14:15 GMT  
		Size: 27.2 MB (27158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5f0165b3e00cf288f1fd4fb6e51bafda5caaaed7b638e5e76a4a918038a2d`  
		Last Modified: Tue, 29 Apr 2025 00:14:14 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fbbfdf793971f5de1c6355d680bf84b150c354011e1f91dc218a2a358c78dc`  
		Last Modified: Tue, 29 Apr 2025 00:14:14 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ff175b722644c0a4efe78e830428f89fbaf3c7905d2a3cd6a201f1fd68dd6`  
		Last Modified: Tue, 29 Apr 2025 00:14:27 GMT  
		Size: 270.2 MB (270167495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:e9bf322d661cfe2ca5d73c1c834a0fcaa2aa7ac3096f6199f510eea9b6076389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12668278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa613b20da01979a619b4e9777fc55fce022322049b1dee0ff9f99f06ee82a0a`

```dockerfile
```

-	Layers:
	-	`sha256:a32e342bedf12464725ca4ef29f6b57259e9ea9765826e5f6d11ea92f514c1dc`  
		Last Modified: Tue, 29 Apr 2025 00:14:14 GMT  
		Size: 12.7 MB (12650098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848934e8ec3056a998d275fd27db849ec14fbf465a43abf1a45aa6cd1f85eb06`  
		Last Modified: Tue, 29 Apr 2025 00:14:14 GMT  
		Size: 18.2 KB (18180 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:291cffcf2f6e09df48b0db489b90985cc60004ad3c2665a77e5fab0c3dffe5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324498187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f495ed3cd56ee6aa636af753e56d9c60883b112f2ec70af79c8bd7101ad8247a`
-	Default Command: `["R"]`

```dockerfile
# Fri, 11 Apr 2025 18:18:21 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1745798400'
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
	-	`sha256:d4ab3e6572bea3b078c2a6787cf3018667d7707d0c4f8e274cb5e037f896fb4d`  
		Last Modified: Mon, 28 Apr 2025 21:10:21 GMT  
		Size: 49.3 MB (49316648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1270e1b37cb9ff8ab1c3629873fc9ae90fe07347f33dea7a72d46b876b8528c8`  
		Last Modified: Mon, 28 Apr 2025 23:46:52 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdc855f0a9af31e12b187ca0a62865f738b6b4a570e48142faaa3d4ae8d2f23`  
		Last Modified: Mon, 28 Apr 2025 23:46:52 GMT  
		Size: 26.9 MB (26873505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa2b3e3219b2f3725d8a5e8cbac1ee3b7da7fa264e281a70b43d5ae5d8929b`  
		Last Modified: Mon, 28 Apr 2025 23:46:52 GMT  
		Size: 924.5 KB (924542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac3fee3a637feca14c22b1a18f18ff130cea68092c4ef1f15f6b912f2de1eae`  
		Last Modified: Mon, 28 Apr 2025 23:46:52 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb683e6cad439cfc7bd590d1dfb1571892eb8dd10eaf5cec7a2170df23d5ea9`  
		Last Modified: Mon, 28 Apr 2025 23:46:57 GMT  
		Size: 247.4 MB (247379834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:5af433bf8fbd641416c5e144bd22338d41a2b54f32424fed43643e18a6bdde0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12475221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9671fcd6232370bd6269016334bce451787b00a69cf4b495b4209b4c71edac`

```dockerfile
```

-	Layers:
	-	`sha256:23f988715d064805b7a6729bfc428902d38193435588ba0fb30312ccf00eb4a5`  
		Last Modified: Mon, 28 Apr 2025 23:46:52 GMT  
		Size: 12.5 MB (12457080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d8efb3cd372de26a7b7c22066d1515777b420ae0dea92faa942720b39e2b45`  
		Last Modified: Mon, 28 Apr 2025 23:46:52 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
