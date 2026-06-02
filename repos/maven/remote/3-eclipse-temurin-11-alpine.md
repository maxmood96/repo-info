## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:fe91274eacd4214a520d3ec84d97ad1d0589c32db57c4b299ed7bd0646b2811f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:dabaebd85a6707fd1b3d82bc29e7ec87585e5e467395d8fdb159a08a35c5c8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174648554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558e2805aa80345e027f20a7c2a0b477031ebdc3be21ef0842fbca96134ee7ea`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 22:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:44:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:44:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 29 Apr 2026 22:44:05 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:44:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:44:17 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 10:30:44 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 02 Jun 2026 10:30:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:30:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:30:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:30:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:30:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:30:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:30:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:30:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:30:44 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:30:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:30:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:30:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c175c39880efd27b1b0b6f4b68db4424c3664c1899709c2068bc4301855817b`  
		Last Modified: Wed, 29 Apr 2026 22:44:33 GMT  
		Size: 16.8 MB (16837661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23b06a78b6e346324b4ccae7f54064e05cc8059b37b593caf9730186b81c6cd`  
		Last Modified: Wed, 29 Apr 2026 22:44:36 GMT  
		Size: 141.1 MB (141074590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b27e99b60546186d5398cb848761881034ad4a2495edd58778348608ab13b34`  
		Last Modified: Wed, 29 Apr 2026 22:44:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5cbe1f675378862d1c920e9f972f54caa6e00e0ef8bf232fd844c01fa839ac`  
		Last Modified: Wed, 29 Apr 2026 22:44:32 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb67faefc4c55970036866e0d99e0ce68be4fbb6a3e98a2348b500ac31f85fa`  
		Last Modified: Tue, 02 Jun 2026 10:30:52 GMT  
		Size: 3.5 MB (3508720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecd7640c3e8d284d4b9adbaa66fca9b125fede3bf405c0597a062b9cebb80fa`  
		Last Modified: Tue, 02 Jun 2026 10:30:53 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f572dff08e68cb5a92b40f5eadc5bed137f216dad3d1fd0fdac24c4d2017730b`  
		Last Modified: Tue, 02 Jun 2026 10:30:52 GMT  
		Size: 863.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6025b605ae4b87122e40c949cd6c2fa1d6c87b5528748a77a6036467ca5377`  
		Last Modified: Tue, 02 Jun 2026 10:30:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:e117b65c24c47ca4ab57d89a5f7152531a29bd73e65ce1c28782fe2669135a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1158972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80dcb55c29aec0a0544a0958dfa681c36dbd9c9523704b3b61320a941a31c83b`

```dockerfile
```

-	Layers:
	-	`sha256:b27aca5791b0c699036b24a116d32e2ff11e5a140f11d85216b660e3f8f8f9ef`  
		Last Modified: Tue, 02 Jun 2026 10:30:52 GMT  
		Size: 1.1 MB (1141927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd0a5aceabd0663f2609e672e354f03de1aa204265a5a3f8017af31c1618302`  
		Last Modified: Tue, 02 Jun 2026 10:30:52 GMT  
		Size: 17.0 KB (17045 bytes)  
		MIME: application/vnd.in-toto+json
