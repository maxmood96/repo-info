## `amazoncorretto:8-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:703c7487a989e45f2a294bf6bf65e39615d04c3a0689d8a95f18ee7e1f05a1bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0ae9374374593458b43af4c586673228dbbf7697df4a77389e9afce85c347c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103612826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7900c67c1df029ffab64d93f9310753b367f9c72a143966c205930c966d5586`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:19 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Fri, 06 Sep 2024 22:20:19 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deea3e2f299bb30f4fe48807a6c261f11f6d36a4e91e98d6fc617fccc96239ea`  
		Last Modified: Wed, 16 Oct 2024 17:56:01 GMT  
		Size: 100.2 MB (100196513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b45c2f448f8e365612a1918ffd415ac8b0a61a2c7dfba5d44bf040bfd875f04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 KB (254323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024ccd1bf5600a5e44ece7c216961deae69e8685a83f850e57b34097bac8cc9b`

```dockerfile
```

-	Layers:
	-	`sha256:6caa471056f4902311281729ba7f6340849f719425126151cdfe0c5096c2c3f9`  
		Last Modified: Wed, 16 Oct 2024 17:55:59 GMT  
		Size: 245.1 KB (245132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9f0abb5b04255628badf2908b2b5e33f013879d7f7cbe72d717dd142300911b`  
		Last Modified: Wed, 16 Oct 2024 17:55:59 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7887818197843d2a6524c27e3d64b286cf37e0e172f54c701d95855903b411ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103319581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d3bc3da39d95a9065dea526da216cd83b1dff82c4cd6f764ff095bb0a37018`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:20 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
# Fri, 06 Sep 2024 22:44:20 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77916e9e33341ec1e73e428b4f21ae347acbd233c42ccab738111bb04ef8c4f6`  
		Last Modified: Wed, 16 Oct 2024 18:08:08 GMT  
		Size: 100.0 MB (99979234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:741a2374fa405e6567e8687c0fc76986f1dc0046dfa967ff1c6a0c5902dc9f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520c515b785ea8002d18365e1e7bee9a7e3d718ecd6674c8abb2edf2c3287d2a`

```dockerfile
```

-	Layers:
	-	`sha256:e6bf85db47b06b291a919ef2830a854ccc0eabd0b03ab354355b7937b112a4b3`  
		Last Modified: Wed, 16 Oct 2024 18:08:02 GMT  
		Size: 245.3 KB (245264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d1866e5379e2aa8a041e3f6fb589f54c068d88fbe02f5cda50b7269381e1e04`  
		Last Modified: Wed, 16 Oct 2024 18:08:02 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json
