## `maven:3-amazoncorretto-17-alpine`

```console
$ docker pull maven@sha256:6e6a5e1ac18aa664f2d648bc9c1fd6f76eaddaaeb1d0036992af57601ca0ef19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:5cc598d68b7495d4ba18c750223382c619cf9e9162c45bbd6a4d514cf8351a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164228748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40be9eaca6deabc74a9d7d223133dd9cbc3b26d25838f95f925fd3a3c6a66bc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:25 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:25 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:25 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 18 May 2026 22:39:11 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Mon, 18 May 2026 22:39:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:39:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:39:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:39:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:39:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:39:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:39:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:39:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:39:12 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:39:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:39:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:39:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70996f4731d80bb777dc007c01bbb313c2d7205086bed0275a9259be9c42ec88`  
		Last Modified: Wed, 22 Apr 2026 21:34:41 GMT  
		Size: 148.6 MB (148583454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f04e855bfdad75039b603a33166ab5e1e48ef975dce3d5080305ccaca35fb2`  
		Last Modified: Mon, 18 May 2026 22:39:20 GMT  
		Size: 2.4 MB (2420131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9570da1b0d9029b3ed561917d0c1fda1d5906408ab704f6c2b9028636f018a23`  
		Last Modified: Mon, 18 May 2026 22:39:20 GMT  
		Size: 9.4 MB (9359968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5533911c61592ece69c1083e15bf38c344ff378a1f106edc8d4abee8c34f883d`  
		Last Modified: Mon, 18 May 2026 22:39:20 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3a2ce0060d57794cc23df6a26623b7f0dc31674d5a8b590d05a81cb1c10ca7`  
		Last Modified: Mon, 18 May 2026 22:39:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:45b4043aa35999f7f011b8dfd7a5458a699f6d467efb7ff9b80fcb7f6e95888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bf2eb0fafdb644844a9412944a45587267596c473c3c39b228ce0d83264656`

```dockerfile
```

-	Layers:
	-	`sha256:f9c021d06268d4dffe3616d40e67ee3e6175598e109f734e22719a7fda1fc7b5`  
		Last Modified: Mon, 18 May 2026 22:39:20 GMT  
		Size: 728.4 KB (728389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446df4550599e8d37daebb544c6d9191a175faf479412ab7fa1d7ecfc0c54550`  
		Last Modified: Mon, 18 May 2026 22:39:20 GMT  
		Size: 14.5 KB (14525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5eea5c703d4f3bf4178f3203005e03ddb4d87522dd6a9bb639ce7e416f4e8764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162959661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d750651e5067e445195a4f7e7a59480e35cff16d38231403d95ffc8f52a845`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:22 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:22 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 18 May 2026 22:40:56 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Mon, 18 May 2026 22:40:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:40:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:40:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:40:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:40:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:40:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:40:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:40:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:40:56 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:40:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:40:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:40:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0529315e3631a56927dc9186f923e06f688e00895e152f54e0716f3971048783`  
		Last Modified: Wed, 22 Apr 2026 21:34:43 GMT  
		Size: 146.9 MB (146937643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c801c77c9dcdef31c4ac37ea6fd395a4407a2b2058732ca954347166670e33e3`  
		Last Modified: Mon, 18 May 2026 22:41:04 GMT  
		Size: 2.5 MB (2461164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4265595b8a6d5170791d4e80f4d6c3e2fb8178f3ca0ec9965654e7dcda3a909c`  
		Last Modified: Mon, 18 May 2026 22:41:04 GMT  
		Size: 9.4 MB (9359975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774a50ca42a7e541c9557ba21635d115a7a9046cb176828cf5c57418344cc2b1`  
		Last Modified: Mon, 18 May 2026 22:41:04 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98cc7fa7345309904e1ae5bc2dfbabe4efb4d1b51fb2d6e42817e58f833824c`  
		Last Modified: Mon, 18 May 2026 22:41:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:cfd8951d98d54a5e10970aa5c804fe3f813d58092b07837ee3570e8b424d1610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.8 KB (741804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77d28a1d231b7e24eca84c8f6e60cd46449b106a07bfb021726b2e4dcd41728`

```dockerfile
```

-	Layers:
	-	`sha256:e520a8160f0f649998ecba381c47dccdebd3899be590cabd0368b7ad6f102558`  
		Last Modified: Mon, 18 May 2026 22:41:04 GMT  
		Size: 727.1 KB (727146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d043d5687b4b70756aadff7ce3b5ab9b759c3d5106f7b0a21224f31902d1a9`  
		Last Modified: Mon, 18 May 2026 22:41:03 GMT  
		Size: 14.7 KB (14658 bytes)  
		MIME: application/vnd.in-toto+json
