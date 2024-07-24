## `amazoncorretto:8-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:3a01025a9ea58993fa0491c34513580b31bba96a4066330e7fa8d34b0ed35dd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dad57c3eba3e25dd16b93c3a9cd4cb0fd5f9bd2cbf006b454a55d5c20400c1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103542783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc82cde5b005e8fb6e3bedeaca851f97d58a115aa5d2147e5fb71230f320510`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe692b3dca96388b35ab3a20be36084c0f29144fba2899034bba12fbde3d81d`  
		Last Modified: Mon, 22 Jul 2024 23:04:31 GMT  
		Size: 100.1 MB (100123743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de7d4e1381146251509b5a6b603380a334cb4bfd29a8924e54e9865246a25f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 KB (254888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bab587b48ca248ce7e73e1be296f99be5a1cb1bbd9e5033712a1a79c4545702`

```dockerfile
```

-	Layers:
	-	`sha256:15d3678659394f74c9ce84812c406f30b37a38f301333146eb3c48e09cf9c386`  
		Last Modified: Mon, 22 Jul 2024 23:04:30 GMT  
		Size: 245.7 KB (245735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5fa439f231ad409aaae11c1311b07a81c0556892cf2dffd3a3b7e6c9a18d03`  
		Last Modified: Mon, 22 Jul 2024 23:04:30 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:97b2e4fdcbed36241cf2dc923b536fd220d36570ed3d1f0154507a9ebdad8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103194515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e293f095c24ca7c39eb6e19372a0a6ce334db98377301757d19d0970448e2875`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0056494a1aa6c3ca1433aeeef8811a49d0fe89dfa3c44ab34b0ee980f38384ff`  
		Last Modified: Wed, 24 Jul 2024 10:38:44 GMT  
		Size: 99.8 MB (99836057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8c99cbac54c0ef86ba07de6df885797a95aa689ebbdd1fe43098eb785c93b3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21420430178f9580c27bf77b2c5bae215e47a7a7b1c4f68892d941d6d6873dd6`

```dockerfile
```

-	Layers:
	-	`sha256:f20d91b4dd898ad56f6b6c173b54cd603bcf1caec9d76091cbac1492bcdde708`  
		Last Modified: Wed, 24 Jul 2024 10:38:41 GMT  
		Size: 245.9 KB (245867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3221c93313e40b51d85b0622e70016f57f6a795e5a1e14c2756a500f824fd29b`  
		Last Modified: Wed, 24 Jul 2024 10:38:41 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
