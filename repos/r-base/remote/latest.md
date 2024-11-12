## `r-base:latest`

```console
$ docker pull r-base@sha256:145f84e25111a3263b9c196f75fdd692a81c4ab70839368c802edf63f6897702
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
$ docker pull r-base@sha256:3a5226a4070a7ff76ee6b50d6ccc668e41cf0be28205d98177d044553a73e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.1 MB (354145749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16d19479021f579c790a1b5e216cd778622d17fd18ef420efc895b937bb1ef9`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c1f3f669a92f4b53dd069b7da2ebc504d2fdec161442dba2fc3ea1f47ff18b14`  
		Last Modified: Tue, 12 Nov 2024 00:55:03 GMT  
		Size: 53.2 MB (53226783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da929976e0644c860ff89c01bf3bf90d08ca8eebe045546aa155e460086ecac`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ff877eea58514c5274f4922d83865e610aae93f32f586d40af40310176e82e`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 23.2 MB (23170263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0581e5b835f0ac2291d2db5a88f801e7a1ae5dfca206e2b95d332790ef9d861e`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 866.7 KB (866744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd925e584ee927e31a8ca9b2eb681fa1b42e26646dbde6385cd4ac5b1e72ae8`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896d66f6f118fe8dea2be4acf5e965f74a53919a7256f733c14d224da1794a16`  
		Last Modified: Tue, 12 Nov 2024 02:37:36 GMT  
		Size: 276.9 MB (276878301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:b2e92e852ff804041179573915be8863a3aa84693ae40688957f952d75892369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12602728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc3d142309ad2c5215d7a422b10fbcba55e82c80ebd43571c88e86019ad068`

```dockerfile
```

-	Layers:
	-	`sha256:f5d10ba5db55a7b685b4f9226a77617e7eb981553a1ad731df9b1400a3d25aab`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 12.6 MB (12584587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a11ef98bcce8fbc308dc5eaa10c61e4ba5981d6f07bc101b764a470df1b9b67`  
		Last Modified: Tue, 12 Nov 2024 02:37:32 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:1cddacf247d9f327093c60c792137246a4d061f0f85681a1e7efab490bb72797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339898639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ba22c9fa76a049d0026cd0e2cec25722d543a93da79a69575a771002f12655`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:697066b3c41c0e748488c93a09f55bc690bda5c8785f15567dcf01882737727d`  
		Last Modified: Tue, 12 Nov 2024 01:01:55 GMT  
		Size: 53.7 MB (53669956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94c0fc4691b456551bd7833239001157ef1c5a57e21b8854676a17daacab6dc`  
		Last Modified: Tue, 12 Nov 2024 09:58:24 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682d39e106c13b72a539a2dede928c047aaad26d643644868c63abeed95de0a`  
		Last Modified: Tue, 12 Nov 2024 09:58:26 GMT  
		Size: 23.2 MB (23157034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8547f477200d37e3b25a6eec4abea6577d04dddc1f35d6b068e2122b50e3a05`  
		Last Modified: Tue, 12 Nov 2024 09:58:25 GMT  
		Size: 866.7 KB (866745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94aa42492dac2a86e833a15c2c96d1ec2c79d1f754515da056d8a811ae53721`  
		Last Modified: Tue, 12 Nov 2024 09:58:25 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199096fa4fc98cdb87b3aa852dc130fdcb83323ce2e07140346f5ef434aebbb`  
		Last Modified: Tue, 12 Nov 2024 09:58:31 GMT  
		Size: 262.2 MB (262201245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:c658a8808f1099b4d00f10500ac9ada91723cab3044eb3131f7f93e82df4b4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12716853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833215e1c8e725bfb96b5e6db051eda2b3d44a1c3d6499b15360c59735858cca`

```dockerfile
```

-	Layers:
	-	`sha256:8415ca72bfcfbc2b3a1ad15de81664b569525c47c613bab8f1664bf6c6f31370`  
		Last Modified: Tue, 12 Nov 2024 09:58:25 GMT  
		Size: 12.7 MB (12698572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b642e99f374e5422c035603af357b7d7e61496e764bc17037c26bdfdd478c6d`  
		Last Modified: Tue, 12 Nov 2024 09:58:25 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:e8aa46b95cae84c46916a4643b1cb3d0e67996830969e9881cc4a586dd2b597f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348802752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a828a3e203fa4894f4534cec7002fe228c631332ad39145c7aa3d3e9ce530916`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bfaf6689cfe5b1b679ac91d30f4af58230d4b1ee582374f94222935bb55a9ea3`  
		Last Modified: Tue, 12 Nov 2024 01:03:35 GMT  
		Size: 57.2 MB (57193587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34edbbc39a239c59085f2e527a3af9e5604d2fabbfd4d44b19436e2f8c6b3596`  
		Last Modified: Tue, 12 Nov 2024 07:50:36 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c001e3a683f95eecb63cf6de0205aae8ec8be7d19020100aea6df353409cc6`  
		Last Modified: Tue, 12 Nov 2024 07:50:37 GMT  
		Size: 23.4 MB (23395986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e987a3b2187b0268c13a31705a705b5da2b99b5b0a8ebb288d1f1760e6df278`  
		Last Modified: Tue, 12 Nov 2024 07:50:36 GMT  
		Size: 866.7 KB (866745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc479dbe021d4ea95b43d4a2311cd575f8df4f7d0b6354474aa43c2d9e4b224`  
		Last Modified: Tue, 12 Nov 2024 07:50:36 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed52b183866b5678b65c8304510d57e9130d223a21c0e8c01ec168c50924a70f`  
		Last Modified: Tue, 12 Nov 2024 07:50:44 GMT  
		Size: 267.3 MB (267342773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:d146e5f36b12d0c1765eb45aca3f76cef083878ff78ff010a42f925b8fc4fbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a4a28be533a83335c0dc87c7e064f5309dbcfec6e3772adfe0caaa9b2a5ff6`

```dockerfile
```

-	Layers:
	-	`sha256:5e0f6a0f477bf8390683280f9c0d20b2989573b6b9ae3fe80da651bc67431022`  
		Last Modified: Tue, 12 Nov 2024 07:50:37 GMT  
		Size: 12.6 MB (12578382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb19f155e7a72dba7695ce208f9a26603964896399ebe1b2566b641c482ed6b`  
		Last Modified: Tue, 12 Nov 2024 07:50:36 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:bab12a807c3b356713af0d32fabba9a132eee0bafcd1792a8afa93d87078f0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (321011112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ba90d60cdf171ca87a26f40e1cffbfc6d6fa62a370a6101e1d18c484868482`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 03:11:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 01 Nov 2024 03:11:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Nov 2024 03:11:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
ENV R_BASE_VERSION=4.4.2
# Fri, 01 Nov 2024 03:11:38 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 03:11:38 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:670975d8b290040812e8ec5deddc536b98b5da6de159f4a0aa63b04735db617e`  
		Last Modified: Tue, 12 Nov 2024 01:04:16 GMT  
		Size: 52.9 MB (52885530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ada7a9d9959b8dd50096aed09163bf18d4d74382a39cd02c45f1fb59a66249`  
		Last Modified: Tue, 12 Nov 2024 08:26:30 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a1fd47c9f1e5d49cb8d313bf6ef35bc393f07d6d5c3460ef733b619df48901`  
		Last Modified: Tue, 12 Nov 2024 08:26:31 GMT  
		Size: 23.1 MB (23121111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae95a358f8a166b1c6417fd83bf3a6822dd48732a51bf2a9215ba730cd5875e`  
		Last Modified: Tue, 12 Nov 2024 08:26:30 GMT  
		Size: 923.5 KB (923489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9afef81d3f90b7b27387df8f928a5a7f96d851b9855375a028cfa2b383048eb`  
		Last Modified: Tue, 12 Nov 2024 08:26:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05689e95f72914465b83f8f140609700c81519dba5bb7e6ee3b4544eebd19749`  
		Last Modified: Tue, 12 Nov 2024 08:26:36 GMT  
		Size: 244.1 MB (244077320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:5ebfd37a3a44388116cd9cf0c22ce6fbc00800662f0f809a7bbcd83c50676bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12404062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d079559fffece78feb038c37316db7278290f14f005e32d11774132202b08eb`

```dockerfile
```

-	Layers:
	-	`sha256:d10a4ba17c1fe2eabe31fab1d4cd3ef0ef52371a35aa9d146ec921b712175692`  
		Last Modified: Tue, 12 Nov 2024 08:26:30 GMT  
		Size: 12.4 MB (12385921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f3e16ab37fed543b21b54f21c2a0126350b4339f15f34a94938af0be91913e`  
		Last Modified: Tue, 12 Nov 2024 08:26:30 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
