## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:5b78fd2690f13f8be55b3215b5934006ed97defaf1d395ec453edaa449dd5c1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:488aedf007512aa3e3860217bfa17a1cb032f9625a9a50d5908436866f80f193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86661699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968e1fc394285dbc909f4c1907994b831bbe369aa871c2e28619a7a3df16da4d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:31:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:31:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:31:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:31:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:31:59 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 20:32:04 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='149565c3de89ef9ceb640312ff77aadea79fb82fa946ae9aab4d024ba25eb47d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:29:27 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Fri, 08 May 2026 00:29:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:29:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:29:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:29:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:29:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:29:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:29:28 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:29:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:29:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:29:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775c53a23a895a8fdcb2534de50a64b420d676e982f81a1e72e88f6b283280fe`  
		Last Modified: Wed, 15 Apr 2026 20:32:15 GMT  
		Size: 16.8 MB (16837772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460aa70bd9e11e0b3714c18bac2dec16818f7a610a20a6da0300e980efa54cb0`  
		Last Modified: Wed, 15 Apr 2026 20:32:16 GMT  
		Size: 53.1 MB (53057252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b05e60fb41b293e444a1006149898fd07dc7d77ec90c74334af217061ac265`  
		Last Modified: Wed, 15 Apr 2026 20:32:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c1bca010c93241bbd54bb2e30b91a40a49144084be3f551e198dbd54ab2e33`  
		Last Modified: Wed, 15 Apr 2026 20:32:14 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51e2b12476f8485ce0afe8d49bfc82501a441d4b9fdc6594085e31866cb27d4`  
		Last Modified: Fri, 08 May 2026 00:29:37 GMT  
		Size: 3.6 MB (3586787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c18cd8419cb1300f2b1b652da76ca86e349671f8a09b4aa658d8e2d0db1dd26`  
		Last Modified: Fri, 08 May 2026 00:29:37 GMT  
		Size: 9.3 MB (9312253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be0176695ade01ca326f269741ffcd6eb64440e1ede8812c57bb8c4aa2b3d6d`  
		Last Modified: Fri, 08 May 2026 00:29:36 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064f57867a495dbec4c06d3259b3bb7b30e063b78f755e863921614c5f019c2e`  
		Last Modified: Fri, 08 May 2026 00:29:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:714343473fe3c120f10f156a4cc928e57fbb941b499b4f271285b684a48a2dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1261388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7ca33b3a3706e55dd3c8147ebd43d7f73424b948ec90e389401896ec0da1c3`

```dockerfile
```

-	Layers:
	-	`sha256:67d7834aad9823e53f8341ac7e96b6f3a65d88e59dfd358582ec6eed1fb347c6`  
		Last Modified: Fri, 08 May 2026 00:29:37 GMT  
		Size: 1.2 MB (1244211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:166721c4b6b55514126e6c4826a0b7eea30da4c1baec0cf35240c71bfd93f536`  
		Last Modified: Fri, 08 May 2026 00:29:36 GMT  
		Size: 17.2 KB (17177 bytes)  
		MIME: application/vnd.in-toto+json
