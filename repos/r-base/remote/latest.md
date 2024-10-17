## `r-base:latest`

```console
$ docker pull r-base@sha256:e7032f2f6fd273ee944a717b436bc66d1a89b1b90a9bbcaafcf1318d68a7d8b2
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
$ docker pull r-base@sha256:498a8b27aeb8338860074cdd8da46c4bbbe423c569502b237e737a3f622cba80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.4 MB (356361011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f983d0e3c9bfa164dc2cd2162c68a53281a490b6c03b3f068e6088f34f50540`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:7cd25c47cea2c8bd0960e59bbb70e07523a0cf45c77c330ba29dd0040fd2ae3a in / 
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
	-	`sha256:bfa02bb5331e16713de983c8b0601bfcd284f32c36808d948bf38003dcc2a65a`  
		Last Modified: Thu, 17 Oct 2024 00:26:18 GMT  
		Size: 53.2 MB (53238722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fd1aa252a44ac7174af140e797002035f132e610f1c7bba5f9b44472334678`  
		Last Modified: Thu, 17 Oct 2024 01:27:38 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19260f24f2bf372f53e3f199d460775976a361cf5edb7aebab326a3e0e414a0`  
		Last Modified: Thu, 17 Oct 2024 01:27:38 GMT  
		Size: 23.2 MB (23164060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60c96a7b22f4ed5e3832ed948db91acd1d80379ca673268fd6d391bda353ba7`  
		Last Modified: Thu, 17 Oct 2024 01:27:38 GMT  
		Size: 866.8 KB (866751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd901c1ea3dfa35e85e78a321400b2e34b35c581599319ada63c3bafe8d9e055`  
		Last Modified: Thu, 17 Oct 2024 01:27:39 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5afc86683fe279970514283cc8382ff66dcc46917cc84f84bef5d2e9e3817c3`  
		Last Modified: Thu, 17 Oct 2024 01:27:43 GMT  
		Size: 279.1 MB (279087825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f591fd18e8da70aa12e929500d831f2d25d42a74539b0a9e57a418a321d1f861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12541293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00627407bf638d1b0c2fbde09f51605b536698837f17fd68ced3e9a9f8ed0d79`

```dockerfile
```

-	Layers:
	-	`sha256:26c018556de2fc4511b8aedde5f1a9d8fdf4871708cd37ab9cefb5856d8bbc98`  
		Last Modified: Thu, 17 Oct 2024 01:27:38 GMT  
		Size: 12.5 MB (12523326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7dd3042ceedbdc78f81d2e7d451e7df7fd1f2afa5fa05faf10b29416956a69e`  
		Last Modified: Thu, 17 Oct 2024 01:27:38 GMT  
		Size: 18.0 KB (17967 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:0004972ec01b6a77dd1b4553a83fcf59f456f4b70825a14c22a6bf55b8092313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341768784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246df9f3d858a090b2d58f805313a9e180d0a88fa6ee8f51808e0eb30ed5a24c`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:e3e9f477c791fc688010cc87eaedfcd80ede2cdd070c953518b515ed1b668a55 in / 
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
	-	`sha256:a6d8e57ff3309f685dd823e43fca05a8da4dba501d2eae9451a046edaeaca8d2`  
		Last Modified: Thu, 17 Oct 2024 01:16:49 GMT  
		Size: 53.6 MB (53599758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dc4246dcdf0dd488a4fd0f50af65577ec29c3023d2a8f5c447fe9abf707853`  
		Last Modified: Thu, 17 Oct 2024 19:56:09 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633c0b67085aa42cef6de6b0ba5fc104066d1810ee8bd4e3864d69e54150bb8e`  
		Last Modified: Thu, 17 Oct 2024 19:56:10 GMT  
		Size: 23.1 MB (23149898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2009aa12eb6cb7bcd731e06996a796754a08e2f7bf40b30dea00c29d6a783372`  
		Last Modified: Thu, 17 Oct 2024 19:56:09 GMT  
		Size: 866.7 KB (866741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f4dce706113cd7aeae4ba94d51f49176f39de1cc6ca66c32854c65fd3ddd65`  
		Last Modified: Thu, 17 Oct 2024 19:56:10 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175d6a49f5674eabd57649259b51838a3526a05ac759cc5781b3f09e15219c1d`  
		Last Modified: Thu, 17 Oct 2024 19:56:20 GMT  
		Size: 264.1 MB (264148728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:2f6e6189ab2bb6e600a80a3019973eba08b44ef7e0885f4310c8a783294db016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12637251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f9ae8978434028d685290e8ab3b2fde1dc7a77903dcf443744c08e3a3b3a7f`

```dockerfile
```

-	Layers:
	-	`sha256:01d193a740f7bde9cb14df00f685d13e3c0813967c80e3044f2fee9368abc93a`  
		Last Modified: Thu, 17 Oct 2024 19:56:10 GMT  
		Size: 12.6 MB (12619150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c11ab29c3153589d0bb84a968aebc3f40ed6c2722364920350b1fd07a195d7`  
		Last Modified: Thu, 17 Oct 2024 19:56:09 GMT  
		Size: 18.1 KB (18101 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:20e3c0703706b56b050edc50f857d79b3e8cb67740e537716e09699573a18900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351052328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487b01a4bf7ee2b716ad0d85a90c816425a91a5e13d576f147ecef3d4fe5ccc4`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:5c4544ac0d27b357afba9feb379224b111f7149e7b3f21fe35317eef03b8bcea in / 
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
	-	`sha256:311042d460227ad120f24056ab56c7fe2202f03f09ec22ed4f93b2ffc0adb201`  
		Last Modified: Thu, 17 Oct 2024 01:23:20 GMT  
		Size: 57.1 MB (57126660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0250a3c713f31fd8ff33eee72c3a3342149bb0abe9e775f288c5cab174cefc`  
		Last Modified: Thu, 17 Oct 2024 13:14:31 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39123bc9ea86ea56f4e4873bd96d8f90ea8b86bfaaaa1c67dd6c9a6678eaccb`  
		Last Modified: Thu, 17 Oct 2024 13:14:33 GMT  
		Size: 23.4 MB (23390118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830bc954c8f43b9b5288d9ff31078908bb95d0e6768fb83f8b364457ec75016a`  
		Last Modified: Thu, 17 Oct 2024 13:14:32 GMT  
		Size: 866.7 KB (866743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c28998189653367271f338a188d22e4c53ecb118c8f1629ac238d326a51a80`  
		Last Modified: Thu, 17 Oct 2024 13:14:32 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79644c0ff15fa253955c4b7445525c9dd824e1c18a13ee535b84f68ce43be585`  
		Last Modified: Thu, 17 Oct 2024 13:14:40 GMT  
		Size: 269.7 MB (269665143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:07691912ebc7636f2130715812cea739e874e4a10b6ce8340a750063b279e52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12535989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5ba93b7285fb35a637c372a7f80c66d7d3159890ee7350c1a6277078bcc494`

```dockerfile
```

-	Layers:
	-	`sha256:a2c5351fda4709ead4dad5489404d2fdb0669a188f1e2512decfd4e72e162b7c`  
		Last Modified: Thu, 17 Oct 2024 13:14:32 GMT  
		Size: 12.5 MB (12517988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cde339cd8c18f1307a8c0b3ecc3664030bc2beba84f0283d5b43f71d7ea612d`  
		Last Modified: Thu, 17 Oct 2024 13:14:31 GMT  
		Size: 18.0 KB (18001 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:7eeff02f1fcece564c0f448d7a22d895ee632c51366594225c077fb87962de8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323266590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56892f0a7024194715db1e280d5d66826274046eaa92784b4294d472bb90a3e7`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:61f096f81ed7cfc876be4edad4438e9e9e439382507d192f09f51c428e99a482 in / 
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
	-	`sha256:f66a11769d6242f4b78b255eed3607d4c3b4b3fa3e8fb47724dd3586e9a6da4f`  
		Last Modified: Thu, 17 Oct 2024 01:51:31 GMT  
		Size: 52.8 MB (52808853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c5822f106b60c857dffe73b2f1c51c848146e97e2c6fa8383d06e82f4b04fb`  
		Last Modified: Thu, 17 Oct 2024 17:49:25 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3747c2ae4ccc7bab30fd98f22984b842f642e80340592f4e58c49b24649220c`  
		Last Modified: Thu, 17 Oct 2024 17:49:26 GMT  
		Size: 23.1 MB (23118360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e03c048bf1bd2738f911af1cb851972415bf16e5da5251147c0006c6a1a282`  
		Last Modified: Thu, 17 Oct 2024 17:49:25 GMT  
		Size: 923.5 KB (923488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64eaadba936bf7c2eb02852c13e890afc1fc976f5b92ad6dffdc76d65adad75`  
		Last Modified: Thu, 17 Oct 2024 17:49:26 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12f8f12dd044417cc98dbe0aeeece3a1ce2f0206679b8576a911662a572071d`  
		Last Modified: Thu, 17 Oct 2024 17:49:30 GMT  
		Size: 246.4 MB (246412233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:ebed7c7719ef59300a42541d8be4117e535e977b9acd5ca00fe3697f17e51ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12343203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e239ac90b251f98f328605bd308d99ac7aaa530794db31e8d5c4f1b5c8df69c`

```dockerfile
```

-	Layers:
	-	`sha256:82d8797fd79892634fc9fcf3e71c611dbe2a57f0045b3148c468718a40a8e7fb`  
		Last Modified: Thu, 17 Oct 2024 17:49:25 GMT  
		Size: 12.3 MB (12325236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb935a568e9dee8bed476461729da8124ce964d13e8b03e38b605e524564f086`  
		Last Modified: Thu, 17 Oct 2024 17:49:25 GMT  
		Size: 18.0 KB (17967 bytes)  
		MIME: application/vnd.in-toto+json
