## `amazoncorretto:11-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:9bd351a8e575536a94719701e926875ba3819109b57ca914fd92f464089ebc99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:75223404fd4a758f8879e771f76f3159b67ec2dca423378065e5f246377e24b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145329853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7327132cfc9d6d3eaee4833ef4a1d3dd3ce27c5969436824edf967e18e7e8dc8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5138a4e6ca98aa7a3b9cf84f7723bc17c44d9069c5894e7a7f2b94ba6189420`  
		Size: 141.9 MB (141910125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7653dcc87b6ad35b247344ad7b2b2e7032a428bca23e27a1002a031dba7087dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.7 KB (397747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d7072d1356b959f3602c0a44e66952749bab451426a130ea193cdbef51534c`

```dockerfile
```

-	Layers:
	-	`sha256:f40894f5a09eae603e06d21ee76eaa7ed234e6b0b95bd86bd530c619a91cefa4`  
		Size: 388.3 KB (388330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78caa7db7c9e1599a8332b6ed291ecd4742e54c89e36b651e488f91bf668f58a`  
		Last Modified: Tue, 12 Nov 2024 02:12:15 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:98886f91e201472356084910aa883868b84ec0a8f4be63613134ade25b60b22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143390457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9bbcb8b355ab4ade3b4b4eac65315cf200ba5e2e678e1b3436cad1e7553743`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da3eda2dd8abdaef10b65d8a6edd96bffb48dd5d1f5532205bf1a801c742f57`  
		Last Modified: Tue, 12 Nov 2024 11:07:38 GMT  
		Size: 140.0 MB (140031211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61644ff456a40f78bd7786733656ad3cbda607071ad99189bafacd7b59cc83ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.9 KB (397907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e117cb784d19041a0cc1c31166a5790fbe7d4d41f305e8cd963c72c9fc422052`

```dockerfile
```

-	Layers:
	-	`sha256:fd2ac91041256620677726cd526fad17ef1a32722fab8cbd89420a19ed20e90d`  
		Last Modified: Tue, 12 Nov 2024 11:07:35 GMT  
		Size: 388.4 KB (388386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43e284ecb72d0d8aa2958a68487adffdf36a67874d886d7a4ae8a11b7474021`  
		Last Modified: Tue, 12 Nov 2024 11:07:34 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
