## `sapmachine:25-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:fc8b4fadac19f1bce1111cfb870184c2abe9cc5b0f491057084c98e4a16ee0fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:2421761944056fa2226ba2f4a2ed6b77dec67c2b86ebcae300c3122e05824a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86203366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1959cbcc8b4e36a615b1dbed9d61847ad5feaecf13ba0003346940361955807d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 15 May 2026 21:21:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afdea5bf17dc9694ecab42867f2a0b1648e1611ea2d34193eda688ebccfcfe1`  
		Last Modified: Fri, 15 May 2026 21:21:46 GMT  
		Size: 56.5 MB (56466682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e2013f3af444475515a86da9e8e21b91075b048dabe604bf49822fbee280348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6088aef506a92723316f2e5c5bc7bad682b7150f634d01b6342c7a1eba879c`

```dockerfile
```

-	Layers:
	-	`sha256:8814a9784c67715f1a8c8adca9d63f5978e9826a14e080ae94d6c8c4423db37d`  
		Last Modified: Fri, 15 May 2026 21:21:45 GMT  
		Size: 2.3 MB (2302993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f07136d2c11f43a12c4b1c2ceaf65b84ebcd6ab9857faeeecf28d0fde79b52e`  
		Last Modified: Fri, 15 May 2026 21:21:45 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0d5ff072597e9cd74315196274c865175c46a0745592e126f2ee5e7da7206c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83008462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9416c8c14e3605e234f91d8b56ff92405d5a1568b7b3440832d369124234a51d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 15 May 2026 21:21:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d82af4941cde058ed90c4bd7a41087f6f7d673eaade88f58b9889c053f21fdd`  
		Last Modified: Fri, 15 May 2026 21:22:08 GMT  
		Size: 55.4 MB (55401839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e362623c37f2319c6c6e7dccf2c14d345b8042f9362570768d5b93a97254e22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dac56e5c13e904b62cb546dcdbba9b5bcdc4e4ee0782db70343bc996b3318f`

```dockerfile
```

-	Layers:
	-	`sha256:61604e66ce775138a358375dbf277cbf96a23a39634301248b21404e17250809`  
		Last Modified: Fri, 15 May 2026 21:22:06 GMT  
		Size: 2.3 MB (2302686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9019f40ca2cbf9deb263ef97e1731665d8d66c4b64c5a7fbdb24238e9adb00`  
		Last Modified: Fri, 15 May 2026 21:22:06 GMT  
		Size: 9.7 KB (9712 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:564fd5d441d9fc86259c9e59ea12974c2fc6176e5cd477288fb3b6943ecd7591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91724696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3ef5aafb49e6034e8e0f1913f5c5094c2c75c0083a2358da7796c748eb4925`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:38:05 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:38:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 15 May 2026 21:38:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f56ba28f12babf340638de823a0dde80f36a3f6c895932f9c0650d95b142ce4`  
		Last Modified: Fri, 15 May 2026 21:38:37 GMT  
		Size: 57.1 MB (57077976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:06a9ed1b414099c7eb020fb6c4d02b5103b4daa225b5089e51709259bfec2089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454ec37b0952077f95d508b2c643937235fd1c1fe7bc42a9b224f258773b49ab`

```dockerfile
```

-	Layers:
	-	`sha256:ddab7b8a41d105611db254fa0f732386f255394e8b4f18f3edaa669d09bffddd`  
		Last Modified: Fri, 15 May 2026 21:38:36 GMT  
		Size: 2.3 MB (2301817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4790f6d47e9552cfef64bb58fde1583db8806390d96be9142e7a02e831e4c7a`  
		Last Modified: Fri, 15 May 2026 21:38:35 GMT  
		Size: 9.6 KB (9640 bytes)  
		MIME: application/vnd.in-toto+json
