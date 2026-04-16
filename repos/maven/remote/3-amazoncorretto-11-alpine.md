## `maven:3-amazoncorretto-11-alpine`

```console
$ docker pull maven@sha256:49fd64bbfcbc196844a31b79a41fd3a1ed444c2dbde550874e56fd04d8b88157
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:81ad31c83fd32b29252d3c7c9a5b822cadb93fb207a9f9bbcfab882f6d6040fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159182656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bacd12d78fc06a7d777da7f6dfaf484e4b9b9ef41197b0ae9f8a66c36901b5e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:28 GMT
ARG version=11.0.30.7.1
# Wed, 15 Apr 2026 20:24:28 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:24:28 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:24:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:24:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 22:50:01 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 15 Apr 2026 22:50:01 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:50:01 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:50:01 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:50:01 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:50:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:50:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:50:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:50:01 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:50:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:50:02 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:50:02 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:50:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:50:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:50:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fbc81a1c67951c4d530fbb1312c89d9c8fdd1fdab502c0ffd7f5b9683e7a7a`  
		Last Modified: Wed, 15 Apr 2026 20:24:46 GMT  
		Size: 143.6 MB (143585979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a541cc7c2454dc614c40b6aca0f42b7b48f8308661fab61f801ac1d10773c822`  
		Last Modified: Wed, 15 Apr 2026 22:50:09 GMT  
		Size: 2.4 MB (2420258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165b09b072d8eb8df9c4adb5f967c0b5522c9a39cc187dc9f2494b1ebf8c25f7`  
		Last Modified: Wed, 15 Apr 2026 22:50:10 GMT  
		Size: 9.3 MB (9311194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdd038e8290e500fa901075bf832095aef1c73fb228a58a1de572ea0cdf049e`  
		Last Modified: Wed, 15 Apr 2026 22:50:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f0c51a9b795ca9c156083923f86f6a76ab90242c08ee58ebc177364f59efed`  
		Last Modified: Wed, 15 Apr 2026 22:50:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:49dd9e2ee7941743739dbd29f6f3766ccaa4bab534980b76ae39b68ab346d9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.9 KB (749894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a369a1cc0c59c0ce8127702233e305d4116654dc6faa180510750fd68de06ddd`

```dockerfile
```

-	Layers:
	-	`sha256:31a0d75682391b208947f5316da2f11e4e8401e4e0be50d9d18f10e206c6636a`  
		Last Modified: Wed, 15 Apr 2026 22:50:09 GMT  
		Size: 733.5 KB (733532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5aa29883342b0206af1f40b5aa701045eee4262ed525dd53c5b48f9f60735af`  
		Last Modified: Wed, 15 Apr 2026 22:50:09 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:44cdbb17c297661d79cb65ac614198748b8f86885150c1f3870ce5a8ed20dcf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157829232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd48314e795b141a3274bed29fad1383baf1c1b76affd9ccfb57437cf9beba1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:32 GMT
ARG version=11.0.30.7.1
# Wed, 15 Apr 2026 20:23:32 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:32 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 23:16:35 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 15 Apr 2026 23:16:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 23:16:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:16:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:16:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 23:16:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 23:16:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 23:16:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:16:36 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 23:16:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 23:16:36 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 23:16:36 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 23:16:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 23:16:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 23:16:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7f15f0553c050361ce115b544e04a69d299081b3ecd16fc7763b671f57d2a9`  
		Last Modified: Wed, 15 Apr 2026 20:23:49 GMT  
		Size: 141.9 MB (141855783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0133e5c0ff27ddf9c6033be84eb7f1a91fc11f3523d90116731fef97d62d24db`  
		Last Modified: Wed, 15 Apr 2026 23:16:43 GMT  
		Size: 2.5 MB (2461356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65903e28035e28d0fa064086addade78944f0181e6b3c0fa9eae5c9d76d533fa`  
		Last Modified: Wed, 15 Apr 2026 23:16:43 GMT  
		Size: 9.3 MB (9311187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d707605e7c73eac4d11f677799f6065f8758f87513f9a9bcb3a7aa4244c18a85`  
		Last Modified: Wed, 15 Apr 2026 23:16:43 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42638556904555e769c87b1503c209c799f9caf170b201187ebc4af76582c3c`  
		Last Modified: Wed, 15 Apr 2026 23:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:b447eb3936b76fcad5286f6a5c28dbe4dc9fde9c02d98b50aab83c469c304022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.4 KB (749421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dc650738a9054010f2d52ab1607c88324b570dbd72b5d91300904b88a0b519`

```dockerfile
```

-	Layers:
	-	`sha256:b74a5419c4a684b225e47f527b9a6968e6b379bb1346566fcf43af39549f069d`  
		Last Modified: Wed, 15 Apr 2026 23:16:43 GMT  
		Size: 732.9 KB (732926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a8d5576af7f95a1ac5751709746fca46549dbb3ec5bdc1b61791eeb5cba64ee`  
		Last Modified: Wed, 15 Apr 2026 23:16:43 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
