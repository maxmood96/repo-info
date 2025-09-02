## `sapmachine:lts-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:173450ca156778c2dae145172acd80054a2ebea7bc5de1865369446cd2ab3451
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:52fcce69cd31aa23c9cce3c127c1ac12ee41f3581830c6254f8bf8d1e378db49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88133805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3192ed4358a3c2259190af1fc443c5b94755c89bc2197327af6973abacdfa29f`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:75b5aec6e2f3448b04da55ce8dba88b1c9a21adaff1065d50b8852b0efcd47b5`  
		Last Modified: Tue, 02 Sep 2025 00:24:28 GMT  
		Size: 58.6 MB (58596870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aed0219ec3064547db82443c691fe7a0c5cd3209abd7e7722ba37ffac07ea847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979606cbcd0412a73445a392ebb90ce993502516db50598cddf7fdb0002d8ce0`

```dockerfile
```

-	Layers:
	-	`sha256:567d41abd3b58e03ae7a44c527f30e8c0770cc31ab9fa9164d6f46a1c29ed49b`  
		Last Modified: Tue, 02 Sep 2025 03:07:53 GMT  
		Size: 2.3 MB (2294813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9172c0fd7e8ce04aa3049256ba5a2913e9b0dffa04f455007fbfdef9bbf404`  
		Last Modified: Tue, 02 Sep 2025 03:07:54 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9a0962c851dc4cfd76928c9bd82456ded8d033f40b4bbba290c1cffd86becb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85090183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a312a2a326d9565c652c3d4798c4b695c1fcf46f07c4e0584bed6b9a2fe9c52`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:7cd7549ff7f63d31e0e205de383e9d7d868a2c1466912a33ec44e8f9c5a8e5ff`  
		Last Modified: Tue, 02 Sep 2025 03:11:44 GMT  
		Size: 57.7 MB (57728714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fe8abe0352c5c85a064efc21ba757d429e522ae5e512ddb8590522d369c842d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29afb5aa988128d42b351ee73b444ee2ac4c6679d35968ba9187ce1827cd2c2c`

```dockerfile
```

-	Layers:
	-	`sha256:459da1a0f373ff7f205556777a4bd41f1846d015b64ff07efdac248fb0f4e22a`  
		Last Modified: Tue, 02 Sep 2025 06:07:07 GMT  
		Size: 2.3 MB (2294509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e07f52c95beae3e68b93ad042a01bcb64f75d0ba74c703107f8a2a1b01a6bf0`  
		Last Modified: Tue, 02 Sep 2025 06:07:08 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:13d972ea80430c2328a7733319e1e7f72bfab1bd315c32d02f4b07dcd8ca6955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93988669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57df5f3b2e988c8b526ebec7a7a88c5aeaddcd0f3504b32b9f65ebf0932d03f4`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:823c5531c4dac79843e1971972065d34a11eb91d4567be7cead399a37a84113d`  
		Last Modified: Tue, 02 Sep 2025 05:10:58 GMT  
		Size: 59.5 MB (59545445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:de4d8db924bd37ec8d44c449db3bc6655037354eed149cce0e8241a28a18933a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d92b9ac5c3910c67f69d4e9c9c5673f3cbcfe4bf0129545613221e6a9d0577`

```dockerfile
```

-	Layers:
	-	`sha256:63e1e56ce6f4e062640bdaefdb22b45f1d5bdaf5565ef638c7d831fbbf156687`  
		Last Modified: Tue, 02 Sep 2025 06:10:54 GMT  
		Size: 2.3 MB (2292850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b744e5001d37cfbbf82b812c1695da9ee1815416df50c0a52ddba6780f07d65f`  
		Last Modified: Tue, 02 Sep 2025 06:10:55 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
