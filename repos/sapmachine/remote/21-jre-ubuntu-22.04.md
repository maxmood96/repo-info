## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:f35a92f5488040583f7730fd94691ee9ed244270e3405c15903e04c5aa2206a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:210b232f53438838d5a98b2f8be8ee359d9b52c7498bcbe3498173c8fbd36806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89361177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1097fa8312694ab0ea72f430608fcd93afabd326770b35386d1d450bb98eaf18`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e805af9f631f7405e404c4b1253971d8b347a8532ade73cfc1815068e9b49449`  
		Last Modified: Tue, 02 Sep 2025 00:25:07 GMT  
		Size: 59.8 MB (59824242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7aded4514f9aa15d04fe6c2d3929c22ef409793deaaf391afbdcbf563e0bd4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa760eb214742023f122b0aea32ecf0f1981bd6624d98f32c1e4a488bbe4f0b0`

```dockerfile
```

-	Layers:
	-	`sha256:48ebff7cc00dfe835f7c0340e22fb5e763104f8b86ea64b924300f62d3a70aad`  
		Last Modified: Tue, 02 Sep 2025 03:08:02 GMT  
		Size: 2.5 MB (2545557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cedbe2f7462c0dd81da6fb50136dc5a5dd1d6179a3cb78c8176d2df2f70d789`  
		Last Modified: Tue, 02 Sep 2025 03:08:02 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9697f58b5ee08f3a86e0bdd1f39c94b1eb2759fec37120358e4501e4bb547aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86306563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e2f7028710e2e55e420af5414c9f59989775e6067f1ea34ef29140e83665c8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063fe434bc17aa56f74f7bf501a5ebec758423fff68627940c158ef276c14b50`  
		Last Modified: Tue, 02 Sep 2025 03:10:52 GMT  
		Size: 58.9 MB (58945094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:826629d4939f84541f6d856eef3d286a375e38a278f7f0f397b8a9768686ac3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d668fbac50c0660ebe913eba3900a1b8451ad77fbb10626eb9a4926f64a9505`

```dockerfile
```

-	Layers:
	-	`sha256:6264d54453d21301d874381ef9d0581be71773ac9ceeb8b0649693b048d93bc1`  
		Last Modified: Tue, 02 Sep 2025 06:07:16 GMT  
		Size: 2.5 MB (2545263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3142fc97be8c40b6617f588f68759d6802da2cf0382ce91b60c43f68d99ad4b4`  
		Last Modified: Tue, 02 Sep 2025 06:07:17 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:720a24eae89d43bc749952bac495f68e7574e4d4360e3366dcea5207247b5b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95384544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68506e7e09a932a82979f18c7db7fd1f772823b31d4c5fcc53ffc1b519f6f64`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3b479f49bcbb4e7541030b6218607a3d1af43ad8828ce8b2d576492ddedb42`  
		Last Modified: Tue, 12 Aug 2025 22:47:58 GMT  
		Size: 60.9 MB (60941399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ff19c89e327a83722961376688e0fb54c745d076babd00903420689555f48ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fe08b9d1fc311bfa8d5f86c40de22d8da40fb0cd74d5d421f39465aabe2a47`

```dockerfile
```

-	Layers:
	-	`sha256:83973a31de35e4472988c75c0bec8fd611c771ecd7e8f2cb0b2905239981ceac`  
		Last Modified: Wed, 13 Aug 2025 00:07:55 GMT  
		Size: 2.5 MB (2543668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5a8730ee032e4906550a1a3e47c691f1f45cfed61486eab58d21fe5c40c8fba`  
		Last Modified: Wed, 13 Aug 2025 00:07:56 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
