## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:dcc66f378f6833327112555515fd882633eda00deb787946131d05d9832c631d
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
$ docker pull sapmachine@sha256:a283fc96a611d884b1ad45035495b2a7437ad922e3778db2cbf88d0c9b2f6780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83920289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9326dfa1cfe5c9a29500d39799e2d781f12d6f7d09c8393efbec8b519fdb6c03`
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
# Tue, 17 Feb 2026 20:35:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:35:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaaa090075a287fc581c06f1a3753ab81f3204fc5c09eb101d960161c252e89`  
		Last Modified: Tue, 17 Feb 2026 20:35:40 GMT  
		Size: 54.4 MB (54382923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:62c8f419f33ac0daf4c8a97f04134ae9fbdffda40eeb66344c87ed49c1fca616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa47ee1a50001992f9797bb46ca810efe7789261aef6670557cb7bbea6bfa1b9`

```dockerfile
```

-	Layers:
	-	`sha256:baca4e8b86fa599f483ab2a9455752947017bb823e385a8e836864d22ea63eb3`  
		Last Modified: Tue, 17 Feb 2026 20:35:38 GMT  
		Size: 2.5 MB (2546027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7875b37b4377f464467d972ce8c44194d6ff1a1b387f0a82c1bf09e25fb1c391`  
		Last Modified: Tue, 17 Feb 2026 20:35:38 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6e844580150b74de8ea2abe182961ff213bc8e81f8ee1b1e343dc327d7a75e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81149065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4128ca2c1fee7c90c34f3d6454c7eebae502062825ec1e6a78a88140bb8e568`
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
# Tue, 17 Feb 2026 20:34:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:34:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7ba040a14baf96e1416508b6020850367bce30231744d1477783399782423`  
		Last Modified: Tue, 17 Feb 2026 20:34:47 GMT  
		Size: 53.8 MB (53764121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dbe314566013199098f78b530c661a66e17706a676d2d12cfdd0f9e545ae9480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b69889fba8725be33314723ebda08335ae2808544bf1b4974984cba18ddbb6`

```dockerfile
```

-	Layers:
	-	`sha256:c25313efe46ed51456a59887bf5e965a23ffb27a0d87edc9678305ef3e4c9e96`  
		Last Modified: Tue, 17 Feb 2026 20:34:46 GMT  
		Size: 2.5 MB (2545709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc81b49d2ac97653e94a9befbf032e0e1a5a3e35274c4f0f8dfe6506d39966e`  
		Last Modified: Tue, 17 Feb 2026 20:34:46 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a696c2a5d02c5ef8d57520209fae12d2b099d595ce2a8c4c1ffe3b6f14af14b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90011986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3094379166f334085cb3e8e854051e67ff3ac484a4a0e0f93fa5669ce7870e7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:41:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:41:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 21:41:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c881ef8c90b95709e0e76f12110e063e0ca8922562fe3085cf8d38bcb1f56f2a`  
		Last Modified: Tue, 17 Feb 2026 21:41:53 GMT  
		Size: 55.6 MB (55565884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:087c4445166a40794da04e9e7c671094161940409a823962d740fede30ec2473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd61d32fe15907e466df48ab8cbeb4bb1e0a5b3fd29230e0b8e1dcf5ca177d8d`

```dockerfile
```

-	Layers:
	-	`sha256:5539c019e712dcf7627e159e3348ffe3101c43c71b1c7b3534c58af42a46052e`  
		Last Modified: Tue, 17 Feb 2026 21:41:47 GMT  
		Size: 2.5 MB (2545559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c94eef4e2dff4e53388b7614a1208f83cdc8d9b8f4a03bead1c4b14a2e56c8`  
		Last Modified: Tue, 17 Feb 2026 21:41:46 GMT  
		Size: 8.8 KB (8818 bytes)  
		MIME: application/vnd.in-toto+json
