## `amazoncorretto:8-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:a9db10f2e526b4f730d453448c8b1296c666d2e2d2e842bc34f86417e2ffc8c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a441d8013f8ac8eee82ea276ba7acdcaab918ab25985ca95b5bd3ccaa000b67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103515764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd9475dbff459958d91086273294c0531ee34edfe3fd70917b836d4fb75ebbb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:5cf9040c5669929577389584bbc869e4612ffe3489d3130a68590798cec73e1b`  
		Last Modified: Mon, 22 Jul 2024 23:04:23 GMT  
		Size: 100.1 MB (100123781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5dc25f36f0430b52724216c3d54a4fe735d4b6d3ae2a71fbd3d61f6e82e91646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f519fd88a5cd258ec1b7a02f3f23de2ae05a51f48faa232e0da0b9c6bce23640`

```dockerfile
```

-	Layers:
	-	`sha256:c41c30dd40b0b6b42a9a45f95069e9a931319ce5729019161767dbacdaf95626`  
		Last Modified: Mon, 22 Jul 2024 23:04:22 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb078d3c0b3c51da454fa7416855d6dce7ce833630dfbf2bf042d1187369050`  
		Last Modified: Mon, 22 Jul 2024 23:04:22 GMT  
		Size: 9.2 KB (9152 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bafe0b6c1ebc1f70241dd3b1b2fcfc4651a5b4f69b1edb8f2feff50fd1fc91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103110963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067308ca46a60dd8eac86c7c2c1dd101f845a3c1c1b387414922d5420ae63f14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:56fa6972279421a2a4affe9fe246924e3db264b8dbafafc4444124333be818ee`  
		Last Modified: Wed, 24 Jul 2024 10:36:50 GMT  
		Size: 99.8 MB (99836718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:69ffdcd660d8d135e9f6ed9deb130ce92d242c1212cfc875ee405ceb1c381c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 KB (254057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6e86bd1b45f145ee61b9084f5ee7fe3f574da83518723a8254ea762b581057`

```dockerfile
```

-	Layers:
	-	`sha256:5019876215c59302a161d08e6801962924b7fc203fc6709c58eebc94e37705a0`  
		Last Modified: Wed, 24 Jul 2024 10:36:46 GMT  
		Size: 244.6 KB (244605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c153a321edc1f3e8f924e4b9699395a61da2eba5bc9b923794c59afa6ff0b1d8`  
		Last Modified: Wed, 24 Jul 2024 10:36:46 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
