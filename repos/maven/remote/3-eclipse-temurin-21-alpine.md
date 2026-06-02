## `maven:3-eclipse-temurin-21-alpine`

```console
$ docker pull maven@sha256:c3b70520630a94abc4bb9d87bb3c6a0bb44f936e0ef1035233727411c7b5b854
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:a17bf53afe01abcfb61f6f64eed6ed34a63db0197e5097addb55a0f6dfe73135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196473342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab4a50607418600528e8c3a91264702b396b7ffdd94651b9b4c92e1b4e6c915`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 07 May 2026 23:59:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:39 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 10:19:07 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 02 Jun 2026 10:19:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:19:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:19:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:19:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:19:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:19:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:19:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:19:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:19:07 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:19:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:19:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:19:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b50ae58d435408a9b026fe52e1670bc1fa8333eabfe9bf8732808b503921e21`  
		Last Modified: Thu, 07 May 2026 23:58:58 GMT  
		Size: 21.3 MB (21336223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcaabbcdfa248e8282ff1b8185b085013c4acad8c1d745f6bc6c254ca2c91cb`  
		Last Modified: Thu, 07 May 2026 23:59:56 GMT  
		Size: 158.4 MB (158396777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b89d263afc40ec784ccb9f91009ff3a1331571314d0a8213a083c9035f3155`  
		Last Modified: Thu, 07 May 2026 23:59:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4011cd827d707fc4492dbd50182b9de9e9d695532577a6760b7fa8a6b093e0`  
		Last Modified: Thu, 07 May 2026 23:59:54 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d95d37bea8e1cb9e956a15e337e08ea6ee4d189308df8d2ca2d37cc920f06b3`  
		Last Modified: Tue, 02 Jun 2026 10:19:16 GMT  
		Size: 3.5 MB (3512769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c495461d1fde9865ae272dca00c2bf6b038dc84ffbde0355f61e443e7dd146`  
		Last Modified: Tue, 02 Jun 2026 10:19:16 GMT  
		Size: 9.4 MB (9359958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93ed623d6748b46f7579899432d1703415245c7a568a3b8abcc1106a41c75be`  
		Last Modified: Tue, 02 Jun 2026 10:19:16 GMT  
		Size: 861.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f81c0d48aa2a5f5ac942d9ff0c3282d1ad9afde569ac235142e2301a30344f3`  
		Last Modified: Tue, 02 Jun 2026 10:19:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:d3d922f615493ade5258353cf7691c73e5fd8c94a1c495e5ef10312195a12e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1260133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3368eb4723443e8826a6afcc3a9abff71d769a1c046096878af3fe1ec343a4be`

```dockerfile
```

-	Layers:
	-	`sha256:dd02ebbf96cedd78f2944da764c8fba4e0836db77ca68989740cb637ebbce7b9`  
		Last Modified: Tue, 02 Jun 2026 10:19:16 GMT  
		Size: 1.2 MB (1243088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54701a6dc3c5d3349a277b58d400f33bebef24f9e19f3b52a3c220edf25dba43`  
		Last Modified: Tue, 02 Jun 2026 10:19:16 GMT  
		Size: 17.0 KB (17045 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b005c0518f8ab6948ec0ba056443cc0bb34cf834703f2ccda634b263bccda0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194880694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb182a9311a10fe8c530d685d49fd0b4363b7da582c8ac86d72068c7b679cc39`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:58:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:58 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:58:58 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 07 May 2026 23:59:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:07 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 10:17:35 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 02 Jun 2026 10:17:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:17:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:17:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:17:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:17:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:17:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:17:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:17:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:17:35 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:17:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:17:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:17:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a9f60e46e53646ef0910131cad063b4c547e8b484db8a7f43c06e8c8d8ee11`  
		Last Modified: Thu, 07 May 2026 23:59:24 GMT  
		Size: 21.3 MB (21321387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7335552e625aa4d940009043b9ade8114a61f7445ad089dd0699e9c2cbd02`  
		Last Modified: Thu, 07 May 2026 23:59:27 GMT  
		Size: 156.4 MB (156402365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbe5c3db0c5dad3a2183ba5e385ef243c43b6847fa16af1db10346a47fb9e86`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319e0f520245ecdfe248ad69c9025626cdb9a8a435ccd3b9a19da574bc33023`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8723eecad0c31eb67a9d2b79ca51a4ebbca57b6730f9a2a9c1d4044655bd0f44`  
		Last Modified: Tue, 02 Jun 2026 10:17:44 GMT  
		Size: 3.6 MB (3593680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573f0df248d64e9acfe0b0919a428a51db7588d071ea105d9d629c8741d593a8`  
		Last Modified: Tue, 02 Jun 2026 10:17:44 GMT  
		Size: 9.4 MB (9359968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d216b8730b80d149b1223cf264e8c99b78da159fe33b9ef86f576f18e6507b04`  
		Last Modified: Tue, 02 Jun 2026 10:17:44 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7abd833574cb114fc4085edca7174b37b3227158ca458239da6e5783ab41f1`  
		Last Modified: Tue, 02 Jun 2026 10:17:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:0a4e115761063c0976c4da17229f0523c0374c8c0ff70df6dffe05ee571b90ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1409616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86defb0f7701f178be0ba7e71382a882d332eb3b0ceada4665649e52f9e8a6cc`

```dockerfile
```

-	Layers:
	-	`sha256:e171239fb87d2734305e4b0a68d6b829cd6c3d67918f2e25794f187e059485c4`  
		Last Modified: Tue, 02 Jun 2026 10:17:43 GMT  
		Size: 1.4 MB (1392440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:131b46d3365d467cccd6a537abf38bffdc766cfedf44287725abf6d874edd7de`  
		Last Modified: Tue, 02 Jun 2026 10:17:43 GMT  
		Size: 17.2 KB (17176 bytes)  
		MIME: application/vnd.in-toto+json
