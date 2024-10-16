## `amazoncorretto:8-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:29340508cc6c7834b1be2b055888bdaa293ca49b54be822fa9e7941ce270ac57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dff9a3865a39cee04841a0548d2e8ad4b7802b4f8a854af9c907488d00f694c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45075281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0373066107df909ab63b7f5901d1415d99b4f08288137461c709bc24304390`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d42d90f9fa61a3cfa7c54ce96ee62958312fcc8943c3d932721eadae8613b7`  
		Last Modified: Wed, 16 Oct 2024 17:55:52 GMT  
		Size: 41.7 MB (41655575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ae883058de9bf0a8044d660df617edcf1ffafdb6269d6ae5856bfd5903bb5030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 KB (193922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c4ecd944fe7ab815856bea32bae8088d0b60294454e966fccf76735851c2b9`

```dockerfile
```

-	Layers:
	-	`sha256:d03cff3451466742ed7d3de974f6a4841216a5350dd93b0e78af2d126635fdb9`  
		Last Modified: Wed, 16 Oct 2024 17:55:52 GMT  
		Size: 185.4 KB (185431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e969b9f061cb826c3757eb6e602702d352fd839ac270ef87d3b8b7f8310408e`  
		Last Modified: Wed, 16 Oct 2024 17:55:52 GMT  
		Size: 8.5 KB (8491 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:92662fc37aef29d8150d90826f1c749ebca1f5391705699589241c2a6e7b5743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44717691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b711818890ae95216e795b600ab7ed9f9f242dd18984f5c8cda167fe9676c7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1ae5ae3f094e2cd0ea7cca6150d7d6b6198640c5cd363883a95c813064c610`  
		Last Modified: Wed, 16 Oct 2024 18:09:52 GMT  
		Size: 41.4 MB (41358588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0e0e3edccf4383d14610212cdac685ec423a49d76e1caaaa563ad24555b64c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f6553cb7118f365f48d107a3107f70e8e135c88747fc15e497bcd9505dd973`

```dockerfile
```

-	Layers:
	-	`sha256:3f62b12e837fc5aa4ba23632f73ad7c33ae2d78dbb481c1cca1f8cbf5148a388`  
		Last Modified: Wed, 16 Oct 2024 18:09:50 GMT  
		Size: 185.5 KB (185539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2bcbbc1316d66abc4d6f9e780e0ac6362ea9f5c8f0e660d0498ef3e23c5968`  
		Last Modified: Wed, 16 Oct 2024 18:09:50 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.in-toto+json
