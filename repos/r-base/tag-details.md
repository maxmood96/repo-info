<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.4.1`](#r-base441)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.4.1`

```console
$ docker pull r-base@sha256:8ad7b8d30361618a0716c6510e6188364a7039e1554fb16994cd004473993afa
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

### `r-base:4.4.1` - linux; amd64

```console
$ docker pull r-base@sha256:d4a6c9d9bd4f60958392bb619d3fac438342ec3a68a5fac1bd18f82ab47a550f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.2 MB (369217450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42279fff3881e232cd62b4404e798e200351e178a3c28d51dc7ec14323c1e2d`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:619723247570b0124cdbdcd330640fb9768a7a0580fcd6674fc64a59361d9b61 in / 
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
	-	`sha256:082e67d038aa34d78979422af7626a1fa8594a4afa81d6465c09f9626234451e`  
		Last Modified: Tue, 23 Jul 2024 05:30:14 GMT  
		Size: 52.8 MB (52821221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63019cb4f70083a8f6d226b3cb6b35e512b6d9bc9f21c75b4b09706b8b2e6e04`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ca2ee447c3a44bbea026d515e3b4159734b453198ca151245de106d6c224f`  
		Last Modified: Tue, 23 Jul 2024 06:21:05 GMT  
		Size: 29.1 MB (29061492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a5cc0c1d108990afeb7e8cbd404eaa149bbc727ccaf00edbc4c5c2f9ca28de`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 866.7 KB (866721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783363ecf354c92210593d9bd224ea37737492a6de08f85de1891f440f47ebd6`  
		Last Modified: Tue, 23 Jul 2024 06:21:05 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaf50c4513920e5b062b36cb655b72263b9ae9faf08f0a6ed807800351647a3`  
		Last Modified: Tue, 23 Jul 2024 06:21:09 GMT  
		Size: 286.5 MB (286464356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.4.1` - unknown; unknown

```console
$ docker pull r-base@sha256:5aebc8fc541776daafb37895b17217cbe27ea19afd59370da2076cca5074f8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12436910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bf82f5e866d43a4d058a685f7ab6080e20d6927ebaf0120c0474c6b4279e5d`

```dockerfile
```

-	Layers:
	-	`sha256:5e013cf08cf1d927c7aadc5ff98b5776545df40c7b8a80fa939d0ef94627c5bd`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 12.4 MB (12418981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d9310389ff18be48145aed662eb549780762ae472fe3eaabb403a27ed2ed30`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.4.1` - linux; arm64 variant v8

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

### `r-base:4.4.1` - unknown; unknown

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

### `r-base:4.4.1` - linux; ppc64le

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

### `r-base:4.4.1` - unknown; unknown

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

### `r-base:4.4.1` - linux; s390x

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

### `r-base:4.4.1` - unknown; unknown

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

## `r-base:latest`

```console
$ docker pull r-base@sha256:8ad7b8d30361618a0716c6510e6188364a7039e1554fb16994cd004473993afa
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
$ docker pull r-base@sha256:d4a6c9d9bd4f60958392bb619d3fac438342ec3a68a5fac1bd18f82ab47a550f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.2 MB (369217450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42279fff3881e232cd62b4404e798e200351e178a3c28d51dc7ec14323c1e2d`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:619723247570b0124cdbdcd330640fb9768a7a0580fcd6674fc64a59361d9b61 in / 
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
	-	`sha256:082e67d038aa34d78979422af7626a1fa8594a4afa81d6465c09f9626234451e`  
		Last Modified: Tue, 23 Jul 2024 05:30:14 GMT  
		Size: 52.8 MB (52821221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63019cb4f70083a8f6d226b3cb6b35e512b6d9bc9f21c75b4b09706b8b2e6e04`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ca2ee447c3a44bbea026d515e3b4159734b453198ca151245de106d6c224f`  
		Last Modified: Tue, 23 Jul 2024 06:21:05 GMT  
		Size: 29.1 MB (29061492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a5cc0c1d108990afeb7e8cbd404eaa149bbc727ccaf00edbc4c5c2f9ca28de`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 866.7 KB (866721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783363ecf354c92210593d9bd224ea37737492a6de08f85de1891f440f47ebd6`  
		Last Modified: Tue, 23 Jul 2024 06:21:05 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaf50c4513920e5b062b36cb655b72263b9ae9faf08f0a6ed807800351647a3`  
		Last Modified: Tue, 23 Jul 2024 06:21:09 GMT  
		Size: 286.5 MB (286464356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:5aebc8fc541776daafb37895b17217cbe27ea19afd59370da2076cca5074f8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12436910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bf82f5e866d43a4d058a685f7ab6080e20d6927ebaf0120c0474c6b4279e5d`

```dockerfile
```

-	Layers:
	-	`sha256:5e013cf08cf1d927c7aadc5ff98b5776545df40c7b8a80fa939d0ef94627c5bd`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
		Size: 12.4 MB (12418981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d9310389ff18be48145aed662eb549780762ae472fe3eaabb403a27ed2ed30`  
		Last Modified: Tue, 23 Jul 2024 06:21:04 GMT  
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
