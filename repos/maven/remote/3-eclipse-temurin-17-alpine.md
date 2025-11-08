## `maven:3-eclipse-temurin-17-alpine`

```console
$ docker pull maven@sha256:ee052302c1dec3bac0ba075e86405808bd3197b327804168fbdcb8b95c0c3c32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:9ff820fb831d3db4a6d14379b2432c85d4f2d843b75bb2cd7bf86dae99005d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181566935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4d1f001317f053f091ec0c4d72ded66e50e3fc6cbe91be9fa323f2be611d31`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:10 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4dfea527f66034c5b6f4ca26afe692ae292fd267fd3b295c7f54f6461c65fd33';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:58:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:17 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 19:25:27 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Sat, 08 Nov 2025 19:25:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:25:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:25:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:25:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:25:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:25:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:25:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:25:27 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:25:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:25:27 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:25:27 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:25:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:25:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:25:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da2b7fa39d9ca89504884bfa364de57e68f656d1fd46f04941d3d34ffdbca30`  
		Last Modified: Sat, 08 Nov 2025 17:58:43 GMT  
		Size: 21.1 MB (21112255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9308f1b3f4d73b7c1a1aaba0b8eda9e9155caf3619e236d0c1a8b410704ef`  
		Last Modified: Sat, 08 Nov 2025 18:22:13 GMT  
		Size: 144.0 MB (143989616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3851e26ddd2575c157cfd1ad2a673f8e8b4541dd5f6a0b8a2f65d3935e10fe6`  
		Last Modified: Sat, 08 Nov 2025 17:58:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03fcaf37379fff8027b1eaf41f78daa4bf57cd4f423a9e9d7015d3bbcf9bb53`  
		Last Modified: Sat, 08 Nov 2025 17:58:39 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b631a1ef8d3eb6858ad9bfba2a1428998ef80d811034e593392f7faad28c3`  
		Last Modified: Sat, 08 Nov 2025 19:25:43 GMT  
		Size: 3.4 MB (3416568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a49a94f033801745489980c9196b8ade7d8442399e2e613198fb654209f946e`  
		Last Modified: Sat, 08 Nov 2025 19:25:43 GMT  
		Size: 9.2 MB (9242591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c3fa187b683d3265e093ceed6f18ed59a01f19b252e2f833a73d8667ba1a4`  
		Last Modified: Sat, 08 Nov 2025 19:25:43 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688c7f6d0b173c3dad663536ad02cb7f6da95c47b2941276c80a4d77ea7992bc`  
		Last Modified: Sat, 08 Nov 2025 19:25:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:08b2a38571f09b9b2ad2856cb733314a9d4b64ff8b632184c4fa130a98f096a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1255070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2a39ce8906fa6b2dd2610fa010cf13cdce1f84779311ec9bdd7989cf208cb7`

```dockerfile
```

-	Layers:
	-	`sha256:8c2fad7056211cc922926c9ddac23e11ed6687e24bf2f95c35ff5824404e78d2`  
		Last Modified: Sat, 08 Nov 2025 21:31:19 GMT  
		Size: 1.2 MB (1235721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72ce89ce24f666c5bfaf7586ef8829a32b558e1080dbb42fb487916a49605e41`  
		Last Modified: Sat, 08 Nov 2025 21:31:19 GMT  
		Size: 19.3 KB (19349 bytes)  
		MIME: application/vnd.in-toto+json
