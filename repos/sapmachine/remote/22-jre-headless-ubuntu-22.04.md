## `sapmachine:22-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:29da66de1bbffa628760fae29897b630aff9c5a0ca62d70dcfa5ce902ea104ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0b8cd3beb7d54abc0456e1d0da3b87d3f1b02946c15569253695c6da3eca31b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87449141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d104ac8bca11099ce7f2f0c8bb259a3c506796586798a71e7e3df3bc4a581e4b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d22069c460f493036754c7f97de80b5664f808367d9028321fe23b93d4ad2f`  
		Last Modified: Fri, 19 Jul 2024 17:59:16 GMT  
		Size: 57.9 MB (57915086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eedfc4b8207e5f636c9f5cf657731d15c6d6bc417b258a31f21b1c2df72bd532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e177a600e0d19e72914862869cbd7886a28b23df2c39575198d9ac64c856d2`

```dockerfile
```

-	Layers:
	-	`sha256:2152e83fd6efb6b361bc2b007c2116f9249c751760de2ab6be6ba851c9787f22`  
		Last Modified: Fri, 19 Jul 2024 17:59:14 GMT  
		Size: 2.1 MB (2148130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a3391de00a00a3d97a8ec46d9310b286f094e15b7e3a521d328b356f6e9517`  
		Last Modified: Fri, 19 Jul 2024 17:59:14 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:bccb240168f7c89da447c300f33771fabe03ab0768246a8d21dcdf05e3702f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84465623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1291e09b2d34080640eb0d8e4b47e3589fda14a75680083cfeea15f72cb84fa`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7d2bba0a01c510877f456fe68b1e765b80510cca8a5d69fd1d19e860cf1499`  
		Last Modified: Tue, 02 Jul 2024 23:57:38 GMT  
		Size: 57.1 MB (57105598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:046586d2c76a53b8b83d38980ff841ac619795123dad3ce39760a8010f3b7744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3d995c63eadd98a2d08446e40acbd433521906033f15342ed9052be597d5ac`

```dockerfile
```

-	Layers:
	-	`sha256:779c551fec6f6f22cda8393920cb251e185784a02803f33308c44b57dba869d6`  
		Last Modified: Tue, 02 Jul 2024 23:57:36 GMT  
		Size: 2.1 MB (2121034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:483abae09207329cf458fe82047d4949fd47b03e6f125442b32ba080e564af4a`  
		Last Modified: Tue, 02 Jul 2024 23:57:36 GMT  
		Size: 9.7 KB (9700 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5ebc3cc81c19f43f5a88670b7b1c63f99ba55a979fa275fc307b87af59fa4182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93829772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca37c8a29b4e39f63c4436cfa57524499f085c88a9a40b88b3cdcb178647b3b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51259b9fed21f163a9934ddfa10eaca7a5f415dcc0e30ad8db3822f46c764d3a`  
		Last Modified: Tue, 02 Jul 2024 21:23:44 GMT  
		Size: 59.4 MB (59368691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:776040d14e0590d5a40973b957731cdd03ecca1e4929eddfff8d70ed0a816718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4098a8b691918ee7c64a7ebf7c6e3a6a9cd5ae5773f3640dcf87abb7684e7c4c`

```dockerfile
```

-	Layers:
	-	`sha256:be199e5fc50879d62432dbfadf0c162cee48a6f683a9f3072bb584848c8429ff`  
		Last Modified: Tue, 02 Jul 2024 21:23:43 GMT  
		Size: 2.1 MB (2125261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aa9cb4e157bb090e95ecf8df9d1ae1347c1d63e7b2bbca56ad67ff8b3d2a20d`  
		Last Modified: Tue, 02 Jul 2024 21:23:42 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.in-toto+json
