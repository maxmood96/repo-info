## `r-base:latest`

```console
$ docker pull r-base@sha256:3e0906a3ceddb17f409b874d8727704aa38e4b7e85029b3e251ec0eeedd370c8
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
$ docker pull r-base@sha256:65045246c0448fdc9c5332deb6342c7ef9887a59795a935b5528e63b651806d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.5 MB (825539064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bf6a913116bbc9cc1620bdd484f58cd6c85ff5c364d77747b43c0c95b992f5`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1757289600'
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
	-	`sha256:96b4ca5ee980768194b7b8007765bc50123c81ee67cf0d113b71633ee6be6175`  
		Last Modified: Mon, 08 Sep 2025 22:20:11 GMT  
		Size: 53.4 MB (53391696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7046bc127e3c775f160f2730956ba97e0a547975209433c3026632fe61a5e6`  
		Last Modified: Tue, 09 Sep 2025 01:39:24 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fe3784d5825943d45fec36770f0bf6d4aa465e3c893db8afd0af5a8a47d252`  
		Last Modified: Tue, 09 Sep 2025 02:17:21 GMT  
		Size: 27.2 MB (27161150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053a30456f96c698e2e41d8998f671b0b5994c895ad3ea08fcfa5ad4a2de8d21`  
		Last Modified: Tue, 09 Sep 2025 01:39:27 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9ac9388d3c46361bc795d035b6aa7b10dc4be1752a4559d14bd61fe60ee3dd`  
		Last Modified: Tue, 09 Sep 2025 01:39:31 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75b8c401baaf144febd059ba23f0e3863e729e26c1b83e55570be491e39796e`  
		Last Modified: Tue, 09 Sep 2025 02:17:01 GMT  
		Size: 744.1 MB (744114067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:f4771b8d49725e5188f2cca2de02c9a3fbe7c2514cbe34ccc7edc1f1f0e50a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12970246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd785356a0a81536d4a5062dd72fb54d401afda5700d63c65177785674eebb21`

```dockerfile
```

-	Layers:
	-	`sha256:8dcf0f941a0e0e281d882d003142c493b3a7a5df2ce37220a2c61b9e2b299903`  
		Last Modified: Tue, 09 Sep 2025 03:13:40 GMT  
		Size: 13.0 MB (12952065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea4042dbe6cbd9364a02fb15667d9e446efcf9204c6d07b6b3b635d3056f701`  
		Last Modified: Tue, 09 Sep 2025 03:13:41 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:1dfe52f66452dd3026855ee5b4db7e9f2c0528928a3c8d866f6cc893255d402d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.3 MB (780317658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fabacc635846a50bb98e959ad8a31d65955e134b1cf6b9ace66c846582f215`
-	Default Command: `["R"]`

```dockerfile
# Fri, 13 Jun 2025 15:18:05 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1757289600'
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
	-	`sha256:2cd29a40290eb73c0f0fb2c946ea3afb7559c33b6f5ca431ef71a23380e9eeeb`  
		Last Modified: Mon, 08 Sep 2025 22:20:17 GMT  
		Size: 49.6 MB (49583182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca2b8aa3419b16fadd01e18eaf3f4809bf998bd1370b484fa5cab5d700d7b26`  
		Last Modified: Tue, 09 Sep 2025 00:39:39 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f83a8e8bf55661df4cda537a6813768f6858f6ac9dd52120bffeb77a8ed4430`  
		Last Modified: Tue, 09 Sep 2025 01:21:21 GMT  
		Size: 26.9 MB (26875184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e2d1827cc05d84d95e9ed2357b76dbf7843e8c1587349d993f10f0aa83d0ca`  
		Last Modified: Tue, 09 Sep 2025 00:39:39 GMT  
		Size: 924.5 KB (924550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12490c9d5a9a67c85914edfa6f7c20055e132caed21d479c39b47bead360d698`  
		Last Modified: Tue, 09 Sep 2025 00:39:38 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130677e9eaee22d989dce2e2cfb227af16c64fc86198116a8bea59af79c00e97`  
		Last Modified: Tue, 09 Sep 2025 01:23:48 GMT  
		Size: 702.9 MB (702931081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:23ff6976aa362146ab2f21cd791917b7f73c836721516d167f8ce86d7b7b5829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12775629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ea9d5201e70f0b4652870fa6592b4fde517dbc9099eb7c2b66fba212962acc`

```dockerfile
```

-	Layers:
	-	`sha256:e0d89f2bf702882c8eeacd632edaebc48d896fbf05c6f664602661eab444716b`  
		Last Modified: Tue, 09 Sep 2025 03:13:51 GMT  
		Size: 12.8 MB (12757488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323aa62df4669bba493a072b9bb13aa2d53e89153bce42ce6f33ded9905e939e`  
		Last Modified: Tue, 09 Sep 2025 03:13:52 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
