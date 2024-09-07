## `amazoncorretto:8u422-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:bad271cd19d4a6574db9842c11a37a35ddc677eacd6b249a7eedd6ff242f4887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:97cb328fefb0e5a87ef02b064fe1470bbd3f61aeb7026ac838352ec4d5d9d3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45019092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffb8d96e75287f56484eb204e3987e8d6d1320ab434dcbde79c5978bdea57f4`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42ac38a39ce917c8fa653be82c1869e9fd3c51eaf89abd93076dfc5e6538eee`  
		Last Modified: Fri, 06 Sep 2024 23:16:50 GMT  
		Size: 41.6 MB (41599386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ad5b25cecb835c71bd4323e3c63197c5e8890c8a88031f4c86c45fa70ac67d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 KB (193840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbe85682a7f3382274f30ace367ab551889c981a1a7c445c9e82fafd02091d2`

```dockerfile
```

-	Layers:
	-	`sha256:98f5b36e6565af6b28204415b7be16fca6497baa75d7e9b27a1b9d285b838965`  
		Last Modified: Fri, 06 Sep 2024 23:16:50 GMT  
		Size: 185.4 KB (185386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796aca45c93ee7845b005b9970f2b67200281a600baebde25b650c261c58996c`  
		Last Modified: Fri, 06 Sep 2024 23:16:50 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9538a2b793ee93f06c2799f4b2670764e6c3c437abda5bf5f04bccbfdb34ffc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44664813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be80675ea7802c0be6238bb31af322e6a87ecd733eed3653fcea58ceb0b18192`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa05f4653f562974719f7a494477ed9b48d6e584aaa7240780c5808b0b31e4c`  
		Last Modified: Wed, 24 Jul 2024 16:29:00 GMT  
		Size: 41.3 MB (41306355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:71988921a0d7d96b0c7245ee783627a533f037475014cc50d442dcf7ba1bbcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30a788467cbcca9f479d7e44137ee12e5ab9964813180cb9fc542494636f532`

```dockerfile
```

-	Layers:
	-	`sha256:93fb06ca027b1d33b593f8fd32e6a409a06a3cda8a8f98f89a11f8d0d5173e8d`  
		Last Modified: Wed, 24 Jul 2024 16:28:58 GMT  
		Size: 185.5 KB (185494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e5c47f21fb8fb8c3c161a15aff969b7694ede48954bd48a48ee4f5c1cb2558`  
		Last Modified: Wed, 24 Jul 2024 16:28:58 GMT  
		Size: 8.7 KB (8729 bytes)  
		MIME: application/vnd.in-toto+json
