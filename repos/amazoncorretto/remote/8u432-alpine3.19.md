## `amazoncorretto:8u432-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:ec60854d414356d3f6df9ae2f42ac6dca3ebf87088104ad1bbe72f0ca5e508eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:921af362e9d146b02bc450a1b88627880b537cbbcc63ab81b347a102d1bbade8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103616817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d1f05e71e2df00031336754cb2a952edf0208f2cc56af7b201b79e76d1e816`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c0af22de4609982503d27cd16889a26c2e6c71d45fdbe8e77b956ed5c3b8f9`  
		Last Modified: Wed, 16 Oct 2024 17:56:11 GMT  
		Size: 100.2 MB (100197111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:01e21d01996c4f6ec2d216ab7393470689dfaee785cf8a2939e0baa9a7363890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 KB (254983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7220787893e6bf5e6239996b774f7bf27a6fa2780e51ac1f727caec18b0ba22`

```dockerfile
```

-	Layers:
	-	`sha256:2e9468b74ca32e95253e9eae109d3dcd4c13f44f170ebcd84f98695f7dcb72b1`  
		Last Modified: Wed, 16 Oct 2024 17:56:09 GMT  
		Size: 245.8 KB (245792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b896f526c612fd417646e11d4844ec0e418e84fc45f967809ead7e4d1e7d7b`  
		Last Modified: Wed, 16 Oct 2024 17:56:08 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bdab83426a1f43dcdd133b3da29ceb7c7c3db2c4b0501f9000c785c8f660f75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103338088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733cbed5308751eaabbb7a153e65567bda7ba74c7302afa92b86f40c18fc65fd`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3522236ec70b3044238d56d02ab22ea1f719f75fd641dde2ed0c2b895fe8c08a`  
		Last Modified: Wed, 16 Oct 2024 18:09:16 GMT  
		Size: 100.0 MB (99978985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2328f586ef0c0d107236cb70ed9283051cbcd18b1367e7126e38fe200be3c935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 KB (255212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d70d85535f9287934d71196f9607d31b927049e53ee4ba3e3383fe9aedd5fb4`

```dockerfile
```

-	Layers:
	-	`sha256:b7bf72ec388ddf4d3399d8ffe05631b45453aaebba8cf84ab7464a0dcb16442b`  
		Last Modified: Wed, 16 Oct 2024 18:09:13 GMT  
		Size: 245.9 KB (245924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2481605f45d42f65d87ff7e3bf9aeeb3140e1faa15b457772b1d446f7e113679`  
		Last Modified: Wed, 16 Oct 2024 18:09:13 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json
