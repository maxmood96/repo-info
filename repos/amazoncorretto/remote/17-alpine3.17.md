## `amazoncorretto:17-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:165a858883a380ba817020c9beb8fd3a0440593efa8d7f888ea103b2400c4cd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:50307bf3f89cb3fad176f87ee077d3f3b8de189cae6f722ded1628ec6429fbe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149410269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3fc0a37b1c68b66bc18a9020d83a40d1cb242aa12a3729f512212415628b38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:d3444c516dc5f23fd7c8afac94b24d4131fe5686c4ed8ff39d4735d58a937bf3`  
		Last Modified: Fri, 06 Sep 2024 23:17:28 GMT  
		Size: 146.0 MB (146018075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ade46c7395c23c034a89a8d94b039bcd0dd22404e2fe4d9aeaea5d6d925133e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 KB (388671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6541bc8f75c9aba0a5b0f7657e6984ce7d9f11ed58ed6b04ed67d223557fe6`

```dockerfile
```

-	Layers:
	-	`sha256:e3e083228144943b31673aa2d6c92c5a8a6ada6d1d485db99a7f8c18640cd9ab`  
		Last Modified: Fri, 06 Sep 2024 23:17:26 GMT  
		Size: 379.5 KB (379501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f5901823f30fce11de92aa0c8c9f2834c53f0f5e2f285a346984e199048dcdf`  
		Last Modified: Fri, 06 Sep 2024 23:17:26 GMT  
		Size: 9.2 KB (9170 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5671210b7993195a6c82a09010ddba3fff14c9caa021ca2f582938f60d7296cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147625231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b900e71f75410598c970edbe48d9e4f0d1fd5b0db107458dea6dc0fc29a7afe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:7d898c3412cf1a9dab89eb64b5d53b9b616e405d8f07eb98067ffd87e5938196`  
		Last Modified: Wed, 24 Jul 2024 10:42:32 GMT  
		Size: 144.4 MB (144350986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4b848bf458600330a90916e48120387577a7590f396c601b1b8bec3d76aa783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 KB (388391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39e4e333e4e06744579489a69be8610324a9d2894ea815b8340398d089bd385`

```dockerfile
```

-	Layers:
	-	`sha256:fc8365768784ac6490ed7e9fd2f15137b70c63afb799f28338c93194ce5145ad`  
		Last Modified: Wed, 24 Jul 2024 10:42:29 GMT  
		Size: 378.9 KB (378919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44236371ca73dc4339e020f9d149ac8beaaa4c8ea5f1e443eef8fea5cbcddff6`  
		Last Modified: Wed, 24 Jul 2024 10:42:28 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
