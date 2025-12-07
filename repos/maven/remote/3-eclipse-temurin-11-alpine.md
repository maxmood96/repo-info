## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:512f72fd9ae3144ae120f3c71523cd3b634d112a097791f93ac944be941a7e73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:8c57d28e5b6c10fad33e8d9f1edfcbc0b3411190c472b7b50ff5b341866aec4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173243338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50fa720c5eb32d8efc90e622e1925e42fdbcde07266764e3eae329090d0fa06`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:13 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:57:19 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 01:43:20 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Fri, 14 Nov 2025 01:43:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:43:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:43:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:43:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:43:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:43:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:43:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:43:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:43:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:43:21 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:43:21 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:43:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:43:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:43:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974df0e0eb67fd6fa35aefb5620f2d84f013b3e0b11b4c38737099a86303d60b`  
		Last Modified: Sat, 08 Nov 2025 17:57:42 GMT  
		Size: 16.3 MB (16289652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b829ff2503da3447968682832d5a69ea284ba1d657a4f8e58d4c799c8c348e`  
		Last Modified: Sat, 08 Nov 2025 18:23:46 GMT  
		Size: 140.1 MB (140102363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217f6eeaed3b8ab583b886e8495c9ca0664bb21717752475480bc1453bb07d2`  
		Last Modified: Sat, 08 Nov 2025 17:57:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81eccc49bc152ef173ac2d3a5ac97163278251fda36902720deae5aa454418`  
		Last Modified: Sat, 08 Nov 2025 17:57:41 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab9ca8d255f9da5348a8da70a5adc9e396a67d2eea3befc419155b3065cb0ed`  
		Last Modified: Fri, 14 Nov 2025 01:43:36 GMT  
		Size: 3.8 MB (3802846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5698351e06f3f7ecb9beb565c010161451cbe8a1feec9faf4aa559d03d72d0`  
		Last Modified: Fri, 14 Nov 2025 01:43:36 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bec2ef56105bc831c64dafb3307f4c6d5bb6e0601b6533d09d74bc9942d6d35`  
		Last Modified: Fri, 14 Nov 2025 01:43:35 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96e1364a92d8e419c11bfd96928c555723a469d12bfd935c5979489b2f8cc23`  
		Last Modified: Fri, 14 Nov 2025 01:43:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:eff20470ed3992b780ccb87d9451ec2e4ced78d81cef7b7a50601c4340450bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1156390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364cd494ebfa869560fddf881a97127afed725c5178f59e04e31812e35e92bfa`

```dockerfile
```

-	Layers:
	-	`sha256:81b9edc1aca414b1bd336a8298bd02e7af70afcfd19bb0b9a4b03214d923c10c`  
		Last Modified: Fri, 14 Nov 2025 03:29:42 GMT  
		Size: 1.1 MB (1137043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2d3d0711cbd9ae2d52827fcccc7da9c0a267761b12be91499e0479dc431101`  
		Last Modified: Fri, 14 Nov 2025 03:29:43 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json
