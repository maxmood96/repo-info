## `amazoncorretto:26-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:030d6e3358ee09b3a96b62bc98add64402090c3d849d6969b9697992850ee22b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dfa085fb90e60973ccc805eb3b273e24b3229025ceefad3e234f4b8761b69bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188535674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5d1d5284a3de449f81f8a06e00084596baca3041ca24f0a27cd2372dc183d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 22:59:48 GMT
ARG version=26.0.0.35.2
# Tue, 17 Mar 2026 22:59:48 GMT
# ARGS: version=26.0.0.35.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Tue, 17 Mar 2026 22:59:48 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:59:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 17 Mar 2026 22:59:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb9c9167e1a1c8f3307494562154382679551edb09c334a071971322fb9fd24`  
		Last Modified: Tue, 17 Mar 2026 23:00:11 GMT  
		Size: 184.9 MB (184907810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4d9ee3b077412d01ceb8bedcf7d5f7f272272ecbd7c2dc5a5ab9f0ca88a128ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 KB (594308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16afad17ed25a4ac9a39dd8bc5bd04636c948087af28b739a7acde35c9ba4061`

```dockerfile
```

-	Layers:
	-	`sha256:4282250ec039107f093b641ef905acad52b608980a43d0ac19a889eb0aef8fd7`  
		Last Modified: Tue, 17 Mar 2026 23:00:09 GMT  
		Size: 584.9 KB (584936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f1493bb7e96b67afe8cc44faca346e3bb6ae595f6aefe8b2e02768a80e4f888`  
		Last Modified: Tue, 17 Mar 2026 23:00:07 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:610042cc06087f256365e15d9f3b1b3128d17073bc02bb5f82eb63b6df9ce3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186581730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f69b753453a53d32615fad72a1852378ece021e1c229e5055420dfcdae71bd5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 22:59:45 GMT
ARG version=26.0.0.35.2
# Tue, 17 Mar 2026 22:59:45 GMT
# ARGS: version=26.0.0.35.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Tue, 17 Mar 2026 22:59:45 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:59:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 17 Mar 2026 22:59:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3830fc3e13fffb9bf1af68edfcf01920a1c36990b537d2bfb46281057ac25675`  
		Last Modified: Tue, 17 Mar 2026 23:00:14 GMT  
		Size: 182.5 MB (182491772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42384dc9d2e02eb025bb9718cbdb46654bcc5bf21eb1e379a1cca7c0ca26b685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 KB (593828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a271feef9ec3beaf3972b76501cfb8e84f11085737a93050d48d6ade2971197`

```dockerfile
```

-	Layers:
	-	`sha256:5016ac7e5fc98557bc53367753769bc6ea3420170bd2496e493cfd55d5f6d361`  
		Last Modified: Tue, 17 Mar 2026 23:00:10 GMT  
		Size: 584.4 KB (584352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcaa7e29ff6a4a3d322fe62a37b642e9769c1fc987184e25c9cf59101134edf4`  
		Last Modified: Tue, 17 Mar 2026 23:00:10 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
