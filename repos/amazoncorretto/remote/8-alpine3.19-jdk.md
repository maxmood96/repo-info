## `amazoncorretto:8-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:6888b71c46ea87519f3f06a737efcfd86d02c6a03f280b42f9f28bc19e255c65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ab04677ba50f13d706aaa605cb6b958e432f78bdc985ca90d60c517be0f66541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103543500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b15f16dd1fdae917f3d3a3a6890767a93e7185b825a6ba3235dbd32101b449e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b029c37f0d522c2e091c955afb4ec8720f38b3e008c1c117f32f3beb349981`  
		Last Modified: Fri, 06 Sep 2024 23:16:56 GMT  
		Size: 100.1 MB (100123794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:681cd2a57184202fa693d5b39d5e56803eda93989dd3175591ffcaea075c99f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 KB (254887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8696169e0c7d15a9621d2f8d80b97b21f9baa28f9f8af566aa3630651579e8d2`

```dockerfile
```

-	Layers:
	-	`sha256:924204ca55c425b1f3de5461a951d79e994ac6cd59da0992a7332e17da392138`  
		Last Modified: Fri, 06 Sep 2024 23:16:55 GMT  
		Size: 245.7 KB (245735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8909278f6bf0f335634fc48725a13c8a63b9395597bd996ad679ddec3efa6232`  
		Last Modified: Fri, 06 Sep 2024 23:16:55 GMT  
		Size: 9.2 KB (9152 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:97b2e4fdcbed36241cf2dc923b536fd220d36570ed3d1f0154507a9ebdad8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103194515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e293f095c24ca7c39eb6e19372a0a6ce334db98377301757d19d0970448e2875`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
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
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0056494a1aa6c3ca1433aeeef8811a49d0fe89dfa3c44ab34b0ee980f38384ff`  
		Last Modified: Wed, 24 Jul 2024 10:38:44 GMT  
		Size: 99.8 MB (99836057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8c99cbac54c0ef86ba07de6df885797a95aa689ebbdd1fe43098eb785c93b3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21420430178f9580c27bf77b2c5bae215e47a7a7b1c4f68892d941d6d6873dd6`

```dockerfile
```

-	Layers:
	-	`sha256:f20d91b4dd898ad56f6b6c173b54cd603bcf1caec9d76091cbac1492bcdde708`  
		Last Modified: Wed, 24 Jul 2024 10:38:41 GMT  
		Size: 245.9 KB (245867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3221c93313e40b51d85b0622e70016f57f6a795e5a1e14c2756a500f824fd29b`  
		Last Modified: Wed, 24 Jul 2024 10:38:41 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
