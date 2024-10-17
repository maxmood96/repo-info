## `r-base:latest`

```console
$ docker pull r-base@sha256:951a2717d7b40899fa0448da911b874f9d1c72dc954cddbae75216aa5f32264f
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
$ docker pull r-base@sha256:8b6e194a0b39b8d8fd6588a9ff0b03cc409e1e64e26ac2deb428d08eaa0801d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (354000930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860231d4935ab2a5122471500b603f7608986d9b1bd12e458a45db409d1a9a85`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:dfa41c5a8e1c4511359423b532cb30507d2ec0cb9ef2412143a4d4a2752d2d0a in / 
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
	-	`sha256:be8a7f4a2cec45419ae4d29243820f77c134b84630752f45d42a7725f62db14f`  
		Last Modified: Fri, 27 Sep 2024 04:43:03 GMT  
		Size: 53.6 MB (53616589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d9661c099ef330077e90bc400671543300a1c30b436cb33b5e64861b0ac46`  
		Last Modified: Fri, 27 Sep 2024 22:22:45 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e571c2121ab5d9d1f56e30b27b9976709c92f72f6859ef4cb8d04e4b396401c`  
		Last Modified: Fri, 27 Sep 2024 22:22:46 GMT  
		Size: 23.1 MB (23149429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b110e8737974804701b4f0cf0569e426a6b2cafb4d779f229a96a51dfa757d`  
		Last Modified: Fri, 27 Sep 2024 22:22:45 GMT  
		Size: 866.7 KB (866741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50763ffd1bad10cde7609ba9036ef3111f9a385e93c10498e9abce3fbc65fddb`  
		Last Modified: Fri, 27 Sep 2024 22:22:46 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77674851e7e2bf4b1dd6c134860b2ae0799f560a0c91e8e8e26851b4423cb6b`  
		Last Modified: Fri, 27 Sep 2024 22:22:52 GMT  
		Size: 276.4 MB (276364512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:13b63f9aa75800a3773c352a9f975ea4e26194cfce34336ead0423bbd8a04e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12526879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3fe2c79a5e895cfeab09be2500528e3758beae7bb5eed7659c672fb1f984a3`

```dockerfile
```

-	Layers:
	-	`sha256:c1c2a006273f2095c5e72277c582fc4089b70bc6d533916dca3496b0345d1a6c`  
		Last Modified: Fri, 27 Sep 2024 22:22:46 GMT  
		Size: 12.5 MB (12508671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e7ad11c5c4089c8fc88593c726cbe11d1427e7562bc8bd8b1e5138ac68bd29`  
		Last Modified: Fri, 27 Sep 2024 22:22:45 GMT  
		Size: 18.2 KB (18208 bytes)  
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
$ docker pull r-base@sha256:908d10f013c6d99c2ebaa9dd179cb07dcd46a150eb867e85bc15ddcf2b249e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334693552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48aade0bcbb0bc1bacce1b84177a6b082176acae6c82089c1d6f6715b20cf63`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:3e39c625eaf60953d8cee79d51e2111b241d054227598d815a080b9fe676b690 in / 
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
	-	`sha256:6254903b6edc85d1dc106a3e9025a77bf951ee477df6401427b61d5e2f6ccc3a`  
		Last Modified: Fri, 27 Sep 2024 02:48:24 GMT  
		Size: 52.8 MB (52771071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943f2b224fce1f40ab1cddd6049c0ac1afcc891c0dabd939eb9f8edb31bd8808`  
		Last Modified: Fri, 27 Sep 2024 17:07:44 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508a3d8711517c72d656fc1fe63b1a2c98a7a9180454425c82bd05d46e99e5d9`  
		Last Modified: Fri, 27 Sep 2024 17:07:46 GMT  
		Size: 23.1 MB (23118257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d78006081c4114633b3e155f66827561d457677bceac7c28059b8d5ee07fef`  
		Last Modified: Fri, 27 Sep 2024 17:07:44 GMT  
		Size: 923.5 KB (923491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c982f8adc6ef361a5c0b2ae14baaee0476a4d3016c09dc14ee113bb0d855c`  
		Last Modified: Fri, 27 Sep 2024 17:07:45 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c18bd7fc7d58d45b73127b2ed122053cc466495dcefac630673b57626af4f4`  
		Last Modified: Fri, 27 Sep 2024 17:07:48 GMT  
		Size: 257.9 MB (257877077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:78879ce3abe4638fa65248a80fa689dd6c8e2e22cec679c4380e0553d531af2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12232675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84c5187d911a72e0f54fd940f0152f39e202fc85996a13096f73bce4b653d37`

```dockerfile
```

-	Layers:
	-	`sha256:5ebb9a42f6843adef5550b165500a4cd294db1cb35adbdcd19170c48c8c73a45`  
		Last Modified: Fri, 27 Sep 2024 17:07:45 GMT  
		Size: 12.2 MB (12214746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4096daa85eef065603a7905ad68764e971cd3d929abf72a698bd745aba432d63`  
		Last Modified: Fri, 27 Sep 2024 17:07:44 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json
