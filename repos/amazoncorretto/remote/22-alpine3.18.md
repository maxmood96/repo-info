## `amazoncorretto:22-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:61da7c24836838b3f18d6fdeca3d45621f9fdf4574f663d95d933d48355cc1ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:36c2fde0d61902f11bc6f0680cd617e752125a684269e1ccb76ef166f834fb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161009954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f218f2938594967211eae70ccf0ec9df668c0c80e86bc529438b38cab66111f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7959fb12c66440d5180bfca2dfc4f259d7bc1b9389b27931e222b4af8aa9c2c0`  
		Last Modified: Thu, 18 Jul 2024 00:56:14 GMT  
		Size: 157.6 MB (157596060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:85782d119a87e5ae76b9d49e7e98acbad0903bb787e08582b58f215f7515fe06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91396222fa11eda3df740cb92e1ff4300fad2ee4eb4ea446bec31e69ac364e2d`

```dockerfile
```

-	Layers:
	-	`sha256:e11e9fc620285080692ecb4c5777ae2b614d0bebc5143a88aa587284841a89ac`  
		Last Modified: Thu, 18 Jul 2024 00:56:11 GMT  
		Size: 381.2 KB (381246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47818492f67065a6c9284aea4f1425d0725fb07bd1a414c9c2c8db812b42e0ae`  
		Last Modified: Thu, 18 Jul 2024 00:56:11 GMT  
		Size: 9.2 KB (9168 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:098a313fdd8abeafd96ad1eb32333f0a805f0bc4480ce66e778c7e8e17ab09e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158532602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f69209d58678890a43cb5d0c9324694519e19a30cb4596e995b98717da758`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796cf498de94a64529afbb555d2b35f784240369fda345d6654c4fee91087337`  
		Last Modified: Thu, 18 Jul 2024 01:29:23 GMT  
		Size: 155.2 MB (155194653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:606d623ec3b0b384e5568e3b3306b29f13d4bb33a802c6c5fb00c72073038695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163ce0b81e013bd6e4c0b8159f2950882c0e959666bb119cf6f91ae41b858b47`

```dockerfile
```

-	Layers:
	-	`sha256:42d9219874226c8f4ae5d2b17f53341fad24b84557092a93dcb68214aef98157`  
		Last Modified: Thu, 18 Jul 2024 01:29:19 GMT  
		Size: 380.0 KB (380023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fb05fda2364df2d4628eab358f8fa986f416e3ac2dd409c8c972db588f6ec7`  
		Last Modified: Thu, 18 Jul 2024 01:29:19 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
