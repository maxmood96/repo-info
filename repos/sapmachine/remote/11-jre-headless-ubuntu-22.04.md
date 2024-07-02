## `sapmachine:11-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:d5bd164a003a776385884259e893455b2bc6a07328c8f3f10d907e0f78717067
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6b34e95404e4cbe5d387660e60c4ad92ebf73ba3018d7f95635fe5e6e303c797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78254864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c21a92dc0c0a8c5c5d54ead50ff8f3e19d03052ef4a2c44012c849f2444da6b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26ee4777de66efba86aba53afc32ca26b2b01c790f6f6860503f71ac77419ec`  
		Last Modified: Tue, 02 Jul 2024 03:32:03 GMT  
		Size: 48.7 MB (48720809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4e0585c3fc227dd25373e8b5c0c5406ec78250065832204545a541b7eeeaf636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2197e6e44b95bf2c012fa6887a3d17621b9001ac77210ae650990ee45c418194`

```dockerfile
```

-	Layers:
	-	`sha256:1cb888db6fdf753db9a678707c3b6aa03d3e0084c8bfad0e65fa2a9fe04d0b0a`  
		Last Modified: Tue, 02 Jul 2024 03:32:02 GMT  
		Size: 2.1 MB (2132091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6900b26b3ad3d90de1e76e1b435d4d180014acc69e5d446cb1728c91122e535`  
		Last Modified: Tue, 02 Jul 2024 03:32:02 GMT  
		Size: 8.7 KB (8695 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:011955ed4fad4a0331b5ab4cfb339d28a14cb714abecf02993ab52acd1c97546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75368047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9a370c5347cb6a2eff8946f37ac9dc6677251bd4232344677bdde11a4d9248`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ed1aa4e599ba5b2d88a80a40462db6912e527110987e0666078cdb7b32a418`  
		Last Modified: Wed, 26 Jun 2024 00:34:36 GMT  
		Size: 48.0 MB (48006265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d0666095fb392603f32a65bfc0539338f6088b83ffeaa1657bfbcf993922c8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b700948c89b37e73061b194262cc859bd076e9b8b27010d4c8ed134644db7c95`

```dockerfile
```

-	Layers:
	-	`sha256:62cd8bcd9faddf32b1a3d59d3cf6545a9cbcca60711f59b58d83834a937087d2`  
		Last Modified: Wed, 26 Jun 2024 00:34:35 GMT  
		Size: 2.1 MB (2132389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:319e94e171e003be208de5d702508675657ad46409b32707cc10cadab5bfdcee`  
		Last Modified: Wed, 26 Jun 2024 00:34:34 GMT  
		Size: 9.0 KB (8997 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fa6d0eb4dbc20e326eb8b5c1df72de4bb5c35ce27528928d683da1405ec5fc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81634453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2013fbadc829a2fda2837cb61da87756f6fa9669a08455be3aa36ab30de85`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223778eb8cee0bd29633d3b6edd4b9b73fe9e67c4aaa30907c090f343f46ac4`  
		Last Modified: Wed, 26 Jun 2024 01:18:41 GMT  
		Size: 47.2 MB (47173760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2f5f923fb1807e340f43c6627bbc6685c6423139b09292f7dd724614581d0fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2144738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a474e02491bc974dcf59b047da5091343c1c6422115eb89c07ac75f99d84f1`

```dockerfile
```

-	Layers:
	-	`sha256:5ee8d1428356faedda7eb638fd914239b6c4f382a9a2213054fee06e69c62e38`  
		Last Modified: Wed, 26 Jun 2024 01:18:40 GMT  
		Size: 2.1 MB (2136006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca25854690e2b004c209a98ded4ff617dfbec31c13902c206205c31ae5c3dbf`  
		Last Modified: Wed, 26 Jun 2024 01:18:39 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
