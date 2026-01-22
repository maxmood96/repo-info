## `amazoncorretto:11-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:fa9150a6a8cb0e380e7916fb0d80fab34fed4f33f795a3cc2bbc85da10a87651
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e14b6d79f2ddeedb7dfca406f23b8ed3ad32c332636b33afd91c41318f34a5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147203392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02088bed18825093251ba3fa46530d99ebf7a4e5b83e529ed7e55f7231076f7a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:58:21 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 18:58:21 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:58:21 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:58:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4d8a93f17b87ddecb592e2976b14a7b5cec1d6dcfffa1be9ec3be48ca1cab7`  
		Last Modified: Wed, 21 Jan 2026 20:16:09 GMT  
		Size: 143.6 MB (143576336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8c52044c22ff08ee8f0e6d022e51f199266f52532f46c953a939bb0ab0b82ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.8 KB (596828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c5487528d78d2343f4a54e8cffb84087fc3b2a745f372a94bc4da891d6f38f`

```dockerfile
```

-	Layers:
	-	`sha256:278b28bca51f9923ef2ddd950658b6c45f355ddc958679fa7ec5a654aeab2d01`  
		Last Modified: Wed, 21 Jan 2026 18:58:34 GMT  
		Size: 587.5 KB (587454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1a8f63ea69746d069503a5a3a86c38f6f1a0d97e9e328c62f48c9d106b84f`  
		Last Modified: Wed, 21 Jan 2026 18:58:34 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fb73b87f7ce3517c248eae882ab609a0720eda07a73a9c56878bd19ac0b72631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145947548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc74051e4e3d7cc5cff677d6bc60d883dd2a24c25a3079b1b31a2ce8931594c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:09 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 19:00:09 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:09 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f91b989ec32a4b7b02b996e6be3d30f01fb1a1865fbbecac9a62cbce48e8b3d`  
		Last Modified: Wed, 21 Jan 2026 20:27:03 GMT  
		Size: 141.9 MB (141858171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7935f421dcdd82eb80ab6d33729e6cf4157bfdd817af5bcd1cc8737dc2160e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 KB (596988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01c232e38eb3f5cec230a8b25ad978b92e24bfb01e3e8b4572e6bd697231a1b`

```dockerfile
```

-	Layers:
	-	`sha256:1f3c310a22374514aefcddd74e47253b25a022e6ef0fda9aed57c891d10d2f98`  
		Last Modified: Wed, 21 Jan 2026 19:00:25 GMT  
		Size: 587.5 KB (587510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3abe7d81d5bdb707bb56b1a2855169660a564b6709bb2d996c76d3a711481a3`  
		Last Modified: Wed, 21 Jan 2026 19:48:24 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
