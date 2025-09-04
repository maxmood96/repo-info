## `sapmachine:21-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:1b4901cb09f95ea3e1dce8a7b55dc8cce5666378ef48233d2c59737f1be9c13e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6523a40678f5f6b75617d228ebd294e2edd6c8513d36211a48158e57dddfb590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244468449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf8f0bd667074b79796bfe85af433a16aad2b7f73b7ddbed4aa6f7413cf00ab`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c3915ff5494fc50134ad6ef219f4ac08ac6654f733763d21c9dc5a1a454572e1`  
		Last Modified: Tue, 02 Sep 2025 21:44:23 GMT  
		Size: 214.9 MB (214931514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a846e813ab19d2c69d2affeb9b433d200255e885323096682977eb5e620c1105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdda9f6799092e21980d9c10edfb40411082fece0404f05081db8aaef1fdf2e`

```dockerfile
```

-	Layers:
	-	`sha256:97191018b6e3ccd21f9bda92f7c44401bfe78f3b995f2d3c2b9d00ca416aab18`  
		Last Modified: Tue, 02 Sep 2025 03:07:32 GMT  
		Size: 2.6 MB (2631042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7190cf3b85b404b5f1e1afdbc6440c82736b2c17bb089ecf0ae9496da5c78a3`  
		Last Modified: Tue, 02 Sep 2025 03:07:33 GMT  
		Size: 11.4 KB (11444 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0939fe3fe45dec937012b877faf2ddbac211b1d545820c3b9fe2d23afce2dee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240468650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cf2f60a4358cb0d8052177f5e62d2684e9fb9da0167b0104fdecb97a01f0c7`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:ce5e0df50f431845cb5ad8633fd857c63749253a9a5a37b95ea54e4829490fdb`  
		Last Modified: Thu, 04 Sep 2025 05:28:22 GMT  
		Size: 213.1 MB (213107181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:94bb345780e3b3c69b5e429b543186dacdf8530774d4aa407851977d148431ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493d1fb9ff7f01b70539865e2b0bf83d4bf25e44556d9cb50698d57d179c74b6`

```dockerfile
```

-	Layers:
	-	`sha256:ac97aa30e5231ca77b1bc441ad43499c5f0f81e563ce4e66a6e9daa5ad66eb32`  
		Last Modified: Tue, 02 Sep 2025 06:06:49 GMT  
		Size: 2.6 MB (2630820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7a6745759f9a46822a8794030fe1dba8fd6e6fd36042bb7e455dc84a350df45`  
		Last Modified: Tue, 02 Sep 2025 06:06:49 GMT  
		Size: 11.6 KB (11645 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e181067858ece907df0c229b47757812cf99c409c87a38a4a367010b58e792d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250208208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0cf7f7933916778e57782113da362a3258f3ed591cb40428aa8eaef0b9837`
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
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e040095c77d2e93eda823a1a585a7ea6681bf785bb0ee1b378c846a01df3678`  
		Last Modified: Tue, 02 Sep 2025 02:08:05 GMT  
		Size: 215.8 MB (215764984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:736d3c5e7008b2f76e1f59dbefbb6e8d831b4c12aad1e10c37e5716a24bb5490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb58ec7fd85f893654053da30651ccbbf756e4078c6c6e568c68908a3dce8d38`

```dockerfile
```

-	Layers:
	-	`sha256:b4713edabb17b10f4f8741d400bf4d1999179d51e8a771655570838e0b5758f1`  
		Last Modified: Tue, 02 Sep 2025 06:06:54 GMT  
		Size: 2.6 MB (2627259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2a71cf37d68e8f160cc73026178df052dd2545522a9271b832b97688f6e801d`  
		Last Modified: Tue, 02 Sep 2025 06:06:54 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
