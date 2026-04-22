## `sapmachine:jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:6f5c41516141373c894b9141f342442d0beb68bc3a948d14b23a7b34277c5bae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:90c229871207c30c62315d7b6b29e3819b955ce018ff15b382f4405bb1179a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256110262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b11b084fcdd9b0d3a144975760fef22b1bc5a27142ecc8863e41c00d57f7`
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
# Tue, 21 Apr 2026 23:02:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:02:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:02:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bd5ba5e4229ebae4f482a5619f459b100f17fc3e353a279b4e2a920cc8f8a2`  
		Last Modified: Tue, 21 Apr 2026 23:03:14 GMT  
		Size: 226.4 MB (226377284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:61dba082eb1d6ac6242e320bee76a82fcbc9598842eba1877c82b5c39b8074b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc762aede099f0948e591d786d6cd9fc296e4cd9533b9f90e10cb5288a59d18`

```dockerfile
```

-	Layers:
	-	`sha256:c402bf0c1b27ee391294f25b714a69501f55425ccb9a3eb48eeb7cf8aa043d47`  
		Last Modified: Tue, 21 Apr 2026 23:03:09 GMT  
		Size: 2.6 MB (2597186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de97b224840466e9af1c9f95389fa35b42eb9c6533ebd1440b774c5760d17955`  
		Last Modified: Tue, 21 Apr 2026 23:03:09 GMT  
		Size: 15.1 KB (15100 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0381cd90b31c9d732cf7bdc1b800d69ec9da5259f5f1fc27281c1b5cff4e4a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253122117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bfffc27212386e21b809971a8d1b03ca267828c6bf59d237bbc0fc47fbc5d6`
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
# Tue, 21 Apr 2026 23:04:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4613ade7e3c3f607887e589b004a1d8c1f4273d12de89cf733d2eb506beef91`  
		Last Modified: Tue, 21 Apr 2026 23:05:20 GMT  
		Size: 224.2 MB (224246332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c4e334b27511bf4a7e2a3d82a3ab623c6fdfb9803d37e8ec7d21faf17b3b851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906a80f84faeb412355828701a5aba7e4b318d4a8ebaf7504db5c49f13f83f42`

```dockerfile
```

-	Layers:
	-	`sha256:77ea87fc6aac0873820d534f2d7d496a28f8e5b2c1e82cce50059414f47ebcb7`  
		Last Modified: Tue, 21 Apr 2026 23:05:13 GMT  
		Size: 2.6 MB (2597891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24baf751b9751c7d85c8dd22831ebf12dcebed11fd2461f8b94dbdc746fa0a89`  
		Last Modified: Tue, 21 Apr 2026 23:05:13 GMT  
		Size: 15.4 KB (15444 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:306330bd39400f647b64a45d7f1c6cbf1a2f6d09f848574f2a40221c4f7bd98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261954601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c928766f0cd0a132537d0af0ab44828ae368dc0d7acfa327796f439738afba5`
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
# Tue, 21 Apr 2026 23:03:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:03:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778bbde58a3ca229166e8cb0daa518b00e18094f931f78db9a7788514823012f`  
		Last Modified: Tue, 21 Apr 2026 23:03:54 GMT  
		Size: 227.6 MB (227640423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e7511814e23191aeca27120a7870d1eed65fe924aee08c3ad5d93fcce1db21e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2609480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056b4d36d6d495b1d37a5d58d0199d47f9aab31964caa77117b9cae2334b4f79`

```dockerfile
```

-	Layers:
	-	`sha256:f52dac13f06b7f7689365b955ca88d7b3d80cb2c2c7469f5aa3cd0b5ab2ab028`  
		Last Modified: Tue, 21 Apr 2026 23:03:49 GMT  
		Size: 2.6 MB (2594216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31fec8b547a7ba793021bfb83b5e8bb57aef3e3268d776fadfe29af21d3b276`  
		Last Modified: Tue, 21 Apr 2026 23:03:49 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.in-toto+json
