## `maven:3-eclipse-temurin-21-noble`

```console
$ docker pull maven@sha256:5d6a18b40b2dc48c2182f9593968f96d8eefc50fc2ebf4671a10ca898dfcad1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-eclipse-temurin-21-noble` - linux; amd64

```console
$ docker pull maven@sha256:486d196b0422fee4f8508e032321bf4c8f27f607b138278a3ceb758117e17219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242277823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7425a5f22f74e623cf4c80e0bdb753c58b1e7a2888efb4b95dfb98fd9d9f5bcb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9020b2985154ebec2e5c41f920cdec5c883d205708c665845a35e46dde13f95`  
		Last Modified: Mon, 15 Sep 2025 22:14:43 GMT  
		Size: 23.0 MB (22958669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb527ddfa98902e1fba0b7248248e722d817019355ef80708d963ebf829ec568`  
		Last Modified: Mon, 15 Sep 2025 23:13:33 GMT  
		Size: 157.8 MB (157809527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2d782ae30b18df0053991978bd0e30982aa4009af2766a228c3cd40be32e77`  
		Last Modified: Mon, 15 Sep 2025 22:14:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed5e853e5b0022b9f4b01830885f97148d5d67a34f2e15c2875b689cd40b24`  
		Last Modified: Mon, 15 Sep 2025 22:14:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29031814c9fcb674cb1ec1cd820b73452f0a61d52dbaa7ad498196f17527ffa4`  
		Last Modified: Tue, 16 Sep 2025 00:15:40 GMT  
		Size: 22.5 MB (22540128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c390f6145cf0c2d474818f2301430b50d568f389306c8427064e62a2a999d206`  
		Last Modified: Tue, 16 Sep 2025 00:15:38 GMT  
		Size: 9.2 MB (9242573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86c7b15c961906bc13debc7b85c6c2a020d28bfec37608ceb240d858cfe1f3c`  
		Last Modified: Tue, 16 Sep 2025 00:15:37 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8caf989c97465756b778381417e378b4adcc2e05066a5b999f32f4ab8d301`  
		Last Modified: Tue, 16 Sep 2025 00:15:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:b1517292e54a4987968d49d9dd930dd650224c97acdc65082899d64847e16fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86ac25d6ffb2cca39b26b458fdbf346fabca567edbf26cf262961c5c708423a`

```dockerfile
```

-	Layers:
	-	`sha256:a4879a486b6292227ecf2cb3feb1d2a78093826fcb351ef4b6756449ac7c3bd2`  
		Last Modified: Tue, 16 Sep 2025 02:27:30 GMT  
		Size: 5.1 MB (5050291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323401ed085ad1984533ebda22528457bfc5cdb72f310293e95b0ec4307b2393`  
		Last Modified: Tue, 16 Sep 2025 02:27:30 GMT  
		Size: 23.2 KB (23179 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1c45047ae7889860da63f9d9d2f6a1e0ef47542ceffb20dcd883559075c9941c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243186554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88523fd847bb771a6bbeadccae14354d210b967dc2cefe458543c1b1ead00a98`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cd1740b29a5bb965ebb362bfb8d273dc9ba0f240ef68128f6ee02e84055a59`  
		Last Modified: Thu, 02 Oct 2025 01:18:10 GMT  
		Size: 26.4 MB (26381127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87f5f2a70a6cc171bf13205e2f9ce69940ba801a37ad35586f19a70d6286dc4`  
		Last Modified: Thu, 02 Oct 2025 02:16:23 GMT  
		Size: 156.1 MB (156088889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8f449d79922c0e36a628bbf672eafe17ba16c521ab5b44f8263538d0c4c02`  
		Last Modified: Thu, 02 Oct 2025 01:18:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60f137ec45d90fce573239a76d125d8413c048b7f55120aa69b39a695fe2e0`  
		Last Modified: Thu, 02 Oct 2025 01:18:09 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730bf961566aca145b6dc6e88df6ab310332a0309dc84d61faf82b646ed9b789`  
		Last Modified: Thu, 02 Oct 2025 03:26:12 GMT  
		Size: 22.6 MB (22608909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8647d5e187b4341be4c97251e6b4faf92db061d65a03ca7ff46b898fdb03e155`  
		Last Modified: Thu, 02 Oct 2025 03:26:11 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2487c5d47331ea838f7d26fe56ef19eab9b93a338d805b09eeb651b3f282a204`  
		Last Modified: Thu, 02 Oct 2025 03:26:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875b3014fd7d50f601812238b4fa16776ba18065439bd9c48a1e10fd4eab8d98`  
		Last Modified: Thu, 02 Oct 2025 03:26:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:72c308e40219f3382cd2843a12bf615cd9cd7e18b492fc17dff45193f4255366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c478da3ca49eaa92f8ca7b6e4ede5366aecc27a00e50bb93e90dc882b57998`

```dockerfile
```

-	Layers:
	-	`sha256:e72094e57837c48d350f321ad08ce1da2afe3419a2bdc5c4d7499da9450b7697`  
		Last Modified: Thu, 02 Oct 2025 05:30:42 GMT  
		Size: 5.2 MB (5185438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff9c2bd178348cdb566ed5d194365c05036d2cf50f761ce62992a9cb457a834`  
		Last Modified: Thu, 02 Oct 2025 05:30:44 GMT  
		Size: 20.9 KB (20897 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:59079fa87e8ee594293fcd6d2c1e1a4143ce92179b1d72812f5f9014c69a7cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252209253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c7509d637aca7f47dd22396b910b6817146951a1a82773ec55a7ec411af6f6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51c0d56abd1175ca1d077b190f670b7bf37d8534c47076746ea522b8dee24df`  
		Last Modified: Mon, 15 Sep 2025 22:18:00 GMT  
		Size: 24.1 MB (24101619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae423e12727408d7fc4535f074c449c2d878c3f98492dac2bff0570d2264f6`  
		Last Modified: Tue, 16 Sep 2025 00:37:48 GMT  
		Size: 158.0 MB (157969921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb13022736037a0563430d6f7bad8c7860cd0ce6fb6d8376dc8ccafc4cb8863f`  
		Last Modified: Mon, 15 Sep 2025 22:20:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc9e9e5ce3ce07a122afd1768e503d301074f9ef219a8da3ea7ca6adeac19d2`  
		Last Modified: Mon, 15 Sep 2025 22:20:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350ef79b8091d4c458d3c92a4884b2ca5c938c430dd79639d71ac78741c6168`  
		Last Modified: Tue, 16 Sep 2025 02:12:37 GMT  
		Size: 26.6 MB (26588514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd41c750d277e78876e8da6550f78547573088c666703d50f26a36e9ceb03b9`  
		Last Modified: Tue, 16 Sep 2025 02:12:35 GMT  
		Size: 9.2 MB (9242590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd189efffacfaa4d19bbdad5b631209205f6c8439e15705905c65a1a0b2fb91`  
		Last Modified: Tue, 16 Sep 2025 02:12:34 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6943ea27a97d477b228596a07785bfcfe0db0978f98aeb8c75dbcda6ec1af`  
		Last Modified: Tue, 16 Sep 2025 02:12:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:5d1b610ba4c47669ae34b81f22c0d9ce1875fc232145e042b9e09bebd759fa72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cd120b7529ca965eaf2fbd025f8124c50ea69068f84bdff0f2550471a280c8`

```dockerfile
```

-	Layers:
	-	`sha256:872b2702fe4484852ae6e76f9cb848f136145bbdbb16fdd3f5a5ad5fdea7c51f`  
		Last Modified: Tue, 16 Sep 2025 05:27:27 GMT  
		Size: 5.1 MB (5100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6624cc57d1d0b9c531203bb95d2d935dcac0e327486166ed43dc55149a2aca95`  
		Last Modified: Tue, 16 Sep 2025 05:27:27 GMT  
		Size: 23.3 KB (23294 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-noble` - linux; riscv64

```console
$ docker pull maven@sha256:afbca2c158120e2f677e4bbb9a75c8d2ae1d6e44e1866c0dfbc568db206abb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244939912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337bace42bba31edeb8fb364ae61dfa329f98ee1439ecf6d578aa7ab4af9f3d0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:58fbc6777cd47d1e58396e2c0f70255ae3bd63d0ac2ea2138ed6e5e91fdd70b1 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fc46b4719a7bc0e446bd2b472a339bdca3990f164daf9dde3e710206f93383d0`  
		Last Modified: Tue, 16 Sep 2025 19:54:09 GMT  
		Size: 31.0 MB (30950703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add0c28d8e21526293bbfc5a04d12064aeafc4d50cbb223859aaa9b4d12efacf`  
		Last Modified: Wed, 17 Sep 2025 10:24:00 GMT  
		Size: 20.1 MB (20142104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f9ff589b4a753a6114b8496c5e8251cd8ce2e8030c94f145ff7df99e802b8`  
		Last Modified: Wed, 17 Sep 2025 12:24:46 GMT  
		Size: 153.6 MB (153602016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e8c2ebd955fec18cbf4c55cdf05515d6ff4da193542e79176122f5233637e`  
		Last Modified: Wed, 17 Sep 2025 11:16:16 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac7adc1bacefb47458cc259427344b18ae91705f1ec9ff58e5d0fa0e145002`  
		Last Modified: Wed, 17 Sep 2025 11:16:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c95a81f5589b6eff8ffd44f0058b77c6d8e6c994f54cd7300242d5393b994c9`  
		Last Modified: Wed, 17 Sep 2025 22:36:58 GMT  
		Size: 31.0 MB (30999020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5777fc6dbbdbef91ddf12b2df7e77df6d0382fdbec4c972e24528e25d5c69a98`  
		Last Modified: Wed, 17 Sep 2025 22:36:52 GMT  
		Size: 9.2 MB (9242589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aeb5e7017e0cdbe97c37046d67c27770d620602ba2027de4eeb02731f866a5`  
		Last Modified: Wed, 17 Sep 2025 22:36:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e564954b92a750aa95dc84cc6452978f5787b264dd97738da9ac5efae57fe02`  
		Last Modified: Wed, 17 Sep 2025 22:36:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:1e11d8c6e5e656b6b5447e73c20df3ad26fa22b2ff55ee0bfd6ae76f0af1e34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5177274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9f1842f1c26bdcc90e11bbe744571986d477b3e12cda614d77ade499a78470`

```dockerfile
```

-	Layers:
	-	`sha256:5bcb36fe0c52efea85498cbfe6d1786893923a0dc0487ae6e6c80f6c1d01b03c`  
		Last Modified: Wed, 17 Sep 2025 23:27:31 GMT  
		Size: 5.2 MB (5153979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117f73b3a4e4eed3768cfe20579ddd3d2d8149d25fdba820aabf6ddb7f7d3f4d`  
		Last Modified: Wed, 17 Sep 2025 23:27:31 GMT  
		Size: 23.3 KB (23295 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-noble` - linux; s390x

```console
$ docker pull maven@sha256:bda67fac79428428c19a763c684fee15291907854ddf6a7f78c79a5f3a3b4bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234076048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96372dea720b0406ddf77bd479bac11c65413ebc32b66a404c44a6224e104d4a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:2df9e8bc7cd2e879b1bb1d4b43960e570cf8bf039e9c92e1b3599d2ec12b6674 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e9a7df0c6e08fd0434347bd07ecdade7cc5d006c086084ec4347cd24546ee1a5`  
		Last Modified: Tue, 30 Sep 2025 17:14:38 GMT  
		Size: 29.9 MB (29906146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f1ea5eb9d14ef06f0cad2dcc418983b1d2acd6ca3029f7a01fc109101a9d6`  
		Last Modified: Thu, 02 Oct 2025 01:19:24 GMT  
		Size: 24.2 MB (24220728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c6a0766709bc31cefe29b80a7f09346109d432f51c71489cdb1ab318e50d9`  
		Last Modified: Thu, 02 Oct 2025 03:24:04 GMT  
		Size: 147.0 MB (147036898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a76c746ae3f881f3fb95536e2f8bcbbd582d5aacb6e3e508837141d34d3c69`  
		Last Modified: Thu, 02 Oct 2025 01:23:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcb6425191eb8b19dcb31595aa98f456ab0858d86211620fce9aac3a5de11c9`  
		Last Modified: Thu, 02 Oct 2025 01:23:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8176ed251db6187e449fe9f07577eeef41b72d8ff2d8ede1520d46bd7dd5125b`  
		Last Modified: Thu, 02 Oct 2025 07:59:02 GMT  
		Size: 23.7 MB (23666216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c917a0dd3c8818e6836a8fae40cbe8eda3c0b04225019815e45fefca21f5118`  
		Last Modified: Thu, 02 Oct 2025 07:59:01 GMT  
		Size: 9.2 MB (9242582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c326581e862d12440b11d615e3af391b6cc9ca431fd121982285241885867835`  
		Last Modified: Thu, 02 Oct 2025 07:59:00 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082a461b9b5413c7948e01ba33cb7fb981c9ea72b84392e02c4ec83305fb9477`  
		Last Modified: Thu, 02 Oct 2025 07:59:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:ae6456e74ed6fdba26d2dc85d3e53cfd7cc39db2f1d1dcdb82dc610b23eee1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb09dfd651742d0e32a381aafa1e58691a4ad9f780d492379c073b7c2cb2f9`

```dockerfile
```

-	Layers:
	-	`sha256:86817929f55eb109250406d0abe7c124d54c03c1d798d2ecd351e2da03f3e88a`  
		Last Modified: Thu, 02 Oct 2025 08:28:34 GMT  
		Size: 5.0 MB (4993243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fcc6cfbd738b163716606cbb829b13db0254b6a16bb19dae4a6490e8f1930d5`  
		Last Modified: Thu, 02 Oct 2025 08:28:34 GMT  
		Size: 20.7 KB (20729 bytes)  
		MIME: application/vnd.in-toto+json
