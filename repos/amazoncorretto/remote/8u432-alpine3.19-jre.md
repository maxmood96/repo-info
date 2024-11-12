## `amazoncorretto:8u432-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:4e4cd6a1bf1fd67ff3a5796b72e102bf308555f7fded74a11cc7425240fb910b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b6e9ac81619923c9b7b35f88242000602100e2d848034605c1c579a013e93f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45075307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c825d811ebcdd2767d67bc38a4a8925372dec44e81b64f8da7defa4006c63d8b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ffde209903aa47af7b754a9688c3760652ed5b664aabec34b38f102966f0cd`  
		Last Modified: Tue, 12 Nov 2024 03:13:49 GMT  
		Size: 41.7 MB (41655579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:09c4535f4109247ea5d4cbf6d2615556ccd79671980a4e93f343ab08c67a3e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c895c8c3f5683ec8323123adeea6eda6a8c51387e15daa30439fabe2d74076`

```dockerfile
```

-	Layers:
	-	`sha256:09df221a86ae8aa588236a3c914df0126171819b2e1dd73da1285a322ab62342`  
		Last Modified: Tue, 12 Nov 2024 03:13:48 GMT  
		Size: 185.5 KB (185524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971b81346f52767c86217dbb39f724075bb44546cb1922dd0574d2c65d641dbf`  
		Last Modified: Tue, 12 Nov 2024 03:13:48 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine3.19-jre` - linux; arm64 variant v8

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

### `amazoncorretto:8u432-alpine3.19-jre` - unknown; unknown

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
