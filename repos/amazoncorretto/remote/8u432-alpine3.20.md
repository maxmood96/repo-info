## `amazoncorretto:8u432-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:12ef3a0b812a25784fe7023991f6edfb22141cd5b4e748b8176d2eddf0516070
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7674ad8c57abbd6c0b43671e40d65a36ba5123fad34712d7562357afaeebc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103818920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95791fb5eb1a91da52217389247734d27eae7647d18c4bb05ed90e77b500b51b`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa2da6d42addfbfca7b5ca6219c65aca738f0b236ec060993dbbc72bbc3bbac`  
		Last Modified: Wed, 16 Oct 2024 17:55:59 GMT  
		Size: 100.2 MB (100195113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b45c736b0da1d7407f5230ce0da40170d9e44c46ad2bbfe53f07474aea697984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 KB (253344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3a886819f524fcaa57ad50f9fa924f3dac78670ea223f4af5d605597aab6b2`

```dockerfile
```

-	Layers:
	-	`sha256:7a2b6e03dc5053c8c8d3e5ed1b1557d9ac5bc9e95eaac12e0971fbef15e51908`  
		Last Modified: Wed, 16 Oct 2024 17:55:57 GMT  
		Size: 242.9 KB (242855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ab1613a436fd66422c0f9c77cc84471093a49c535ed4f1a11bd8735a20220e`  
		Last Modified: Wed, 16 Oct 2024 17:55:57 GMT  
		Size: 10.5 KB (10489 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ae47de60f5f77a8c44984673982907c11442de96426c9b2e7f28c47304454317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104066346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d50ae7c74ee931edba2cdb7226c8f63dda7f4ff0f7189e909a066a2dfb928f`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7a182f095259666dd2097cf8d13bf59e3b52a322ef6a9395ec022201ee5a8f`  
		Last Modified: Wed, 16 Oct 2024 18:10:28 GMT  
		Size: 100.0 MB (99978700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:92ad1291b17ccc8cc352cc5c7aa47b59b94dd769bb54f8d5a403b0071a396a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 KB (253668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589dfa36e42b135f0579d0d9489f56eb029484db46240c5611937aac46361a34`

```dockerfile
```

-	Layers:
	-	`sha256:0116d1ae47ffb659fb39c9df86ff9a37574d5bfe3b6815e489f2876b3f72bd8a`  
		Last Modified: Wed, 16 Oct 2024 18:10:23 GMT  
		Size: 243.0 KB (243035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330e53be7da652f9ac8c1273c61a3e85536560b8c59b1446fef70859e3410d2b`  
		Last Modified: Wed, 16 Oct 2024 18:10:22 GMT  
		Size: 10.6 KB (10633 bytes)  
		MIME: application/vnd.in-toto+json
