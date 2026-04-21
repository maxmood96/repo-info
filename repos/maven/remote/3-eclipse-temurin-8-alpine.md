## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:0970d2377d45c79529ba850d0a0efdfbe9a6071ba842a20453709fd1021fa840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:4c30e47d0c6b843f636844c462634f4213baa449e3016f2bd2231b3e98faf7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86661595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c550c5e7fdfa5bc4a5ac42cd405d2b379272c993b2ec1e4c2650360351dee233`
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
# Tue, 21 Apr 2026 18:11:07 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 21 Apr 2026 18:11:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:11:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:11:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:11:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:11:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:11:08 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:11:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:11:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:11:08 GMT
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
	-	`sha256:404ba1c2c7c743f670ee336ae7ad31b5177c3a9f9e1c7e7fa8ff56ea44f060a9`  
		Last Modified: Tue, 21 Apr 2026 18:11:16 GMT  
		Size: 3.6 MB (3586739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dc51cbea0c561f76c0014e1f803dfcc63d56fbad69df26dbb382eb37e71605`  
		Last Modified: Tue, 21 Apr 2026 18:11:17 GMT  
		Size: 9.3 MB (9312197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c35f17647b23390b129db467a405065e4b5d3c41ab149bcbd3765edb91036c`  
		Last Modified: Tue, 21 Apr 2026 18:11:16 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ba2abfffbf48270b48eba4e97cea75238bff80a4d16549f5a6e391a411b105`  
		Last Modified: Tue, 21 Apr 2026 18:11:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:07e16cdc132d6f310ef45954144bff80e3c2f7f5e6dd5565b41ab3409c3a0ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1261234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9435300dc4b49469480c1c25bf3bafd3c644f66a41456782fd8801217e5ccc`

```dockerfile
```

-	Layers:
	-	`sha256:49b6537f16eeae5e8fd71c83663e6b28432e916b23744c09fa96525c9b541d94`  
		Last Modified: Tue, 21 Apr 2026 18:11:16 GMT  
		Size: 1.2 MB (1244211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b45f8f11f91be4309ce8887b0924255056a91a7c133fe9fa97ba4db9120fc69`  
		Last Modified: Tue, 21 Apr 2026 18:11:16 GMT  
		Size: 17.0 KB (17023 bytes)  
		MIME: application/vnd.in-toto+json
