## `amazoncorretto:17-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:a4bc19b7dcd0ab81309e45638bc4dc500cc58a9b78480008ef211ab8658f41c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:87dfcf388172d2097cd44d16f0e587e5dd9c09918bef65e3f6255eae0b204bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149433519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9d392d896e5f66374655ffaa22c579e36e8477763eaf68bfff17ad2aadff3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
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
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4869b4ec1fa54dd0f6a038b979bce6d5bc85a493f83861a293e6c17512ebb8d0`  
		Last Modified: Mon, 22 Jul 2024 23:04:47 GMT  
		Size: 146.0 MB (146017879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cc19dc5b22ca65dc9f7c15a1505cf98ed3149e418784b046afb377363619b260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 KB (389275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c65c8a5099ed69ef8fe74491bfcaa703965d09f52db9a7e80e88a0174157c00`

```dockerfile
```

-	Layers:
	-	`sha256:82695c118257b829eaf358ed6d19d7de88db975f796b7b663227a7100a2f1ece`  
		Last Modified: Mon, 22 Jul 2024 23:04:44 GMT  
		Size: 380.1 KB (380103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3685c1bc256b34d9e4f4098834ddf051be447564df99dc9ad5f2eb46b1fe8142`  
		Last Modified: Mon, 22 Jul 2024 23:04:44 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c42a0b9a62f3a81ea2b0efa023b8c68dfe1796e874f83740171114700759dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147688590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e741326161628e0da27c557a0346f30ac8aac30babe79b70320bb886a72429`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
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
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ad20501618025cbc0fb2d405c801152d1983ede65054d1a12ef82019207e5c`  
		Last Modified: Thu, 18 Jul 2024 01:16:57 GMT  
		Size: 144.4 MB (144350641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6421fa81dbd9ca72329c56aabc14a6f0d7d9182ba4516a7008b94725b28d34f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.0 KB (388993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bef00ea000919645f2db95ea32ea6b4d375d689a741707faf15047775460b2`

```dockerfile
```

-	Layers:
	-	`sha256:f1be24c1074fc8908667e1c47a04bfb582cf077074a712f7bdc0e94047afa15d`  
		Last Modified: Thu, 18 Jul 2024 01:16:53 GMT  
		Size: 379.5 KB (379521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf7dd75d9c9188540cd6a9a5fa05c834e39022801b6b6b63101d5e4d49e5150`  
		Last Modified: Thu, 18 Jul 2024 01:16:52 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
