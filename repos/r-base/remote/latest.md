## `r-base:latest`

```console
$ docker pull r-base@sha256:1dc9aea7bce8f683c4d5534a5f112dae48842a66194385d3b253ffdb016bda24
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
$ docker pull r-base@sha256:082c2466bc3ab052ea50a49b4d0609e3e80e546d7379ac731bbe01cb9adf4594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.4 MB (359417769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1abc4bce0dd0812cbe7cf2919fbda10664249313aa381be4df803d15dcd13c`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1736726400'
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
	-	`sha256:6b9b09e5bd5862e77d8a11756f2940766adfbf008b1b99f2e5908ebefec90b4c`  
		Last Modified: Tue, 14 Jan 2025 20:38:00 GMT  
		Size: 48.3 MB (48276087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d6ca7373ac7962bba9e3c37f460445edd6ca78127a197f59f8fa3520e0a37e`  
		Last Modified: Tue, 14 Jan 2025 21:19:21 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8698d3b91b4a836957ceb2cdd3963961d3725595cbbbbbf82fb39ab104401237`  
		Last Modified: Tue, 14 Jan 2025 02:17:53 GMT  
		Size: 26.7 MB (26697492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ca80362d9d8303fe73761a7cd36f8f126bd3a270554134f8fd40f76ead2e07`  
		Last Modified: Tue, 14 Jan 2025 21:19:21 GMT  
		Size: 866.7 KB (866744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3032d075a01ab10fc67f1eeedb94bfaf5fa8baa0d15de2b035cbb3459ddb26`  
		Last Modified: Tue, 14 Jan 2025 21:19:22 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df070c6530cee0551e417ab4d0b8462ed9a52202fb74c4c25152cc75082fd4df`  
		Last Modified: Tue, 14 Jan 2025 02:17:58 GMT  
		Size: 283.6 MB (283573788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:a7887dfe7de7aebb2121cfe133ec34a8a0494695bc3a4e955d0f619e1c9a64f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12642035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe755426c93a7b6b1316aac58b6ababba85b1af27d6852456d063137a4aab288`

```dockerfile
```

-	Layers:
	-	`sha256:ee9c016553c994b54be27de815cb527e595acada466aa931585cf1c01a67f978`  
		Last Modified: Tue, 14 Jan 2025 02:17:53 GMT  
		Size: 12.6 MB (12623894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9d87528bab14deddd39beecea81f200acae79f527e3d692a8c2979848f99b15`  
		Last Modified: Tue, 14 Jan 2025 02:17:52 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:d8a5128e0bf1017eec19033c48920b94330b0dfd9d66411cef6838299dc4eaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344938305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8517a5c26c117a3c741340035b6e3760d17f3becd75e66fc0bc4e4b0bbb265f0`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1736726400'
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
	-	`sha256:815bead3f6991928b64cef505ed69cbd5a441a6bd7c3256bb2cb7ef03b7997c1`  
		Last Modified: Tue, 14 Jan 2025 01:38:19 GMT  
		Size: 48.7 MB (48661504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a13b5060d496ee306894c2c4f7c558068796c91e9e2a477414fd07c2856984`  
		Last Modified: Tue, 14 Jan 2025 06:22:56 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b086858fcaa976202d7f66d0238c3425e2432ae5dd2f1aaf7c5c0c5cc66206`  
		Last Modified: Tue, 14 Jan 2025 06:22:58 GMT  
		Size: 26.6 MB (26601123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f61f4e7b136874bb264f09ad2601f26fa1eb05ec22bca3173d0b6bcb4cc8851`  
		Last Modified: Tue, 14 Jan 2025 06:22:57 GMT  
		Size: 866.7 KB (866740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bee86b5458d18ac9e348c1e91784475f0658981fdce78d6c746de8b99d7923`  
		Last Modified: Tue, 14 Jan 2025 06:22:57 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d317228a623b822403f301228908e01e04d09d5750c423b59a8e22c96e0d40`  
		Last Modified: Tue, 14 Jan 2025 06:23:05 GMT  
		Size: 268.8 MB (268805280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:499156f8ee8d2c303acc67792431a1f5d4b52149a040744818e0b0681069e880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12745524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d082bb8874bd7f458dc4f21c3fe42c347383816b45d70c1b06d061a4daed5a`

```dockerfile
```

-	Layers:
	-	`sha256:f5b748b6a8a5f3da5ec44595edfb61090ee42207b4ae442add727ae0e97df7a6`  
		Last Modified: Tue, 14 Jan 2025 06:22:57 GMT  
		Size: 12.7 MB (12727244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb71536fe57e778fe097ec9112033abb97cd9a4a20282544790285ce5116dd3`  
		Last Modified: Tue, 14 Jan 2025 06:22:56 GMT  
		Size: 18.3 KB (18280 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:2614d12ed9a421361c49c49206778dbf4788ea2d08753c96400a54fac2559deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354461252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdab7ac64e4e4c42a7d14e77d15d5abdc60152f0e792efbaa142c67a400af12`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1736726400'
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
	-	`sha256:2af2e0cc696c39045cef14b1e616df607fb1a880e337f0e0e1a99c9469aead80`  
		Last Modified: Tue, 14 Jan 2025 01:39:55 GMT  
		Size: 52.0 MB (52043128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b70bc1b4f8f316356005d2e1851ad0aadd4764be4bace9d2b8451bab0ab5c7`  
		Last Modified: Tue, 14 Jan 2025 05:04:02 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7c3055221d6620dea77e0221147c311580c007cbaf035468bffe591e6f6ebe`  
		Last Modified: Tue, 14 Jan 2025 05:04:03 GMT  
		Size: 27.0 MB (26957128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0542cdc1d2dc953f21d6a67c121701c4beb6350a98b672396673816c7b6698f3`  
		Last Modified: Tue, 14 Jan 2025 05:04:02 GMT  
		Size: 866.7 KB (866744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688b2098afa9d456d43c21f4aa5126731a266c5ee38d0aa83dbf45d79f0fab22`  
		Last Modified: Tue, 14 Jan 2025 05:04:02 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984f2fd149b92d897edbaf261ccde901633ceda3a3e9fd41a8713594309def7f`  
		Last Modified: Tue, 14 Jan 2025 05:04:13 GMT  
		Size: 274.6 MB (274590591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:538b19f41a52c4d689bb6b5f8bc1c26310ff0f08806a674a7eaf30d9f3f1bb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12641992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1cadb18d97ff606c72bd4330b77c31946149cb5c5bdd3618357bc8a47b7b4e`

```dockerfile
```

-	Layers:
	-	`sha256:88441e19da87f123542de7ab0100c68525c057f5d32e8526075167b2c4abbbf5`  
		Last Modified: Tue, 14 Jan 2025 05:04:03 GMT  
		Size: 12.6 MB (12623812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d36902c5b06edf27dd131a36131a250fbb8aa3c1bf613b3b5fbde6fc28add6ba`  
		Last Modified: Tue, 14 Jan 2025 05:04:02 GMT  
		Size: 18.2 KB (18180 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:5ff67bde4dd0dd27acec9337e78a554298b8dc7ca809b23d5b23928715f2ac48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (327021805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73d007a2ba627de9c398a5e265d45028c079e28fa3fd5c5d9c1d15f4293eb37`
-	Default Command: `["R"]`

```dockerfile
# Fri, 01 Nov 2024 03:11:38 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1736726400'
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
	-	`sha256:44a67b26070060f0727a3c7840a2ae53f8a453471c9d7bc5e966fa51b11cf84b`  
		Last Modified: Tue, 14 Jan 2025 20:34:28 GMT  
		Size: 48.3 MB (48329735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea494f9c20b17ff3e29b12b5cb7b071767d082ebaba97c9c34ff3e01716bbdd3`  
		Last Modified: Tue, 14 Jan 2025 04:40:03 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48129d2e5217c4b742321599180014ffd3344308780bf9acc5443feb442f8e49`  
		Last Modified: Tue, 14 Jan 2025 04:40:04 GMT  
		Size: 26.7 MB (26668591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c57cf2c92a85ac7dc99798f2feeae611b160316946a7072977ca72e595dc5a`  
		Last Modified: Tue, 14 Jan 2025 04:40:03 GMT  
		Size: 923.5 KB (923489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c8bb5143e09f19fb11c7190b913a8c675758c1dd6e2f495a1709242f1a0a9d`  
		Last Modified: Tue, 14 Jan 2025 04:40:03 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ec11c55d199138a94a1b8a35369421edc8470ea0c0640eb8e34bc8553ca3d8`  
		Last Modified: Tue, 14 Jan 2025 04:40:08 GMT  
		Size: 251.1 MB (251096331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:b9c9e6a0b23a70d0166eef5f6ce8351638a938882ff2194c53acd29b734a1344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12448955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844df5103bfacfeada42cea952ec8824b73f941499bba39d90415f2449cf224d`

```dockerfile
```

-	Layers:
	-	`sha256:dbca7338bdcb21b31c022d080411ea02969a3f46f31c70e82c4c9ee2e8470f9e`  
		Last Modified: Tue, 14 Jan 2025 04:40:04 GMT  
		Size: 12.4 MB (12430814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b5f99c84579321289f777300541d3c5f4ff5ab46242fd795211decd32d52627`  
		Last Modified: Tue, 14 Jan 2025 04:40:03 GMT  
		Size: 18.1 KB (18141 bytes)  
		MIME: application/vnd.in-toto+json
