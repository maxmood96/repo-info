## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:944c66515e2fda70315aa1665644bce48578b345574e93f0850163cc8f98a53d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:06faac1a76c5de3b829d8b544b47bccd15a1a2d70d088d53e54f31497b79f8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85776445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9aef282b5166bdee1c18c5205dcdca40529a09d6125b3c23a63dc5c157f118`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Jul 2025 06:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='21e28ad4faf34a2d353252ea363d57afe8d72f9d55f66a54e4e99fd1acb7786b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc9e5a155a7ff06c0190ea62107ab1a927e87f603ebbf7a293a0f96aa156ee7`  
		Last Modified: Wed, 08 Oct 2025 23:01:38 GMT  
		Size: 16.3 MB (16289659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93265a0ff65ce60a966752d25af81c37784a583b19f7d06efc02dbe0e78378da`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 52.6 MB (52635416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bf4f6cfaadc211f87c2de87c1251cb65e3da0c8d13918165069ce606153159`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1db43729eb563fea67456a3da0efc23000862940ff05797f125d3eadf8db99`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10abc925e3e54dea35ed8cf56b983d5f44f14fcede4c2dd7aec62f44bd2b166e`  
		Last Modified: Wed, 08 Oct 2025 23:51:04 GMT  
		Size: 3.8 MB (3802847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7301a0608cf2b7c702191eb720da4bac019fc058dceb267f138909467b3a9ef4`  
		Last Modified: Wed, 08 Oct 2025 23:51:05 GMT  
		Size: 9.2 MB (9242594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c677c4b078e33a84a2d98c07e33e58f6033b43495bacff0c0af38b60e8733f`  
		Last Modified: Wed, 08 Oct 2025 23:51:04 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896607499444f36bee299e8c737a0841aa2ce17c33a5f1f3205a89b9ac682500`  
		Last Modified: Wed, 08 Oct 2025 23:51:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:def8d30442f244d89354734bd733a2e966aa4b50f3c145b1b1ef548083229687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1257734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a487fc7c9f2527ca449b2e426fdf9d51898e90f87e4da5263d5ebc35c2ca94`

```dockerfile
```

-	Layers:
	-	`sha256:fd4ecf849122fac7405858402ab00a5dce0a547c0b27bbb5ec73bf0c88500701`  
		Last Modified: Thu, 09 Oct 2025 02:29:03 GMT  
		Size: 1.2 MB (1238361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729128ac5e5468d3bff88f19898407c1b1ddd8c0fdacce538a08310963f0f83a`  
		Last Modified: Thu, 09 Oct 2025 02:29:04 GMT  
		Size: 19.4 KB (19373 bytes)  
		MIME: application/vnd.in-toto+json
