## `maven:3-eclipse-temurin-23-alpine`

```console
$ docker pull maven@sha256:2b8768b5d5d48024d25102948ca27aa124eb617a4f2e45b73742a246fadb267d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-23-alpine` - linux; amd64

```console
$ docker pull maven@sha256:092afa0aa4890d0f0869a996ddb9e4cd58809ca4c6d1c2dd2e88e9155886cfcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202650530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25431fa1fe5a9b136aaba05423c75fc7936481ff6fad8b2b688d0d4935182f49`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Sep 2024 17:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b55c5c881a2fed17ec5a59feaa33d9263703b399d1bfae3a5eaed3f140aa4570';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='2c05c6dfea23a83fdbfaf5b03cc3cfd8d998c8069e930e0e585a39d4a99f3d99';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3606bfc1ff94989733a3efb303d50016e471489b714ed7daf1ae0490f80b52`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 20.9 MB (20908716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02e9501475e83106c0e84ddee25cd2eac588c2e8f0420fbdcdf0d6f8fc1f694`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 165.5 MB (165542611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9e4bebda8fa04819d9e8f002171cb240080cb024c4413c6d8313d5da284bba`  
		Last Modified: Fri, 31 Jan 2025 01:30:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b0c9453479824b697beefdd4f4a6e47fc09a3d0e65f2b8b1bc732ffb696fd`  
		Last Modified: Fri, 31 Jan 2025 01:30:45 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a279ea18891f2c1c04e50df12b9af8fdcd41a257d1e89b5ec0f0a873b3f80f`  
		Last Modified: Tue, 04 Feb 2025 06:14:43 GMT  
		Size: 3.4 MB (3383610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8f59a0fa405b989be26390659df59316cc2674f1dfeafcd27939e4a2db5bb7`  
		Last Modified: Tue, 04 Feb 2025 06:14:44 GMT  
		Size: 9.2 MB (9170423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbccf1a4a53fc4255a4f963392f1ac3b0b244e9b8097da8a0c211e3b79abfa8`  
		Last Modified: Tue, 04 Feb 2025 06:14:43 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2053ad7f433e7916f4245ac16410a417bf4e04c148da3bec87a4c7d928b2f307`  
		Last Modified: Tue, 04 Feb 2025 06:14:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:979293aa79705f499f6a0a5a3740c718077e733670b35098d17f7ee68edbdccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1247338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d7f3ca06a52ee6fc524e86d22f0a5be387f59bec7de38a78fc24cb9ec95bbd`

```dockerfile
```

-	Layers:
	-	`sha256:7e5e45cde6e8f2da23e9325722e901abbce1c436f661455fc668ed06c10a942e`  
		Last Modified: Tue, 04 Feb 2025 06:14:43 GMT  
		Size: 1.2 MB (1227957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea596d3a05c59380f6fb66bb94032a61a88f2f7ec759fe2224271a736a35811`  
		Last Modified: Tue, 04 Feb 2025 06:14:43 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ff30fd04fa6e6a0c7c68f9f6c0cacfd91d4a403b674e9164a7a0b8a7cc64a37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (200952726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c49f7aed5b461d8a0f2ce7dfbe04d7f6c5da60ec356fce318fa2d0dcbd19fef`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Sep 2024 17:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b55c5c881a2fed17ec5a59feaa33d9263703b399d1bfae3a5eaed3f140aa4570';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='2c05c6dfea23a83fdbfaf5b03cc3cfd8d998c8069e930e0e585a39d4a99f3d99';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceae889eece3aa36cf341c7932ef99f4d89a493af360439046e550e71531cbc`  
		Last Modified: Wed, 22 Jan 2025 21:08:48 GMT  
		Size: 21.0 MB (20965085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ac014d0f23ca2bf7377d7b0924fc88363caa8aa3626caf271f03e078df59e`  
		Last Modified: Fri, 31 Jan 2025 01:51:12 GMT  
		Size: 163.4 MB (163380016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7683d41d19879a68bb63398afd385926f8ee1656682373247b65fcd1a1a04b78`  
		Last Modified: Fri, 31 Jan 2025 01:51:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9b0efb10bf6ee2483a1d96b2fd983feb86d4f57ab99b2839d4241bf159e4d`  
		Last Modified: Fri, 31 Jan 2025 01:51:08 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c6720e50a2845e966af53408c20d5a7f9e84cc47f43e101362762816084f47`  
		Last Modified: Fri, 31 Jan 2025 06:33:32 GMT  
		Size: 3.4 MB (3441368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531edadbbbcd9c9d7422c63f041021b4093b2904f9b3aa951d55302895306e01`  
		Last Modified: Fri, 31 Jan 2025 06:33:32 GMT  
		Size: 9.2 MB (9170444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c655be6f6357de67e781682dbc5c3d87a4fa4d8569731552bf29e78f0ccd382`  
		Last Modified: Fri, 31 Jan 2025 06:33:31 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfb09fb87a2c7c3c67d23a89fabf66988232731c85ff5ed03c310dfb4f848a9`  
		Last Modified: Fri, 31 Jan 2025 06:33:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:fbf57d6253505c509ee2416d942536f0354bd871a4cd3a864beb1e9a5b851ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1396852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd83680155564bb85f61b82840d4f1c08bc4066b1fe92e62567acb17dd20d2`

```dockerfile
```

-	Layers:
	-	`sha256:f7f28f72434fa009cef8658650aca37b03bb80666ff2ece1aff3a3e6427d913a`  
		Last Modified: Fri, 31 Jan 2025 06:33:32 GMT  
		Size: 1.4 MB (1377338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe869e04f2950d97172b64a74812058df50f2609c4434ce1630b043c613e1df`  
		Last Modified: Fri, 31 Jan 2025 06:33:31 GMT  
		Size: 19.5 KB (19514 bytes)  
		MIME: application/vnd.in-toto+json
