## `amazoncorretto:22-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:4b00240d8a663a7353f8e99858002911e78c1a785faef5304de8f82ea9c1e507
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4a22a70d6efbf7d3863d2564c201a7a64498df9373f80087523ed597e2b710dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161220099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad83d8031e298811461c4adfba5bbe973af1105172c459d75cef1d38a47fb95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3033a7d37db666ef239184a0fd25c7e469e10b5e27177edb44d51baa9dc4945b`  
		Last Modified: Fri, 06 Sep 2024 23:18:15 GMT  
		Size: 157.6 MB (157596292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7c9fa98b033d30ae1ae034c2249087c4f4357855de40fa4b4d4fe94623cd311c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5e590eefd4058bda4cc4163500b63dd88aee90733df095ae93a334dcf05c28`

```dockerfile
```

-	Layers:
	-	`sha256:f6694a7071173e6593bd98c9235d156186879d877b25f3a96f7f92537fc160ba`  
		Last Modified: Fri, 06 Sep 2024 23:18:07 GMT  
		Size: 379.0 KB (378977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638a09d6f30d4e7d9606d8222231822702e4666ebe3e6e29b94b20a2ce8fb6f2`  
		Last Modified: Fri, 06 Sep 2024 23:18:07 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d835e68c4accc0cb8809ab3496a1abb184814b9225187c806f82657f75c6b919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159280830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb271c7b69e49ed895b4065dd60201da1c658ba7db1fb1391d20cacf6711a49`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5893b25a591ff47218e93b92f9fc1ff73ccd174b6e29550140ae40f4b8c6a93a`  
		Last Modified: Wed, 24 Jul 2024 10:48:47 GMT  
		Size: 155.2 MB (155193896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5cba8ce9c0ae790657dd5439d823eb9c02627e6a2ec19711b418cd0845579455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb3d90184be45edf159b910f8b2dcc16a7a2a510e1ebf5f9ba5fe83078e63c`

```dockerfile
```

-	Layers:
	-	`sha256:4f8f9255456c40ccf099f26f05a2522aa6042629956152d91aa817fcca2ea5ce`  
		Last Modified: Wed, 24 Jul 2024 10:48:44 GMT  
		Size: 377.8 KB (377802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4970d5896f1f03a96bdb09c4433ca744a4c87797a719334d7907ca88082997ce`  
		Last Modified: Wed, 24 Jul 2024 10:48:44 GMT  
		Size: 10.8 KB (10823 bytes)  
		MIME: application/vnd.in-toto+json
