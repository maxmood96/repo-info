## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:c6ddf401e4af7472c0b697bfa73b6bf250521fc1208537d2e37cb84e348da9d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:ad82ce876c5737385eb0a9c135c1dbe421ca61918725b3aa5c8a52e158ffa548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177060402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24b02c43eace3ee21b3ae0f46421afc60f82742db0bdb3a5026ab8f13dd18cb`
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
# Wed, 17 Dec 2025 20:08:40 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 17 Dec 2025 20:08:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:08:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:08:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:08:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:08:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:08:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:08:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:08:40 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:08:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:08:41 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:08:41 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:08:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:08:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:08:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d4bc3368d3809cd8ad2e688cb5fe01f46190980ebdbfcac8e9822be3643f0c`  
		Last Modified: Wed, 05 Nov 2025 04:48:38 GMT  
		Size: 161.6 MB (161569892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72da1183d0606624a25de519945e4a706a53f8eca9207d7ddc4b1ad1140209a8`  
		Last Modified: Wed, 17 Dec 2025 20:08:54 GMT  
		Size: 2.4 MB (2374767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548ec9b6fc69786a062e485108d54609582471c6470709216a7551d4042fcfd3`  
		Last Modified: Wed, 17 Dec 2025 20:08:55 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88454940de31f989afeb562094182e1e14ac66ad3a2be7bbe06e71211b94e9ad`  
		Last Modified: Wed, 17 Dec 2025 20:08:54 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1882c4a16a7ed4d4425d27bad7f9c7aa077453dcc6af6e6e72a4e168f65a014`  
		Last Modified: Wed, 17 Dec 2025 20:08:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:a182a364ca4743c687266faf55ba9188f0b29242796ec9f93a274f5ff5273a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff372a307662a97daf2d8d32a2dc7dd0ed08c055e71ec3430f5d7b1fd8c5c48c`

```dockerfile
```

-	Layers:
	-	`sha256:74eda6b43270024f3353a4219959e979307132cf5f1542ca410336fb363d90ac`  
		Last Modified: Wed, 17 Dec 2025 21:29:20 GMT  
		Size: 726.5 KB (726526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c02ab8bf1eccaf951df3b770df0e87d3fea89e34b87b9249b50c9a0f3e364dd9`  
		Last Modified: Wed, 17 Dec 2025 21:29:21 GMT  
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
		Last Modified: Tue, 04 Nov 2025 23:25:34 GMT  
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
