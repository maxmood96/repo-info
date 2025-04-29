<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.5.0`](#r-base450)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.5.0`

```console
$ docker pull r-base@sha256:7fdfc0aba1aff5374e19e31fd0f16d11a86e83a65c5ce7485b9d3062636d876c
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

### `r-base:4.5.0` - linux; amd64

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
		Last Modified: Mon, 28 Apr 2025 21:08:31 GMT  
		Size: 49.2 MB (49248241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24a0c0353042563a8461a2e88770df812545be5bf865cfe4b438b450e04a1e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:18 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f7cf404813c9a8a5dd85f839b610121ff2e54b52d1c87036d2b051a686d54`  
		Last Modified: Mon, 28 Apr 2025 21:55:19 GMT  
		Size: 26.9 MB (26888780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8b192ea797887c620f901aeabb49ff3aa52c9eb1be5515ee1a8b58a8df5363`  
		Last Modified: Mon, 28 Apr 2025 21:55:18 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48707abf8354c01ce5f82f8fdbddd730c0cadf92b91979724c8b886b9f873436`  
		Last Modified: Mon, 28 Apr 2025 21:55:18 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391b2048fd61f0a0aa2ce9ad974cb1f99afc5e19ef7a56b1db9b17f7dfebc54`  
		Last Modified: Mon, 28 Apr 2025 21:55:26 GMT  
		Size: 280.3 MB (280313027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.0` - unknown; unknown

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

### `r-base:4.5.0` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:524070b252875866c5a9c4aac35f365eee0098585dfbc82618a4b30d11169244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.7 MB (343697170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918df4be04c40c8c4ef736e6856e81b6cbc891871e2c67b5328432c8d60724da`
-	Default Command: `["R"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1743984000'
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
	-	`sha256:9c4cb0c74a61b785b62934a6d6fd4ab95b7ed41be5718849de5c3a44f7208065`  
		Last Modified: Tue, 08 Apr 2025 00:25:28 GMT  
		Size: 47.9 MB (47922424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65641f9f54f40d999da9f9e0e0db7c3168058553956071fee9af295055f6a46`  
		Last Modified: Fri, 11 Apr 2025 21:12:05 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100ab83beb75ed90f30645c83a950dbb23936da710e5e4b3b8b9fe8a00bdc8e9`  
		Last Modified: Fri, 11 Apr 2025 21:12:07 GMT  
		Size: 30.7 MB (30654511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef6425ed6b2177fedd59267667e72e58f69b50b568803c2bc3e08710ebd11eb`  
		Last Modified: Fri, 11 Apr 2025 21:12:06 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070075f617b377b3bca8ca58a6722fee9f39477e6131a55fb891d844bb1d241c`  
		Last Modified: Fri, 11 Apr 2025 21:12:06 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2741417242b1e31d9dd85f9ef5ac09d95149c91d92e27d37c9a36f455b3743ee`  
		Last Modified: Fri, 11 Apr 2025 21:12:12 GMT  
		Size: 264.2 MB (264248086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.0` - unknown; unknown

```console
$ docker pull r-base@sha256:ebdae926c0b5e9b792ad0600467b471b06339093947fb517b6e909275f4f1df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12722973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661cbc4b9c0afece8831f24ad1c6b93c500635e272848035fdd2d5661279fde8`

```dockerfile
```

-	Layers:
	-	`sha256:772456c4ea8865b9a19f2ec6c834d5e18f51cbc0e14c5021ca9ff957121f3d8e`  
		Last Modified: Fri, 11 Apr 2025 21:12:06 GMT  
		Size: 12.7 MB (12704692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fada660ea40d1d95f51b98553eb09bb3045ef5e0f879d0461304d479ec218e48`  
		Last Modified: Fri, 11 Apr 2025 21:12:05 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.0` - linux; ppc64le

```console
$ docker pull r-base@sha256:70ccbe103ea683abe93632729c75229bd03e1e29094b4372f11b767e7b1a60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 MB (352873477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe0dbadf6249e8a8b6a9ce0ff9fad58cf53cb1f58b88e1dfe6dd0411e6ebd9c`
-	Default Command: `["R"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1743984000'
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
	-	`sha256:94af65771ef5ac9ffd033a7f6e815eb76cbf2f6d30662a8ee31535fe2e877af3`  
		Last Modified: Tue, 08 Apr 2025 00:26:28 GMT  
		Size: 51.2 MB (51205081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd1bc3bc37bf3186d5e902f7a518d0bf35717f452e4cd0ba1b3142330bac9f4`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7145d40106fb401dea44aeb46892c95726cdf61c8a68e766e3801bf579cd06a`  
		Last Modified: Fri, 11 Apr 2025 20:45:14 GMT  
		Size: 30.9 MB (30885971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da407ab06e695749a9529c07eceb917e5c0a2002cb5f481497b2c8897f21f46c`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398a784d24729b5ffce1d8c1a9d0f0ce9ef1878ece4d5ecb2d3f1c572af5d9f7`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a7dc33b44df48d88a97a6dd47e6d2966150fa8d9417343d2d459e7e8e6ee2e`  
		Last Modified: Fri, 11 Apr 2025 20:45:21 GMT  
		Size: 269.9 MB (269910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.0` - unknown; unknown

```console
$ docker pull r-base@sha256:e234faadc4714f8490d1542d567c7728af874ef754f7c4ab239a2acf696bf5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12625387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf7297d9bee6944697630ffa359de3341609442dbfe64f9fe4e967a5707f128`

```dockerfile
```

-	Layers:
	-	`sha256:0d251be70af51f8526a025b0f4025c0767032a4063ba2e996f92f8e8dd66753b`  
		Last Modified: Fri, 11 Apr 2025 20:45:14 GMT  
		Size: 12.6 MB (12607206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14deaf896df33b97145024f7e527340fa5f28a806407f8cef5519bec18e712f0`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.0` - linux; s390x

```console
$ docker pull r-base@sha256:bdeac5f48fa5c573cb54e969fbe8a1d50ade286ed781dc88cadd106c26b4d54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325671966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbc78a7f6f74584e16f5f3556b436a9482b4dde1f6610e4836ed8c3d8c0f2e7`
-	Default Command: `["R"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1743984000'
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
	-	`sha256:48a40651234402db43f1c969ef6cb47f45fce4911e1b97bd34c6c3560c0dbe3a`  
		Last Modified: Tue, 08 Apr 2025 00:26:20 GMT  
		Size: 47.6 MB (47577869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c167db55143fbe259f7b3ed883cbcdf0a48ff9bce493db0881cd8dcf6888b4e`  
		Last Modified: Fri, 11 Apr 2025 19:12:51 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57addaefeb1ce4cd33eda9ba4d1089b742977d847b483ad271dc32408c68d57e`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 30.0 MB (30012650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4af72354faf3ededa2b4bc1c1298685b920e62e586f339b4ee6c85786d162e`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f588160484ca2e1396694a042b8799e2dd102da694535dabbfe040bfebe656`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6324197b1aaf814935d08c12aff8c6e9d1e7f8bd6df1c4595d5a4af40646e321`  
		Last Modified: Fri, 11 Apr 2025 19:12:57 GMT  
		Size: 247.2 MB (247153240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.0` - unknown; unknown

```console
$ docker pull r-base@sha256:ad5298a7239b73e031e3c45e2ba90ec07eaf10384aa1159b7399fc7fa46c7fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12432378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656cc6e464442422307246daa629bb9a060f8660e08eacda82dbec2ca3eef028`

```dockerfile
```

-	Layers:
	-	`sha256:122fd534226a13ae34a6b62c12cdcacdb9201335e2c331eab0df98657e9529f1`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 12.4 MB (12414238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d8f9fcbe5db59720a0243a51118f9b42bac86d0b6c26c32bf377dfa7e8fe66`  
		Last Modified: Fri, 11 Apr 2025 19:12:51 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:7fdfc0aba1aff5374e19e31fd0f16d11a86e83a65c5ce7485b9d3062636d876c
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
		Last Modified: Mon, 28 Apr 2025 21:08:31 GMT  
		Size: 49.2 MB (49248241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24a0c0353042563a8461a2e88770df812545be5bf865cfe4b438b450e04a1e6`  
		Last Modified: Mon, 28 Apr 2025 21:55:18 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f7cf404813c9a8a5dd85f839b610121ff2e54b52d1c87036d2b051a686d54`  
		Last Modified: Mon, 28 Apr 2025 21:55:19 GMT  
		Size: 26.9 MB (26888780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8b192ea797887c620f901aeabb49ff3aa52c9eb1be5515ee1a8b58a8df5363`  
		Last Modified: Mon, 28 Apr 2025 21:55:18 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48707abf8354c01ce5f82f8fdbddd730c0cadf92b91979724c8b886b9f873436`  
		Last Modified: Mon, 28 Apr 2025 21:55:18 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391b2048fd61f0a0aa2ce9ad974cb1f99afc5e19ef7a56b1db9b17f7dfebc54`  
		Last Modified: Mon, 28 Apr 2025 21:55:26 GMT  
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
$ docker pull r-base@sha256:524070b252875866c5a9c4aac35f365eee0098585dfbc82618a4b30d11169244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.7 MB (343697170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918df4be04c40c8c4ef736e6856e81b6cbc891871e2c67b5328432c8d60724da`
-	Default Command: `["R"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1743984000'
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
	-	`sha256:9c4cb0c74a61b785b62934a6d6fd4ab95b7ed41be5718849de5c3a44f7208065`  
		Last Modified: Tue, 08 Apr 2025 00:25:28 GMT  
		Size: 47.9 MB (47922424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65641f9f54f40d999da9f9e0e0db7c3168058553956071fee9af295055f6a46`  
		Last Modified: Fri, 11 Apr 2025 21:12:05 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100ab83beb75ed90f30645c83a950dbb23936da710e5e4b3b8b9fe8a00bdc8e9`  
		Last Modified: Fri, 11 Apr 2025 21:12:07 GMT  
		Size: 30.7 MB (30654511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef6425ed6b2177fedd59267667e72e58f69b50b568803c2bc3e08710ebd11eb`  
		Last Modified: Fri, 11 Apr 2025 21:12:06 GMT  
		Size: 868.5 KB (868490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070075f617b377b3bca8ca58a6722fee9f39477e6131a55fb891d844bb1d241c`  
		Last Modified: Fri, 11 Apr 2025 21:12:06 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2741417242b1e31d9dd85f9ef5ac09d95149c91d92e27d37c9a36f455b3743ee`  
		Last Modified: Fri, 11 Apr 2025 21:12:12 GMT  
		Size: 264.2 MB (264248086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:ebdae926c0b5e9b792ad0600467b471b06339093947fb517b6e909275f4f1df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12722973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661cbc4b9c0afece8831f24ad1c6b93c500635e272848035fdd2d5661279fde8`

```dockerfile
```

-	Layers:
	-	`sha256:772456c4ea8865b9a19f2ec6c834d5e18f51cbc0e14c5021ca9ff957121f3d8e`  
		Last Modified: Fri, 11 Apr 2025 21:12:06 GMT  
		Size: 12.7 MB (12704692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fada660ea40d1d95f51b98553eb09bb3045ef5e0f879d0461304d479ec218e48`  
		Last Modified: Fri, 11 Apr 2025 21:12:05 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:70ccbe103ea683abe93632729c75229bd03e1e29094b4372f11b767e7b1a60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 MB (352873477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe0dbadf6249e8a8b6a9ce0ff9fad58cf53cb1f58b88e1dfe6dd0411e6ebd9c`
-	Default Command: `["R"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1743984000'
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
	-	`sha256:94af65771ef5ac9ffd033a7f6e815eb76cbf2f6d30662a8ee31535fe2e877af3`  
		Last Modified: Tue, 08 Apr 2025 00:26:28 GMT  
		Size: 51.2 MB (51205081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd1bc3bc37bf3186d5e902f7a518d0bf35717f452e4cd0ba1b3142330bac9f4`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7145d40106fb401dea44aeb46892c95726cdf61c8a68e766e3801bf579cd06a`  
		Last Modified: Fri, 11 Apr 2025 20:45:14 GMT  
		Size: 30.9 MB (30885971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da407ab06e695749a9529c07eceb917e5c0a2002cb5f481497b2c8897f21f46c`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398a784d24729b5ffce1d8c1a9d0f0ce9ef1878ece4d5ecb2d3f1c572af5d9f7`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a7dc33b44df48d88a97a6dd47e6d2966150fa8d9417343d2d459e7e8e6ee2e`  
		Last Modified: Fri, 11 Apr 2025 20:45:21 GMT  
		Size: 269.9 MB (269910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:e234faadc4714f8490d1542d567c7728af874ef754f7c4ab239a2acf696bf5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12625387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf7297d9bee6944697630ffa359de3341609442dbfe64f9fe4e967a5707f128`

```dockerfile
```

-	Layers:
	-	`sha256:0d251be70af51f8526a025b0f4025c0767032a4063ba2e996f92f8e8dd66753b`  
		Last Modified: Fri, 11 Apr 2025 20:45:14 GMT  
		Size: 12.6 MB (12607206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14deaf896df33b97145024f7e527340fa5f28a806407f8cef5519bec18e712f0`  
		Last Modified: Fri, 11 Apr 2025 20:45:13 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:bdeac5f48fa5c573cb54e969fbe8a1d50ade286ed781dc88cadd106c26b4d54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325671966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbc78a7f6f74584e16f5f3556b436a9482b4dde1f6610e4836ed8c3d8c0f2e7`
-	Default Command: `["R"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1743984000'
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
	-	`sha256:48a40651234402db43f1c969ef6cb47f45fce4911e1b97bd34c6c3560c0dbe3a`  
		Last Modified: Tue, 08 Apr 2025 00:26:20 GMT  
		Size: 47.6 MB (47577869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c167db55143fbe259f7b3ed883cbcdf0a48ff9bce493db0881cd8dcf6888b4e`  
		Last Modified: Fri, 11 Apr 2025 19:12:51 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57addaefeb1ce4cd33eda9ba4d1089b742977d847b483ad271dc32408c68d57e`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 30.0 MB (30012650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4af72354faf3ededa2b4bc1c1298685b920e62e586f339b4ee6c85786d162e`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f588160484ca2e1396694a042b8799e2dd102da694535dabbfe040bfebe656`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6324197b1aaf814935d08c12aff8c6e9d1e7f8bd6df1c4595d5a4af40646e321`  
		Last Modified: Fri, 11 Apr 2025 19:12:57 GMT  
		Size: 247.2 MB (247153240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:ad5298a7239b73e031e3c45e2ba90ec07eaf10384aa1159b7399fc7fa46c7fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12432378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656cc6e464442422307246daa629bb9a060f8660e08eacda82dbec2ca3eef028`

```dockerfile
```

-	Layers:
	-	`sha256:122fd534226a13ae34a6b62c12cdcacdb9201335e2c331eab0df98657e9529f1`  
		Last Modified: Fri, 11 Apr 2025 19:12:52 GMT  
		Size: 12.4 MB (12414238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d8f9fcbe5db59720a0243a51118f9b42bac86d0b6c26c32bf377dfa7e8fe66`  
		Last Modified: Fri, 11 Apr 2025 19:12:51 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json
