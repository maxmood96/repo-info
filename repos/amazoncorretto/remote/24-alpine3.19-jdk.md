## `amazoncorretto:24-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:e908428bdef9206b474fa08c55fbd08d359bc5dcf934602c443bd957597d6e71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d72e9cda54ed89023eca330b4399ca39fc423e47baff2caf3f0983913fbf59d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180190342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8139e0aa4447a226fa36b0533b0d0f0363b90d2273004a239d89e6472bf02287`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19f65e5e1fc1b2806fb851e8d4072cb4a7c3a8906b00770a1d675e506676e72`  
		Last Modified: Wed, 08 Oct 2025 23:00:35 GMT  
		Size: 176.8 MB (176770527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:accc86619ec30794eeee69da3a44ed1a39911140ea9ccf240b5df36ed3200fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 KB (400891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa592c26af9dee1c374587e215b634a74520699184c53063eea50ac24699d09`

```dockerfile
```

-	Layers:
	-	`sha256:60eece625c4ba40ed229bcca530ae9bebe2895d1a2221b8613dd7e60b7d83ddd`  
		Last Modified: Thu, 09 Oct 2025 00:50:53 GMT  
		Size: 391.5 KB (391477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792b8ec63781d2fe23564af9ec16e6ca92cb66f10e3d4d18c8476666d79e177f`  
		Last Modified: Thu, 09 Oct 2025 00:50:54 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8abb7d137dafe9f54b573ce7efb9412213b786fc4e346df911b26c52f51df872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177876598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c9004b7da42ad41d377e11bbe17ead94bad9f2c11ef8e5e1b4d1a3cc4900b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
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
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ab74e96c65f8387dce6d419f052b28aa549e2415e6eda533975a9b3e41c964`  
		Last Modified: Wed, 08 Oct 2025 21:47:50 GMT  
		Size: 174.5 MB (174517297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:64f22d0ca4a63d5122b38db1838544e3c5547feac7923ace59e0637a5a968a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 KB (400412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e72896b56a020f0a3f9747d78a95d7d611b39f0906e6f2164771bcdebfbc6a`

```dockerfile
```

-	Layers:
	-	`sha256:c67415de96205f938cad26d4139240860d665228d9a9dfd090dd3ea53c5dd634`  
		Last Modified: Thu, 09 Oct 2025 00:50:57 GMT  
		Size: 390.9 KB (390893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6807a36cead648503a2fb0a687563170ab38d84443fb68dd4e70281de14a7af8`  
		Last Modified: Thu, 09 Oct 2025 00:50:57 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
