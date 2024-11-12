## `amazoncorretto:21-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:f5a8fdbbf18d1661cb92356a87fcd61e26efed80d9e1a5b944c90d76a8e74284
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fd83e3939954a4b342fb9211195cbbd8d027988247f16a670447a1b09b6090c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162346326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb9058587b017be7242de5d342515d2d5adea0a5064350c13cf8489cd9b68a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4268172303977b76b01af0970b0b0b267a9e433573feb8d929d57b9ec26096d`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 158.9 MB (158929925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:705586867ad505bb451b234ed9dce27833c35cc566efce07e00964b28f75941d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14195116862b9d1d9ce1c6a05d2b482f9ae55bf45efdfc8dd3615354f44be815`

```dockerfile
```

-	Layers:
	-	`sha256:160de646b2ec1ec9da26ee561a2b2cc485c7c6c8f6e5114fe81a3cb13faa4304`  
		Last Modified: Tue, 12 Nov 2024 02:12:42 GMT  
		Size: 380.8 KB (380761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4207ab5a76b8e9650874d9049cf96f70903735f61df524db6ed1ba0d86d8f406`  
		Last Modified: Tue, 12 Nov 2024 02:12:42 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b1ba596d6e5d347d9908f2a42cfe4f94a6b243ea2351c7bc36fd96d4dbf6b2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160219202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abef023c11f3de4b3ac37f445747c9c4a0f263471ba877c58c99cf899cd4547`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:20 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
# Fri, 06 Sep 2024 22:44:20 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:8d15a1fe49341816fd9f574595b7e285e7940761cfb43b65904b165b10286415`  
		Last Modified: Wed, 16 Oct 2024 18:37:16 GMT  
		Size: 156.9 MB (156878855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be974952bb1645762e365c40d2f5ba41b1834896c31125bd8814a51956bdd86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.4 KB (389392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec7806b401d12de011c9d53cc6e8718755094abb61fbfef7724351172dca7a9`

```dockerfile
```

-	Layers:
	-	`sha256:00de2199547efbf7ad03f46673a4085d873f70c7423da50d7640554715cd9ada`  
		Last Modified: Wed, 16 Oct 2024 18:37:12 GMT  
		Size: 380.1 KB (380086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02849e16f342c05fee9cd59adc56e7012c3c547e10b1e16fc3fbff1b85bc550d`  
		Last Modified: Wed, 16 Oct 2024 18:37:12 GMT  
		Size: 9.3 KB (9306 bytes)  
		MIME: application/vnd.in-toto+json
