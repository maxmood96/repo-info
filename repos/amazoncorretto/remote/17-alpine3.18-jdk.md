## `amazoncorretto:17-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:d9d9c8ba138c98ebddcd71cd01cae371661836690cb9d835cf7d589be7355078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6793bff6ea9ee12727ac172f12035911abc4ac3c2193db5af69ebfff858d9f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149066060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3002363862d49edf2e742772fa6e1772ac62335f980268d5113fc1dca1be4d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:b921c125852ad0e9e3e421d92b4a36fd5790b188966cfb26000f7f1220b7d1c3`  
		Last Modified: Tue, 12 Nov 2024 02:12:22 GMT  
		Size: 145.6 MB (145649659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2d91193d3726c4bf2f66c352ad72cc7c1a1591268201a803b92492a164bb0195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 KB (390286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120b7f775bfb594c898f0c30b63776b51c1214680a791f376d00917d5e43cc1c`

```dockerfile
```

-	Layers:
	-	`sha256:396a3f52c225213b54a7ba017a04dd31026e48582ae77ef923bed28340901988`  
		Last Modified: Tue, 12 Nov 2024 02:12:19 GMT  
		Size: 380.9 KB (380864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df42273eaeea4778b8732817308c1854fd052093de3493b2dab22af25c7423`  
		Last Modified: Tue, 12 Nov 2024 02:12:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:71fedd85a199ded68dbcc2b9edc2204d7c04ad276efc1bcd55522c7e6dc319e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147275452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157da672fdfe0cb7da013c462c3ad386a888f32c1fa8aefe5316a751efdce995`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:20 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
# Fri, 06 Sep 2024 22:44:20 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:20b74d3b9ed335fbe43398dd3822e24860bea37ca78d2f86da7108d2f914193b`  
		Last Modified: Wed, 16 Oct 2024 18:29:17 GMT  
		Size: 143.9 MB (143935105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4ed4a191b1b96e424144e7e515282a1a30273522914e43cc2bdf1e4e5d2b145e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72925581d0600c2d05c954634adb4f5af8a978fb4bbc19e154bcf44d44c1128`

```dockerfile
```

-	Layers:
	-	`sha256:e5df933c69d5db7b1c9fa3bfa30b46f6bd5a27478af6f0d6cb5b0bc00558af9b`  
		Last Modified: Wed, 16 Oct 2024 18:29:13 GMT  
		Size: 380.2 KB (380189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4981287a2135793e2825d17bbd36115d460e29022be448f58dc1a951d2ca9b6f`  
		Last Modified: Wed, 16 Oct 2024 18:29:12 GMT  
		Size: 9.3 KB (9313 bytes)  
		MIME: application/vnd.in-toto+json
