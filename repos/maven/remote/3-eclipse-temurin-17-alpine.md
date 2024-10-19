## `maven:3-eclipse-temurin-17-alpine`

```console
$ docker pull maven@sha256:78eacfe227ed08d5a019051508482f220caaf4d2508e2469c3b9c8db0d258a4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:2154dfbe37742542527e11e181fbfc7bdfcfd367e996e3cbca0e01831272d23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175485819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36af46afc7c4f906aeb8efc422777826a95706ecb530534137f567076875d5fc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3ba0c79b665a51306cdf9ebd9321ad95c566194f795f39eaf4506b0ef10344`  
		Last Modified: Sat, 19 Oct 2024 00:55:14 GMT  
		Size: 14.0 MB (14032613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2782f0e27146317affcb7ab3b70fcb40051fd269dde22bee474569cd898fabb4`  
		Last Modified: Sat, 19 Oct 2024 00:55:17 GMT  
		Size: 144.4 MB (144395059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f384070c28627cbabe986d12be40f60f9e53420470e8441c5c4b417b52d029`  
		Last Modified: Sat, 19 Oct 2024 00:55:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8268bcec589870bc9c092f2cad1f0dae2cab90a0513e18184854c53b3e43ee18`  
		Last Modified: Sat, 19 Oct 2024 00:55:13 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b75bbfffbffc8a710955e8377176e80557d82171025a397f2cca45dd2caa4cb`  
		Last Modified: Sat, 19 Oct 2024 04:07:00 GMT  
		Size: 4.3 MB (4260639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7323e5373f86137f81a302bb3123e45f2c3771a941eee8a0e21fdedda2dc87`  
		Last Modified: Sat, 19 Oct 2024 04:07:00 GMT  
		Size: 9.2 MB (9170422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f0091360d69a6f95bc4743a30db3ab9b0b412170f454f7e167119bdc2d28c5`  
		Last Modified: Sat, 19 Oct 2024 04:07:00 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6192670104cf153d6f0d92e43e8fd4d0c04d40a95a66270a556e33978c53f2`  
		Last Modified: Sat, 19 Oct 2024 04:07:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:600301d6d7fee47a3271c31375551aef717dda9268faf524d5d81e772f8ff1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1147771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12cea2386fb4f2790491e8dd05f5a8a664f6a26dcfd9f732a4a5b9c5ea03899`

```dockerfile
```

-	Layers:
	-	`sha256:9b7e65797e26b2c627ee87a9e6288a07bd53b48c5f9c4071f9ada9bad73eac20`  
		Last Modified: Sat, 19 Oct 2024 04:07:00 GMT  
		Size: 1.1 MB (1128388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f212f2388485bf24f670aafeeca0baa7238cb096aab504f1038b6f89f332ce`  
		Last Modified: Sat, 19 Oct 2024 04:07:00 GMT  
		Size: 19.4 KB (19383 bytes)  
		MIME: application/vnd.in-toto+json
