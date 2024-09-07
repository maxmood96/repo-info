## `amazoncorretto:8u422-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:6f34cbdf05afe17dd275b15d82255dbbcf7c0987405b96d0f0f2f4107a5041fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d66a2dba0e72189c58d280f28f99e66968d9f328000f3ab447d2144d3be199a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103515959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb6cb41e0eb07c8ccc6fc69d8014111b6ab90c3dbbd8b81afde3e6312998e45`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
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
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac45a1b3328851d3a69f841b16c469a5c65d8453f58c091d793e936e6aefb5fd`  
		Last Modified: Fri, 06 Sep 2024 23:25:38 GMT  
		Size: 100.1 MB (100123765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9dc2f3640f36c209f375f22c019fcbc59fe8ebd752fb74e384d78b871a9cf815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b129dac7c45c0d2202f739026c94121d9d8fc40c78f62fe98391d4122d6336`

```dockerfile
```

-	Layers:
	-	`sha256:857ebf6e1e7e05b0bbd551d7e1447c253f4c02139db719d636a5785439b78d01`  
		Last Modified: Fri, 06 Sep 2024 23:25:37 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0671cf9bc2ff4009fb04a8c24b86df6704e9039b294e0ff3b26b6b67530008d9`  
		Last Modified: Fri, 06 Sep 2024 23:25:37 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.17` - linux; arm64 variant v8

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

### `amazoncorretto:8u422-alpine3.17` - unknown; unknown

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
