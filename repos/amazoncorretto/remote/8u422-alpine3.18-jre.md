## `amazoncorretto:8u422-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:9107c2dc3e382273e61084773d71b1fd250210a51610d5876fdc8c9004c572b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:67449ffe634ce5fa0bd41cb4d720f000331571c8ec741d264f4335093393e61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45013402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe9e56416ca41c4c1e56b2ef19b24c54a08c76edf0cd829e89af12a0122eabd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994b6c44122c1740447d00036a8ab4f84d32dad3cdbd06a4df7a47feb3d0d423`  
		Last Modified: Thu, 18 Jul 2024 00:55:51 GMT  
		Size: 41.6 MB (41599508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b7c3dcef4304e4e5530a26155e867894440ef0e122caa6eb7cb8c1c69b71f2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79700d1c75462cb796aab4ecd00ef9e6c32b328c2d6dcd70832e5fbe9870707f`

```dockerfile
```

-	Layers:
	-	`sha256:d1c9fb36ab3dbe8ddab3d40f63dd9960eb2502d8294c9f84e0bfd3a2b46c71ff`  
		Last Modified: Thu, 18 Jul 2024 00:55:50 GMT  
		Size: 184.7 KB (184726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55ce69013b46bf78f833c360b2a6dc68848a90c53cc212098ffab588651fe080`  
		Last Modified: Thu, 18 Jul 2024 00:55:50 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:179b950737b722524a7a26216ebce97018aeebee9b50c6a0d6138626f8e12cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44644472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b926887987079bba23ad9b82aca78f8d6fbe332a4864b9156bada22990ade361`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c2872bbb5bc3028c7442502e2f7daadbfae963779e5add7caeb05af60b8cd4`  
		Last Modified: Thu, 18 Jul 2024 00:59:55 GMT  
		Size: 41.3 MB (41306523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:956b6bc9d565843925d309b343266e46793255ca04e6653300353d507fdb5e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bce433e601efe3f0713a7bf5d616b369b8dee11f396156a36125e9da679c65`

```dockerfile
```

-	Layers:
	-	`sha256:f6dd45a28358e60eb2950a38fe34462c7d58b2739672dc3c1e4545f589d9d015`  
		Last Modified: Thu, 18 Jul 2024 00:59:54 GMT  
		Size: 184.8 KB (184834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3abc526d8b81de54a50d2760cafde97a19ba25b23eb90534057ae607458adcab`  
		Last Modified: Thu, 18 Jul 2024 00:59:54 GMT  
		Size: 8.7 KB (8730 bytes)  
		MIME: application/vnd.in-toto+json
