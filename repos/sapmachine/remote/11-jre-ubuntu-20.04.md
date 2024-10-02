## `sapmachine:11-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:5943b948f8665974a142b84103101984294571794dc9b4141b748c45b7b34dfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:28006515858b55e965e28fc817f1cb70b2fe217a893df906d6b9658c2dc44c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77013603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be52eb7bfda26482f9e0fb45f6ec244c8cea1c60aea99434095705159a244f98`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa7cf78dccff63f694f32b8c64deef782e1a165640d67a6aca07e237c814e2d`  
		Last Modified: Wed, 02 Oct 2024 02:00:13 GMT  
		Size: 49.5 MB (49502551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:460e8fd1a4d0073a6c97c3713fa879cc80d4e9a672476a3d227e7f465fc600b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1c75fc500b75dcc5a5ac0c7d464961b6ff36449925cd7a19efab7da0ef84b2`

```dockerfile
```

-	Layers:
	-	`sha256:e6978112164df1d45ab943f8d4ebf751959f4b1f047e1462d85821723a187336`  
		Last Modified: Wed, 02 Oct 2024 02:00:11 GMT  
		Size: 2.3 MB (2291720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a8847e5b3bd113c7f87973c4ef898bd056fd998c0b2b1585fbda337b3fe7ae`  
		Last Modified: Wed, 02 Oct 2024 02:00:11 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8ddfed6794cfc8686bd432138a31095a957bb0509783c3885f93cc82ef7b528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74790849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812c1150a9123e9b6ec3983f601acbc058eb62ae7cc5c085dee3bd7228c930cf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897243a38981fdd4acb92d45f55531dbc29487a20ef179080712811b4b89d8b5`  
		Last Modified: Wed, 02 Oct 2024 04:10:04 GMT  
		Size: 48.8 MB (48817257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:13ddbe85271213ab71ddf8381782c869f167b6a74d335a708f293a37efbd276a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4bfdee2d3416f1a028a1d539f33a98de6f59bcec4e28c61c8154598214a413`

```dockerfile
```

-	Layers:
	-	`sha256:35ce0e6e7322e80ce4c6ed8ffc09daad34830723c4f1bc8dc7ef885a43fbe8fa`  
		Last Modified: Wed, 02 Oct 2024 04:10:03 GMT  
		Size: 2.3 MB (2291984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbcc1b60c1f44421dfe5e309382ca0a2b16edbd58974ad9536be2feaaa17a48c`  
		Last Modified: Wed, 02 Oct 2024 04:10:03 GMT  
		Size: 8.7 KB (8669 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:016174727da7e22ebe0bb393003eae056cfa7c4c067924ebbd63e4228c31877d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79821862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3db0b8e53965f62e0a894c4748345ca2dd73619b6fea74267dff51ed9816be`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2182a614e4227c3e51b6bca07b68db48a80468603874b6683abecdc7f05e241`  
		Last Modified: Wed, 02 Oct 2024 03:28:57 GMT  
		Size: 47.7 MB (47745528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5acc757ca6622e41f5cd0a36eac1a7b1d36d2501a74c0c28cd1f38f8549fda80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ad3c88a6f373ee32c9fa103230eafe2caf185ecb3242b83cec2d416bd203eb`

```dockerfile
```

-	Layers:
	-	`sha256:2e6c4f8ecb989fc473b998781307d6ceeeb388bdf864d317b7c2edbc16078ff9`  
		Last Modified: Wed, 02 Oct 2024 03:28:56 GMT  
		Size: 2.3 MB (2295491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893d7d21a64d13bdcdfd439f008a2f59f6ddda5629ee4654b858289fb3bc58a1`  
		Last Modified: Wed, 02 Oct 2024 03:28:55 GMT  
		Size: 8.6 KB (8610 bytes)  
		MIME: application/vnd.in-toto+json
