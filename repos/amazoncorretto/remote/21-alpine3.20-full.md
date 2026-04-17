## `amazoncorretto:21-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:3d1bce6174335354d15b79a84c55c4bc35ccc3ecb1211eb911e3d54232c983f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3576f949075c62bfe7e83e6f32d8206de9b99b678c309b0d588edce490f64849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165208543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f2b8ac8cd82a2447371898acdcc4690d3a83c9e39bc6612a7143a66709c541`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:43 GMT
ARG version=21.0.10.7.1
# Fri, 17 Apr 2026 00:22:43 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:43 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9e132a2a5ff4f1c6f30e5c9f06cf23dd4d2356f123c7bcc1ea3291fc95815a`  
		Last Modified: Fri, 17 Apr 2026 00:23:03 GMT  
		Size: 161.6 MB (161578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:68ecd9ddd2a657cdcc97fed87283cd68609d4d22113896a71a121538cd0df2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 KB (589931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4838b624a1ddd69773a80d5f79e92c25cb3a3f8263dcf0c89d1643469f0b28`

```dockerfile
```

-	Layers:
	-	`sha256:18924a23804a746329676fc7b475cd3dc19c801abca67e8ead398e123602610c`  
		Last Modified: Fri, 17 Apr 2026 00:22:59 GMT  
		Size: 580.6 KB (580557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ef5eeb0d4100ec84c8cafb153e69c69319279bb0637f0961f13431ba8944e4`  
		Last Modified: Fri, 17 Apr 2026 00:22:59 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fd4e0965ca5e16371f08b8df5f36f4bb4419f8ccad8c0f2e6880c01a6261edb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163711919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7992a79cc16bd1619f17b13eb420fc13fcf591637cd070b5942b472bc56320b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:01 GMT
ARG version=21.0.10.7.1
# Fri, 17 Apr 2026 00:25:01 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:25:01 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:25:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:25:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a153d0efe0061c262e6682b90a30eec975f3271b2a01782c1959b258c2f21cc3`  
		Last Modified: Fri, 17 Apr 2026 00:25:21 GMT  
		Size: 159.6 MB (159619600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bf097d9695970f843f5dbed78c84a271d40cde10b31a2b6a2d8b3e8690c49f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 KB (589453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689312434d98a076888d1ec0ff9c8cb07446084296cb0a58b6592888b54cd960`

```dockerfile
```

-	Layers:
	-	`sha256:3906eb55cf4139a75218a9ffa4ed0e3b0fe907759dd0d9fbaa3982cb7c59990d`  
		Last Modified: Fri, 17 Apr 2026 00:25:17 GMT  
		Size: 580.0 KB (579976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30601c41c5a210985d11db44074db9f43eac28877649f23a52d89902c7f0d04`  
		Last Modified: Fri, 17 Apr 2026 00:25:17 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.in-toto+json
