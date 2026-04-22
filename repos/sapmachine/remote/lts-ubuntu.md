## `sapmachine:lts-ubuntu`

```console
$ docker pull sapmachine@sha256:13a545a53a066eb20fdec3464a5542191813775a824a756947a663399834033c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:38f01eb978d4e65e7c42d30d118298ea5b012132f61945e9fff16124b7291afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6411313a8bf3187f1509f1bffbdad2458745b66f5cf8a5735d57a37968e8024`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:03:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:03:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe89b5c4a3bd861f4dd6d16089945ab0b061e1a1a0d9e1b858a526e0ebf40c`  
		Last Modified: Tue, 21 Apr 2026 23:03:53 GMT  
		Size: 222.2 MB (222185103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:39d5e9baf4b5733fecbd01159389fea874156e4613e43502f8f59b508c87e25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1645585bb34db8bf41868cb7853c43ba5f28675c4c85ec2ffdffe65403b64be3`

```dockerfile
```

-	Layers:
	-	`sha256:5df1b7e0a637a47703c245b0dad3e6533a03028f75fc3b69d03abb42a45d8c5b`  
		Last Modified: Tue, 21 Apr 2026 23:03:47 GMT  
		Size: 2.6 MB (2599461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06fbebddcef77b37958116bf9076f3c24409c43496da145c307e54da1e1c377`  
		Last Modified: Tue, 21 Apr 2026 23:03:47 GMT  
		Size: 14.8 KB (14842 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3e69ce75c66998663a371f49d27a94cdf83a4ad0820b946dd8ca8486d30a566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248866285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d016d191880cc5709d1ff6e25b4ea5760ce027b6b7269dcdcd5812b5375162`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:04:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:04:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b2565ef4daff9da8eb2ec43bc93c9094fb39f959a542afc23787d6a927964d`  
		Last Modified: Tue, 21 Apr 2026 23:05:00 GMT  
		Size: 220.0 MB (219990500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e8a6171d77a7579cee7cae5a2737945ab25982b85ec4468ab888e87d28f2e2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf210814fb070fef63538b07cbd6ba18ccd9681ba1977b7c7f378e46d66bc4a`

```dockerfile
```

-	Layers:
	-	`sha256:029f398da93443d1140c7bbcd623bf2d7cca0d6c58c8eff54e0de78532337220`  
		Last Modified: Tue, 21 Apr 2026 23:04:55 GMT  
		Size: 2.6 MB (2600154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3531b7218bca7e8d37811a6dbf4b05b2efc0ee157df626a239aa5a4c6cdcba`  
		Last Modified: Tue, 21 Apr 2026 23:04:54 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8333387541168f14546146d7cdb2f5a4095c0e8aeacb3ee4e52dbf25c60d2284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256666228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c909133e2acad36f332db087ea38da5446853aa5d48ea6e6869bd0aba2054f30`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:26:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:26:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 23:26:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f9b6b8049499a8cb46748347013393bd725969caa313978b9f1d5d15879e22`  
		Last Modified: Wed, 15 Apr 2026 23:26:53 GMT  
		Size: 222.4 MB (222352050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:46a8e470d44e24cc1c1a0ebf9c6ba54b11db6587b32253d1c30254f4639365b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2610851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d77db00c8220cf1b25123163332c44997d848c7b7e90a9096c76cc87d56b7e9`

```dockerfile
```

-	Layers:
	-	`sha256:ef8ffe0f270ee6fdbff6e136bb6786fbaa08bfd2797e073410b33ce8093a4093`  
		Last Modified: Wed, 15 Apr 2026 23:26:49 GMT  
		Size: 2.6 MB (2595851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825e56a05af965fdd3a6333ddb5109b5e68ccf281a28710faf0b533879404ac5`  
		Last Modified: Wed, 15 Apr 2026 23:26:48 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json
