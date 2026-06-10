## `amazoncorretto:25-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:d0915ce12f1c011cc332c32ea21ec8ad85ef47b03e46f1a4bfa8c5cd602468a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f410e203926614c1c881e0c2bef1a9b44d31745332795a1ee3b09087d43b4997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184889042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ccc32921bf38da659b50ce7cad6275f6b6b2275a5a1d94786a1becb2118bac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:16:05 GMT
ARG version=25.0.3.9.1
# Wed, 10 Jun 2026 20:16:05 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:16:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:16:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ce265cb26b20d8816a2ad0602632269a02258516905a827f2bae164e7d962f`  
		Last Modified: Wed, 10 Jun 2026 20:16:28 GMT  
		Size: 181.0 MB (181022287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:705918c88af88926d83d26445f016c63d625dbefbf007bbec035a00e93212b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.6 KB (603554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339440a9b5bfc55880a7f050a804536c99eceed016aa784c675793249857a2c9`

```dockerfile
```

-	Layers:
	-	`sha256:41abab7066ecce920eb669368a85f4c216e33c26308ac06add138678daf076d9`  
		Last Modified: Wed, 10 Jun 2026 20:16:22 GMT  
		Size: 592.9 KB (592877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4496611064e92e2855709bc4f60ae79c11c23942de8f71510dfbe60001e1a56b`  
		Last Modified: Wed, 10 Jun 2026 20:16:22 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b46689ad685cc29bcff36b4f4db799686fdf9235d90b846a5dec74a5ed1c2bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182839968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fa4e6fea6ea5000ede86a7a4322e560cdf3e4c9715df8b3360972fe5daaa08`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:42 GMT
ARG version=25.0.3.9.1
# Wed, 10 Jun 2026 20:15:42 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33b730143411dce15bf64440e97c83cf93ed7493459fab653be6afcf61dbb46`  
		Last Modified: Wed, 10 Jun 2026 20:16:04 GMT  
		Size: 178.6 MB (178637638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f242a6974e5a2b67294bd8fcf36b6508ca89a76bb6f91cf5e3d17f178d9093e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 KB (602520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cad48c519cc6944b329216459b1d2ba478c12281258927f2b7db6041efe3690`

```dockerfile
```

-	Layers:
	-	`sha256:ecef05094c84166593cee6236c99704ae49eddfb00ecddf7cfd174733e34787d`  
		Last Modified: Wed, 10 Jun 2026 20:16:00 GMT  
		Size: 591.7 KB (591691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f98f06f9e8fb081581c1208b33a4b63ea6bbb06112d1940917d7131b9a563c`  
		Last Modified: Wed, 10 Jun 2026 20:15:59 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.in-toto+json
