## `amazoncorretto:11-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:503ef4512afd32d64e8185a48444799afe641fe49d4ce9f415ae0fc3e0ef4531
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c8eee507c7dde07a1b34640402ee3acaccc69262033aa377035b90b95a1137d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147132101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a298bb24d234704690abe60a5996311a674aa2bbe55ea9b7b1829d2527c2d51b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b64f3bbf000606c0c9b556c924770eb6213d249f3c5e3d917d8e8bbfb72b948`  
		Last Modified: Tue, 21 Oct 2025 23:26:43 GMT  
		Size: 143.5 MB (143505045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3706956e406ebf49cc4f33f5c32b4f091a58e293912ff7b3cdea2b59a0a49c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 KB (596871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f65a25becf31dc907cf12e0f64b5abf7919ffa8cca6d6db338210452e0f696`

```dockerfile
```

-	Layers:
	-	`sha256:a811a0497090b9104251c4e26d562013e1798958045c4775e36afef0d30796d1`  
		Last Modified: Mon, 19 Jan 2026 11:17:55 GMT  
		Size: 587.5 KB (587454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1399b9bbb9b5834173417a20f270d398dc8390dc22ffc32d0e77efba0b7623c6`  
		Last Modified: Tue, 21 Oct 2025 23:26:40 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3024be4609ae94c1e0a2cee957085bf708d95f700e45c92efad0cf278db6dd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145882140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f8cad60584c92507b259011a1f814495b3e51eac9d74f9629bb45558af4d29`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Sun, 07 Dec 2025 13:54:57 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251acdd70e7f4ae5d7148c36b10935a959b2bbec659b1294834d8106d5c29b4`  
		Last Modified: Tue, 21 Oct 2025 21:49:41 GMT  
		Size: 141.8 MB (141792763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f1a8c8dce1d351bf678644cc72305a9f291783061a41a3470911e963d4c32953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 KB (597031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadafe3c945ad18a5f1926e8965450245c0fa38321c8da33dae36b864ea9e02a`

```dockerfile
```

-	Layers:
	-	`sha256:e42405527c152ab7167a106a57b24e1e3c15b748920f534c2f19ecabafe420d1`  
		Last Modified: Tue, 21 Oct 2025 21:49:38 GMT  
		Size: 587.5 KB (587510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a07514052a9a860f678565d0d8057fdd37a51b67a3579d6171e039e5757f9eee`  
		Last Modified: Tue, 21 Oct 2025 21:49:38 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
