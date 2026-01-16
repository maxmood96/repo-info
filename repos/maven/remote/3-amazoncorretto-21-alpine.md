## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:6f846c6b166ff2c75ed190024e05c97cd321c7d410c0819761e5048be2afecac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:4d0e4a12cf5568d6ebf3b17894e3feb65c09137bb1a096536581c54775c11dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177060387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce067eb2e3a48afef99c6d864b2ca386adc4b789611c889caf03b0a45df92d62`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:06:54 GMT
ARG version=21.0.9.11.1
# Wed, 05 Nov 2025 01:06:54 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:06:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 16 Jan 2026 02:45:22 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:45:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:45:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:45:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:45:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:45:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:45:22 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:45:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:45:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:45:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d4bc3368d3809cd8ad2e688cb5fe01f46190980ebdbfcac8e9822be3643f0c`  
		Last Modified: Sun, 04 Jan 2026 04:57:58 GMT  
		Size: 161.6 MB (161569892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31494b7ab944c3095f890e5d342b98b0c9d55d67fe28a10252d883642aa2e6fa`  
		Last Modified: Fri, 16 Jan 2026 02:45:35 GMT  
		Size: 2.4 MB (2374764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3ea0111633ec62f937aac29b02ea11811319fe54b4da9b55f16b2feefa829`  
		Last Modified: Fri, 16 Jan 2026 02:45:36 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf4f098bb56893b1486f4537f8266615f0aafedf1d5fce7c58427f1b1a1c145`  
		Last Modified: Fri, 16 Jan 2026 02:45:35 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65314585c55bcbb3114eed41c138953614e137b0b7bdab3cec43f60d6b8ae98b`  
		Last Modified: Fri, 16 Jan 2026 02:45:35 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:4b856c34a44116e7c34dbc1b9b02fb0eaf2e980ba9d106eece8b1922a691670d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290e063d8ec23002c3596fa55c73dac2e84d3a20e9244340889d61e64eccc74c`

```dockerfile
```

-	Layers:
	-	`sha256:e4d38c46172407da1678107b2b4880801fac292e6d6410580caffdf7f9ee6820`  
		Last Modified: Fri, 16 Jan 2026 03:29:23 GMT  
		Size: 726.5 KB (726526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfcba5cf2aa23a3f17fcbf66a081a04a4818dc4c248fa10e108d74b1ae47dc42`  
		Last Modified: Fri, 16 Jan 2026 03:29:23 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:92f2f6c03fd9a11aea9730692cd7ad91e7c21e8593a9bdaecdf7502f1d26edf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175445487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11264be9fbe2a9e7a55cbc11a3336057698b26f12c7c6401c6a83c5c8a8da98b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:21 GMT
ARG version=21.0.9.11.1
# Tue, 04 Nov 2025 23:16:21 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 17 Dec 2025 20:06:56 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 17 Dec 2025 20:06:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:06:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:06:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:06:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:06:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:06:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:06:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:06:56 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:06:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:06:56 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:06:56 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:06:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:06:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:06:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fd450f0185222facf50c3585803b24553a293cbfa900eb12641a7831d0da01`  
		Last Modified: Sun, 04 Jan 2026 01:36:57 GMT  
		Size: 159.6 MB (159588499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4421c0242f80c0672954cf61281a4b5e7a0cf9b1455034ee6a5684bb2dc9dfdf`  
		Last Modified: Wed, 17 Dec 2025 20:07:12 GMT  
		Size: 2.4 MB (2405638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e168b6ee0dc35acc220debc0d1be2118a701eca06d044a6ec2f4c8b42435bce2`  
		Last Modified: Wed, 17 Dec 2025 20:07:12 GMT  
		Size: 9.3 MB (9312240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55b0e1c00b6861abedc6ab67d59cbee731bfdf700094e55a1341ae20a20957b`  
		Last Modified: Wed, 17 Dec 2025 20:07:12 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa8dadd4e97a57ce9afb2b53c0f7fb7ed54764b5c14341ad6dc24ac6a2424c`  
		Last Modified: Wed, 17 Dec 2025 20:07:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:b6b77c2a0b5dfa1073f5edb7aecc45c565e4fc18a9d58f3cfd40fe4757ec8f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 KB (742427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26153a29710a2dc8c79345ab339f6953bd30b02f9527c53447f5bb8ebfdcc58b`

```dockerfile
```

-	Layers:
	-	`sha256:738aba74d664f3934494f3828f3753cd8e9c1c9d0c3ec5adb393346fe9bff2f5`  
		Last Modified: Wed, 17 Dec 2025 21:29:25 GMT  
		Size: 725.9 KB (725933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f1344ba1ad00687f682a8dd6030405eb681e25d465e6799fd7df706753f0a8`  
		Last Modified: Wed, 17 Dec 2025 21:29:25 GMT  
		Size: 16.5 KB (16494 bytes)  
		MIME: application/vnd.in-toto+json
