## `amazoncorretto:8-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:30bb8a1bf34ad07a13ef47433c40ebf085c99cff89f3d1480dfc3ee203224afe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0d7dcf5cd96438f7e4c873768fbd35be60c19f873ff7ac5b28333084300f900c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103614596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa35fc6894417cbd33cdad98f499a903ff1bd56f68067b970aeec7bbdf0fbb84`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f57e41e59d0c9c80fd27629e7c742fb2f4e4d20fab24b9cac2dab0be7e70e`  
		Last Modified: Wed, 08 Jan 2025 18:09:06 GMT  
		Size: 100.2 MB (100196622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a82f2a18e64ad2c642912644c6131b87e2eb7f392cf20b8b649edc57f66e16ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5d8bdd5da1d8997cf4d3555d7b0bf120fc273e8acebaeffa25b34ad9563ff`

```dockerfile
```

-	Layers:
	-	`sha256:47b6ca7dae9b2cdfa0aeccd65c6e8dea2550b7242b8b48b2eea4373b3ebdbcbc`  
		Last Modified: Wed, 08 Jan 2025 18:09:05 GMT  
		Size: 245.0 KB (244973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1dbcf95ade1837a05994c9665053be03731061fee60588ee0440047d986a950`  
		Last Modified: Wed, 08 Jan 2025 18:09:05 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:823ba0ae717aecf92a8a4ec15ce57ba6eab60bf69190808704b14b487d39df3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103316574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f260e643538c8239ce778ac509234810051f5cac24a283930a884eed73e0e988`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335135b5f2fee53ff65c7c488fd85f6226d228d698c17f2bbff8f82e82fe0051`  
		Last Modified: Tue, 07 Jan 2025 07:19:05 GMT  
		Size: 100.0 MB (99979139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ea8c00d9f0288d76821e4f6e4cb89f0f3f2b71ed68fefcf6f28aa6b0b017ec70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff475b77a97ccd28950f3685dd4bb5d79e84caf803334337afad3cc29fcfb1f`

```dockerfile
```

-	Layers:
	-	`sha256:1bd5f7b387edc8003f4f78d25a1e552412935cb669fba7480602184bf377003c`  
		Last Modified: Tue, 07 Jan 2025 07:19:02 GMT  
		Size: 245.1 KB (245105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ebb6060f35fc96a05fb1ed947523f1fa96f9c50befcf2bb8aa7469d0b4b1ad`  
		Last Modified: Tue, 07 Jan 2025 07:19:02 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
