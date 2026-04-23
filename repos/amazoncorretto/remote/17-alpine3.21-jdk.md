## `amazoncorretto:17-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:6011347b0242decca0d0ca4f8a88b422e1e7b4e519069c1e1621219a91282d12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:554d956b42dfd8aee6385cfcf72505afba71dd4403c30f82798c0a010d6b816b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152226585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b9b5d24aae0fd5580aa8de999f6cbd1d81ec1cbbec2427b236b01133b34fea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:20 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:20 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3115a1c05e2c56106e105fad452a6d950fffdb57b9151bda604a6aec3ed735bc`  
		Last Modified: Wed, 22 Apr 2026 21:34:38 GMT  
		Size: 148.6 MB (148579710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d2fbfc0fb67e5db5b8527695045742861dfaeca40f1f96b3c76f5f62efa006c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 KB (596588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66574b147857f63016e92b5eb9f8d63b39bc63dd2b9a3a8567e07b30a04ce935`

```dockerfile
```

-	Layers:
	-	`sha256:67b175123389c0779b93685f1e5d08cc7b368794e8630cc805ec9eec50761028`  
		Last Modified: Wed, 22 Apr 2026 21:34:35 GMT  
		Size: 587.2 KB (587209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1e5b6a44017d06caacdf109fe12942c8bfebb88ffa774ce663cc4ad98a055f`  
		Last Modified: Wed, 22 Apr 2026 21:34:35 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ca76fbb4594de11573b54069cfa122473a88c5f9aaf2d67feed245c9c443c881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150925739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cae8252bc8474139acc7b9fdad3c6dbce99781477c9915f79a0407a4f6958e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:06 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:06 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:06 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b64163a396aa8bc6c6455534de8d96d294aee4951438aa95a576c3ef8908`  
		Last Modified: Wed, 22 Apr 2026 21:34:24 GMT  
		Size: 146.9 MB (146931274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:022597405244d6c4d7d63e68a3cc4252508ea9623b9b6372f402ea8fe5526e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 KB (596111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340a24d9b12d1a9d41d500583ece10ad66a79a4905222e603a1e02ef29994f2a`

```dockerfile
```

-	Layers:
	-	`sha256:86970b61084c2aed8a298cc94d92e1af1b170a2d24a25862285a5771f81e02aa`  
		Last Modified: Wed, 22 Apr 2026 21:34:20 GMT  
		Size: 586.6 KB (586628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1db0447fe7aaf8983e8d1378c39fb4837e0c0b5f066df9f55c39965dbb63c6d`  
		Last Modified: Wed, 22 Apr 2026 21:34:20 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
