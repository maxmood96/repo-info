## `amazoncorretto:21-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:a98ed1b643548908d47ed794fa8541aa60e6eedc8faeeddd30d179ff477f4454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:de6ff875872d6a67261a198a0ceec56969565cd197d11f873871ce206699df57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162346173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b3a1521859ec9696c435706ddc43e020c5dcdeaa1b978583b2ed44706e0216`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:19 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Fri, 06 Sep 2024 22:20:19 GMT
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
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589ac23588bc1a736179302a647163aad704e0f638ffae13cb20bcf252ae2ee2`  
		Last Modified: Wed, 16 Oct 2024 17:57:22 GMT  
		Size: 158.9 MB (158929860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:360e89876b5e9e2702ee036416654b9b16c7bce2369c294ec5ab11d9e1e90e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.9 KB (389876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2ff3b64336ec73aa4472a3ec7c18b7534361c27f9d37af85600b31add07db1`

```dockerfile
```

-	Layers:
	-	`sha256:2042e23a42687300505db70c79206b7c1779d378a81ed6c422e77f0d946e1a41`  
		Last Modified: Wed, 16 Oct 2024 17:57:20 GMT  
		Size: 380.7 KB (380668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba134ef88d73a4d88fb1c54c2c5bdfe2ba716bb1ab1357b22523ab0e05c6cb1`  
		Last Modified: Wed, 16 Oct 2024 17:57:20 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18-full` - linux; arm64 variant v8

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

### `amazoncorretto:21-alpine3.18-full` - unknown; unknown

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
