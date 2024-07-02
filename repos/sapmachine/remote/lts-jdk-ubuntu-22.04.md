## `sapmachine:lts-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:950af7db94222c07a1da9db98358066532a30b53c35a6cf7012696e35feec07d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0dadd3e7e0376e65fc0f1042838f4cce18514d52a57678d5c0650cead06b66fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244605096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ef7b1393b8e9d90cf08428b85338ca28f6c588fd17affa21016203fbfe3ef`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488f015eaa0c4b57c8656d6a8e84010c13970aee4201c13af793ab1bb4e77dc6`  
		Last Modified: Tue, 02 Jul 2024 03:32:08 GMT  
		Size: 215.1 MB (215071041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7b939edae7ccc2b49fd8da14a362710f75e9b52eeb20c39c86a3f53a753e555e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7659319105e0e7b6a17f31d46ef0674618b2568a47d5a8c02c9b33b734fc90b1`

```dockerfile
```

-	Layers:
	-	`sha256:69d32a38d71abb297dcd75c2ea346fd3209b16839c66628b38ba449d9997fa07`  
		Last Modified: Tue, 02 Jul 2024 03:32:04 GMT  
		Size: 2.4 MB (2444960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:995ed7f9dc827e13d7860a911c54c61dec777b601cb801edcdf3d0958fc16c9a`  
		Last Modified: Tue, 02 Jul 2024 03:32:03 GMT  
		Size: 11.2 KB (11209 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d9d358ab336e4ead02db46ff625f148a5d8d5a267fee820a45d7fb57b15331a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240481994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed9ba7df37648061161b6b24a548529ce034799603f2ea873c3d3b281bde807`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a848d38bcbce76ab42f0c5becb6077fd33a5d8945e9cf84feafee03cd748fb`  
		Last Modified: Wed, 26 Jun 2024 00:06:52 GMT  
		Size: 213.1 MB (213120212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08093ea4bf1945574e99b57ef0a091a99195ba1aa177570f0b4b8b33745a0ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2293d0a454c7457f00e2fcaaee3a6193aa292554d6be26b4dea85804aaa673cb`

```dockerfile
```

-	Layers:
	-	`sha256:f381e8ca1307fc869ea4187d12f4f53e77fc6c3f041e8e20ea6b83edf6fae9dc`  
		Last Modified: Wed, 26 Jun 2024 00:06:48 GMT  
		Size: 2.4 MB (2444736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a7d535ba6f5317e5900e491f76131dc29beae223ad8e435c98d078faff5dc53`  
		Last Modified: Wed, 26 Jun 2024 00:06:48 GMT  
		Size: 11.6 KB (11605 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c3fdc1e369604b10b76d91cb5844598a78184b383c39f610948cb908b3253dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250842125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3873275ca440dfad4b0c954c66b642bc591ce7166b0761f1996f2024ae38fbda`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba829c5a8e359969f5c851aec724d2e76a139651dc9208d6aab68b5a00308c4e`  
		Last Modified: Wed, 26 Jun 2024 00:33:39 GMT  
		Size: 216.4 MB (216381432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ee06893e1a525e7fcf0ee8c655cda1d09562fa4599786df1f645ab1380d79b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b61c40203215e31e70253ca1047318f6a5d98cfdcc80094c5e2ea0aa3a2212`

```dockerfile
```

-	Layers:
	-	`sha256:d7688419982714b53160e169cd38712c86aa4a45b1ffba7a1cfb4e97689c65e0`  
		Last Modified: Wed, 26 Jun 2024 00:33:34 GMT  
		Size: 2.4 MB (2447038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5af042d3f0aaf9a857ee58fe8425b8aa517671038850e6ca33ec4b77cd3df8c6`  
		Last Modified: Wed, 26 Jun 2024 00:33:34 GMT  
		Size: 11.3 KB (11294 bytes)  
		MIME: application/vnd.in-toto+json
