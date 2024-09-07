## `amazoncorretto:17-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:bb604335084c7d7b63a231dda8bbf27bf4bd238ab4621ef74d5d12bf7bbe0bf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fa6f161f26509950444a5d40b5fb468c047500716ca1f14f95d1bdd9a407f1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149434152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c828f62eb5ced8e01c6ea3368df5d2f764a792decb0f0fcdcc3178a66ff818f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
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
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d81ad08527a10e4dee0da098b704b778c391f4dc37d7f14d9c45ff4401aa`  
		Last Modified: Fri, 06 Sep 2024 23:17:28 GMT  
		Size: 146.0 MB (146017839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2ae4c403f1d019c4494b7a88176fa7765ad1c11650c8c45af496c92cf7e64179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 KB (389275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e31e45d54196b1b58b44d4f90b119b5b4f82769deef6f7f8bc95a46e8ed86b`

```dockerfile
```

-	Layers:
	-	`sha256:27fd695ecc5e2d989ddb80e81427e79a3f283c5bb4c838828e2d22001f1f6eee`  
		Last Modified: Fri, 06 Sep 2024 23:17:26 GMT  
		Size: 380.1 KB (380103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc457047f2a2d14f6d2033c9a911342e5e6308a3c6e4ca531e0d547067e9ac99`  
		Last Modified: Fri, 06 Sep 2024 23:17:26 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18-full` - linux; arm64 variant v8

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

### `amazoncorretto:17-alpine3.18-full` - unknown; unknown

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
