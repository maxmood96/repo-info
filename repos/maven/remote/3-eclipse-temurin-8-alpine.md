## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:cafa93940ae41fe1e4882200b3a1cd39981b9f7127024595a8b571f41eb0c9e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:9b4d4c9cf9d4b30d79191a41d0e12d8363cad0d6354ce8555656b651913480d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86660594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4173f605b479b76b259edd8c7f1afe1a7e5ec6348e879f02691f606107200246`
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
# Wed, 15 Apr 2026 22:49:12 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 15 Apr 2026 22:49:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:49:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:49:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:49:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:49:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:49:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:49:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:49:12 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:49:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:49:12 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:49:12 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:49:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:49:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:49:12 GMT
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
	-	`sha256:4e90ede1cfabe209e4c63e4476703e6392494a551cf998ce124de8246739b70a`  
		Last Modified: Wed, 15 Apr 2026 22:49:21 GMT  
		Size: 3.6 MB (3586718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e33b7e569959a3b6c4df2070f2febd4f30ebfd4a1e50493a323f4e6641d4e5`  
		Last Modified: Wed, 15 Apr 2026 22:49:21 GMT  
		Size: 9.3 MB (9311190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36333eb64f43094cfcc59dacb63559256279a8d8ceb4abeeff84bfdbb35d9c92`  
		Last Modified: Wed, 15 Apr 2026 22:49:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5097af2bca3a35055fc0e865d6f3898ad55ef8874bf038ebb523e5552f289242`  
		Last Modified: Wed, 15 Apr 2026 22:49:21 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c0fd28166ee2eb94ed117781a8a611b8d6e031824ce75cbc617764cef7acaa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1263540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27edd80b0ae74e6edd23ffab86ba7eba70202a3f70b286677e6e4c33343c4e5c`

```dockerfile
```

-	Layers:
	-	`sha256:1829e0c0bff2357da39699058f64b565953f02bc56ca8baf96b1ea9c6b90ceae`  
		Last Modified: Wed, 15 Apr 2026 22:49:21 GMT  
		Size: 1.2 MB (1244211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f232d93ea26e4371a8f0b388829bc1ab5a4ed1b4fbe49c8e88b9b787e5d313`  
		Last Modified: Wed, 15 Apr 2026 22:49:20 GMT  
		Size: 19.3 KB (19329 bytes)  
		MIME: application/vnd.in-toto+json
