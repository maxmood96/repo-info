## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:76ed86cbb9d3b82cae223c73dec4428eb0830e91fe691e62b4e67bb06775028e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:dbf96c7f7333a6802c4acd0850f11c3dc1f81f7368c04fb6e0851fdb69718d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116335016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da922bd8963c90ffda9a032777429b886b2aefc2a04e10b05f08b1ad268fbb3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:58:42 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:58:42 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:58:42 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:58:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:58:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 09 May 2026 00:20:59 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Sat, 09 May 2026 00:21:03 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 00:21:03 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 00:21:03 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 00:21:03 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 00:21:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 00:21:03 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 00:21:03 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 00:21:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 00:21:04 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 00:21:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 00:21:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 00:21:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78799819c2ab46aaeea7584a6e63546f8614eabfc576be9cb56de175814cb8`  
		Last Modified: Fri, 08 May 2026 22:58:56 GMT  
		Size: 100.8 MB (100751417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c03e978ec602572c3ea00854a6f56a69558d6237dc2837c1adc1c8c15c473`  
		Last Modified: Sat, 09 May 2026 00:21:12 GMT  
		Size: 2.4 MB (2406161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f764ef3c3c11cf4c5aa45f50667ab2104a2dac28aa606d88acaa41ba8945edb`  
		Last Modified: Sat, 09 May 2026 00:21:12 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0b6bb2b4efb19b0820a4876e561109178f4fc5e778c28a6739f22dd73f4f9d`  
		Last Modified: Sat, 09 May 2026 00:21:11 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bc17afcfa98ebe1fcc45d06c1f564fe438f47dee912ac51e1960c55d5f6ece`  
		Last Modified: Sat, 09 May 2026 00:21:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:6ab46c6b963e37dd798547be1a8645a24a7644f89c2c30255f199245fa53ec78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.9 KB (406949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52837aa188d92c854023e7b72acfa9aa9cea1a350174f19fe6810f2884e7e6ac`

```dockerfile
```

-	Layers:
	-	`sha256:d2d2588527ef97f25a4c90b4a0bb8890565e3859fdbb38f91d97dbb503530b44`  
		Last Modified: Sat, 09 May 2026 00:21:11 GMT  
		Size: 392.3 KB (392282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b09a9e334876d74ae4f0f2cc4b295b1bd3216cc299240f247c29abfb8a0d9e9`  
		Last Modified: Sat, 09 May 2026 00:21:11 GMT  
		Size: 14.7 KB (14667 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b93dd9d7e198284ff8ed3bcdab5ed604f0159d6ec3fa2644ff92deb17ae9fc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116506568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc18e36206a62123e3f6537acaa9f885c3dfbc7721895de0f9f24aa9b2dbdb5a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:48:37 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:48:37 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:48:37 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:48:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:48:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 09 May 2026 00:18:43 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Sat, 09 May 2026 00:18:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 00:18:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 00:18:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 00:18:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 00:18:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 00:18:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 00:18:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 00:18:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 00:18:47 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 00:18:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 00:18:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 00:18:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2b2750547d1382e8902a58f482ede14d5484098b6dbba6954feb54a9e3dbe3`  
		Last Modified: Fri, 08 May 2026 22:48:51 GMT  
		Size: 100.5 MB (100544688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f99ca239705853c573b3626f01f4854832dbcc5e3779cd99dd2bbd5267ec380`  
		Last Modified: Sat, 09 May 2026 00:18:54 GMT  
		Size: 2.4 MB (2448770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221a2565c401314f7bb74304b38b86470f4f960c51a58994a9823aabeedb908c`  
		Last Modified: Sat, 09 May 2026 00:18:54 GMT  
		Size: 9.3 MB (9312231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb71c44546ed765375467ac0e51cce20818a17ff68078f6a1c1141716e93859`  
		Last Modified: Sat, 09 May 2026 00:18:54 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702c7f27b711557ea1d9bb9eaf9ef2e038e20d0e7435b423fd6e2a97e9d24005`  
		Last Modified: Sat, 09 May 2026 00:18:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:b2414f6902a431ea6afe7e1fcb601ebd6aec39bebb678fd5e4922148dc94c10b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.6 KB (406552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c4e1dc9a50d03f647f4f1e002310352c6dee54c1755fa7b0aedd286232a071`

```dockerfile
```

-	Layers:
	-	`sha256:652b383957d0502f27576bec5375b5207e01ecc99d240102d0bfa68cfeb38e15`  
		Last Modified: Sat, 09 May 2026 00:18:53 GMT  
		Size: 391.8 KB (391752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b208770a9b5ac8347d9fb4b423bb38287e21715ee470316e3c05c90936357611`  
		Last Modified: Sat, 09 May 2026 00:18:53 GMT  
		Size: 14.8 KB (14800 bytes)  
		MIME: application/vnd.in-toto+json
