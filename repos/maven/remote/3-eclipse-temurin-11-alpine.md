## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:870e4674676b7ba71842d2c214355d6db3398d851dd7fbbc9b04d0ea19f2610f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:2100423e63d7d2b6e056a4c9abf128eac8556b797eb5546ab81cbac66f35efe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174519905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf20a26427c0471ce08f81e4974f8e00ed131fb0ae32f464a25aeed52dbdec8`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:15:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:15:20 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 03:51:32 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 17 Mar 2026 03:51:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:51:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:51:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:51:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:51:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:51:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:51:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:51:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:51:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:51:35 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:51:35 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:51:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:51:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:51:35 GMT
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
	-	`sha256:0e03198ce1bcff72d14da682b57422ca0339a46a5a480a429fb7dfc1584cf098`  
		Last Modified: Thu, 05 Feb 2026 22:15:37 GMT  
		Size: 140.9 MB (140916724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ec050240a37b134eae130d1c8a581f8dc3f6a1812c89605de53cbc4807a7c8`  
		Last Modified: Thu, 05 Feb 2026 22:15:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b685f9f516a02949ff913848fd8f5097682da3f014f7f123cd6d47c1c03e35fa`  
		Last Modified: Thu, 05 Feb 2026 22:15:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e59cbf194e08047a64c0faf31a40f3c8f98d077704f4e37a80345a93fd4f14`  
		Last Modified: Tue, 17 Mar 2026 03:51:45 GMT  
		Size: 3.6 MB (3586850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdedd2ddd4143c01e49ad4035a0128cf5487935e2d102ddfe319ef561e7dd35`  
		Last Modified: Tue, 17 Mar 2026 03:51:45 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d9b283cdf1db018f4036b5b45b83569a449e0128eb1f074ef265833755b35d`  
		Last Modified: Tue, 17 Mar 2026 03:51:45 GMT  
		Size: 862.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f993b1e223265936e136d8ff5f3369998a6455a9f8740ce9f1a6d883b12c252f`  
		Last Modified: Tue, 17 Mar 2026 03:51:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:5a59dacaa67f59a31b2091751b07f1c9b3d174cdcfddf3134d8f932ca006fe1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4aa6378e5d6b2b383a85f26d517d45ab2e3b09cb46e13581da8c3f513e28b3`

```dockerfile
```

-	Layers:
	-	`sha256:ddd8262b111173cbcc86cae3825b47998c5bb18470312adde63accb38587b554`  
		Last Modified: Tue, 17 Mar 2026 03:51:45 GMT  
		Size: 1.1 MB (1145471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a6a9b11dc16fc6695521d11336afbd749f9e277a5b03e1b7d5e72a4cdf061b`  
		Last Modified: Tue, 17 Mar 2026 03:51:45 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json
