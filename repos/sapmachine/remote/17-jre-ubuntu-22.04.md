## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:67fffe4ee7329370e4ac15e29e1fa24a51bb9d9b50c4cfd4b429f559f827a243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:86952d4563a1702466b061c97b4c9e6cb3b49cf337cd9cea6d77647e63af937e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83409361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4eef19d5ddb0d6c28f9a8bc1c235370ec46400a369b7c99908971b30e21873`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b93e66d2c05869a1db94fe327104d6e4e464cfe82941cf4540c27e31fb586c`  
		Last Modified: Tue, 02 Sep 2025 00:25:49 GMT  
		Size: 53.9 MB (53872426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6d050a1567dfe34d942a4b3f657dd72c0c28b620ffa7900b09e3d168e66607a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48dadffd27e2a92aa35ddf0b5bbebade801c651a73c0b0cf62cfa157e2b028a`

```dockerfile
```

-	Layers:
	-	`sha256:3a4e82931b9f6250dee1970b1fe2681bc386224263d0fdd05e160125c24a8071`  
		Last Modified: Tue, 02 Sep 2025 03:06:10 GMT  
		Size: 2.5 MB (2543639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64bc20f998f7c0bae77e3398883f52e74b0ff5364b548dfc091a83b460fe9e5`  
		Last Modified: Tue, 02 Sep 2025 03:06:11 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:20a35e4c55a6447a6340852d4f32916b3136d385535b338100356bd50e95a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80609222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0a8ad6434eeda65e96718a6264aaf86935b7f9c91089e3a5fc1c1ca5a8d11`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081416af9bfaa68e187748efbb60a7393dbc9230a80929ff1ef1d9e45e5fecb3`  
		Last Modified: Tue, 02 Sep 2025 03:17:21 GMT  
		Size: 53.2 MB (53247753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:79f7b79ffa8c4f340b8298b25575e1560975ed26696670e6c163a7ef16b76bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1c6ef119e72913f24cd1cbe5cee2480b7a48fd54fd66d02531159e01533553`

```dockerfile
```

-	Layers:
	-	`sha256:b577ceb6b36adb6542ec39bd0c2ead7ba30cd2b6dcfd424e3a9bd4e3fe01ab33`  
		Last Modified: Tue, 02 Sep 2025 06:05:28 GMT  
		Size: 2.5 MB (2543321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46ce9e39c47b399adaf190cebefc405167a08b0f1e34b143d708ef170d7cddf`  
		Last Modified: Tue, 02 Sep 2025 06:05:29 GMT  
		Size: 8.9 KB (8924 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:81c04a6f2c49421f115ff94a29d507ff375e2d3930a522518cad0f95185932a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89387887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a674037408cd6a7a3b49c8d6a2c7f3b4b998d2cd78685e4a7225ff476913a865`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb56efdcfdb633b22947bfa4c82540256728a22f0da4aa80f49def392ac2e14`  
		Last Modified: Tue, 12 Aug 2025 23:02:19 GMT  
		Size: 54.9 MB (54944742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:12bc804a7120fb04a8eaecdc4f4032f1ae1eb79cad9e32dfda923cf24160b56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d1ab141b3a29803927776b0dbab86754c188f146ad02ef65fd326fd91a32f8`

```dockerfile
```

-	Layers:
	-	`sha256:62668d00e46b327548834ab6270eedfdf29b2ccc7cd8970fa07c9bcf323c162a`  
		Last Modified: Wed, 13 Aug 2025 00:05:50 GMT  
		Size: 2.5 MB (2541738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed63e89ee9346e90e4b83789b900659e75e976322ca20ef47089dff18900600`  
		Last Modified: Wed, 13 Aug 2025 00:05:51 GMT  
		Size: 8.9 KB (8865 bytes)  
		MIME: application/vnd.in-toto+json
