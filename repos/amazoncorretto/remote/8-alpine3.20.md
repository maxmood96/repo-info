## `amazoncorretto:8-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:9a7bc130ff419d3cc78207803a3632e6de5cabe903037a534e43446b4bca8ad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:32e5ad0451d37179e0c5ea05fdb34675cb5520bf369d852e617e1d16c917c8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103819027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296840f5588bc26e60d42c9f877a5e633ea94788394b2fdebb8f940870084dfc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd673a69bb989e881613aa2f9ca6cf895ac2a03e364198ab3c0a2ce4444c8afc`  
		Last Modified: Tue, 12 Nov 2024 02:12:07 GMT  
		Size: 100.2 MB (100195123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:191dfbe7ee6c8eac2d3e6f6d7384052fc130f4af2915b6d52bf76ccb201349b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7f798417b63c8c8157f47feec1b6b294ed0cce8c423bb0f1d8ff813d10b5fb`

```dockerfile
```

-	Layers:
	-	`sha256:f9549a6291fa58266939436e2604f442cbfc5b60a45ccb1a8a081ad466b799e9`  
		Last Modified: Tue, 12 Nov 2024 02:12:03 GMT  
		Size: 242.9 KB (242948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7188992261675a4407c38642ef70506c481805bb2e5bc449d6312a5d9636bf87`  
		Last Modified: Tue, 12 Nov 2024 02:12:03 GMT  
		Size: 10.7 KB (10695 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ae47de60f5f77a8c44984673982907c11442de96426c9b2e7f28c47304454317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104066346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d50ae7c74ee931edba2cdb7226c8f63dda7f4ff0f7189e909a066a2dfb928f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a182f095259666dd2097cf8d13bf59e3b52a322ef6a9395ec022201ee5a8f`  
		Last Modified: Wed, 16 Oct 2024 18:10:28 GMT  
		Size: 100.0 MB (99978700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:92ad1291b17ccc8cc352cc5c7aa47b59b94dd769bb54f8d5a403b0071a396a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 KB (253668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589dfa36e42b135f0579d0d9489f56eb029484db46240c5611937aac46361a34`

```dockerfile
```

-	Layers:
	-	`sha256:0116d1ae47ffb659fb39c9df86ff9a37574d5bfe3b6815e489f2876b3f72bd8a`  
		Last Modified: Wed, 16 Oct 2024 18:10:23 GMT  
		Size: 243.0 KB (243035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330e53be7da652f9ac8c1273c61a3e85536560b8c59b1446fef70859e3410d2b`  
		Last Modified: Wed, 16 Oct 2024 18:10:22 GMT  
		Size: 10.6 KB (10633 bytes)  
		MIME: application/vnd.in-toto+json
