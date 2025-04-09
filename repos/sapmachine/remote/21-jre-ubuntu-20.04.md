## `sapmachine:21-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:122709504286d6f9945c510f6c6a9ff24e8ecccaec0db215313efe79f4dc5cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:4ae106c2181057ecdb8c59b2845e377c4a824ad68805284ca75533700fe0a26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86777011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270737b2f5643671956d1faa9e14fddf153d0ec26b24a9b76920ef820d05435b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e7e955ed826242e8a293f0ee75669320ab1d9f7c3318c085072f776629fca8`  
		Last Modified: Wed, 09 Apr 2025 01:21:31 GMT  
		Size: 59.3 MB (59266617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:673b824422091b2009f897bb892896d878c85e1bdfad67132f795111da7f42cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522093eab188cec6fb4a3694557f91c4998e4b965f8839d01795101d6847dc64`

```dockerfile
```

-	Layers:
	-	`sha256:57fee8ac6d009c0e951287dd4cd0c928c72209c9ec2d2b0265b9ac7260d18d63`  
		Last Modified: Wed, 09 Apr 2025 01:21:29 GMT  
		Size: 2.3 MB (2301221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472cd35b7adb1e0d370f4ccc890069c5f9de00566cc9d976a3161379c762a95e`  
		Last Modified: Wed, 09 Apr 2025 01:21:29 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:86a373aeaf46931ffc4f91e51ac27d2c1ca2f8e7391e6b23aefecf4188900e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84418137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce618332710fbaa19b39a47d2bea992e89f5bf8a7be40d6db254a3673ae8db`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08996497c274dea7fc4e853341821af1a98b169d5b984a8249f532162d3544`  
		Last Modified: Tue, 28 Jan 2025 02:46:35 GMT  
		Size: 58.4 MB (58444309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:90af6417200a7c46d6349add821146384fe36a4be37837e4709f81b3bed054f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003e8367ec523d0e8a5c9b2cf31b676304e1240ea2f21bef693c0bbd55cd4f89`

```dockerfile
```

-	Layers:
	-	`sha256:089225c48cff6b8ce1536755e44c77c7b4deae0b7e94125f610aa66397dd8e11`  
		Last Modified: Tue, 28 Jan 2025 02:46:33 GMT  
		Size: 2.3 MB (2300783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df18c3c7a4287e082290c5807d408706f13477c4ae68fa6fb8855612ce1c3f2b`  
		Last Modified: Tue, 28 Jan 2025 02:46:33 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0d381122b0b3d03f31091d74784cc6f76b2fec68f83792056e6b2e4dd440a481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92544521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd06f3a37577c81b7724095be973bcf89eb37851fd213a0ad87eae1ed214e49`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41b16f37b2e483e6feb6ee84788edabd5afe8c7fcd8de1152c48c5b301aa908`  
		Last Modified: Wed, 09 Apr 2025 07:07:18 GMT  
		Size: 60.5 MB (60467575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:12d155a28f3d59b744bf0832842ebe427f0ccf16f26306442bd036a36216987c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b4500688f5269ef7d0bd7431afb45b666e19ac3ceb8474348aa3e935eb0a49`

```dockerfile
```

-	Layers:
	-	`sha256:4524ead280aae2daa268d992efbee8eb23821d136e4f8650219336c43f68ba5c`  
		Last Modified: Wed, 09 Apr 2025 07:07:16 GMT  
		Size: 2.3 MB (2305000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f375a70088f998c8c37394fbe8a0a4c406d40554a04d9b51b75654f03cecdaf`  
		Last Modified: Wed, 09 Apr 2025 07:07:15 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
