## `r-base:latest`

```console
$ docker pull r-base@sha256:90cb3fa582a1b81a347e61dc1043d9c6fb5d61e7a0bd66d34e3fc6c736caa9fb
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
$ docker pull r-base@sha256:414a7b6ccae7756ebf94903a4bffd2a37059a1e417327ff53a050f2af6345d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.0 MB (369973295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9f21d74515f1ed463f2b80a7a5850f89887408d41f965b81d268b6262b83ea`
-	Default Command: `["R"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1766966400'
# Mon, 29 Dec 2025 23:38:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Mon, 29 Dec 2025 23:38:24 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Mon, 29 Dec 2025 23:38:32 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:38:33 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Mon, 29 Dec 2025 23:38:33 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 29 Dec 2025 23:38:33 GMT
ENV LANG=en_US.UTF-8
# Mon, 29 Dec 2025 23:38:33 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Mon, 29 Dec 2025 23:38:33 GMT
ENV R_BASE_VERSION=4.5.2
# Mon, 29 Dec 2025 23:39:15 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:15 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e82aece8925851cd125cda205a5f722be8e2b918d6f6178dae37c8a5cddc74ef`  
		Last Modified: Mon, 29 Dec 2025 22:30:46 GMT  
		Size: 48.8 MB (48830059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55c066e7b5b356cf2e9ffd7bc6ebb9576b1d7730c422af5682747e8735cbae5`  
		Last Modified: Mon, 29 Dec 2025 23:40:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f72e0c8ee47764ae48eb6a80a0a0d8aa2bf5ef72700c912c2da8a0ca9f91d6`  
		Last Modified: Mon, 29 Dec 2025 23:40:08 GMT  
		Size: 27.0 MB (27033272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559df7c6541617c43a72db83e3644d9f245504421f233a4b81e04f3e1db50327`  
		Last Modified: Mon, 29 Dec 2025 23:40:04 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d1d9ebd53ff017bab7995fa0a6816d521475c28c1bc5a98545266f8573f918`  
		Last Modified: Mon, 29 Dec 2025 23:40:04 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f4714e75e22a0cda8ca6d8c138e43af8bb2a7ccfe38e6c6f841eb455157b18`  
		Last Modified: Mon, 29 Dec 2025 23:40:11 GMT  
		Size: 293.2 MB (293237816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:0436729172f7f4822d43608eec1b006c1196be5bfd23a40e202bc31f46f38935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12967671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5251205b0dffef92b23e026a1cbbe79bcfa56311e4adc7cb34986e1ebb2b086`

```dockerfile
```

-	Layers:
	-	`sha256:ebbd9aa0c68a404a9c2e0eee6b0b21fc78e576b4dedc99a9ce585cf5bcfc5509`  
		Last Modified: Tue, 30 Dec 2025 04:14:09 GMT  
		Size: 12.9 MB (12949573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42c667f3322c2227b39cef5c5478a6a71ac246e49c58f338a8a18006fd273bd`  
		Last Modified: Tue, 30 Dec 2025 04:14:10 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:ea288121a27373928048ef75a63ee115f98d6135ccc3a883683c75ca4827b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (351008108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5529489be57874311a911cf41149c327d4358fc84175e64f34a195b17a62e3`
-	Default Command: `["R"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1766966400'
# Mon, 29 Dec 2025 23:41:58 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Mon, 29 Dec 2025 23:41:58 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Mon, 29 Dec 2025 23:42:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:42:07 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Mon, 29 Dec 2025 23:42:07 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 29 Dec 2025 23:42:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 29 Dec 2025 23:42:07 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Mon, 29 Dec 2025 23:42:07 GMT
ENV R_BASE_VERSION=4.5.2
# Mon, 29 Dec 2025 23:42:49 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:42:49 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:7e1126b01c9de189d1405152c74b9a40a3f428e4a1cd28f6a8d42a9464c64c0f`  
		Last Modified: Mon, 29 Dec 2025 22:30:45 GMT  
		Size: 48.8 MB (48831994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d299acef9fa72793862091403013245e47fbd7b09ed66fb7a65112372477f9e`  
		Last Modified: Mon, 29 Dec 2025 23:43:38 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd025538b2bea03b2971801fc41f6bf4817cb464c2e3232ef5a0d37efb94efd`  
		Last Modified: Mon, 29 Dec 2025 23:43:40 GMT  
		Size: 26.9 MB (26895488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087894f9932ca126c4cd1c50e89ba14f813cc8cc7453ffe4dafb1027b2d1bac6`  
		Last Modified: Mon, 29 Dec 2025 23:43:38 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0eeeb84c9be911ddaf655e34abf6e38470b06d62edd5f5487b1fa69f6c815f`  
		Last Modified: Mon, 29 Dec 2025 23:43:37 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f77424bf2d95b94605e9464513a4d5bf3318e8c1addf73881ae65a64acbe6d`  
		Last Modified: Mon, 29 Dec 2025 23:44:09 GMT  
		Size: 274.4 MB (274408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:66db5c7fc4b7e8bbc106f2967b385ed51c6b0b3567e2a7295be8784d95b39a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13056918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfbe06a314952f48d59ce74bd37c94ef4459f77cdfa0eeacb92e7f1b146ac89`

```dockerfile
```

-	Layers:
	-	`sha256:97fc0722375e9fed643d2c574836cfdbafcb8f1c31542ec6fefa679984f6354e`  
		Last Modified: Tue, 30 Dec 2025 04:14:19 GMT  
		Size: 13.0 MB (13038680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5590d178ae63364e49a77451f043c0e260444354a93ee46b6dd7a04f9fd18071`  
		Last Modified: Tue, 30 Dec 2025 04:14:20 GMT  
		Size: 18.2 KB (18238 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:ebfe5c57edc99a7e0b7e3a0ecdff8851fef32fab45470409c031e9d4b392d7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361436264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f6bb4fd5cea8e8222e6dc263216bad7abee6fd8c70fb1ffc567bedb3e56660`
-	Default Command: `["R"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1766966400'
# Tue, 30 Dec 2025 17:27:57 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 30 Dec 2025 17:27:57 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 30 Dec 2025 17:28:29 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:28:33 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 30 Dec 2025 17:28:33 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 30 Dec 2025 17:28:33 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Dec 2025 17:28:34 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 30 Dec 2025 17:28:34 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 30 Dec 2025 17:30:30 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:30:30 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:5a75c60b8a87177661c6b4e6d045cd20aa06dba288dc0ccace27182fc9ab2ac7`  
		Last Modified: Tue, 30 Dec 2025 15:10:00 GMT  
		Size: 53.5 MB (53522114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7cb81c778008bf715119911d5b8ddb3e1810313ff62be2208f77411d8b56a3`  
		Last Modified: Tue, 30 Dec 2025 17:32:12 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d5c046096af019231304bf88f00effc86ea07629b701646b0c058ff6ee4040`  
		Last Modified: Tue, 30 Dec 2025 17:32:16 GMT  
		Size: 27.3 MB (27318543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c63712eedbd249f5a4dc81723c4625f8c38da4741bc0efb8f147af9553b6c8b`  
		Last Modified: Tue, 30 Dec 2025 17:32:13 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a8c8795ffe0f1d5330f8f35b80cb4778743aea6effb77593eab8557a7d4f96`  
		Last Modified: Tue, 30 Dec 2025 17:32:13 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d06e3dcd31306faf0a9ff22f2f20746dac372d95ade24ce1e305ba5f6e68ea`  
		Last Modified: Tue, 30 Dec 2025 17:32:18 GMT  
		Size: 279.7 MB (279723456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f6fca1473bcc6c4bdc7f900c9f93ebb0c19c1064e4e13e85c2b378d70aaf7aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12952263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164ec1de1db95c3014520b5b5e91ebef8d92865e7e2f6131bf07ed6301b31d19`

```dockerfile
```

-	Layers:
	-	`sha256:31fe2a5a9133d493f289627fcfb77782175048fcf2821f1756085b2a0928e2c1`  
		Last Modified: Tue, 30 Dec 2025 19:13:44 GMT  
		Size: 12.9 MB (12934125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d597700fca5fa1b5b98bbae228d8d92320e59cb8ac837d755047b5094b5ba48d`  
		Last Modified: Tue, 30 Dec 2025 19:13:45 GMT  
		Size: 18.1 KB (18138 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:b19ee854d45410b9a6088d96726455681f888a13b8a9c1145811af76323ca54f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.6 MB (335580622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34b2c6859c51379bf82bd996bcd254b4dbe2c605d8adc3c0681362ead91ca78`
-	Default Command: `["R"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1766966400'
# Tue, 30 Dec 2025 03:21:57 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 30 Dec 2025 03:21:57 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 30 Dec 2025 03:22:07 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:22:08 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 30 Dec 2025 03:22:08 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 30 Dec 2025 03:22:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Dec 2025 03:22:08 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 30 Dec 2025 03:22:08 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 30 Dec 2025 03:22:52 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:22:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d80a003d64b5d1f3f24e1220fdcfc94ca6acd0d70e01a648724ee4bd7b9a4035`  
		Last Modified: Tue, 30 Dec 2025 02:09:22 GMT  
		Size: 48.4 MB (48397554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02f4d8a54f08ad476e30e3009f9dcaae915a8000f22c18955cd9b9cd5dc862`  
		Last Modified: Tue, 30 Dec 2025 03:23:55 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dfb57ac3b78c28339cdb6c4233950bcc7fc2bf517b01b5f6537367594d01fc`  
		Last Modified: Tue, 30 Dec 2025 03:23:57 GMT  
		Size: 27.0 MB (26974347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6700927c387e03bd927b845b0351d304a41d22051fb959d916f40546fb9205`  
		Last Modified: Tue, 30 Dec 2025 03:23:55 GMT  
		Size: 924.5 KB (924548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaae045b0c2d82135f673ac099b1154e887ca61efbc946292eeba445a40682`  
		Last Modified: Tue, 30 Dec 2025 03:23:55 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f02153cf5b8973c08b64890dcadc2f3f4ff5bac07883e66aacb65aab095675b`  
		Last Modified: Tue, 30 Dec 2025 03:24:04 GMT  
		Size: 259.3 MB (259280512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:413f3bb2dc76ebfc79ac9876365acafa7b2ae0a667c07f040fd267cd1d6be0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12769390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fe5b901efd469bfa2ff994a808052cdd0cb72ec6d46aae69f4dfd607a9535f`

```dockerfile
```

-	Layers:
	-	`sha256:75446a7275c2c64b68d9db89c91eae73fbf0521455bf21452602dc66032ede15`  
		Last Modified: Tue, 30 Dec 2025 04:14:36 GMT  
		Size: 12.8 MB (12751292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8a9ecc6dc32f3311d0a0b2cef9f1c5dd5c73ad9a9dc5093c427e2cd6eb11b2`  
		Last Modified: Tue, 30 Dec 2025 04:14:37 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json
