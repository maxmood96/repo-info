## `r-base:latest`

```console
$ docker pull r-base@sha256:57499c281ed28c80a4b63955e3e5ced8809853c6767a9badb01b033637279d4e
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
$ docker pull r-base@sha256:564c8783ae0f658f0037cf2c715c421095e5514883f6c16292d7489e3aaf702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.6 MB (906617660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d3330850fd34169dde39b12125810dd1a2a671105551949059692a3b5d6658`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1759104000'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e53bf7ab07ea4ef0bdd293b1b3d03f786cf07ef52cf9fa96c661bdb1e7e3d20a`  
		Last Modified: Mon, 29 Sep 2025 23:36:06 GMT  
		Size: 49.7 MB (49736817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1739ba4a068e335e01fc904ae81d99cc11752b3b71ae52c1885bc88b747170`  
		Last Modified: Tue, 30 Sep 2025 01:00:49 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141afeeacd8046518cd7561d58199400526f6f54b97dc7eb976987cb2e15d7a8`  
		Last Modified: Wed, 01 Oct 2025 00:24:50 GMT  
		Size: 26.9 MB (26931588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20940053ad3e800c586b3932632d9d6e19c7f6362b655966b30ed2a11077589`  
		Last Modified: Tue, 30 Sep 2025 01:00:48 GMT  
		Size: 868.5 KB (868479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4204fef9dc6cf6f0d7972602992a582a28c6205c73db2c8fc3691aa0d44006`  
		Last Modified: Tue, 30 Sep 2025 01:00:48 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7648885b131bf3526039f23002dc5609e8d3e7210b2052d46576605438d0ada8`  
		Last Modified: Wed, 01 Oct 2025 00:25:54 GMT  
		Size: 829.1 MB (829077117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:da85048876a7bd60cda5200de2af4cc9deaee5fa9a47ce852a6cc84cf9c0710d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12977424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0818ff59005629f1242a75bc4d2cadc25e9caec8a5e372f35b95c4a8b59bb9ae`

```dockerfile
```

-	Layers:
	-	`sha256:29ce68f025d5efd4aee721aa71059b500b3709fbb1d0580402cbebfa5cc624ff`  
		Last Modified: Tue, 30 Sep 2025 21:32:14 GMT  
		Size: 13.0 MB (12959284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ccb6bb49722f06908364bbc0ef2ea6dce78313de7ea51c3322426248051688`  
		Last Modified: Tue, 30 Sep 2025 21:32:15 GMT  
		Size: 18.1 KB (18140 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:8ab665e0c73aff324550c41eb2e4cdf518fc7fd2a212d5e7f0ad1d78c67846c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.3 MB (907313803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8801e8579060a6eeab54356001cd4c1a8848f94acba9f3f5a694f7234d693664`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1759104000'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:eaa39e59530b026aca4c6a2bd8547ebc0f3668ab204470b61baf267315ca1cf9`  
		Last Modified: Mon, 29 Sep 2025 23:35:15 GMT  
		Size: 49.9 MB (49879876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6d8b27766ec162ab54e0c39f45add92e46478873c4c2113870bd9f9ba2c2ea`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399d92e242ff93e15683524c4a3b4d97eeedf7fc18cccfa151a8d903db2dc81`  
		Last Modified: Tue, 30 Sep 2025 00:14:27 GMT  
		Size: 26.8 MB (26811312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfcdaee09a4326c7ba5aa5f688f7fbdf5c3d3c1c096c61b44ded2561ec04513`  
		Last Modified: Tue, 30 Sep 2025 00:14:23 GMT  
		Size: 868.5 KB (868485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae441a104f64421b247783a5be570ca18cd6e4a7441848318aad7306242475dc`  
		Last Modified: Tue, 30 Sep 2025 00:14:23 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caf831cf6abb84df815b81bf7b280ae0416a9baae73d89c0c33e4bc177143ec`  
		Last Modified: Wed, 01 Oct 2025 12:35:41 GMT  
		Size: 829.8 MB (829750470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:7664801aa1a5781f9a4b7a0adb6eee732e62b8f77cf1a3dbe05dbe6ce511295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13067309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673f81af41e6f7a9e1ea65efe89b381213510f04e7db50a79be00ac029fb233a`

```dockerfile
```

-	Layers:
	-	`sha256:4482697f479952be41ad892ffff869daae8ab5874b440f829e92758949193de9`  
		Last Modified: Wed, 01 Oct 2025 12:30:33 GMT  
		Size: 13.0 MB (13049028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1af6d7f9b132d13e59961f36eed26766dcb19c1cfdf7b4a66ee5bb3cf76930ab`  
		Last Modified: Wed, 01 Oct 2025 17:35:10 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:5dba895dad2afd2483026fbaa2a66e06467a86fd6da48f2b0e4e1974b4d965f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.9 MB (825946922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a53083a77f9b127865cd5bfa55d941abaf772c9212dfd7c97b86ab92334590`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1759104000'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:62b863443040ce1d4ba90e93d398f94c1ec68f34663867e17f1e7b87f9d7dc79`  
		Last Modified: Mon, 29 Sep 2025 23:40:28 GMT  
		Size: 54.8 MB (54750878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9579dda30d7ce698e4d091baa6d143063984553691b058c3775516e245fc5431`  
		Last Modified: Tue, 30 Sep 2025 02:06:23 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6622ed1fe49d460a959bdce1a315ed84ab0b7839c6cff30447455fd4825d2a2d`  
		Last Modified: Tue, 30 Sep 2025 02:06:27 GMT  
		Size: 27.2 MB (27189114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39034bfc7cdd4944d4de0f2dbe6717bda1f53e0612dc232e7bc99628cf7032`  
		Last Modified: Tue, 30 Sep 2025 02:06:23 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bed2326d054bbfea74104c671f1f6e32767546b33c92c0880903048fbbfd77`  
		Last Modified: Tue, 30 Sep 2025 02:06:23 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc7f609d90b81126d6bff33ef6f88ce231d559fff8d9dd425fe173e5a04b4bb`  
		Last Modified: Wed, 01 Oct 2025 19:32:31 GMT  
		Size: 743.1 MB (743134783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:440b6218a0b67eceeb1d16c7c86a96c02d46445a8116ae3d01e3dc810c202960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12963250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09338300f4bc3e6fc069a663c691fd637b9ccb33fdf48a87a2ac992cb93aa23`

```dockerfile
```

-	Layers:
	-	`sha256:371112f92f13b6d609611c9a98e14200e489b3e288bcc8e3f7826c61d410e25c`  
		Last Modified: Wed, 01 Oct 2025 21:13:39 GMT  
		Size: 12.9 MB (12945069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8e735d9ac96ea1ccb4cc54cee99f0d0bc7e2190573ae6838428955a850b2f1`  
		Last Modified: Wed, 01 Oct 2025 21:13:40 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:1f892814f22c1bbe4b1b9326560ca446327f515b68985c4d9faaaf35591a1131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.1 MB (779071928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2914a7804a6ef48a687ebe19604acccb17b6cb1b1753cf5639fc7624109e53d3`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1759104000'
# Fri, 13 Jun 2025 15:18:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Fri, 13 Jun 2025 15:18:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jun 2025 15:18:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
ENV R_BASE_VERSION=4.5.1
# Fri, 13 Jun 2025 15:18:05 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 15:18:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6a0a4867ef73eaafaa3876eab73c35b9c7a731cb8449516b6e6ca5e9b88df7e9`  
		Last Modified: Mon, 29 Sep 2025 23:40:06 GMT  
		Size: 49.6 MB (49576013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae547ce45d67efcd40d95bbe43f0795d56eaf4c24d63af83287738f3880afa9c`  
		Last Modified: Tue, 30 Sep 2025 02:55:28 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaf0b9f57910c182b962cebc6cb1501a6bb3747f831a7321331a33c7a9d0afe`  
		Last Modified: Tue, 30 Sep 2025 02:55:30 GMT  
		Size: 26.9 MB (26884935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f600ca9ed2aee60da366fa073de6a94f3ee8dd9ddd227308331d7ba3b7b490`  
		Last Modified: Tue, 30 Sep 2025 02:55:28 GMT  
		Size: 924.5 KB (924545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ffd961c4ea6f21f5d5a223b87f42aa6cd40edb2f1da7a9b3a26ba015406433`  
		Last Modified: Tue, 30 Sep 2025 02:55:28 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96eacfc8f20b708eb92c9465b2c1266c152d96157e0cee7f1697378c50be821e`  
		Last Modified: Wed, 01 Oct 2025 19:26:20 GMT  
		Size: 701.7 MB (701682774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:a7e3aea6189c0180c995ee243c3d8af71f8e611648d6708aa1c1de4f9d7f05dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12768637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a937fd8d3792cf164e5b8284777e28084d718a2c0476be6d669a9fd0552c7eda`

```dockerfile
```

-	Layers:
	-	`sha256:973b478f84040af33870db412cb08c1a1fddc6bb683e425e2ffa3bc465bd9261`  
		Last Modified: Wed, 01 Oct 2025 21:14:02 GMT  
		Size: 12.8 MB (12750496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4331616f8e1e22f6efdab98e52939989d674d1369486ef92d00e970eae0a5e`  
		Last Modified: Wed, 01 Oct 2025 21:14:03 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
