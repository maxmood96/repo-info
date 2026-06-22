## `amazoncorretto:8u492-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:76fbd2d44056c66cb4a69696c9db8949ea534b25ef962ed40aab6921001deb2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:06974279bff854d0130a5ed2831215fcfe6d191d53745e35b61bae0359709278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104539969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddb52d98dd003d7fa01669776e705a341ad692c6517c3d6fba3c6ae1bbc2d90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:22 GMT
ARG version=8.492.09.2
# Mon, 22 Jun 2026 19:53:22 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:53:22 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:53:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:53:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e7ee3d7f404030756e683eb66fd45d8660f6df45690a3e2309aedc94713622`  
		Last Modified: Mon, 22 Jun 2026 19:53:36 GMT  
		Size: 100.8 MB (100752374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8450870795f3194e96b4b789ffab8391fa3903f033e0f57cb6bf1743735c089c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 KB (257034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549eade215adb57647f08888860d88d2cdd7ab00f2ea61d50d483d23cb2b37dc`

```dockerfile
```

-	Layers:
	-	`sha256:a652ee1acfac5bea949dbf2c0491c579a49fb84af4974a54f7ebfe039068b12b`  
		Last Modified: Mon, 22 Jun 2026 19:53:33 GMT  
		Size: 247.7 KB (247679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0dd0e35852cb3a4fe31e4724fa5e49f70c04d73bcd795b8c141dfdc1e1a1fad`  
		Last Modified: Mon, 22 Jun 2026 19:53:33 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:56825a4a0d905a1eb6a7fd7d181fdcd8c301f227df37b56946ea3401f227dade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104665748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9092c79c1de8eb02c7ff348b76b830a44da49712b72bd1925291d5534e566c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:05 GMT
ARG version=8.492.09.2
# Mon, 22 Jun 2026 19:55:05 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:55:05 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:55:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd28169ed99d585d718edb77d3fa532e913b80ef553411664feed903a5ad81b`  
		Last Modified: Mon, 22 Jun 2026 19:55:19 GMT  
		Size: 100.5 MB (100545262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bfb0fd149330d2ba72fe13bec4073bdd42dcadc09e6b0e2615a3c55e94964102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 KB (257270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac4e5d408e4cee48dd7a015bc5e9d99b90154cceaed50e7856a171ea84635b5`

```dockerfile
```

-	Layers:
	-	`sha256:a8f3a86ff6b89313637d5173853173ee9ba690346717f7cc369de3377324198a`  
		Last Modified: Mon, 22 Jun 2026 19:55:17 GMT  
		Size: 247.8 KB (247811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa84915392363f7a4069a842318080996153036107548fcd78fce50affbcb62`  
		Last Modified: Mon, 22 Jun 2026 19:55:17 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
