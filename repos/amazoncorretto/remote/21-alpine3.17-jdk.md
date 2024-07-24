## `amazoncorretto:21-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:63cbe5e500fa84c6899bb93a3d15de44bd3d3c29f336474d44a4d375370e9350
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ac4d4c0d35de5fbb02b50311e15094c71900111e7e8a09c5f7d764a1b0403942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163117934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc5b4923e3022e3c03c5f7a43e9068b81a9085e9dfc2db6d58c2c20a9c2489b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44c00d4452a5e223d458603c605088f00231c18389875ceca615c171907e0a1`  
		Last Modified: Mon, 22 Jul 2024 23:04:51 GMT  
		Size: 159.7 MB (159725951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b318b6cb187542c29a2fd81a6b37c61b4ce70ccffb2b4059f704ee231ba8f43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0503e82e8047a9ce690f5da518cf5885fbd12130af9cccbf39acb63d1b644757`

```dockerfile
```

-	Layers:
	-	`sha256:aff4177fafd2c62204918eaca2510cc174611d9b36fc1646a24ef199f3db8672`  
		Last Modified: Mon, 22 Jul 2024 23:04:50 GMT  
		Size: 380.1 KB (380051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aad8d527268cd33d9cbd8975c489c535a16f8165538202a17e116436b4ad16aa`  
		Last Modified: Mon, 22 Jul 2024 23:04:50 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7a06a101c173d7f3db72118ccbcb60888bcd3b17f50d68d230ad31fef34522f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160755587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7ac312f5a711afc14064c50c5b9dbbd94490a3de0768c0aa0da1a26fbee25f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdbdf0f0c52af4de33f458c34ed59b7436bc44fab66acbb988a948adda29273`  
		Last Modified: Wed, 24 Jul 2024 10:44:53 GMT  
		Size: 157.5 MB (157481342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:09cf2717bf9e3374a5055df6810b087b36cf7ab43a92e132fc8ee82cdc23819a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7381988c11306aef527c247dacf94385c53ec838d9f1115be1c276d7c39606`

```dockerfile
```

-	Layers:
	-	`sha256:373bf87914cd83bb8e31cc07e9a537179cea2b4315d6c3fd375e7bc6f1624051`  
		Last Modified: Wed, 24 Jul 2024 10:44:50 GMT  
		Size: 379.5 KB (379469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f665170e8e289a9da5403c12552f7cb963d4a7b54d571005ba5d4c14a21548`  
		Last Modified: Wed, 24 Jul 2024 10:44:49 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
