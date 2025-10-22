## `amazoncorretto:25-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:c938e094312176f505ab86c40b09635ec5fdeb11152149317e82854fd329be1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1b83fd6db358ae2f335e517609029065ab17c45dd0939bde1e5278ecd9d47f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184337221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4b11e480f6e9f778fd17a7b52ea8695a1bf27339c838519533bdeddd230f8d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a168f027bb57f92b736bb567d5cff668055ea4caa3a75c69c013fae72cb3ae01`  
		Last Modified: Tue, 21 Oct 2025 23:28:31 GMT  
		Size: 180.7 MB (180710165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:91f2836a6f3ec180ef5e8c6d81b76885fa705acb695667a1b120a2e6ae835d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.1 KB (599067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaec2880610f593e26ac2af668f9fe9283e1c146c41239fd04ea0a893fef498f`

```dockerfile
```

-	Layers:
	-	`sha256:ec8580e15e65e8700b8da8a74d91dfac15a27a30ba852350f6e3a79d0b7d0973`  
		Last Modified: Wed, 22 Oct 2025 00:53:58 GMT  
		Size: 589.7 KB (589653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5e437585f290ab0fb8e3d2bd143d7d941d4900b4957ae90ee99a0cb73a59e4f`  
		Last Modified: Wed, 22 Oct 2025 00:53:59 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:175703ce0da7427423dc7639717e6ec45b7fd1fc8d287569387ed63d5db1e981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182464482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb6c2de6ccb85681ee498dc67b8ded9a2e6207db567ac2d4d45c2002f3eca99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c3c280d44e57282d5c069840e4e687e21c2bfc7c1fb5d2f07abfe18bc7bbf9`  
		Last Modified: Tue, 21 Oct 2025 21:51:36 GMT  
		Size: 178.4 MB (178375105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5fd62644b0170dd99d947111c60ede222416a0a22f8949f012b06041294e50fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 KB (598587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70786a1ae25afcd1c9426e83fb188d65ccffc28d84a45cdd4e532ae9c3526824`

```dockerfile
```

-	Layers:
	-	`sha256:e6432ce9c70c7fb185ed14497ff157a95ae1f18193208155a922ee617b50c24e`  
		Last Modified: Wed, 22 Oct 2025 00:54:02 GMT  
		Size: 589.1 KB (589069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:650638fe64fa255065eb8944213f7fea2c16e9ef8990254f81f5100a77894661`  
		Last Modified: Wed, 22 Oct 2025 00:54:03 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
