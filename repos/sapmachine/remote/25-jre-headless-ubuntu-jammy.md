## `sapmachine:25-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ecf2108dd2ad827e541f3078eea5e68436769e68397f84349bb96d7e7b5f0b19
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
$ docker pull sapmachine@sha256:070dccd41ead3cbc576fcf0b6feb0e0eb55521a0d2ec933399b2c7a54d47c099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85665889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c9e8616d88b0e145aa4de2466ec4255bf13c85b2d8a5ddfc6a5250885c0876`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:05 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:34:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37f58f5d501835cd3b2f618f1de2e78749342fdb13f55c26266e45550a4c167`  
		Last Modified: Tue, 17 Feb 2026 20:34:19 GMT  
		Size: 56.1 MB (56128523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ca36e3933a1fbfa2a9e8aa47308bb6c6b8228eba68bda58a3dc362f0a1236333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44ba8a4f42471bcf8511363b667ed12fce674c74e62d19bd2a9b7c1a987bba3`

```dockerfile
```

-	Layers:
	-	`sha256:f034441bb8d1cf18ff78884e7dfbed82dfc9a1d3588090bbce736fe6cd09ad46`  
		Last Modified: Tue, 17 Feb 2026 20:34:17 GMT  
		Size: 2.3 MB (2303043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be4ccb169a7dae3cd38f6c9489ba3a9c805304f8a6ac1b3209e30c1b3fdd27c`  
		Last Modified: Tue, 17 Feb 2026 20:34:17 GMT  
		Size: 10.3 KB (10271 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:af570f5065fef1212f01c90c38da0b995344a05011820bf87a62ba0149ab398b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82430139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcecf3ecbb33cf5deeb81b058dbf0050afb809d4bc4500c204ec0ba2a5dc0990`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:32:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:32:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a522932d9f5a075717828058147bebac756621e1cdec6f826e247ec768a37ba`  
		Last Modified: Tue, 17 Feb 2026 20:33:10 GMT  
		Size: 55.0 MB (55045195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec9fcf4c8cc1d3fe36a53b1345ac1aff272c6026596f901031dd92dc491990f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99205f3e56ebefb75e1c69a2e67026c8f2c3a27f4bce26f63bf74614f2a6aa2`

```dockerfile
```

-	Layers:
	-	`sha256:1d9083a45bc2050c46bf48eb33db742f5f401eb86ac2a51059387fcbf5915097`  
		Last Modified: Tue, 17 Feb 2026 20:33:08 GMT  
		Size: 2.3 MB (2302760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb3c9ddfa11556ab19a3972ec6f558a72f9ba5be36b30a34657b6b0a4b30c8c`  
		Last Modified: Tue, 17 Feb 2026 20:33:08 GMT  
		Size: 10.4 KB (10424 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5a0e15c87e0cd88c86117e13d2565a255e3f74c33a00bbabda8637f1e35f1ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91284179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807af6b47bfc7ce7ce516ff230d330d036e0132eef3305f55acfad6c30504db6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 21:16:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:16:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 21:16:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0159c8c076a5f6316bd42808a626d76edeb59614fed705a11113c28ac394fb7`  
		Last Modified: Wed, 21 Jan 2026 21:17:03 GMT  
		Size: 56.8 MB (56837217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eebccabb60d1ac571b6b9dc5338372e934149a1a348cb79ce1d8896218a1f442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d9a237d6fd1f0249e93037cbabc2d38ea351993f1ed8646ab962d8fe1bc159`

```dockerfile
```

-	Layers:
	-	`sha256:88d3e5dbb7983eea69a3fccec402b50d7710466ad592a1d08755c58f8238ff50`  
		Last Modified: Wed, 21 Jan 2026 21:17:01 GMT  
		Size: 2.3 MB (2301867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11bebbe39bba05c02bee8dba3485112041fdb033e3a30e7aff8891bdb51aee28`  
		Last Modified: Wed, 21 Jan 2026 21:17:00 GMT  
		Size: 10.3 KB (10339 bytes)  
		MIME: application/vnd.in-toto+json
