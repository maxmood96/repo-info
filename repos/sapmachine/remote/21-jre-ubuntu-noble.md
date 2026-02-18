## `sapmachine:21-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:502b4a7363c3b8b9d60c65c68a92f3cdae907d4109fe93b0b2507b47092b72ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:c1298bb59eb5bbdec182d96331a3a4188a876298ba9230b4dce638fb7fb0a73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90469018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd5b7e0ad5b401f4760e698837b7509c2a22c7d08c36be51b6df2fe810ab548`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 19:22:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:22:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:22:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de8442c4254ec1d924039452799e87a989534265c84481049dd5bdd6f972e3c`  
		Last Modified: Wed, 18 Feb 2026 19:23:08 GMT  
		Size: 60.7 MB (60741407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:451cc0469455cec54a9bcc6e1a90d638c5215b3758f6d7529eb2afeb1613e15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7c55f8246903f4d4a4a78cffcb14c75180086768de99c3e8d3ff141072c0d0`

```dockerfile
```

-	Layers:
	-	`sha256:f998543700317c1e1cb651dba170d28b74dee7e5418a32d8275a4a1439461e8e`  
		Last Modified: Wed, 18 Feb 2026 19:23:07 GMT  
		Size: 2.5 MB (2521068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:887ed89a92222261bfe01db93f2f491dfc2e2253023d048af39043378051f5b9`  
		Last Modified: Wed, 18 Feb 2026 19:23:07 GMT  
		Size: 10.1 KB (10086 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a4a0c3ec9356b5952b04c529db2b2c7e98a97e6eb58ebbc5ab5775567323b278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88798758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a725697f81e381eb94e98b1e7efb15f3ed15731a82536dc74f560225b586d5ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 19:21:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:21:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:21:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035eb000f79d3c724a0959a0b7acdb48a704e874e757d19b9fad7287447cc46c`  
		Last Modified: Wed, 18 Feb 2026 19:21:49 GMT  
		Size: 59.9 MB (59933638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8da93ded44fc8839ba1584546b82bc2ce4a11ec00732095156bfaf50bbd634f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d33b34de187232325d2778959cdc1dd3b0cdd87991c6cf04fdb978f7b6c2e4`

```dockerfile
```

-	Layers:
	-	`sha256:58e5ec34f9e8ced2be04d608c53deebcd1f41ff30d41181362b5ad30e9d23600`  
		Last Modified: Wed, 18 Feb 2026 19:21:47 GMT  
		Size: 2.5 MB (2521584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07411f0a75653cce76aaad27f1ef0aa81f76c2f98311ddfd93f8bd764cdb1ad6`  
		Last Modified: Wed, 18 Feb 2026 19:21:47 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:07f683cafc5715ecc0f9c289421a7e6fddab0e06f830500af460b78be2915b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfea1900d4e142e13063712c468f8a337636a130cc03823bcece3c8c57234c2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 19:15:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:15:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:15:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e697db08fb5c6a04a1a318f75b24e60c4a29dc744827ae10fc5a088c4a7f525`  
		Last Modified: Wed, 18 Feb 2026 19:16:36 GMT  
		Size: 62.1 MB (62077081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6d12a5d1a51a91b35007f9d648a4327f4ac95d33089b4e3e27cc55cbfb17c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fbcee025f0cec13512cd1eba39862aafd0d8b692b67c2321eeba4d1d83f2cd`

```dockerfile
```

-	Layers:
	-	`sha256:f3bec3864034ed1806a47696eca42257aebd8c1900220ad3cc7252e5e6513237`  
		Last Modified: Wed, 18 Feb 2026 19:16:32 GMT  
		Size: 2.5 MB (2520566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79792400613eb2a99d9dc3ce121dbad313de67582f83e391b298e156c72f35f9`  
		Last Modified: Wed, 18 Feb 2026 19:16:32 GMT  
		Size: 10.2 KB (10153 bytes)  
		MIME: application/vnd.in-toto+json
