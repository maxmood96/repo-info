## `amazoncorretto:17-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:23ee84c9fd63306018730e5fc070ab6e623bf94294235afecd9d39f5d26c81fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:72e0e21ab23d6f2b4410460895eeebc1615faf9f574b741d26c44f16f9ea08f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149057175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4478a041c368e36feb180f5ce9ab80f62394caec5812fc211cf35ee151b388d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f26f5be93edbd7d77bfa9627d393eee48be5fbc335bb4995392026fa35b21ac`  
		Last Modified: Tue, 07 Jan 2025 03:29:47 GMT  
		Size: 145.6 MB (145649543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2b3b3834511489206419d0f8fc8432ee81756f3112bcaae0f340b24b47d945b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a365aae5a2599a13b350bf628051cf85f393a4bf9c221480b7724a965013d611`

```dockerfile
```

-	Layers:
	-	`sha256:1fcb7fe8ae4dfb88936e430f553310e32d4d73b4dcc76bebc0022cc738537764`  
		Last Modified: Tue, 07 Jan 2025 03:29:44 GMT  
		Size: 380.2 KB (380236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d37d5a713a5f7ab2d2d0e5e01098068afee0ac30b40edecd5a2d40f80836a0c`  
		Last Modified: Tue, 07 Jan 2025 03:29:44 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:94ac2b62e44e3e6894e768a70e9d65cf8e91c82d351f5e23fa147ef6ef52a29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147272443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37406342095f6dde08fbc6a983a10d651c083929f989bca869aae0240419fbd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc44348b713b011df0252765b9d6f82671c6ed492c3aa2653ff5224e6fe826`  
		Size: 143.9 MB (143935008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0e50973a10bd7c70352008c528f10bb9fe1e8536aa80d0c6210b25df0c7f893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb657b8139a01a665e748793adf5ba0c2bc114920ae7cd1d68e8f1273b181ff`

```dockerfile
```

-	Layers:
	-	`sha256:5b7590d758bbb5ab417998e92ef79936e983e56da4e744ed9c53624863d354f4`  
		Last Modified: Tue, 07 Jan 2025 07:23:08 GMT  
		Size: 379.7 KB (379655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7595f6a3d99f4063f69cfc9550781f7190775d02261ab5457fd6537440d95f`  
		Last Modified: Tue, 07 Jan 2025 07:23:08 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json
