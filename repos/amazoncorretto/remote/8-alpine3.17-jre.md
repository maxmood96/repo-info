## `amazoncorretto:8-alpine3.17-jre`

```console
$ docker pull amazoncorretto@sha256:4526fcf71d2193821f083b66a7f5a5712e52eb94a7d7ee1e4925a7b7e93057e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.17-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ce9221d2c58509e0ff00556742b223c74ceee4a7189b3ca1bb9e510f2e7a9139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45047760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cca21d10bc4965d99c9141bd4597c3a8d01252e90bb1e30f1e68c819a8b3108`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
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
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e9a95dc2ce9ae97aeb9eb97664d161538614414e3023cf671bf3b735b1a1f0`  
		Last Modified: Wed, 16 Oct 2024 17:55:52 GMT  
		Size: 41.7 MB (41655566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b1bb21c8a0241fa569856efe29e97753ba72f3c61e6a0e6997cc79a077df4289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 KB (192661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6d8faaed22b1d0622f22e3b2aeb8494dc9749c0e2dcf49c1328cc342f83df5`

```dockerfile
```

-	Layers:
	-	`sha256:db065164531f67ce2c26c267d8557dea50069ae1b0dc42bc16536ad368525459`  
		Last Modified: Wed, 16 Oct 2024 17:55:51 GMT  
		Size: 184.2 KB (184169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67f5a38b3885f5a2d1d718a89dbbdec1f05808f7953c3f6a998d4bde90f4d3d6`  
		Last Modified: Wed, 16 Oct 2024 17:55:51 GMT  
		Size: 8.5 KB (8492 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.17-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9367cad8016073196443dca6c55e8ecbcd3f6572a5e4cf521819ecfd80132d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44633698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72a5c0ee802d22b8fe8a51aee133096e46f6b27ea1b19f19d3a4c6a8f60be66`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
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
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6d3421120f41e2f520aa9b2c40bb295c29f9165dc829bd35c69cc44a5547a5`  
		Last Modified: Wed, 16 Oct 2024 20:29:24 GMT  
		Size: 41.4 MB (41358626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3818620c9c272bf51258046f79fde1a3064f5156ce98977cfe162978eaf480df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c67292d1b0ae1df42c143eb804f590e17b629a996494ffd12cc27e51149e02`

```dockerfile
```

-	Layers:
	-	`sha256:298dba43bee6ff78f8af69c04a6a20554293a9368a52e4a60ab3ed273619ac6e`  
		Last Modified: Wed, 16 Oct 2024 20:29:22 GMT  
		Size: 184.3 KB (184277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2157c125335d3d14b8e7a0b9669454db4f0d7cf92b240dd0979716e9df73925`  
		Last Modified: Wed, 16 Oct 2024 20:29:22 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.in-toto+json
