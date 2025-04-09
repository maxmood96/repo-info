## `sapmachine:lts-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:c6b381b84bf5de56abbd9d8612ee1893a95ff121bb9896dfdbbe4e451580c2bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-focal` - linux; amd64

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

### `sapmachine:lts-jre-ubuntu-focal` - unknown; unknown

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

### `sapmachine:lts-jre-ubuntu-focal` - linux; arm64 variant v8

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

### `sapmachine:lts-jre-ubuntu-focal` - unknown; unknown

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

### `sapmachine:lts-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c744236b6e72cbe6b22f4886cd27af89895c9a6df41feeff5365d974d41aac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92544135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebc37e1cb328845ce47cb79b141868f072e583faf3bc28cf2b6ede36d0bd36`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4f8eb21766997318bfde5dad610db0d9f6702fee17f2225367f72baf1c7c7e`  
		Last Modified: Tue, 28 Jan 2025 06:04:46 GMT  
		Size: 60.5 MB (60467629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c50f7f27654cf1f7190126e1d183167bfbac8225eaf95a5fba9e713f2264aeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed4b3eca01bf10aafca557f64154f6b5a7e742f5b4cbff4e1bce1e901f5b5b8`

```dockerfile
```

-	Layers:
	-	`sha256:2012f190821dac4f7772f0622aa4a2ed76ba48429cdf94ab15c4a00c80902fda`  
		Last Modified: Tue, 28 Jan 2025 06:04:44 GMT  
		Size: 2.3 MB (2304900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8ebd5796675487e93f767d9da6a9d4cb3898006ab58e32f519a221ca7922666`  
		Last Modified: Tue, 28 Jan 2025 06:04:44 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.in-toto+json
