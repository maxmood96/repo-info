## `amazoncorretto:17-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:e9b0dc4bb5a39fe68976dc3e70419d9788e0213c70902eb099f444b30bf37402
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:50307bf3f89cb3fad176f87ee077d3f3b8de189cae6f722ded1628ec6429fbe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149410269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3fc0a37b1c68b66bc18a9020d83a40d1cb242aa12a3729f512212415628b38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3444c516dc5f23fd7c8afac94b24d4131fe5686c4ed8ff39d4735d58a937bf3`  
		Last Modified: Fri, 06 Sep 2024 23:17:28 GMT  
		Size: 146.0 MB (146018075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ade46c7395c23c034a89a8d94b039bcd0dd22404e2fe4d9aeaea5d6d925133e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 KB (388671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6541bc8f75c9aba0a5b0f7657e6984ce7d9f11ed58ed6b04ed67d223557fe6`

```dockerfile
```

-	Layers:
	-	`sha256:e3e083228144943b31673aa2d6c92c5a8a6ada6d1d485db99a7f8c18640cd9ab`  
		Last Modified: Fri, 06 Sep 2024 23:17:26 GMT  
		Size: 379.5 KB (379501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f5901823f30fce11de92aa0c8c9f2834c53f0f5e2f285a346984e199048dcdf`  
		Last Modified: Fri, 06 Sep 2024 23:17:26 GMT  
		Size: 9.2 KB (9170 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e3841a96f2b9d275b54ca1484ad3efc103bb3c3682e438d512d3044391cb4206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147626019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6730aa7e327f5ea1e01bb49ef1c0817617c214047b6b90ae7013a91e28a7036`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0768d8b4e23905d1bbe4ed77f4f75decd6d29c2e98603ca1e86fe9dc7bf470`  
		Last Modified: Sat, 07 Sep 2024 12:11:10 GMT  
		Size: 144.4 MB (144350947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e6e4956dc5b59e904fdf9aa7e649e54fbdf9784f8b819c559263ff83f6498082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 KB (388391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3126fdb0c31466b9bf40c17b0ecf1a74ea4462a85d49bf895749bfa89f844d`

```dockerfile
```

-	Layers:
	-	`sha256:0ab3f40eba374f76a86baddde27d85ed6d70c565e0db71275425afccef893580`  
		Last Modified: Sat, 07 Sep 2024 12:11:07 GMT  
		Size: 378.9 KB (378919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7788f22c88e60e264bc4c1f82f8be000c61469424e10ea0510e093a4f2555094`  
		Last Modified: Sat, 07 Sep 2024 12:11:07 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
