## `amazoncorretto:17-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:baf51e0837bd3110657203298414f922f4a460af43b4fe1410063ddc6c632c71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18` - linux; amd64

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

### `amazoncorretto:17-alpine3.18` - unknown; unknown

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

### `amazoncorretto:17-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ac22493d77e900e529b0f7acab8a5a55095b36f313c7c54f21599c3fe53d7d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147690145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0079a7be70f69df0964e2b8729db1538617196183939377fd9b607f3a7fda0a8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
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
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc82dc3a1db2009973c699c95e172526f08b777cff2fa033ade6e891255b468f`  
		Last Modified: Wed, 24 Jul 2024 10:43:06 GMT  
		Size: 144.4 MB (144350651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a611f7ee3565337127cdc6085a56d3dc4b875b88d3f7341f26c1a7db1396b61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.0 KB (388992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e284d4ffb705120b06837b14a14c3345b0a5334df301ddd8602b841d591b739b`

```dockerfile
```

-	Layers:
	-	`sha256:16648857de7ceac999094c17b99691f815f2af93db179e882537a27f211bcd00`  
		Last Modified: Wed, 24 Jul 2024 10:43:03 GMT  
		Size: 379.5 KB (379521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6b4b25436a1ab644632f418161de66419e7c6c5269ac10a0791a84b5be4d9e`  
		Last Modified: Wed, 24 Jul 2024 10:43:02 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json
