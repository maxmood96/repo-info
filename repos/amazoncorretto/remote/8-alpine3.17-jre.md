## `amazoncorretto:8-alpine3.17-jre`

```console
$ docker pull amazoncorretto@sha256:3062e21f58670134f1c76a1839756d6207b5472e55ddeec2b14d11da1046a9f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.17-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:729665f8e26af60540e8f84b7f4e8f7199568c0a1681113720f6f2c01b71e137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44991614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726f7705e4c8a8255c102f2b84f2a35f081699c198ae7770ba2a2be89b86c37b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
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
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ba0a91d42dd541325483d36a0605ecfcaffb51a2b0a5eb84e1a295de0c7453`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 41.6 MB (41599420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:033aa8cb4f449eee42ad159e5cea71c3be4c8063f7b9aa29baf757df31807b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13a4a42b73f59028522609b37e16a69bda179471fc313339e9dd633d6180d0d`

```dockerfile
```

-	Layers:
	-	`sha256:0a9b2c9856b5ea22da2da46c4704166839af37d85de2d0578188e90cc322e503`  
		Last Modified: Fri, 06 Sep 2024 23:25:19 GMT  
		Size: 184.1 KB (184124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbd4f56ec957737ff1f6f5c50cf55eca85a0662dd7508db72459fcd85d13c1e`  
		Last Modified: Fri, 06 Sep 2024 23:25:19 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.17-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b07b39f63ef57aa189b88ca614e50832c976dcd69a7ab9bbae792b422edd481b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44581264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf25ae574cf55c2b538c73b31ae40a20584ec94c40c6e73080a345c4e41ce9a7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
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
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157b1dcdbcd5a0ec6b58277d86899f732b040c41fbfb93ade974f2158631900a`  
		Last Modified: Sat, 07 Sep 2024 12:05:30 GMT  
		Size: 41.3 MB (41306192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0cf20f37d9553c85c99ddff4b572cc6d97a2aaa45edeb5791e0da555d579fb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6371b0c5ab935b520fe874d48d44246e841344419402cfa6e14684af42813826`

```dockerfile
```

-	Layers:
	-	`sha256:d9569639be26e6931163725e24ed71877b14032e02c6ee4423ad3e4d2d25cde4`  
		Last Modified: Sat, 07 Sep 2024 12:05:29 GMT  
		Size: 184.2 KB (184232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0229b92dee3d05474139ec11ab27c93d3e20b18468e7bb6e40cd8343c8904723`  
		Last Modified: Sat, 07 Sep 2024 12:05:29 GMT  
		Size: 8.7 KB (8730 bytes)  
		MIME: application/vnd.in-toto+json
