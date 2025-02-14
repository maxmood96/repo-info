## `amazoncorretto:21-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:58c17296dcd293d685e36fa16fb96216c9bcea5c810a879308abc463a2616d44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e19c11be21bb2e5f1a777444f072df59a973143ad72f99d1e699658fef396bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162597224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53a9cdbdfbf683f678303ade17da4d553e6aa52a21fe9088777e45f6507d887`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7ffa540251e9599ab59922560a3af58866443327324e0f8d0ccbbfeee8f508`  
		Last Modified: Mon, 03 Feb 2025 20:29:53 GMT  
		Size: 159.0 MB (158955509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d9c2a699c42efe1b8523ba2f08e3270ec1136cca11a551a7394a559d8a4f2223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 KB (394306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03759323ffd97405d5adb2d99b39d20769931901933769b057ecf6f391f69ca`

```dockerfile
```

-	Layers:
	-	`sha256:657ea3328fb69d4209e63e4a1f01c5c63eff9982d14f1ca564877fd90fbcf8ea`  
		Last Modified: Wed, 05 Feb 2025 02:18:50 GMT  
		Size: 383.6 KB (383586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24bd79a38e5d4b16aa88de6fe270f43ec05d292e2521ad641a8feebe6ee951d`  
		Last Modified: Thu, 13 Feb 2025 15:20:07 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:315076929d4f0ef03add2944431b0c80f791c32ccadcb19a863435c37d62768e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160927649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e3956b4ffb190da821b672300c20d7dc39dab1d0a6889c90cb2f335893f991`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aada83d83790f5e1e6295c05005003bb6287cc1e27f1d258a9822c644a474a`  
		Last Modified: Mon, 03 Feb 2025 23:06:21 GMT  
		Size: 156.9 MB (156935290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:52fae48a3417c803f72c63248b14167c48533675a9471ea0e5a4f5a664464736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.9 KB (393923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b5f7d40d1c6b025040bbd552c6f719f63ba275d78c78cfead46ed96398dd05`

```dockerfile
```

-	Layers:
	-	`sha256:0a4da304e1e8f62d2cf447e34de55ee9e8568da6114b98998efd9fcca2196e31`  
		Last Modified: Wed, 05 Feb 2025 17:40:15 GMT  
		Size: 383.1 KB (383053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9346fb7fabc804758a91891018f13b77faf5c1fa7321cece2ace4141946afdf`  
		Last Modified: Fri, 14 Feb 2025 10:03:07 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.in-toto+json
