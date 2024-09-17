## `maven:3-eclipse-temurin-22-jammy`

```console
$ docker pull maven@sha256:c2e8197a332d5ab41a8868acb39bdd804cb91bcedd1a47c719f6fce27d04e247
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-eclipse-temurin-22-jammy` - linux; amd64

```console
$ docker pull maven@sha256:107c57493f423a60205995b7b2bf93422111f864a4eb40d3cb35457d71dc373a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233852083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54df993d51835093019afe7994733ef46df9d78454a7895c4fef3d38d5afea8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ARG RELEASE
# Mon, 19 Aug 2024 08:57:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["/bin/bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 08:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e53473ef89c58a3ae8cab2f73437d003f9bd9664351171fba498eee3ed8aa3`  
		Last Modified: Tue, 17 Sep 2024 01:12:07 GMT  
		Size: 16.3 MB (16312687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81647d96d9af9b8fe31faa2e76281f07d155fb82419ae9bcb245fbbb56342fbd`  
		Last Modified: Tue, 17 Sep 2024 01:12:17 GMT  
		Size: 156.5 MB (156487244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25400d7d5a29a60391c05ebf0e850556d3581cafb9875293e74b320c5752a4c2`  
		Last Modified: Tue, 17 Sep 2024 01:12:04 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015152ee7f7239c7531d32771b0221257b9272ce32bb356f86399dd7f1bfe0cd`  
		Last Modified: Tue, 17 Sep 2024 01:12:04 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8991c1767c10cc59f7ffa0073683e65f67808f2f5bb6f7379de8d34fe49780`  
		Last Modified: Tue, 17 Sep 2024 03:02:35 GMT  
		Size: 21.4 MB (21438484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edceff601bf44f13b47200a78c263f13248144830f10a46235d2dde72879cf5d`  
		Last Modified: Tue, 17 Sep 2024 03:02:35 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc2387185aabf750ecec1ad8893246773c22d32a9d4d5c47e23da4f4a4b04a`  
		Last Modified: Tue, 17 Sep 2024 03:02:35 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1495c08f562c45300d18b80232a0c33bc0d1a0f645599173034017275993654`  
		Last Modified: Tue, 17 Sep 2024 03:02:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:bfa71cadbbc8b443e99319567cbceddec16bbbb799ab0f4e536758cd7844dd1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b10a0ce752820eff6a3686d53fb00c771621dcfc1ea1924f0f20f96b47769c`

```dockerfile
```

-	Layers:
	-	`sha256:cc573b8839c72156747f97f7a63516bfd82f8a6e9b0e4423ed53fb1c849ee93d`  
		Last Modified: Tue, 17 Sep 2024 03:02:35 GMT  
		Size: 5.1 MB (5118477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8a9d54b66782f91d6a826044377aa99234e3a1a9f160e6e6b1ad0b07591c98`  
		Last Modified: Tue, 17 Sep 2024 03:02:35 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-22-jammy` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d415138d0d778761abf496675a0e67e76b671920f5d66f74ea48553a9ece9596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231186849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79be6ceb7383badbfdc869eb90dd5d3c2b2cff2850aff1372b2aa27d462c6a2a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ARG RELEASE
# Mon, 19 Aug 2024 08:57:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["/bin/bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 08:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4dfb29f3dec7dad83e608bb6b033555afdaabce186fd1d41817283d4beca74`  
		Last Modified: Tue, 17 Sep 2024 01:41:38 GMT  
		Size: 17.7 MB (17721887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6edbebfb17969d8acf2127f8daa9b18091108ad969772f1397288490d96adfb`  
		Last Modified: Tue, 17 Sep 2024 01:41:46 GMT  
		Size: 154.5 MB (154501023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6db0701159875940b6ee4743e7ddd59448a6b16404d592a91e9f53a118928e`  
		Last Modified: Tue, 17 Sep 2024 01:41:35 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581ecec97f552364809f52639eaef8bd8729ee0bc4c917c0991c17c33e5f3db7`  
		Last Modified: Tue, 17 Sep 2024 01:41:35 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51ba9f6201bf9a29f67eb7bea66bd69876cb8668a8a12d131e046eaa1bcfc43`  
		Last Modified: Tue, 17 Sep 2024 09:37:01 GMT  
		Size: 21.4 MB (21393111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e5914bed744299fad99725a4345e1762e6c350b10022ae2f321c876048ca5b`  
		Last Modified: Tue, 17 Sep 2024 09:37:01 GMT  
		Size: 9.2 MB (9170431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e09ea9addfa3f45d7a3a7fec2e6b2398c47a751bd67bd48b747e05f093339e9`  
		Last Modified: Tue, 17 Sep 2024 09:37:00 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd02516f068a91f49954778b119f0fed3f1be954d1e6b1f9458238fe29ddc78`  
		Last Modified: Tue, 17 Sep 2024 09:37:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:d50fe480af81b4fd0421ac81b5ef964fa61bc3b24800de8653ad6a955c8c042b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5241028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383832e4057495d85b9d213c0b2f9d2978b8e02862de02f33ec380be533c42b9`

```dockerfile
```

-	Layers:
	-	`sha256:ba2ee1a976d20f3076267bfe627015ebcdda337c28eb4c9a1fa905974c1b448d`  
		Last Modified: Tue, 17 Sep 2024 09:37:01 GMT  
		Size: 5.2 MB (5220725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f6b00da700083d0f818b9b87fb4e8582856d19d36616c77ff8212b70ef8a5a`  
		Last Modified: Tue, 17 Sep 2024 09:37:01 GMT  
		Size: 20.3 KB (20303 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-22-jammy` - linux; ppc64le

```console
$ docker pull maven@sha256:4a02a89888bc4ed8c48e570c7d0bed368527469b4dcdc38a8e91c807a9192dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243785336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8cfbbb801039481376ff0600dfd8f29395b024377478de874883b00d697966`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ARG RELEASE
# Mon, 19 Aug 2024 08:57:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["/bin/bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 08:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1964e43dd3e3012d81a12dd72d3bcf1a25d7b6d254e81c159107d36b06f8460d`  
		Last Modified: Tue, 17 Sep 2024 01:11:07 GMT  
		Size: 17.3 MB (17277948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b2cfe588f70ef7a83be4faa4ea62a25c49aacec1f7fb28dab9dd7a5f45161e`  
		Last Modified: Tue, 17 Sep 2024 01:11:18 GMT  
		Size: 156.5 MB (156469903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677fb5a0acecf580ad7790ad6db9a8b6706e3cfe060b7dd431d7cdf844219300`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5fac14e568fd8af3501aa8ddb3bf59b2856cb17c886e5e3ddad47a027b5b20`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7559f22acdf8184c4aa3f4bd126eece838e348b38c6b7ac4877c15145ae36e`  
		Last Modified: Tue, 17 Sep 2024 09:28:05 GMT  
		Size: 25.3 MB (25278276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595f291fcde4f9f2f069567286e7053da725ebb6161c6626e1da6cfafd4d522e`  
		Last Modified: Tue, 17 Sep 2024 09:28:04 GMT  
		Size: 9.2 MB (9170426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e924205803960c48ec9b7c1d2a9e2a569ea669a144a65f27700acbf18f7ee6b`  
		Last Modified: Tue, 17 Sep 2024 09:28:04 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bba21b21f8670d5052033dcc7a15d674be069a97618425e0e6cc363ca6848da`  
		Last Modified: Tue, 17 Sep 2024 09:28:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:7048f056b2431c02bfcc2d04f890c1362f76d9cfcc7ae5ae05243c106286d562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dc09e2073d579c5492e18bbea0bc96195d655d1dbea3b00dbf683ea67b01f1`

```dockerfile
```

-	Layers:
	-	`sha256:81330dca738fb693b8763a16b8290e3b7f1c3092a2f19c31d74eff80295cc0f3`  
		Last Modified: Tue, 17 Sep 2024 09:28:04 GMT  
		Size: 5.2 MB (5151121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31da65e4f3c14688f775fd4123c69c17de8756ee479e4921a1771ef53fcd0bb`  
		Last Modified: Tue, 17 Sep 2024 09:28:03 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-22-jammy` - linux; s390x

```console
$ docker pull maven@sha256:f512dfbefa8f9c24b76d0bf92bb964af5dd3caf06bb33def28bf669a39177f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221083637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de48baa01fe76e5a45b9e345dfbeac68a1789cc83073deeb8766d48eb67778d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ARG RELEASE
# Mon, 19 Aug 2024 08:57:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["/bin/bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 08:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512728d648d250a98524685ed3996dcd0d405068bd3bdf4937e1915d7d8e7019`  
		Last Modified: Tue, 17 Sep 2024 01:41:45 GMT  
		Size: 16.1 MB (16124414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d61c675d2a4217fa18b2044c89f4c0f144bf514c5f00a13cd2edbd2ce1958f`  
		Last Modified: Tue, 17 Sep 2024 01:41:59 GMT  
		Size: 145.6 MB (145550026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7b94dbdfc54d031ac4aad906368a10a45c65e1159f35100e30ab9e7a8643a9`  
		Last Modified: Tue, 17 Sep 2024 01:41:43 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e84b35b60390aa3a617f8c84fdb1ca91d68b3cf1c366776ed30bf9ca8eca701`  
		Last Modified: Tue, 17 Sep 2024 01:41:43 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347e99f2ee512a3aefe52bea63a808aa8f8fad0201affe84a802e651f5b1abe5`  
		Last Modified: Tue, 17 Sep 2024 06:13:31 GMT  
		Size: 21.6 MB (21596197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f765d69f5a37e532dd9afa0156f04c53d96fd141a788461139fa5e03574df673`  
		Last Modified: Tue, 17 Sep 2024 06:13:30 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cfc02fe9cb128529ae89bd7625121a101646aa257aa3c37edbd84d15f88e77`  
		Last Modified: Tue, 17 Sep 2024 06:13:30 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aa9fcec133cf4d3bd42d48ff18ffe54881eb0192063edcfd2705b69b2db8`  
		Last Modified: Tue, 17 Sep 2024 06:13:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:f2c8157505a1cf3a5c9a373b293c4d3f27220770bca37435f5735373117441aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5065777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18283cb2e0fa17ef783dc3c8d5469c5c8a1c67b793b954a0a1b05448f6ff8969`

```dockerfile
```

-	Layers:
	-	`sha256:81b386e5a00c573d83f2401f763ce282b26fe7c538a3d416258db003d073cb3d`  
		Last Modified: Tue, 17 Sep 2024 06:13:30 GMT  
		Size: 5.0 MB (5046102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece61be0d24e6b76323a1e04331a01679f8b4cc4a36eea705b1ac948bbe8ef61`  
		Last Modified: Tue, 17 Sep 2024 06:13:30 GMT  
		Size: 19.7 KB (19675 bytes)  
		MIME: application/vnd.in-toto+json
