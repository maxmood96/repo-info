## `maven:3-eclipse-temurin-17-alpine`

```console
$ docker pull maven@sha256:daba549390631041b8660d350de7f0e30a5ee79074f25656be2c768d591ac63b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:69c356d384881478f36bd0647188393f9ef642cf07ea00c24641a204225dc838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182847993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a297c8099f6520e0f4465a00c0d8979d1a57dab943a615dcc8edfeec4fcbf25`
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
# Tue, 17 Feb 2026 22:31:08 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 17 Feb 2026 22:31:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:31:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:31:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:31:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:31:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:31:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:31:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:31:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:31:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:31:08 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:31:08 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:31:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:31:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:31:08 GMT
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
	-	`sha256:23854dc5c9eb380cd7f7ab023f2da98ad64926f23f61237bfae6df416baa7323`  
		Last Modified: Tue, 17 Feb 2026 22:31:17 GMT  
		Size: 3.6 MB (3592996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a352896eb3f825b4b473bdf96b1e03ff4e69dd32087d5da0d37b385042c608a`  
		Last Modified: Tue, 17 Feb 2026 22:31:17 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cd88d0b691b11d64196717020bce0fad8d953b000e6333103902e22022e670`  
		Last Modified: Tue, 17 Feb 2026 22:31:17 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb05ec44a9458ab03e5a8b6e387bf1e10a27a90d061a829050220113c448a8f`  
		Last Modified: Tue, 17 Feb 2026 22:31:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:1a6d11367d8cb5d05fb847683b6b30efafb486e5285b9baad6b24af63962757d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1263514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9985a34f771a7ddf784a359027f3c6ba18bb1bd12326428fe818794ba9e852`

```dockerfile
```

-	Layers:
	-	`sha256:6695851af7e14774cce3fa543587787d49a296e7c94842b8ef366ceefc450988`  
		Last Modified: Tue, 17 Feb 2026 22:31:17 GMT  
		Size: 1.2 MB (1244167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2046a01c90ca92c44cd85a050f77369cc52e3371b62b683cf0469edfb383df`  
		Last Modified: Tue, 17 Feb 2026 22:31:17 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json
