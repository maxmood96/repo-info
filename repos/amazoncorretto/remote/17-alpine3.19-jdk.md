## `amazoncorretto:17-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:858d1163d0eb571c698e9ed22cb21b48473c4fc21410dc3f373dd0baa2865a21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:63d141d176e186719cdd207b2798edf3c338d3006e476a276b2b9d6907abbc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149069629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5249495cb7e82701f9af101a91c48861f1313a737d2283e1549ab8c9a9bd79bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba407145c9401126c3dec836fcba3e11997e54f81df4d4144407ff22c0aa6dd4`  
		Last Modified: Wed, 08 Jan 2025 18:13:20 GMT  
		Size: 145.6 MB (145649387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e9085d81ff004710cf6f1c159eef2de0b3a6a71162711af07a9726746c5fe1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 KB (390317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b37bee8ff94e0be05d9a4ef67efbb2988fb8d235a30c208dfa91453ba02f72`

```dockerfile
```

-	Layers:
	-	`sha256:aaa7c501f2e149097506c74ca0c5965f2b943b00e2c5776d29ab24f9f19519e3`  
		Last Modified: Wed, 08 Jan 2025 18:13:18 GMT  
		Size: 380.9 KB (380895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd9feeff97d2f64327b0d31ba1df3339524e1d1d46db000aa58c63d0092edc4`  
		Last Modified: Wed, 08 Jan 2025 18:13:18 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:53426060cd1b6e61bc01c7bbb0ac95d823d3db273638fc1986d6857092beff4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147287079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee9926e9fc31c9252a362d21cea96ca5b35b69432c6a6e9c3ff0bd599726c67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Last Modified: Tue, 07 Jan 2025 03:03:15 GMT  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6772fa1cc9bfa9729d45025ef93edf9404d8b45c5896ae466905dbfbcb455ba2`  
		Last Modified: Tue, 07 Jan 2025 07:23:42 GMT  
		Size: 143.9 MB (143935131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5f2de1ac6eb255b906174f59453646087280499654b1774e25a0c093adfce7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab9270cf06fb935283bad5c705693aafc285464a882d6cd8aa13bd342f6945f`

```dockerfile
```

-	Layers:
	-	`sha256:d5efb39943155ca4e789d57eab654d32065d028de72ceff6aec25555ef33f085`  
		Last Modified: Tue, 07 Jan 2025 07:23:38 GMT  
		Size: 380.3 KB (380314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd143d9a51250020c0ec3de5b54b66f7be84f23ba3fee1221930a6b92b0f7917`  
		Last Modified: Tue, 07 Jan 2025 07:23:37 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json
