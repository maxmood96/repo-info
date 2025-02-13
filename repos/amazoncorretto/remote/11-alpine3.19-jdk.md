## `amazoncorretto:11-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:75e395850ffba8943170793d43f4a9d37fe5d912d84b2b6482b70938e6c6ed43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:39026718dc7a177a5b98aa4ec08f33ce2cbc4623ad7f0ec71e41b9d15b8bd9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145331051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646b7c91f54133c42dd403cbe48f1ea99ab11854712ee61385af66186eef1e25`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cdf64e434667ca4b8ab00619aaec3ea7972be2838e100ec7e094bfa77311d7`  
		Last Modified: Tue, 04 Feb 2025 09:13:08 GMT  
		Size: 141.9 MB (141910809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e3675cd8f06263d148d3205c3dfed1ec984905b2a11d3ebc91ccc19709fea18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 KB (397110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be780465b94da688d7abf0fd02ad5855ffb62d1c09055abc51087341f62e27b`

```dockerfile
```

-	Layers:
	-	`sha256:14899c4b8bff09eb9b9c42b29f39854d8cd22d43a0f838c89de89b95dcc83126`  
		Last Modified: Thu, 13 Feb 2025 10:18:34 GMT  
		Size: 387.7 KB (387693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e38bbe18b1a20cf7007e5dd851913aab050e537acbd19d830291dca8b9a646`  
		Last Modified: Thu, 13 Feb 2025 10:18:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:558caade6a6bc14ab38adf0796284eca9799441dc944561de03437379ce32946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143395417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd774f6d608362a6349179c9614c210d450d73095ffaefd914b7a765e48f23f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cebaa16c89f6b249f96b1bbbb360c4eb148bcc597be19109eb7ea74b6fc4741`  
		Last Modified: Tue, 04 Feb 2025 11:46:34 GMT  
		Size: 140.0 MB (140034885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:52c57b1dba49d2d3254fae2b629d8023c43f9d2099ee27ff25f7bb4fbd64b12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 KB (397268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c07609f9a5d8750c89593641952432414da852cf1a4edd80ef1316af4292f2b`

```dockerfile
```

-	Layers:
	-	`sha256:d5ea8a624c986005c96479cf33829e05362d2248a03a802a2e3dcd68a8fae997`  
		Last Modified: Thu, 13 Feb 2025 10:18:34 GMT  
		Size: 387.7 KB (387749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f878ba04dba5eb132f133e3245a50e19418efbfe2fa56e3a7c839439e16583`  
		Last Modified: Thu, 13 Feb 2025 10:18:31 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
