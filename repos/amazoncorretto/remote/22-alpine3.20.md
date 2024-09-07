## `amazoncorretto:22-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:d36f9da84f78b4d933284ed516423ddfcec6c3e8ce1d3db800f715942a0968cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.20` - linux; amd64

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

### `amazoncorretto:22-alpine3.20` - unknown; unknown

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

### `amazoncorretto:22-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8afbb5325b2a78e021a259d2ebbf8edf4acfc6333ed89f898e42a61e0326a4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159281526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3c61241d3ef8164d5c70161541298abacae97c7fb2edfcb42102e2e50735dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2251b4995505272639eb5fb27f50591491b82fac889fa964871649f57d8fdb7`  
		Last Modified: Sat, 07 Sep 2024 12:18:02 GMT  
		Size: 155.2 MB (155193880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0b791306fe0910dd5f96d6cf9c1194b092828b1375f46683cb916fa74312a83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a6e6b05a03ed4f2a7aabd5195493eefb1d89f97210243a3ab43cb6ec812803`

```dockerfile
```

-	Layers:
	-	`sha256:33a0fe6046a06f48ee8349638ac4e32fb0eaa89e880fca80770ec7471236360f`  
		Last Modified: Sat, 07 Sep 2024 12:17:58 GMT  
		Size: 377.8 KB (377802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88b8865ecc307c3eb453b4886440a9d3969043242b9d96360aa81a51afd848a6`  
		Last Modified: Sat, 07 Sep 2024 12:17:58 GMT  
		Size: 10.8 KB (10823 bytes)  
		MIME: application/vnd.in-toto+json
