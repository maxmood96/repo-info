## `amazoncorretto:23-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:7dbb2b2db947f986df872b5b0ecd3eac6a8d7aacd3464ae8b25211fed3874862
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:18f6c94d5300f36939bb6a3bf49b2105c5bff06fa1471ee8f716f6c946235675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170050961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716db8a9b2aa85f8da63a6060ebf9b90d29db66f591c747863b7a78352e63486`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c654a578bfae04c65120099d3b6cc8966ba267adb0f1966780501a8fc8d74331`  
		Last Modified: Wed, 16 Oct 2024 17:57:22 GMT  
		Size: 166.7 MB (166658767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f2f270fa2c1daa75b975ac477b27cf50b098a74bb6a5aaf9a670c298e40b0d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.2 KB (391221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28aed80b5d441601ed1d255a02fd9c59b5dacd193132acea7310394fd553786`

```dockerfile
```

-	Layers:
	-	`sha256:73e2a37242fc59119d528fe7339b619f36853ea0738c77f9f78d77a5f9b581e4`  
		Last Modified: Wed, 16 Oct 2024 17:57:20 GMT  
		Size: 382.0 KB (382014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7757953f054158ee17be3bf1f34c64ad324babb0fac54e09638e9148d90eaf1a`  
		Last Modified: Wed, 16 Oct 2024 17:57:20 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ccd69948f3b119fd9e93f711514421106810f3c1997b3d8683573f2c801843f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167628145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212c471a3a2222f55e17d3c32fe7127f9c2fbbedc04a561add3f22b96a1107e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f456ac30f635639d28d783e4498cb1d4aee5ec7b6210060d0c5e41a7fb767d0`  
		Last Modified: Wed, 16 Oct 2024 18:43:58 GMT  
		Size: 164.4 MB (164353073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d27c29fc6eb64c98d5dc0b931d48498687cded1a968c348d762e35b1e28ab297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.1 KB (390096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f845883d1bc99f0fef94868dddbb8258a75f8951629963aae25b71ba8b64d6cb`

```dockerfile
```

-	Layers:
	-	`sha256:7ebe267fac995366f255edde4cee8ce3075018a4177ea9a54a868207ffb39c53`  
		Last Modified: Wed, 16 Oct 2024 18:43:55 GMT  
		Size: 380.8 KB (380791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6353a8b55231f8219b234586c5a68128921a32d1fca4a451559621219efaa7a2`  
		Last Modified: Wed, 16 Oct 2024 18:43:54 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json
