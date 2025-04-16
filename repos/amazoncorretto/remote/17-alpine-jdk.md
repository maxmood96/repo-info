## `amazoncorretto:17-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:f68eae2a31c62fec8b987bd2dd3fd1831fbef671074ccdc1d652b3aafa6b121e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1a70b6f11045be510604f3f254f120baeb74c03e394e4ea712ef10bdcae2ce52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149394029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40d1391b71856749ed128e7610ba2e3b7026b95dcdef00ec3ba284367bef635`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5df5939bdcf113ce439bdcecfe24681c539b1c385300c7ef0aa8ff1d356a6f8`  
		Last Modified: Tue, 15 Apr 2025 23:55:45 GMT  
		Size: 145.8 MB (145751782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bdc00a04a5d4d5d844725727fc7ccb05e81f95d555c29edee9a4d76619591821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.4 KB (394421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f936c5678b87ae1b5f5e19b22dff7bb17b3b1ca7c4fbeed15dc4ebe0d47795`

```dockerfile
```

-	Layers:
	-	`sha256:13bd23704ca2a6fb32a8e48bdf632abb1591f45687478b94b5b7cecdee6c52b3`  
		Last Modified: Tue, 15 Apr 2025 23:55:43 GMT  
		Size: 383.7 KB (383697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dadc8d7ad934cb120b16f36812743a91b19ad0158360269859826eda99a4ef44`  
		Last Modified: Tue, 15 Apr 2025 23:55:43 GMT  
		Size: 10.7 KB (10724 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b200f2b0558e4d1b54ca5f3d35e3897826b029140991023bef84f51ed9b6c106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148014877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9e9fde4f85da34136a9b934c25468043cfd5afac7f31d358d108e2bae5e79d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d520162c6753354e5e79a046db31a8e0753238fbfe99ec01f51149be0eb89db`  
		Last Modified: Fri, 14 Feb 2025 22:37:38 GMT  
		Size: 144.0 MB (144021848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a0eb9569c9821446b8f9207f6f5cb3c276bc2f72fdd88b67fc91585e4d831be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.0 KB (394041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec352c08b065875931145de03e4317e19e6b9241a19ca74c2c1e115def64a0d2`

```dockerfile
```

-	Layers:
	-	`sha256:b895cbb513760b29cbdd5dcf400456970214586b32e2066dbf6a63b534564ceb`  
		Last Modified: Fri, 14 Feb 2025 22:37:34 GMT  
		Size: 383.2 KB (383164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e26734d36200440b75d4017363b3bead079fae6e9784eca524c20f12c9c4dd`  
		Last Modified: Fri, 14 Feb 2025 22:37:34 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
