## `amazoncorretto:24-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:4ba8ea3e090ae8aff557e5997b744c6c88df299f00756f3ba790537ff212071c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2e69d0a4d2311db719ba1784a23635032f1f7121709dc1005014aea7ce8363ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180574043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040a4c173250f06d976bf80a7bbbd71f41a294baf251b40bea267f283a127539`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63602b751a24310624bf9cad31459544814f09f70ae0eb51daafb075b4c9e47`  
		Last Modified: Wed, 08 Oct 2025 23:50:55 GMT  
		Size: 176.8 MB (176771591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d6c6bd401cfb65c02367c07b90878b9588f3d04327281c04239962b13c5d0409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 KB (401576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ec552ef6527ea04c78aa9b72cefa43f7ddd5b1aa8cb1b7d6f973bffcce269c`

```dockerfile
```

-	Layers:
	-	`sha256:4207a4c58dbf668a89f14b675a85e000f1ecad7d5470b81d21de755a6399e84d`  
		Last Modified: Thu, 09 Oct 2025 00:50:42 GMT  
		Size: 390.9 KB (390856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7f52fd5f4bb6a0d3ac04f13cf586193ab1aa754cd976f5c941b3d861a6c0c7`  
		Last Modified: Thu, 09 Oct 2025 00:50:43 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c43e94d785a468e896176fa8318c752254753a7dbf046ef563238e7ea8389fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178656558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c5d76ad57089ce278beb376ecf1932ce01f664a860e18fe5900ed0996caafa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26aab9f285413a75ef5ecfd6345b20510af722c181c6851e8b1ddbfa4a43a303`  
		Last Modified: Wed, 08 Oct 2025 23:18:04 GMT  
		Size: 174.5 MB (174518489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e46d5c9dab5398b03a19b07cdf7e3b08089bf5f104138610cd643d49f24cc0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 KB (401193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac8adf4802cb7063a65f3788cdb1bd300807c43291d25f85a39cf9b02593bf8`

```dockerfile
```

-	Layers:
	-	`sha256:17837db7b1b2c7b2d96a2d76796b15f1e935ba54cd4c36a40cc9861088661329`  
		Last Modified: Thu, 09 Oct 2025 00:50:46 GMT  
		Size: 390.3 KB (390320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5214755650c22baa63fff9ab9aa7c29eda85130f8262be906f6ecca6714b5e`  
		Last Modified: Thu, 09 Oct 2025 00:50:47 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.in-toto+json
