## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:7d1041daf03266cae5fb63f35ae42ddc630028ae4c8c96635066d0a49c7cecdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:51077e2384da16b5198221e69ced5cf9c48ad257db679443a1f9b765fe6ffe7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86661386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b9a86711c3dcde83236bf7bd370e242351734abf541d3e540a8385e47e4ef1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:12 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='149565c3de89ef9ceb640312ff77aadea79fb82fa946ae9aab4d024ba25eb47d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 23:28:45 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Thu, 05 Feb 2026 23:28:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:28:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:28:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:28:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:28:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:28:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:28:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:28:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:28:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:28:45 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:28:45 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:28:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:28:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:28:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba30a9b9fbd57b01a8081d96f19cccf9befdb10d3a054b012d5419c813f251a`  
		Last Modified: Thu, 05 Feb 2026 22:13:27 GMT  
		Size: 16.8 MB (16839871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b65cc608a32035ca289bff3c4fea696fb1ecf0823a86c91ed423dd94dbf4d8`  
		Last Modified: Thu, 05 Feb 2026 22:13:28 GMT  
		Size: 53.1 MB (53057148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ec9d3b4a0ae2f48cbd3f356a2342c62ba56808906410a919e563894ca3963`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4758e0f4968b23dbc7eddea73b3296e03df78caea6faffd00fde093c4fdd8f`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378dfd8bb313106921848694bde55b36ce8e453a3254cb3e4745079ce70f35e8`  
		Last Modified: Thu, 05 Feb 2026 23:28:53 GMT  
		Size: 3.6 MB (3586836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a31bdc3c55905bee662f6162f96ef49eb142a301deac1cf419fa366f8b2458`  
		Last Modified: Thu, 05 Feb 2026 23:28:53 GMT  
		Size: 9.3 MB (9312233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6c11012e4b4bf37b4261f1327bd979d5e1ba091a52e91591941dc8b26f40f3`  
		Last Modified: Thu, 05 Feb 2026 23:28:53 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de05472921e4da8803e6ccf9130b60fec6aec7d8415efe2c04c60f1421db442b`  
		Last Modified: Thu, 05 Feb 2026 23:28:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:22fbccb7680eee55ca942f673dd976fe3be0c88d5f8689b817c31b9fdcce33f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1265508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b449668e5606024621504e94f4b0ad6c3d46ac0b51f314e16e218cf50d69af7`

```dockerfile
```

-	Layers:
	-	`sha256:1dcb00fadaa55e9acd3ad6c0ba7b923948159bc283f3cf6b99834d1a8beb0adf`  
		Last Modified: Thu, 05 Feb 2026 23:28:53 GMT  
		Size: 1.2 MB (1246178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4fe7cacfa516019ac4ed5d34b9ac32ebdeb7934ce5535faf4d99ad9036065cd`  
		Last Modified: Thu, 05 Feb 2026 23:28:52 GMT  
		Size: 19.3 KB (19330 bytes)  
		MIME: application/vnd.in-toto+json
