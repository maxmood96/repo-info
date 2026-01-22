## `amazoncorretto:25-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:ddafa73f38ac5261d99a0415beefc1c1cfa08872fe2af78a37339ba8ce572f08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bfeb11bc7a52f4e5bfa8919aed6d6229d4dde1536eedbbc7ee438f70c42972d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184567940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39d114bf526728373f394be768c62de085bbc8e940cd29d0ff0fe4fb3961df8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:43 GMT
ARG version=25.0.2.10.1
# Wed, 21 Jan 2026 19:01:43 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:43 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136b601e48494a8290ffb62d325b32dd94994c7e7cac65f53d6507e8ad5d4c0a`  
		Last Modified: Wed, 21 Jan 2026 20:03:49 GMT  
		Size: 180.8 MB (180765488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:35eb0727425dad3c6516b1deff366894333fd94283dd5c1e5c72c16c37e52ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 KB (601509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab857ceee46e17d1affd5f6aa21e19113024f29315b7fcad05eb673aa72a7c9`

```dockerfile
```

-	Layers:
	-	`sha256:adbf7dd95d08e02a94837eb8228e0222e01b716b87a5b087dcfdebf8da656af1`  
		Last Modified: Wed, 21 Jan 2026 19:02:00 GMT  
		Size: 592.1 KB (592137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d10517660a87438e8ddd6463305ad1a99a4684c2375961e88b0f7e3b6b3e4a`  
		Last Modified: Wed, 21 Jan 2026 19:54:34 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4f08ab3b9630e0bade0f5264f217a6014518fc2b00bc9bebe2836024a21668b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182548700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5847ee7f0ab48f357335c7248650ef462126e3bf627d2f46eb670788ca2677df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:02:01 GMT
ARG version=25.0.2.10.1
# Wed, 21 Jan 2026 19:02:01 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:02:01 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:02:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:02:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a98f64dec7f57d2647fdae231fb2b4171649e55a8cc3c684f1cb70c248cc2`  
		Last Modified: Wed, 21 Jan 2026 20:28:44 GMT  
		Size: 178.4 MB (178410631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3fe71f0dd325446675e8603fb340190a4943526ccc8b38e2ccd99f147323cb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 KB (601028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf78d2115e727971bfa35682e03724ac33e384b08f7bdf65ff4b5c2de4d1301a`

```dockerfile
```

-	Layers:
	-	`sha256:dddb192213431cec90d463584ec0ee75a7b20e2943525a501a2744229c3d3dae`  
		Last Modified: Wed, 21 Jan 2026 19:02:19 GMT  
		Size: 591.6 KB (591553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3512f38fc7c4647925fefd8cd05d4c8a2e579d1ccd85d16c22e04d7e6ae618`  
		Last Modified: Wed, 21 Jan 2026 19:02:19 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
