## `amazoncorretto:21-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:ccffc59dfdf0b4226605aaacdf33187a2e15943f8c8e5dbd33bbaf4035fd4fbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:69d2f90b4fecf9c0e94d1bc13fa4ebc2da78214e5235c8fb8cdebc54380762b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162376342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bf1d2080d36c221a3afd695a6b60aa4af2fb98db8d640c27110825ba2fe4de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
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
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2520b603c490ae641e4b5bf6491e293e99982e947e16318d832e1e54b5ba04`  
		Last Modified: Fri, 14 Feb 2025 22:58:31 GMT  
		Size: 159.0 MB (158955474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:30ff6b3c9079c4d01c41dd9dda02dd43d5352da7bb5b84142c09dada1937b936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a88f86bbad13e665632916fd3534fe99cf6ff5c71c3fef28f288e1bfec287c`

```dockerfile
```

-	Layers:
	-	`sha256:0c5f931f20adfd0d6d5ffec2acebc2b46e0c7b7572d376b9847d94f9071bc16f`  
		Last Modified: Fri, 14 Feb 2025 22:48:44 GMT  
		Size: 380.8 KB (380790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5e20dbb1e512df8b5d3c1b24c60f8fca80a106706f3cdd84b051b8dfa98cc2e`  
		Last Modified: Fri, 14 Feb 2025 22:48:44 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1c2929845a7dedc375c55424795d02c9b9153c92ab89a80944f8543531fc08a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160295817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a235c26aebdf6df29f1fc801880eb4e84e918a3970f52aee442949b09c4e79`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8068bc7985e5bb1345a87ec8c8c043730dc5f78f17b1fa62bb67b5ae19e31911`  
		Last Modified: Wed, 05 Feb 2025 17:28:52 GMT  
		Size: 156.9 MB (156935285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4e55ee5face74406c765dffd41a90e8a7051213b14debe9df67706663a7b5fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82219d064d6394a1de9a843cb7dcdacadf44ad61ee8f1c8c5e9f2f9dbe6ab383`

```dockerfile
```

-	Layers:
	-	`sha256:7c70a50b8ab47ac3f189377754b4b89b17b81596e1974d56e29cc4255f95e23c`  
		Last Modified: Fri, 14 Feb 2025 22:48:45 GMT  
		Size: 380.2 KB (380209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3e4794b0abd632644b815a0cf629c1d9e541fcc0ba447c8c16db5fc30ffca`  
		Last Modified: Fri, 14 Feb 2025 22:48:45 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
