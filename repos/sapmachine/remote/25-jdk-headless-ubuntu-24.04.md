## `sapmachine:25-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:677d3dac235ea269edaf39ecd420c5b4dbb489b8799df029ed58a3a5d17feffb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:cd90872aa48167d7096db049cdbebe75ce8abcce9dd43fba79c1569807195598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250730191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b67a598460469027ac1c3344003f80b467f465831cbdb73a444f7c6e5c076c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:23:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 02 Jun 2026 08:23:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46156882d7c7fedffc8d393ecc2ee7f86da9ca147ec1f9ee36d10da0d41e7c8d`  
		Last Modified: Tue, 02 Jun 2026 08:24:16 GMT  
		Size: 221.0 MB (220997386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fddfb9465cdaa6551322bda532c442eb7c674cd90e7e7c0300bf49b7772911aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3242b5ac04abbd92d7e6667e91ee9d41771622724fe8b20d028b2acd8ec084f5`

```dockerfile
```

-	Layers:
	-	`sha256:208defbf4a0006ca88fc84c256c7f23b3088c9d0b8533a81134e7098bdd95b8a`  
		Last Modified: Tue, 02 Jun 2026 08:24:10 GMT  
		Size: 2.3 MB (2349915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d456355980ca128ee4fbe13cd7dfd2a166b7f28c6b79f26f7bdfa1b3b319404a`  
		Last Modified: Tue, 02 Jun 2026 08:24:10 GMT  
		Size: 11.3 KB (11264 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8ebf82bcf21e6e9226112d27f987a4991e3a0702e4d0382ad857e361a358a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247670602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41766c1cd9b7002e6e385aa55d9e3d88873ebd78d6b0e52920d291535dcb4d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:24:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:24:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 02 Jun 2026 08:24:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400d0c5c8c93533fb5afd25cdabef0256932cb0716b9fc73d5210907dd8090b4`  
		Last Modified: Tue, 02 Jun 2026 08:24:35 GMT  
		Size: 218.8 MB (218794196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7a584e0f4751a6ba96f48d30a43e10fc5c62013583fc9522889561f332783c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bee945b5768fb21b891e74c391124a12a35037e48a0613159072f117f18cc2`

```dockerfile
```

-	Layers:
	-	`sha256:c148c3fab048f0e3d9d2aba5eec264ec709bf6f638a5284a67e29810c57d3596`  
		Last Modified: Tue, 02 Jun 2026 08:24:30 GMT  
		Size: 2.4 MB (2350455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb0bbbe02de518cb9cea7587ce3ba1d8345e79410dfd92971754335433159aa`  
		Last Modified: Tue, 02 Jun 2026 08:24:30 GMT  
		Size: 11.5 KB (11452 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:69df045bd3b7ef4595eb048deaeeca9109574055cd5fd53654ea84452ebb2aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255826375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6881b85fdf42daaf7e75dd65458ec38f936f5d6dc35034fdedbaa8e15b9ba7b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:54:26 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:54:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 02 Jun 2026 08:54:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e97d8179e178a1e4c0d21bd3860533f2db0852c56e0517652ee93d4c9221f1`  
		Last Modified: Tue, 02 Jun 2026 08:55:09 GMT  
		Size: 221.5 MB (221512276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:76e9e29767303e6f92971156a2f520b84a0eb4fd27c1d741f3e940d0ce0f0fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2358137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4ae95f6346ed71d94204571fb3b29a322f9960634805861f1aa92e9b89a997`

```dockerfile
```

-	Layers:
	-	`sha256:f416dbbe640beef139a47f78a8a34c7132822ba71b0f3371486ba75eb09c930a`  
		Last Modified: Tue, 02 Jun 2026 08:55:04 GMT  
		Size: 2.3 MB (2346786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaaebf3eceeceac6a203c3179c7e54d1e0e1ed935380e2a9bf5d9849cbcb537c`  
		Last Modified: Tue, 02 Jun 2026 08:55:03 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.in-toto+json
