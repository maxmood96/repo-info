<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.5.3`](#r-base453)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.5.3`

```console
$ docker pull r-base@sha256:ce88ddcdd15d9901a55439de10791cae3598644c2221332dc5b90dc6ec837084
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

### `r-base:4.5.3` - linux; amd64

```console
$ docker pull r-base@sha256:136ba9c034cb876c1203137dd03cbc7bc4412f710e1c19de76d8ad93667abbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368131717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efb24b83565f014c44b8615bfa83b201eda23b4ccd5ef8bad4acd7f8e7533d`
-	Default Command: `["R"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:40:32 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 07 Apr 2026 01:40:32 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 07 Apr 2026 01:40:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:39 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 07 Apr 2026 01:40:39 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:40:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 01:40:39 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 07 Apr 2026 01:40:39 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 07 Apr 2026 01:41:18 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:41:18 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:22b89b881e9d5422fc9da3425719efd67131de7d79df86578efa8c704089ea0a`  
		Last Modified: Tue, 07 Apr 2026 00:12:02 GMT  
		Size: 48.6 MB (48587086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d775ff3b26c9776e8949fc9252c4ec201c908e4f4aaaafceb47ce56fcd1eada`  
		Last Modified: Tue, 07 Apr 2026 01:41:54 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f18c5eac657d7b35f2375b062137e3c00708da4da9f00747ccb427c59ae95df`  
		Last Modified: Tue, 07 Apr 2026 01:41:55 GMT  
		Size: 27.1 MB (27106015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5131f03edf7d92cb9f739f57fafc215b5b7d4d9fcde53c60baa9613dee7009bf`  
		Last Modified: Tue, 07 Apr 2026 01:41:55 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420b49147ad99b9e8ffd588a6e79dabc1dd7398523a1b87b116223a00c8acbaf`  
		Last Modified: Tue, 07 Apr 2026 01:41:54 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce540ee0de8327c539c6e495f1de3a7dce6c8337fb390b25ebfb0b3be05a006`  
		Last Modified: Tue, 07 Apr 2026 01:42:01 GMT  
		Size: 291.6 MB (291566392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.3` - unknown; unknown

```console
$ docker pull r-base@sha256:9555901b227b40106a4c5456cffc3f360249423c40f8676c0fa6c34ab469764a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13044746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c3490fd80ccc915588407fddfc793a8cfbc3066e1191a6b5927358fc4f8a66`

```dockerfile
```

-	Layers:
	-	`sha256:db9579c040f306626dc67ca906838314441f2fca88a37ab8594a41b0f5254310`  
		Last Modified: Tue, 07 Apr 2026 01:41:55 GMT  
		Size: 13.0 MB (13025587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508f67c4576dbd1d27dac138c791d95bcc6a77112d4108bb80dfecefecf97746`  
		Last Modified: Tue, 07 Apr 2026 01:41:54 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.3` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:4281e2567f63d84f1f3f7251b4a207c00764a9775972e5ce307c378d5269460b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 MB (351398626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c725a2e2dd8af39f4782e48352d0f134986fe66b6045ce8542d1ceff1d2a0c`
-	Default Command: `["R"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:43:13 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 07 Apr 2026 01:43:13 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 07 Apr 2026 01:43:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:43:23 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 07 Apr 2026 01:43:23 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:43:23 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 01:43:23 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 07 Apr 2026 01:43:23 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 07 Apr 2026 01:44:08 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:44:08 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:270e6fb5e8158c645c59da5292196f6d4ac5d2b940fb597c6b350535305ec493`  
		Last Modified: Tue, 07 Apr 2026 00:11:14 GMT  
		Size: 48.6 MB (48643357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a221563de127d80ee61953c100ceea195bfcbd02a31825ec69a8b088e33a6a52`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0a86b26e177ff6b8587c1a84acb87ce65f00838184628ad71ff421f5147e30`  
		Last Modified: Tue, 07 Apr 2026 01:44:46 GMT  
		Size: 27.0 MB (26953560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efda2a3a164d408d7b02e7914b886d99a97d946c0810fefc117d3f3d36da65e3`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a5a115834fe90c74514c28c625b0c537ba2d0b454d7ed479743186c790fe4e`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ceadc30f5c52a6cf6b8bfacc7fa9af25f350355689f10986a28798f6c5b229d`  
		Last Modified: Tue, 07 Apr 2026 01:44:52 GMT  
		Size: 274.9 MB (274929486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.3` - unknown; unknown

```console
$ docker pull r-base@sha256:635abd99387b60a8c8abb3eca62a3b6c73e31449654f7e66e96587c6df333aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13147134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7a5ef27fed6539c7a904cd992b0a1c2daf4f09acd0b523b82cc80e35e6e2c5`

```dockerfile
```

-	Layers:
	-	`sha256:051e7bdadff29b3563e029464035e28c9d88d374f98454953f2fd29301789fbc`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 13.1 MB (13127833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00dde9f504eb5334e93c6772fee03b7446af71bdf3935fb2bcf1f575ca25542`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.3` - linux; ppc64le

```console
$ docker pull r-base@sha256:aee895497ad35581a322e2400fabc86029af7f96042e850cfaa6f2da711d38b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363942457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56571e3c80320b8f8e91c8fd3f26c1a732d7d0422fbab4ffaeef8b13aa5aa788`
-	Default Command: `["R"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 04:08:41 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 07 Apr 2026 04:08:41 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 07 Apr 2026 04:09:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:09:09 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 07 Apr 2026 04:09:09 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 04:09:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 04:09:09 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 07 Apr 2026 04:09:09 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 07 Apr 2026 04:11:49 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:11:49 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d2fff16aab3eb8d89b3bdbae0814c0146f162ecacdf526ba2f4a1dfd7b082ae6`  
		Last Modified: Tue, 07 Apr 2026 00:12:16 GMT  
		Size: 53.9 MB (53851239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d244606985c8fba1ab58a562bf3b577b999e2fbb4661310361d28c409a577ab`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f79bf7373af22c1f1d4b77a5e9becb01bc664a3ebf74af1cdb4795e1db927b`  
		Last Modified: Tue, 07 Apr 2026 04:13:04 GMT  
		Size: 27.4 MB (27416201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebddcba1cadd3bf56f1f2fee24ee7524f0504234985824803b5cb26474698b65`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8a2a77cde68fcbea97bb8f109506629e7af424cc643780e7ae507a8658840a`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2544b72dd9dc8236201dfdeece6f90a786590df70ef05effb90c542e6e4daf0d`  
		Last Modified: Tue, 07 Apr 2026 04:13:11 GMT  
		Size: 281.8 MB (281802797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.3` - unknown; unknown

```console
$ docker pull r-base@sha256:d74dba730e372cb2e0a56538901a42ba231b99b74ef7e395d115b7dba423d1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13029399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd63f08bead5e9c9a360559d1f19ec5a8ed926385cc6138daac35a40be9b61b5`

```dockerfile
```

-	Layers:
	-	`sha256:8ed8aa891a6804cafb2ae079b93007dfc65eb08bc615d2bac74a9060d7840953`  
		Last Modified: Tue, 07 Apr 2026 04:13:04 GMT  
		Size: 13.0 MB (13010198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5c2934c18501ce1ef132738f28204db1a5911837fcf013a27a891524643476`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 19.2 KB (19201 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.3` - linux; s390x

```console
$ docker pull r-base@sha256:452bc332522fcd9b65108006d3f712eec103f0ef3bf69a02c3d1f2d29a294793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336666285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c71b509c13a3051596bf375af7d17de83c77c156648f28258e721b7c3ac6533`
-	Default Command: `["R"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 02:57:12 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 07 Apr 2026 02:57:12 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 07 Apr 2026 02:57:23 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:57:24 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 07 Apr 2026 02:57:24 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:57:24 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:57:24 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 07 Apr 2026 02:57:24 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 07 Apr 2026 02:58:25 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:58:25 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:06fdbadcb6481afb3ff06f57eb876e2c2622ce9f86876789a8dfa6db27908938`  
		Last Modified: Tue, 07 Apr 2026 00:13:02 GMT  
		Size: 48.3 MB (48291597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef51998dbea1d3d725064291b6c397c8e4b9fa98d8eed8428de6ed45ec099ba9`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e17c62bcfb65bd3923b823c7de42bb73eab9cadecd312f167e54542002607`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 27.0 MB (27041502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842cb61db307433266ce2c67fe643cec0f8bae2802bf271e7320008fb38e46b9`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802377a313a0ba6a1de6d58fcf0fcee6579e76eadd3784356ef64ca63a11ec8`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7322a735e32a8c64f267f4be453f1eff3514bb257dfd8f5074b4354bc1c3d11b`  
		Last Modified: Tue, 07 Apr 2026 02:59:21 GMT  
		Size: 260.4 MB (260404906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.3` - unknown; unknown

```console
$ docker pull r-base@sha256:5cac6835119f0433ea5a5fd87f4df21ffadb7b04435057ad32b5da083b514b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12846478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a4063d19e6c46bad1c332479d74f26cc34e9ae5cb4eeab925cd8b64b2efee6`

```dockerfile
```

-	Layers:
	-	`sha256:5fb72a44170199e5fe50bc5f39e15154080c05638789dfcb0ec9f666ab3f5d92`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 12.8 MB (12827317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75561746fa992d0cbd0ade573a1dbb94610ccb79ab2cbce16c3a7a115c4bf47b`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:ce88ddcdd15d9901a55439de10791cae3598644c2221332dc5b90dc6ec837084
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
$ docker pull r-base@sha256:136ba9c034cb876c1203137dd03cbc7bc4412f710e1c19de76d8ad93667abbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368131717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efb24b83565f014c44b8615bfa83b201eda23b4ccd5ef8bad4acd7f8e7533d`
-	Default Command: `["R"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:40:32 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 07 Apr 2026 01:40:32 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 07 Apr 2026 01:40:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:39 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 07 Apr 2026 01:40:39 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:40:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 01:40:39 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 07 Apr 2026 01:40:39 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 07 Apr 2026 01:41:18 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:41:18 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:22b89b881e9d5422fc9da3425719efd67131de7d79df86578efa8c704089ea0a`  
		Last Modified: Tue, 07 Apr 2026 00:12:02 GMT  
		Size: 48.6 MB (48587086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d775ff3b26c9776e8949fc9252c4ec201c908e4f4aaaafceb47ce56fcd1eada`  
		Last Modified: Tue, 07 Apr 2026 01:41:54 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f18c5eac657d7b35f2375b062137e3c00708da4da9f00747ccb427c59ae95df`  
		Last Modified: Tue, 07 Apr 2026 01:41:55 GMT  
		Size: 27.1 MB (27106015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5131f03edf7d92cb9f739f57fafc215b5b7d4d9fcde53c60baa9613dee7009bf`  
		Last Modified: Tue, 07 Apr 2026 01:41:55 GMT  
		Size: 868.5 KB (868488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420b49147ad99b9e8ffd588a6e79dabc1dd7398523a1b87b116223a00c8acbaf`  
		Last Modified: Tue, 07 Apr 2026 01:41:54 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce540ee0de8327c539c6e495f1de3a7dce6c8337fb390b25ebfb0b3be05a006`  
		Last Modified: Tue, 07 Apr 2026 01:42:01 GMT  
		Size: 291.6 MB (291566392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:9555901b227b40106a4c5456cffc3f360249423c40f8676c0fa6c34ab469764a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13044746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c3490fd80ccc915588407fddfc793a8cfbc3066e1191a6b5927358fc4f8a66`

```dockerfile
```

-	Layers:
	-	`sha256:db9579c040f306626dc67ca906838314441f2fca88a37ab8594a41b0f5254310`  
		Last Modified: Tue, 07 Apr 2026 01:41:55 GMT  
		Size: 13.0 MB (13025587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508f67c4576dbd1d27dac138c791d95bcc6a77112d4108bb80dfecefecf97746`  
		Last Modified: Tue, 07 Apr 2026 01:41:54 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:4281e2567f63d84f1f3f7251b4a207c00764a9775972e5ce307c378d5269460b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 MB (351398626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c725a2e2dd8af39f4782e48352d0f134986fe66b6045ce8542d1ceff1d2a0c`
-	Default Command: `["R"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:43:13 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 07 Apr 2026 01:43:13 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 07 Apr 2026 01:43:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:43:23 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 07 Apr 2026 01:43:23 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:43:23 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 01:43:23 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 07 Apr 2026 01:43:23 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 07 Apr 2026 01:44:08 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:44:08 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:270e6fb5e8158c645c59da5292196f6d4ac5d2b940fb597c6b350535305ec493`  
		Last Modified: Tue, 07 Apr 2026 00:11:14 GMT  
		Size: 48.6 MB (48643357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a221563de127d80ee61953c100ceea195bfcbd02a31825ec69a8b088e33a6a52`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 3.3 KB (3315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0a86b26e177ff6b8587c1a84acb87ce65f00838184628ad71ff421f5147e30`  
		Last Modified: Tue, 07 Apr 2026 01:44:46 GMT  
		Size: 27.0 MB (26953560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efda2a3a164d408d7b02e7914b886d99a97d946c0810fefc117d3f3d36da65e3`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a5a115834fe90c74514c28c625b0c537ba2d0b454d7ed479743186c790fe4e`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ceadc30f5c52a6cf6b8bfacc7fa9af25f350355689f10986a28798f6c5b229d`  
		Last Modified: Tue, 07 Apr 2026 01:44:52 GMT  
		Size: 274.9 MB (274929486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:635abd99387b60a8c8abb3eca62a3b6c73e31449654f7e66e96587c6df333aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13147134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7a5ef27fed6539c7a904cd992b0a1c2daf4f09acd0b523b82cc80e35e6e2c5`

```dockerfile
```

-	Layers:
	-	`sha256:051e7bdadff29b3563e029464035e28c9d88d374f98454953f2fd29301789fbc`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 13.1 MB (13127833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00dde9f504eb5334e93c6772fee03b7446af71bdf3935fb2bcf1f575ca25542`  
		Last Modified: Tue, 07 Apr 2026 01:44:45 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:aee895497ad35581a322e2400fabc86029af7f96042e850cfaa6f2da711d38b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363942457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56571e3c80320b8f8e91c8fd3f26c1a732d7d0422fbab4ffaeef8b13aa5aa788`
-	Default Command: `["R"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 04:08:41 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 07 Apr 2026 04:08:41 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 07 Apr 2026 04:09:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:09:09 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 07 Apr 2026 04:09:09 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 04:09:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 04:09:09 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 07 Apr 2026 04:09:09 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 07 Apr 2026 04:11:49 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:11:49 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:d2fff16aab3eb8d89b3bdbae0814c0146f162ecacdf526ba2f4a1dfd7b082ae6`  
		Last Modified: Tue, 07 Apr 2026 00:12:16 GMT  
		Size: 53.9 MB (53851239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d244606985c8fba1ab58a562bf3b577b999e2fbb4661310361d28c409a577ab`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f79bf7373af22c1f1d4b77a5e9becb01bc664a3ebf74af1cdb4795e1db927b`  
		Last Modified: Tue, 07 Apr 2026 04:13:04 GMT  
		Size: 27.4 MB (27416201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebddcba1cadd3bf56f1f2fee24ee7524f0504234985824803b5cb26474698b65`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8a2a77cde68fcbea97bb8f109506629e7af424cc643780e7ae507a8658840a`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2544b72dd9dc8236201dfdeece6f90a786590df70ef05effb90c542e6e4daf0d`  
		Last Modified: Tue, 07 Apr 2026 04:13:11 GMT  
		Size: 281.8 MB (281802797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:d74dba730e372cb2e0a56538901a42ba231b99b74ef7e395d115b7dba423d1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13029399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd63f08bead5e9c9a360559d1f19ec5a8ed926385cc6138daac35a40be9b61b5`

```dockerfile
```

-	Layers:
	-	`sha256:8ed8aa891a6804cafb2ae079b93007dfc65eb08bc615d2bac74a9060d7840953`  
		Last Modified: Tue, 07 Apr 2026 04:13:04 GMT  
		Size: 13.0 MB (13010198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5c2934c18501ce1ef132738f28204db1a5911837fcf013a27a891524643476`  
		Last Modified: Tue, 07 Apr 2026 04:13:03 GMT  
		Size: 19.2 KB (19201 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:452bc332522fcd9b65108006d3f712eec103f0ef3bf69a02c3d1f2d29a294793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336666285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c71b509c13a3051596bf375af7d17de83c77c156648f28258e721b7c3ac6533`
-	Default Command: `["R"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 02:57:12 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 07 Apr 2026 02:57:12 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 07 Apr 2026 02:57:23 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:57:24 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 07 Apr 2026 02:57:24 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:57:24 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:57:24 GMT
RUN echo "Types: deb" > /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "URIs: http://http.debian.net/debian/" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Suites: sid" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Components: main" >> /etc/apt/sources.list.d/debian-unstable.sources 	&& echo "Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg" >> /etc/apt/sources.list.d/debian-unstable.sources         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 07 Apr 2026 02:57:24 GMT
ENV R_BASE_VERSION=4.5.3
# Tue, 07 Apr 2026 02:58:25 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:58:25 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:06fdbadcb6481afb3ff06f57eb876e2c2622ce9f86876789a8dfa6db27908938`  
		Last Modified: Tue, 07 Apr 2026 00:13:02 GMT  
		Size: 48.3 MB (48291597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef51998dbea1d3d725064291b6c397c8e4b9fa98d8eed8428de6ed45ec099ba9`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e17c62bcfb65bd3923b823c7de42bb73eab9cadecd312f167e54542002607`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 27.0 MB (27041502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842cb61db307433266ce2c67fe643cec0f8bae2802bf271e7320008fb38e46b9`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 924.5 KB (924547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802377a313a0ba6a1de6d58fcf0fcee6579e76eadd3784356ef64ca63a11ec8`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7322a735e32a8c64f267f4be453f1eff3514bb257dfd8f5074b4354bc1c3d11b`  
		Last Modified: Tue, 07 Apr 2026 02:59:21 GMT  
		Size: 260.4 MB (260404906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:5cac6835119f0433ea5a5fd87f4df21ffadb7b04435057ad32b5da083b514b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12846478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a4063d19e6c46bad1c332479d74f26cc34e9ae5cb4eeab925cd8b64b2efee6`

```dockerfile
```

-	Layers:
	-	`sha256:5fb72a44170199e5fe50bc5f39e15154080c05638789dfcb0ec9f666ab3f5d92`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 12.8 MB (12827317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75561746fa992d0cbd0ade573a1dbb94610ccb79ab2cbce16c3a7a115c4bf47b`  
		Last Modified: Tue, 07 Apr 2026 02:59:15 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.in-toto+json
