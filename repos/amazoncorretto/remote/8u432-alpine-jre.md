## `amazoncorretto:8u432-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:ba73486cebad33b2ef1ed2f418f6df1574aca01657486b64d68af5e4b5d7aeae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8dd1bbc29b01a1d2ce9a26f6955a3873635801041521c39b1b75b421f4cbcb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45280419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79af4bd4f9ee2773abc16090fd8515787ae6dec2ef372f814dc34cce3e3aa2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e455188ad1af7931a1327bbee3397dd55462a2fc888361d9e59a98170e8d4c8`  
		Last Modified: Wed, 16 Oct 2024 17:55:55 GMT  
		Size: 41.7 MB (41656612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da7297d6e1744cc8470fa26743d6a296d61dcdb79642d614a4bb0665a7e23bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 KB (191008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c400eaf9055eabc2c08e9ea033c5c8efec558d48d026032999959ebf48a403e5`

```dockerfile
```

-	Layers:
	-	`sha256:99ebf8d2f820720064686ef2df343cc1c66003e6b07c03e4880d05bf6f1663fd`  
		Last Modified: Wed, 16 Oct 2024 17:55:54 GMT  
		Size: 181.9 KB (181856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7c296b56b60b521e5461817f22026718396595287736045669a128147ffead`  
		Last Modified: Wed, 16 Oct 2024 17:55:54 GMT  
		Size: 9.2 KB (9152 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bc5cd20ad91e6af32503dd301ae6c2c63e2384d60919fa845378dc2cc6450021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45445872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdf85141bde86d0d47f78c752bf7129ab06472a8461dd91961ab2f3341b4a14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d21706bd8ec37e9bf81ab2bce32aabc59e2bef2883f768c342b5916c856c6d`  
		Last Modified: Wed, 16 Oct 2024 18:10:54 GMT  
		Size: 41.4 MB (41358226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb7b17d9e7d4b79a28afefde3bd6a288f9bbc4be3b2cfa7babce22a55f98d024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d7cdd601c568ca3b24bd8fd7a2c9b015ca00145c43763eafacd1f4feb6a3f4`

```dockerfile
```

-	Layers:
	-	`sha256:c5993914b28afbe14c0341136fd02466a018b7db6c01b61b755d5b7f20a69f78`  
		Last Modified: Wed, 16 Oct 2024 18:10:53 GMT  
		Size: 182.0 KB (181988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3963b89a8cdf51dc4734b311fde7b833d399f0871fcf2775c7b3ec4d7317858d`  
		Last Modified: Wed, 16 Oct 2024 18:10:53 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.in-toto+json
