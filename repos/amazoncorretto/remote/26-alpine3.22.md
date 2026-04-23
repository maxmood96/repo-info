## `amazoncorretto:26-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:c3ba5cc83ba1300ce68ceaa652fe765e0498c72117041c83f3ddce472dba7768
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:698161f13ff9c6bbc7d4ef78039f6c2761ff65a8da19e4ac478fb2437cf12d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188745521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d793c1715b1cc05683c9707eff36e011c9a9c4c4f2fe69ea5028fa313d244c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:52 GMT
ARG version=26.0.1.8.1
# Wed, 22 Apr 2026 21:35:52 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9349e7071a3185b59fadba1ef058dfda78fb12b6616b7a78a4deb225e61a78d0`  
		Last Modified: Wed, 22 Apr 2026 21:36:17 GMT  
		Size: 184.9 MB (184937332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b94482727c198ef7fc42f90bc3a557e735cd6a0e01f0e8130a1c738e19bc6157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 KB (596963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e839fc3b5c1f18f2429f7fc1c514292f1999d11c9d90a28feec0898091bd9b`

```dockerfile
```

-	Layers:
	-	`sha256:0fcd321abf4c2af2905ad2d61b0ceec24ccea13c119493269d29491bf0b41d2f`  
		Last Modified: Wed, 22 Apr 2026 21:36:10 GMT  
		Size: 587.6 KB (587592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7215798a5594774774f0c0bda96c73780d0c404f8d32abb521d69b4aa51fc7a0`  
		Last Modified: Wed, 22 Apr 2026 21:36:10 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3e5a9577abcdf704c2719235c33e00e195fc4bed16156031a5b2a0a760303398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186645706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175a8cd0566c1830d13d706374ba4c992209801213618171d7c747933698657d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:56 GMT
ARG version=26.0.1.8.1
# Wed, 22 Apr 2026 21:35:56 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a830bf146c66405e0a06bb5923f3b3966cfd0d83c60ec598c387964e99d8d6b`  
		Last Modified: Wed, 22 Apr 2026 21:36:18 GMT  
		Size: 182.5 MB (182503812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4dc1aeef5994354b9630cfef70c08c543fb09822e4134fccd1720846c64e2ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 KB (596483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59133797e40b6dd7fdad859f6d9c0c5ecf09a9fe9569e526ca4b77da8969d91`

```dockerfile
```

-	Layers:
	-	`sha256:5ff7700cbe8699430db82684932f65a812f46b81ee1411e58acd0020bbb60620`  
		Last Modified: Wed, 22 Apr 2026 21:36:13 GMT  
		Size: 587.0 KB (587008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9e37bb61535c2b610669b3ed207a7a87d811c781f8a550cdfa8bf0144e3c69`  
		Last Modified: Wed, 22 Apr 2026 21:36:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
