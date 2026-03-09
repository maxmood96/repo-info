## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:79d9a7674f4b260308da7efc63967be92ed0a09c99c44c94f96fd060885ce890
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:c64aad57c37f9ad3fb8279a72812061b019547773a5acf43a7ad229b0105d220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87046694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbafd06e1f5be0c854157e6d8d1a063b9e945e57cd56b033ae66217aa77d1ac7`
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
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='149565c3de89ef9ceb640312ff77aadea79fb82fa946ae9aab4d024ba25eb47d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Mar 2026 19:13:05 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 09 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:13:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:13:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:13:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:13:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:13:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:13:06 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:13:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:13:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:13:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:13:06 GMT
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
	-	`sha256:07b65cc608a32035ca289bff3c4fea696fb1ecf0823a86c91ed423dd94dbf4d8`  
		Last Modified: Thu, 05 Feb 2026 22:13:28 GMT  
		Size: 53.1 MB (53057148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ec9d3b4a0ae2f48cbd3f356a2342c62ba56808906410a919e563894ca3963`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4758e0f4968b23dbc7eddea73b3296e03df78caea6faffd00fde093c4fdd8f`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c8c6593f2ba49787de5563bb9c934e2172cfa8cf72b52175a9fdfc8a97dddb`  
		Last Modified: Mon, 09 Mar 2026 19:13:14 GMT  
		Size: 3.6 MB (3586847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9ec1080912737c4dfca3bf050f64bf1432080356acd254f66e5668002809ac`  
		Last Modified: Mon, 09 Mar 2026 19:13:14 GMT  
		Size: 9.7 MB (9697525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d52f277f740b9a533c1e641921e7eb07c3ff784937ca8775b40e7c4b334ddf0`  
		Last Modified: Mon, 09 Mar 2026 19:13:14 GMT  
		Size: 861.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1915b8ccfac9abc1291e7dc56e9f3c2d01849ac1b9c9739807f79b5e848304e3`  
		Last Modified: Mon, 09 Mar 2026 19:13:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:0d20c7f53ba083e7af1f9839e0d71ce6eb15698bdf8251c6b48a416e23eb3f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1271985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7427433aa3fca46218088e7ed925947009cf11689317f59df19b02b0d3935a`

```dockerfile
```

-	Layers:
	-	`sha256:206af8de05f4897a723f54ba641bb778ca3942628afa2c7864d4c2cfea197c58`  
		Last Modified: Mon, 09 Mar 2026 19:13:14 GMT  
		Size: 1.3 MB (1252655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6239d374a1d8d4a7a559dfeff6aecad28749335daae265a0e96b676e85a8e1cf`  
		Last Modified: Mon, 09 Mar 2026 19:13:14 GMT  
		Size: 19.3 KB (19330 bytes)  
		MIME: application/vnd.in-toto+json
