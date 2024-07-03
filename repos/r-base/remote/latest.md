## `r-base:latest`

```console
$ docker pull r-base@sha256:5c9f320ff22ccf261d4121a4f6737a1d487f53a391921ebed37608c12ef2628e
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
$ docker pull r-base@sha256:41b686a38758c502c8288c6938b25fee7ee4be8bf22724c334c5391f7ff7fa6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346768492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16511f39cdb4feed86233da87cf2ad791f99e1b78279703cdccfc8c7445a9d5d`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:e38abe5f09ca03d90c91799e2e69d68a1147a8f86ccdcdd987a89bd602110b19 in / 
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
	-	`sha256:0b5855eb0983f9340ca03ffa4e6c325cd705d287572d0eba3b70fa2461444cdb`  
		Last Modified: Tue, 02 Jul 2024 01:31:14 GMT  
		Size: 52.5 MB (52458235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eaa0d0058d44b58a67b63e3474f3660932d3b21a43a9846f5294c38db950b2`  
		Last Modified: Tue, 02 Jul 2024 03:14:50 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b44935c971fffd83f5705ad8493bf7f5eaa90ce55e4239dfca95861618f903`  
		Last Modified: Tue, 02 Jul 2024 03:14:50 GMT  
		Size: 23.1 MB (23106287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591bb1537093c88cfdcf31d2b0dcbb3cf51f50f39869f1a9ee315296b11a013`  
		Last Modified: Tue, 02 Jul 2024 03:14:50 GMT  
		Size: 866.3 KB (866328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573ae39628a2c9b0386ed3eec620824a952f77f858845000f2e20a0fd9340b1`  
		Last Modified: Tue, 02 Jul 2024 03:14:51 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147142df7a5316b0ffec0c19c0d017ae1944d2c22b7ef6f49ac8bc8966962a1`  
		Last Modified: Tue, 02 Jul 2024 03:14:55 GMT  
		Size: 270.3 MB (270333985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:3ea7af3baab349c8593154840815afa7794d8f525ea7b1c6faca1f062eb38140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12383872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7fbb7a29f6cb4638437dfcb9646e67ef95699d09dddf46f768f9b9bf097731`

```dockerfile
```

-	Layers:
	-	`sha256:e535fb9fa8c452e08efefd1b59844438bbea0caa94bb64284e107b5bce035a2f`  
		Last Modified: Tue, 02 Jul 2024 03:14:50 GMT  
		Size: 12.4 MB (12365943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b84a1d009c2e62dbe9ad54929d0371306cb43a847e1315c0030683ec868c8e1`  
		Last Modified: Tue, 02 Jul 2024 03:14:50 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:f68a4a54a15c7f17e4832a7da0f28149349799baf53231cccf6893274bbc062a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332332592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99abd27b3220fe7ec5e47ec6ab8103974677269f739425f325b155fe0a47903a`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:d903c4ae068c559394a45c9b09837213d003094120e0b425a361699336d83198 in / 
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
	-	`sha256:e58d0af417c026077a461ba61e4cfb256505119f4bd4894be8db0fecf047f618`  
		Last Modified: Tue, 02 Jul 2024 00:44:50 GMT  
		Size: 52.7 MB (52693311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290fa96c855462bd9078a25f68ed51280ea55982c4f5557b9b76874c2a629474`  
		Last Modified: Tue, 02 Jul 2024 22:46:38 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d754d694da2b5a1c87510d86beadbbad95853959f9e0099d38ea2bfc599ffa`  
		Last Modified: Tue, 02 Jul 2024 22:46:38 GMT  
		Size: 23.1 MB (23098394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e735aa47db17f7beb928bb6ec09c733172de1953e2c494f3ced63e2bc70be8`  
		Last Modified: Tue, 02 Jul 2024 22:46:38 GMT  
		Size: 866.3 KB (866327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12713eb8ed12dc30d9c1446e13c62974fe88352ce62d5c00ab767b5811243f22`  
		Last Modified: Tue, 02 Jul 2024 22:46:39 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1614c1e2666d838b14677a7aae3a4ed6ccc4e1586169b874d7d9bc5acae3aa7`  
		Last Modified: Tue, 02 Jul 2024 22:46:44 GMT  
		Size: 255.7 MB (255670903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:0dff62af27445ed0902df8e681a072dc806dacb5d2b402e64e697c4a01f177ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12486434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626882a797652e20e208001960d1c36517cd17e6e83db01e0b727733cc0df8ec`

```dockerfile
```

-	Layers:
	-	`sha256:b7e5ff5166535af1172013ce30e5c30fde05e72277272440279c999028eedb61`  
		Last Modified: Tue, 02 Jul 2024 22:46:38 GMT  
		Size: 12.5 MB (12468226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b7f5aeb5fb44d119b95cc42d50d84aa8e08c19f196dd8ed68d9cbd3b7c8c6f7`  
		Last Modified: Tue, 02 Jul 2024 22:46:38 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:2b451c82fd738269ba9cfc78907253a3ced148b230e39c6ca1172f026d3443f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344822094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76f88c911717a4cdfd043c53fceccf43792ae483a307f1b81cd1d06a20d33e4`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:7e6fd591511923e3855e4ab948bf72e13d53b13ca80fbde003a5f4db88ccf6e1 in / 
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
	-	`sha256:784dd835b92bc08b6c713559b16a29ba502fd55f92d2d87be387713feb691dc2`  
		Last Modified: Tue, 02 Jul 2024 01:24:50 GMT  
		Size: 56.3 MB (56345211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00609584585a23fca6ee8cd58e65bfabcde46357a8080af9d8fcbe5960bd378b`  
		Last Modified: Tue, 02 Jul 2024 19:48:49 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de784ea4029cbd8d6af0733b6661cce044523bba9107b4bea467836c2da156`  
		Last Modified: Tue, 02 Jul 2024 19:48:50 GMT  
		Size: 23.3 MB (23337152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db13bf2d261fb904960b5c39926dc023155ffd7f6164aa3255f8be8684c93354`  
		Last Modified: Tue, 02 Jul 2024 19:48:49 GMT  
		Size: 866.3 KB (866326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4500850a324fa26621251d6729f56023bb3a7dd49f8b361b1fd7637988c7512a`  
		Last Modified: Tue, 02 Jul 2024 19:48:50 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d0fe4c576f4f6621cd9f6671033f858c521b969f1d6f4ca4d48b82112dbf6d`  
		Last Modified: Tue, 02 Jul 2024 19:49:04 GMT  
		Size: 264.3 MB (264269741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:1715bceb1b09b04c69af1f9c9f9eeb4a9afcf19d2999158f09283a248460b87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12384484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d25d4f695fafada52a360462cf55fa8ed3d6ba743a7f95a6253e1718df0882`

```dockerfile
```

-	Layers:
	-	`sha256:86bf2408aedae2c713395cb9aeb9dfa3356e6bd1b6c0e3b4cfe750a827d4d4d7`  
		Last Modified: Tue, 02 Jul 2024 19:48:50 GMT  
		Size: 12.4 MB (12366523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:070af7e99526412c91130e0734c88637bd006160ca8d7e95d568c1b51d88a873`  
		Last Modified: Tue, 02 Jul 2024 19:48:49 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:a4f3154396948e9fe8e677bae8165960ed9d10dfff4126f294cb9bbe3be51259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317256885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d228d15c6893e0a4b6b1d1c469aa3da2003d3072fad1cd885a1f315b8d19ed`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:a3d0277ebd5e534d85f6309dd13540dcd7d838f81af596e67ff78d6b72e96db3 in / 
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
	-	`sha256:1a1a0e77f0e4b483396fe1b149e22bc15176f45180204020be0f831ea7223f9d`  
		Last Modified: Tue, 02 Jul 2024 00:50:39 GMT  
		Size: 52.1 MB (52089470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be2bb53e5e3da23d804ccf7c1262382100f19fa10760bce0229966fa9dd53a2`  
		Last Modified: Tue, 02 Jul 2024 10:10:05 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7644d3c6af965c75f10b297867acf4bc4fa4b02c1f9b12f3c70eb96bf49262`  
		Last Modified: Tue, 02 Jul 2024 10:10:06 GMT  
		Size: 23.2 MB (23216725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cdb8e6b73bf92e3d69bc0c7544fa6e8025d3214c4500bbf45d529ccbd8a585`  
		Last Modified: Tue, 02 Jul 2024 10:10:05 GMT  
		Size: 922.3 KB (922278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d331fc6463fb4e262d3b0cad3c14ce20268136df0aa187c443d18573a3dd08b0`  
		Last Modified: Tue, 02 Jul 2024 10:10:05 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec204c2c7b65224946d278d361a5457c0c915c52ef96240d068d2e1c1713e969`  
		Last Modified: Tue, 02 Jul 2024 10:10:17 GMT  
		Size: 241.0 MB (241024754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:d1017faed9eafaee2a4709f80ac748982b19acbf303ee5b9dac610c003b4257a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12192439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2884be7dd75bfedd3631b663e39d8ec2149e6159b8d12a862a8e269729c6ec2`

```dockerfile
```

-	Layers:
	-	`sha256:a2c80b91dc7e6aad6e727a96840838edca244a132135b6b3e97a1fe82f217c8c`  
		Last Modified: Tue, 02 Jul 2024 10:10:06 GMT  
		Size: 12.2 MB (12174510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08db5992541cb78e4eb412027442023ae674e84aaea65c35027de10b700b5074`  
		Last Modified: Tue, 02 Jul 2024 10:10:04 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json
