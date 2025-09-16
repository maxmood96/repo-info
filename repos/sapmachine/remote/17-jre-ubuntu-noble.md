## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:4964750bd195240c5d800b5ab0c2b40a5a40b692f6d995995a93ad1e9262a540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:5683bbde8f32fc28736e154d139b103c0a24891d2fa3c9219997c991b8c88a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83978991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ca7bc75dcc1a22e4c8a7a7ba7dfb32f1c2ccf4f32df7afd0ae254c73775e6a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a372870545edbf944a6a55d21e55bfd431378ef4ec2a2680a1a87118aa00ea3`  
		Last Modified: Mon, 15 Sep 2025 22:28:01 GMT  
		Size: 54.3 MB (54255541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:564191e4529f390c8f55b94ba82e92f503142b9d738d9fbfa58b47498a6b2227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd744339c69ccd9d98cc82bf98dcf41569a3608ceb74f630cc0e254f131eee94`

```dockerfile
```

-	Layers:
	-	`sha256:54a932adfcd96a17f42bfb24a58c00f929ce8a3deaa93dbaf7ff39fb561a75af`  
		Last Modified: Tue, 16 Sep 2025 00:06:18 GMT  
		Size: 2.5 MB (2517386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:863ec887071963eb46dc41cf61b4cddc62a686ae00681ab3a935438871d5b349`  
		Last Modified: Tue, 16 Sep 2025 00:06:19 GMT  
		Size: 10.1 KB (10093 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6ab3e94009872a451f2e0882260933bd7acc4e5a212d6edbd6eaa8af81eae4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82547353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd2ef3b70f78b3328d0a65cf56cc34ea430f52aa614a5957eb8c3b0ad533150`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d13fcf5e68816da45ac532f9de58b47cf8809e262dff27c39fef63823e7cd4`  
		Last Modified: Mon, 15 Sep 2025 22:26:34 GMT  
		Size: 53.7 MB (53686036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aab0fddff443196378400ed46ec3ab2442878fc04481ed11be7d35c884382ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8310fd198b1a80d9ebdc8e55149245bb37f834d70427cb4d43261a417fd15c8`

```dockerfile
```

-	Layers:
	-	`sha256:cd6a1a2f6e295d106c591023d4c8d475fcb1937e59d291811cbea5ecd39ffe4d`  
		Last Modified: Tue, 16 Sep 2025 00:06:23 GMT  
		Size: 2.5 MB (2517902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0932a0309584b3742f1aededcd052e652afcd8ede9683c5d9f54082ba3225ed`  
		Last Modified: Tue, 16 Sep 2025 00:06:24 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1e73daef899f2b87fe6f34f840c280dbafd0a0c2fc77e6f19b36e6d680b37d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89776667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f03491c42a9cc78b56f76006884541f48947a8baa9c7dbca57c5f115453063`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0a6c511c47b4532acbf346237df1f7e829ef289043a065f9adabd23f087a12`  
		Last Modified: Tue, 02 Sep 2025 05:15:44 GMT  
		Size: 55.4 MB (55447134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e0957ef0273113f0f3e902bbce7a54319ea9fad8dab6d754f92f811c0bee3b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2525623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4f311f599a68b77b991b22da418058432cf4bc037f3444ce2a76351e3af074`

```dockerfile
```

-	Layers:
	-	`sha256:f095305184eb716741312911861bf4970a362a02ecfa94fbdc7fa33917c37134`  
		Last Modified: Tue, 02 Sep 2025 09:05:07 GMT  
		Size: 2.5 MB (2515463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3755ce707a1e565fc4c181c9c4f09d9332f22d884c51ec2df07760b11683e79c`  
		Last Modified: Tue, 02 Sep 2025 09:05:08 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json
