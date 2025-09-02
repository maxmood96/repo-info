## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3a2fbaa22c5665f0b4a9f53b561317831b2b629ccbc3052f250dae77871d97ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:588b67a767d562b59dd179e2643cce43134991f409752afde57a1619fe35518d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82180783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22faf5d3e39724bc7f8b0b5f0d4f9e192b9ed566e0038d3abc8ada17d9664731`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:8d5996ca15321cba057723b93272ad655ca346c8b0f22cf09e3bebc63c7ce5d3`  
		Last Modified: Tue, 02 Sep 2025 00:27:08 GMT  
		Size: 52.6 MB (52643848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:34a83f673c0de6bca0727eb2297d2b6899dca81fbe86d25432f275154ebad36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c91996efe6e721ae5a6ecb5eddb88ece112dfaf654660a4c2f59bfea8fbf933`

```dockerfile
```

-	Layers:
	-	`sha256:57660add7110ff34869ee9380dfcc2c2c7515df67b7722ffaf64018edc89a0eb`  
		Last Modified: Tue, 02 Sep 2025 03:06:01 GMT  
		Size: 2.3 MB (2292859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84e94b275e03dd4a7d47fadc2f11444b18f45ee8a818220ac9417b1123111937`  
		Last Modified: Tue, 02 Sep 2025 03:06:02 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4bd9011fed1a613257b8b28a357ce45e159cb3bbfc6a28f4366fed132ab0222c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79389788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a416bf1c669006f5d814d6549f6d949a2b2954abe7524e34da1cd0986b7af09d`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c0c580adcbdcff33f793c31f7143f72328c32bf0b506316babab10f19b462f01`  
		Last Modified: Tue, 02 Sep 2025 03:17:50 GMT  
		Size: 52.0 MB (52028319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:868b8c4ec16b41f06006056fa437e822245ee5c93d8d00c64c29be4766c48b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8fdebff41e0da10b16a41a299e11578882a9f52a34d42371f6d03ef86a3850`

```dockerfile
```

-	Layers:
	-	`sha256:44196ebdb06b7f9f70cb1bb3d5a132be0bd25905ec0ec1a5fdbce83d7b485583`  
		Last Modified: Tue, 02 Sep 2025 06:05:16 GMT  
		Size: 2.3 MB (2292531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b2df98df9b200fd5b520a5a2b21fa7e889a6fc3f7522a9876175f48b27b65d0`  
		Last Modified: Tue, 02 Sep 2025 06:05:17 GMT  
		Size: 9.0 KB (9036 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d8e5d358755723cf073b0700107a999bd223db55304e12fdc0531412188f990f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88006545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56282f263b62ead4cad1aff779f55690ce39d795b75878411ced6b44f8df4336`
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
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a19f264150628563aebbf30daaae47de06a6f6db5f859d952a8d7f26dcc3f7`  
		Last Modified: Tue, 02 Sep 2025 05:22:40 GMT  
		Size: 53.6 MB (53563321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cfd15f0f53c25922030b4e1e02f027e5ad4b82c05bf6e58f448d017deae3af78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f28f40b1bfed67e11c1dc7557ca242cb61fb82289a6971ca8e72ca1c10812d2`

```dockerfile
```

-	Layers:
	-	`sha256:b32c0a110eff6900116616147f8f0d82d4b6fd51b142ac2a0c7c5459c2ac3997`  
		Last Modified: Tue, 02 Sep 2025 09:05:18 GMT  
		Size: 2.3 MB (2290884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b7a176e6509a3b0bfeb88f442b4c39d38b09aa0b3114db3a736b65c948f6f0`  
		Last Modified: Tue, 02 Sep 2025 09:05:18 GMT  
		Size: 9.0 KB (8976 bytes)  
		MIME: application/vnd.in-toto+json
