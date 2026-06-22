## `amazoncorretto:8u492-alpine3.23`

```console
$ docker pull amazoncorretto@sha256:af3f9072b888d7a452054380080ac9989de695f60284e861b4b96758da3d61ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.23` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd6edff8a6d451b2fdeae4486df5c1db6e623f2dbd8fb4cc0d99544ebde8ca5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104595828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff9134d5a362f351954d9a4d2615691388de99f72f89d368f5974763a31b754`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:42 GMT
ARG version=8.492.09.2
# Mon, 22 Jun 2026 19:53:42 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:53:42 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:53:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:53:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f3c4d4c9c4dedbfb87c6fd93779b4557362fa6c8ecb6c2c79586261408603e`  
		Last Modified: Mon, 22 Jun 2026 19:53:56 GMT  
		Size: 100.8 MB (100751407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f8577a2d8149e7584b403def5efb8a73cea570ac7b5810801d840f5adb5bc429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 KB (255750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc513f4608b898536b1c5a185fb2b1c423dd0d460da5940aa12ce809f118da4`

```dockerfile
```

-	Layers:
	-	`sha256:cc31368f59064ad331a60421a5aecb5ac6ea6f4eeef70bf00aa7070e05b3c660`  
		Last Modified: Mon, 22 Jun 2026 19:53:53 GMT  
		Size: 246.4 KB (246395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a2a82a0924398b5a936d6675a28d41b4426de53b59103549f895b3c13f41979`  
		Last Modified: Mon, 22 Jun 2026 19:53:53 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fb1eae10ce19a263687296fb3e1674090c12172f32fa90249dfa47f9f58307e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104726683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79244fbf288ae4078e0edc0ef6c88bd30b9dc8cdd7f8537b7829e08f52d7425d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:11 GMT
ARG version=8.492.09.2
# Mon, 22 Jun 2026 19:55:11 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:55:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:55:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acebb8a27a8a24e1782e5c771db390498b6dbf05653299f2dc32dce10ec19d9`  
		Last Modified: Mon, 22 Jun 2026 19:55:26 GMT  
		Size: 100.5 MB (100544823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.23` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3c85795030ee8af9530b1f0fba76ef5b34cb12f81c746af1d00e2258f251f594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d887aef89fb778174c109c7c3047295310f49705e0633c3f56c76ac0fbdb5f`

```dockerfile
```

-	Layers:
	-	`sha256:a3be0b857d1e98795fe994432c67544ff5f8126cc0d34437e33ed3e48512121f`  
		Last Modified: Mon, 22 Jun 2026 19:55:24 GMT  
		Size: 245.9 KB (245877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb9bb1d0fbb3db4e4a820654d6b7ae93b6143a56337555d922c6cc97ae21b5e`  
		Last Modified: Mon, 22 Jun 2026 19:55:24 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.in-toto+json
