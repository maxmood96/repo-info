## `maven:3-amazoncorretto-11-alpine`

```console
$ docker pull maven@sha256:aec28c948861ee974a7737260f19c74c04c3cd6f95003adf8535c85fa27e67c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:051f09ba7fd4f429ad75ce0e6760bf0817f929e8f7a77ed2c62201c322b89e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159181210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71810fbee611136dd29a1366502ce703367459a2b978649a6299fc0eea19137b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:46:21 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:46:21 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:46:21 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:46:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:46:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 05 Feb 2026 23:29:29 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Thu, 05 Feb 2026 23:29:29 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:29:29 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:29:29 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:29:29 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:29:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:29:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:29:29 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:29:29 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:29:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:29:29 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:29:29 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:29:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:29:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:29:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d986d7e858d6100508f42bc906b71c57de3eadb7c1b125079ed3f059f3f83221`  
		Last Modified: Wed, 28 Jan 2026 02:46:38 GMT  
		Size: 143.6 MB (143585877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a672754b52c0e62e82ca7ec5b7ebed793e1addd6c76e53e404b4fdb48e2ba898`  
		Last Modified: Thu, 05 Feb 2026 23:29:36 GMT  
		Size: 2.4 MB (2420236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e43a3bfa2c631c4f4f24ecd7d3c3742215edf33b9dfd0b28de05fc1d2fa8abb`  
		Last Modified: Thu, 05 Feb 2026 23:29:37 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04256ef19ca1c4865f8ce943cfc0804b8a04cf7e94f7ec6c882191af96650498`  
		Last Modified: Thu, 05 Feb 2026 23:29:36 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030e2de17f0dca6b0ea3f9e96a1b2642c11f45d6939b14842f6b9645d3f4631b`  
		Last Modified: Thu, 05 Feb 2026 23:29:36 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:8d0c1b908d3c5f6c92cd9dcfee4e9ddc4114a43bc72381437cf15b5b14998747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.9 KB (749878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c647e11b273033371e5cd130b9b4a1949512127e51d0e27a0c832f44cbf68b4d`

```dockerfile
```

-	Layers:
	-	`sha256:8cbf9d4a43cec820ae75549e2c1095ea0b403a61b3fb47c921fad1870ee592b6`  
		Last Modified: Thu, 05 Feb 2026 23:29:36 GMT  
		Size: 733.5 KB (733516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cddae9a4606a13346570a63df344b83f49df3eca0260bd34ef24e06001447415`  
		Last Modified: Thu, 05 Feb 2026 23:29:36 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:13ba105de0fd2116f0ac1fb942d92a334e1382d3db24a9d8e0fb785098a59795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157827467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed209616906d5d7c33fdda4f67ecf3f8728808ce12c6811918274f87117023f7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:01 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:47:01 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:47:01 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:47:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:47:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 05 Feb 2026 23:40:29 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:40:29 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:40:29 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:40:29 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:40:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:40:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:40:29 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:40:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:40:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:40:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552dd13d8c7000c34c67e3db376e66141f2a096e4c79b9abd594731ea071a2d`  
		Last Modified: Wed, 28 Jan 2026 02:47:19 GMT  
		Size: 141.9 MB (141855734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1845cbb746d69efe488fde0fc626aaefa4170fd7b03f69f2f51ade63ef9791`  
		Last Modified: Thu, 05 Feb 2026 23:40:36 GMT  
		Size: 2.5 MB (2461358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb493fdbb81bd1220f1b6027048d302fad4fc7078429ab621f4b56201dfd0701`  
		Last Modified: Thu, 05 Feb 2026 23:40:37 GMT  
		Size: 9.3 MB (9312248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5042a33e85f6e449d9d30a7d4dcd9a18bcbab2ff829f0d5bad0d2a05875f61`  
		Last Modified: Thu, 05 Feb 2026 23:40:36 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c0bda66c2ac10a34844ea937be28947b7f4084426bf4a399637c47567e8e1d`  
		Last Modified: Thu, 05 Feb 2026 23:40:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:3e933915656f617c9ba15722a84b6da17309328209c2d46b44def0ce79f01c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.4 KB (749405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7e4c4349259697834873dcf2da9004459daf8992b0d098bb674b16b2f1ad99`

```dockerfile
```

-	Layers:
	-	`sha256:30675762c47b5e721e85213d5bdc32bf4b478c7f6ec0abf20aef66ad740182be`  
		Last Modified: Thu, 05 Feb 2026 23:40:36 GMT  
		Size: 732.9 KB (732910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03ea42a481959bb908842e5f947657608790597d8240446dd410e1c764ccb9c4`  
		Last Modified: Thu, 05 Feb 2026 23:40:36 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
