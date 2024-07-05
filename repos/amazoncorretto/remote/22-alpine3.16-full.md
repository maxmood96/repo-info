## `amazoncorretto:22-alpine3.16-full`

```console
$ docker pull amazoncorretto@sha256:62b4c0736361e1feba150df3c059424f084c109ac6493e248821b2d209f8a95c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.16-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0ade0586fe5ddea456ac69d105045cfe6a88a3685b1db26ef7033e8e3f7d7ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160891337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a1473c99a7b1558bd4ee14c7729def55a95118376667cfad02a4a29c978b97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=22.0.1.8.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d1ac8060f9a34acb77b8adf279ef04d17091132bac651c8fe46dcc807496a9`  
		Last Modified: Fri, 05 Jul 2024 19:56:35 GMT  
		Size: 158.1 MB (158083500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.16-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5f937873c86c34b2e550605cad3d511d6879e658f35fdb4b70351a63129ecb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.7 KB (383704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e4bf9cd299a38c27bfe3e9d2c33fb0a5fdc6594bdf1f46b3f17f2e8a3cc45`

```dockerfile
```

-	Layers:
	-	`sha256:c61e8d135de6ebbcd4db730d12e0f8bb7cb9a57d452acb0e4fb71a1a00eaf1bf`  
		Last Modified: Fri, 05 Jul 2024 19:56:33 GMT  
		Size: 374.5 KB (374535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5929041142f3760b15276f60dcedf622648211b3314b40bdac0a7e866379f4`  
		Last Modified: Fri, 05 Jul 2024 19:56:33 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.16-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:43eb03d62aeaa4c076ce21c11209189c9c9253f5ad9e45ac7ee5d98518fd089e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158142296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae5a12daf91dce01853a1a62999f07483fab56088f321bcbeea2647cd2bb7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=22.0.1.8.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f691990d1f63c151a438f4cb5c0ea7049e8d3b54e0f666cc5f5a06979c929fb`  
		Last Modified: Fri, 05 Jul 2024 20:30:27 GMT  
		Size: 155.4 MB (155434013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.16-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e62bc59b1e2885f3df94b292a5a22a9b2259fb91a0e44fe08a0892a9a84fd28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 KB (382781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e67d01644455439f0a5c1e2aaf210df97767b95ac8bfd05af21b76d6d7818b`

```dockerfile
```

-	Layers:
	-	`sha256:834ee5407fc067e928ef649ec17112415f6c9ac052add1363cd06b1931232fd9`  
		Last Modified: Fri, 05 Jul 2024 20:30:24 GMT  
		Size: 373.3 KB (373312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab56f8d6512a8da86ac7dad6517a46e2cdbde33623d9cfea0a6b999d9a629ad5`  
		Last Modified: Fri, 05 Jul 2024 20:30:24 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
