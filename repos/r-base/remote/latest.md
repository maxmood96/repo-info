## `r-base:latest`

```console
$ docker pull r-base@sha256:b5a6c333a61afc0fb92f707a49138d56be8af256d64eb1d91031aaa43331a4d6
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
$ docker pull r-base@sha256:48b795821b53ce25891ae643ce384cbacdbc6a6fd561092e23699ae57cab9ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352547718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a9fb76a7d3e889b89b50cb577544985fbf3ee8025acb0407c28e710503e57`
-	Default Command: `["R"]`

```dockerfile
# Thu, 13 Jun 2024 01:23:10 GMT
ADD file:641543c898704e70b2f0fdc6960cf28865c10fff8d9e502bca973f3032f48ee5 in / 
# Thu, 13 Jun 2024 01:23:11 GMT
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
	-	`sha256:86f6cd73387be605d114f6a6b93a5a5db028ff60a33da4e42acb4d10aa73746f`  
		Last Modified: Thu, 13 Jun 2024 01:29:06 GMT  
		Size: 52.3 MB (52277771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc3f58ae08f09664e56165bdaea49040ce9d1547211fbd64e1be83681663c38`  
		Last Modified: Mon, 17 Jun 2024 17:54:36 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf448164e2c6240d5d28dda6d99323d154f72b9fd1e503eb25000f28ab8182ed`  
		Last Modified: Mon, 17 Jun 2024 17:54:36 GMT  
		Size: 29.1 MB (29086519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a42572e9d9df5f8fb1919130714054584298a057bfddc354947a5812d6e6dd6`  
		Last Modified: Mon, 17 Jun 2024 17:54:36 GMT  
		Size: 866.3 KB (866327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fded07a8bd9fd62a0f2d4bab85c55195d7e1a0e188781677bbf5ffe11b6140`  
		Last Modified: Mon, 17 Jun 2024 17:54:36 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e6e0dbf1b05f53027d677b21d6d14252342ee43009a12ea656809e7ad9838c`  
		Last Modified: Mon, 17 Jun 2024 17:54:41 GMT  
		Size: 270.3 MB (270313438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:069917195fec5a808f40c82e06cdb2b1253013bf3bd61e6cca6b0e5a68c38f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12356850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbfa7128bc320f3125fce122949304a55620b93d52b661f78b3e18d0dcb3fe8`

```dockerfile
```

-	Layers:
	-	`sha256:d47b642144ce817ee3215e699c0404893bc873c3ea0e7019cfc55fcfa83b872a`  
		Last Modified: Mon, 17 Jun 2024 17:54:36 GMT  
		Size: 12.3 MB (12338921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb41b0bb7f9a1a87d3c54eb28c382a2c02812a3a412f577a3ddc4a07f3577944`  
		Last Modified: Mon, 17 Jun 2024 17:54:36 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:53b1183a3aee3c4f7661715ea5050c4349364dd5506ee3b9ac72c8e7d99ff6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345813855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3950044fc3112196004266c229053d74e15265c2062f80b27b62f055eb78d0`
-	Default Command: `["R"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:20 GMT
ADD file:01c0f4d76bf24fca2751abe72efa9c7df45d0b92b1a1e4ec04166ae4f86e0e5e in / 
# Thu, 13 Jun 2024 00:41:21 GMT
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
	-	`sha256:bf8309700f9bbb327bede604070aa78243b4af661147b0f82fa09c9fee807790`  
		Last Modified: Thu, 13 Jun 2024 00:46:35 GMT  
		Size: 52.5 MB (52514403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600a4a7abde0d128b958ada7041967bf0bc7e8d1c421fd211cd3dea7299f6de1`  
		Last Modified: Fri, 14 Jun 2024 01:15:31 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2c2a2f75707bb2fecc7c06b17c1926d2f32a79b0dcd205287589b1dbf042c`  
		Last Modified: Fri, 14 Jun 2024 01:15:32 GMT  
		Size: 23.1 MB (23088718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b41e3af61026d979c57a33df77d062b4c047302f92a0c9360f95da0219ffc5`  
		Last Modified: Fri, 14 Jun 2024 01:15:32 GMT  
		Size: 866.3 KB (866328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a285d402501daaa7ff64921613e8190d86dd9a3b4541ccc9d2034cbc8778d25`  
		Last Modified: Fri, 14 Jun 2024 01:15:32 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fcfc2b64b53fc5a1553ca6dab8f2a81b4a271586c5eb1f0eae4689ec47aba0`  
		Last Modified: Mon, 17 Jun 2024 18:40:43 GMT  
		Size: 269.3 MB (269340748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:d27c4582b1cf41b59639a8c3c02bca697d0eb2f4e82f90f04ef8db63f046f24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12402660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a82279c6ecb906e12d836deadad0321c81b264c57702881efa5772be40ebd5d`

```dockerfile
```

-	Layers:
	-	`sha256:786b5ca98202bd5442230e7838317bf0befc89dac808900facd4034e0cf316b3`  
		Last Modified: Mon, 17 Jun 2024 18:40:37 GMT  
		Size: 12.4 MB (12384452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e695436365cc047ea38c44a7319ecb9881cb65fc64abdf6ab52e5180c8b0b804`  
		Last Modified: Mon, 17 Jun 2024 18:40:36 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:b6db1fcfb122945e7bfb5370894760f406432ad25bed960d0ad2340fad436bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 MB (351415972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1224d79c3338613e62ea6fac765babb08b0484ff67c8954224f5af02657b9ff0`
-	Default Command: `["R"]`

```dockerfile
# Thu, 13 Jun 2024 01:18:57 GMT
ADD file:a0c25580162c011cc186a00ff527d3dccd6ebde9583f49d925d9c4a0bcf07470 in / 
# Thu, 13 Jun 2024 01:19:00 GMT
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
	-	`sha256:c17ef498846c0b5766aa996aaf6ece599537a2132a98b21abc95e98de5797774`  
		Last Modified: Thu, 13 Jun 2024 01:24:41 GMT  
		Size: 56.1 MB (56146522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf17d59ea2618f21d2f6298f4aca59b482668c00c5d8bbe1dceb4b36e69c1915`  
		Last Modified: Fri, 14 Jun 2024 05:13:56 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01df415577231747e399a2a9caed4e453cbe90669562e40f9759aa093ab1c91b`  
		Last Modified: Fri, 14 Jun 2024 05:13:58 GMT  
		Size: 30.1 MB (30124447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64daafafffbe5fa554b9e80872335f55389dc28cfed0c0e847418168d0d8602a`  
		Last Modified: Fri, 14 Jun 2024 05:13:56 GMT  
		Size: 866.3 KB (866329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb17b4b8171d4c9f61cc4b9980f01fddd81af5521c304a6a19a8e1d73aed689d`  
		Last Modified: Fri, 14 Jun 2024 05:13:57 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa2ad6cca1b5a1ad215028f643efaa089a067923bf44c9c86412008a9ecdab`  
		Last Modified: Mon, 17 Jun 2024 18:08:35 GMT  
		Size: 264.3 MB (264275014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:92f36d418d3a65b6879668c904483664465aa8064b4af2880412ab21e56b9fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12329706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e89e12ee461343fd710048c2198a86be02cf6e4fdc2443ec391896dd452d29`

```dockerfile
```

-	Layers:
	-	`sha256:4d6627620d326e2252ca430557fdb11723541c58925a0fab2724534eeb91168f`  
		Last Modified: Mon, 17 Jun 2024 18:08:28 GMT  
		Size: 12.3 MB (12311743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31e3996ac57ac596d9e4fcbcce6afffaf588be5e53b16f58c53505aadb0d6ea5`  
		Last Modified: Mon, 17 Jun 2024 18:08:27 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:4d6175539c768f47de32c1386df5187dd22386b64ff14dd242b36d7b29ca13c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330111965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa83c411e2b8693515947269d6e636a69b7a1b6347b4e5897ce38e86a89e3e2`
-	Default Command: `["R"]`

```dockerfile
# Thu, 13 Jun 2024 00:44:54 GMT
ADD file:10228c4b34e8ce576af7bd79fcb17c133b1ea50ced4c4e3086c0d133e54eb0a8 in / 
# Thu, 13 Jun 2024 00:44:56 GMT
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
	-	`sha256:6eb6b57af9d4e65be8055ff33f3b560adcb2c0d5f354553283f30c55e9a081f3`  
		Last Modified: Thu, 13 Jun 2024 00:49:43 GMT  
		Size: 51.9 MB (51895345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04249ea9dcc36fa3a64d73b3a3e537928ba8beedf83c762f849918174eef64e`  
		Last Modified: Thu, 13 Jun 2024 12:39:44 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042f7cfa1e706dc9a7aec15a7f890607019b188d0268dd6f4a34459c215bac80`  
		Last Modified: Thu, 13 Jun 2024 12:39:47 GMT  
		Size: 23.2 MB (23211640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6d562641d54f66850fc3f64b72e825e7c26d99173106df91f138fb1f636027`  
		Last Modified: Thu, 13 Jun 2024 12:39:45 GMT  
		Size: 922.3 KB (922278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301375afdecf9c6913b104cdf8175803f5ab96beb88c38bac0ee3f72a59c5ac0`  
		Last Modified: Thu, 13 Jun 2024 12:39:46 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a39bc5aae323e4ecc91e18b6ae862b716e00494ef7960d48a878a25c01a1ff`  
		Last Modified: Mon, 17 Jun 2024 18:02:04 GMT  
		Size: 254.1 MB (254079045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:7430b624df488bed67e2970e9dade7b041d560bdf5fafac54389caf3b609093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478b92b302abe110cc61f846c0ef7faab158181f6daa9684c8348f46a0a36c11`

```dockerfile
```

-	Layers:
	-	`sha256:97be11e8434052d15d07a5222f033138991c189b75da751b5447df648a5e27fe`  
		Last Modified: Mon, 17 Jun 2024 18:02:01 GMT  
		Size: 12.2 MB (12158805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c00d2ea95de5dda768c0bc19648464636dacd416ba7c6db6cf03d54a61beae`  
		Last Modified: Mon, 17 Jun 2024 18:02:00 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json
