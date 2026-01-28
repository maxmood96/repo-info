## `amazoncorretto:11-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:155d16c242085b39f3b6b0b1137fc5c5421c0060be9239e61a2f4e8d123d6f6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6b70b453484a17a2b2163e8aeeb621d8e92be9bbb1d1efac4d4c1bb8114b52a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147204214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa24388752880f1944cb2b9fd41520b5b628d8ce0ebd9223b4c775f74bc67d7e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:44:40 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:44:40 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:44:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:44:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ada83a3ba195182e8a9925b59ed2af14afefc96064c21366efd2587cb04d2a`  
		Last Modified: Wed, 28 Jan 2026 02:44:56 GMT  
		Size: 143.6 MB (143576350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0528bf37d94c2bf5303248c10b2ab4a4f11f98d46cb12534ffb20e161b8be15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.8 KB (596828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e070be8419e9c98f687a4a2ff6f6b670cb773a2810652435ee526063c6325ad`

```dockerfile
```

-	Layers:
	-	`sha256:525131439faae7485d5594419e8bcdbcecdbcb7fa02df7a8168f7138ece51632`  
		Last Modified: Wed, 28 Jan 2026 02:44:53 GMT  
		Size: 587.5 KB (587454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c9a90618383730da26ecb283ec12e3462642a6a9409d5d2608e071bdafff86`  
		Last Modified: Wed, 28 Jan 2026 02:44:53 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20` - linux; arm64 variant v8

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
		Last Modified: Wed, 21 Jan 2026 19:00:26 GMT  
		Size: 141.9 MB (141858171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

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
		Last Modified: Wed, 21 Jan 2026 19:00:24 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
