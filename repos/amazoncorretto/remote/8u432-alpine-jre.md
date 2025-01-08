## `amazoncorretto:8u432-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:e43691f625c6ac50b1c1f26261322c5b18629f258d744a7515d0e3cf3d4d0942
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dac900d5b979ba6f75254817b4cd67ed633763fc9166dc993f1f29c04a39c8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45270573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e05b079343a5978b477d87f2a25f55f233e18abf8a8dfe9bd4a876e7065829b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6961f5a14c8de2bd0592ceb17aff78869da7d0ed69a1b810056183b189625c2e`  
		Size: 41.7 MB (41656574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:376eb1646c8283f793b6bb4c4bfca732c912a27934646ce6a358c80778906dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e496bbfdcc89631caf71eb0597ce76bea831e5ed02bf56e34610adfa212900b6`

```dockerfile
```

-	Layers:
	-	`sha256:4b0da7e4f803540760b2f66f46fc902190477fcefed8f82c03268cfe6a2de832`  
		Last Modified: Tue, 07 Jan 2025 03:28:39 GMT  
		Size: 181.8 KB (181761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4a92dd6abadcd6d4d2c6890c2a95c034c0b45324502b8cab30ce27448ac721`  
		Last Modified: Tue, 07 Jan 2025 03:28:39 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0fbeb4b9882ab3ddebadc23e23b6614492a613506dd8b2f733950ce8250b5cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45444838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84d7769b47723d929b9f4740dbcd5bf7a354c321ced1987cc1919eee4cabefe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb11b32f228dfe7054d12111ed17f86a606243e60b90fa23cd5e60f830417bce`  
		Size: 41.4 MB (41358152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6a72754cecd82a29743d9686aff6781036b1e7d189e5ad47d928625d56a335af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 KB (191355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424b1929cc41c1877e3cc07ee5fd0be35041511506034758a22604b9e56f0869`

```dockerfile
```

-	Layers:
	-	`sha256:aa95375f2a611dd180cdfa394ed2c8c67624309ad228b62daa259a8daa549f30`  
		Last Modified: Tue, 07 Jan 2025 07:20:57 GMT  
		Size: 181.9 KB (181893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:836e0c3d17591313eead4569eb23d30584397e02322f3d80bfe328b77077e17a`  
		Last Modified: Tue, 07 Jan 2025 07:20:57 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
