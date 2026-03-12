## `maven:3-eclipse-temurin-17-alpine`

```console
$ docker pull maven@sha256:7f66736d217644821b8bad2f43aae25159d7eac85e80495d3cf1d09f6e809f91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:5f42cb7f2fd7989252e346c16f43faa54cad6d8f14179dfad4796c3304b90587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182846928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a04a44acde50d0a830b13163f99500ab185388818a34e41f4b9d987b8091ea`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:17:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:17:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:17:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:17:14 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:17:14 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:17:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3246fb1834d21c22ed717db9f8ba3f07e0f562bbeeebdc44a7499d5eb6df47bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:17:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:17:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:17:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:17:21 GMT
CMD ["jshell"]
# Thu, 12 Mar 2026 20:14:43 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Thu, 12 Mar 2026 20:14:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:14:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:14:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:14:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:14:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:14:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:14:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:14:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:14:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:14:43 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:14:43 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:14:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:14:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:14:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a547da4fe1538a9de970334bfb206793ffde2bd214a847994365c731033eeff`  
		Last Modified: Thu, 05 Feb 2026 22:17:35 GMT  
		Size: 21.3 MB (21315075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c540078c28f902907cb8db0fe7898ee78430d17c840a361da6ef7827dba16f`  
		Last Modified: Thu, 05 Feb 2026 22:17:38 GMT  
		Size: 144.8 MB (144762403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd2436f004e3c25b262ab1b7a9ff98f09c80c2bb3359c7e6fc8b4c4364bb969`  
		Last Modified: Thu, 05 Feb 2026 22:17:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946c51efe0fd37b3c13616ceba0f5a7fcc6c82f60c8679d6cf5e8fddd8620fc9`  
		Last Modified: Thu, 05 Feb 2026 22:17:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68292c373793b02bc5fa74340653c0ee06cec638620935dbe1a64ae3e0447016`  
		Last Modified: Thu, 12 Mar 2026 20:14:51 GMT  
		Size: 3.6 MB (3592994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d61f539a0e837cd5129cca084ac142311b926c7148fbc086d33dbe335e14210`  
		Last Modified: Thu, 12 Mar 2026 20:14:52 GMT  
		Size: 9.3 MB (9311177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd0c1058d9c314c9bb06221accf81d39e35a250c17dc2c0349ffcf132713e81`  
		Last Modified: Thu, 12 Mar 2026 20:14:51 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958662be68864682e76a9bc554071c6017c95a96b2b550c63e4714424bc667b`  
		Last Modified: Thu, 12 Mar 2026 20:14:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c9860f1b5e97b3689619fc5f49e741c7c754e385b644f451a79e8cda09008687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1263502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522b1072402eac8d1fc73b645510b38cbb3330686be5f9c57e477c29e10aaf96`

```dockerfile
```

-	Layers:
	-	`sha256:8fc1a5bf7b43dcc7682d4fd25fc4bfb4e0a9cc71f30bb76c66142cf4e8728af8`  
		Last Modified: Thu, 12 Mar 2026 20:14:51 GMT  
		Size: 1.2 MB (1244155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b833cd473034dac2c2fba5f194f297075ec4620079a5d2e62c3a52d204f7bc3`  
		Last Modified: Thu, 12 Mar 2026 20:14:51 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json
