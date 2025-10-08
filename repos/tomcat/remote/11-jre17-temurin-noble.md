## `tomcat:11-jre17-temurin-noble`

```console
$ docker pull tomcat@sha256:ad2b5f40b0b03098a69dbb0ffb2eb6a370bcd6a09305f2638cfe106e25f46e89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:11-jre17-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:5fb1709ed4e6b25783446a291df4c1d6f2a0e6278d6471c3da6d9b70410a9722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620c791966084ba3c4b1715deaa06b84688cb85c5171e810a277f7e37db440b7`
-	Default Command: `["catalina.sh","run"]`

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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 20:03:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 20:03:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_VERSION=11.0.12
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_SHA512=85f8cfec9b1cdb9c7484b416c6e00cd7acb89c45e30090563b5d8f9c83c7e734bc9f5d32e110af129c5ea7d11f5632097c3e5230fe027e0219a9b0f52f42efac
# Tue, 07 Oct 2025 20:03:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 20:03:28 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 20:03:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1afecb2aecaac596c3bfe3842e5cdd25fdae298944f8f8f8ce941d10053b14`  
		Last Modified: Thu, 02 Oct 2025 05:02:01 GMT  
		Size: 19.4 MB (19377076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe7cfa1d33eb27662d719b0453a4aa99e985fbbf30d59eea6b585c9125b08f`  
		Last Modified: Thu, 02 Oct 2025 05:02:13 GMT  
		Size: 47.0 MB (46986051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7f66453a1228e751e68d6b59d18bbfa2d2d4d26283f443e024cd9513fce9f6`  
		Last Modified: Thu, 02 Oct 2025 05:02:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97bd3321835cc8bcac72b0a75887070e2671a1d46a4d821b6a8f9c863dd4b29`  
		Last Modified: Thu, 02 Oct 2025 05:02:04 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5581261c6efd8b012d35b624ae678808e07be26af4b534549a6d50b6ca12407`  
		Last Modified: Wed, 08 Oct 2025 00:12:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45caa5f17170859a52713b422abf3727accfd7289b24165bc92bcc71527d9886`  
		Last Modified: Wed, 08 Oct 2025 00:12:25 GMT  
		Size: 14.1 MB (14101064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09becbdb60e24f432ee117ebd8474458b29cb2b0e0177f5e3f3c385db48d6fc`  
		Last Modified: Wed, 08 Oct 2025 00:12:24 GMT  
		Size: 224.8 KB (224776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:475a82f26316a022c7d8ae21763b159d18a8d54420abf5d537846aa76aca9b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31beb29f19ad740c6278637f01e81673078a83d8c3a217462b10c909b12f1893`

```dockerfile
```

-	Layers:
	-	`sha256:c16a67ea10f57c95fcb02147e47ed79b007019148699c17f832b10c37d40f404`  
		Last Modified: Wed, 08 Oct 2025 02:39:06 GMT  
		Size: 3.3 MB (3349604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64932ee631856d47e36a24413c4aa7d56d41f47dfaf897ebdf7b20855a2e309d`  
		Last Modified: Wed, 08 Oct 2025 02:39:07 GMT  
		Size: 24.1 KB (24083 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:1ce2ddc56e30104eb4b80c24ea1cd3cd0309b8535cd408f531176f553f05e91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103870101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ddaf3af7fc59aa9cdf0aacd1b56f167d7724de2a82147c6d4de667b792e595`
-	Default Command: `["catalina.sh","run"]`

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
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 20:03:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 20:03:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_VERSION=11.0.12
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_SHA512=85f8cfec9b1cdb9c7484b416c6e00cd7acb89c45e30090563b5d8f9c83c7e734bc9f5d32e110af129c5ea7d11f5632097c3e5230fe027e0219a9b0f52f42efac
# Tue, 07 Oct 2025 20:03:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 20:03:28 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 20:03:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955e4cac40683ccc18f496e6cd22d3be09393c68232e5a7794fec7918d832a54`  
		Last Modified: Thu, 02 Oct 2025 01:12:58 GMT  
		Size: 18.1 MB (18087070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeca8bbee399b84243dc8d476a8b8090e42f57f8b9d04b1d9ec0553399e729ce`  
		Last Modified: Thu, 02 Oct 2025 01:13:01 GMT  
		Size: 44.7 MB (44656845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1ee78a4d693d77c5255a5cdd32d84f245d1b53b0353e3652325fa97935a903`  
		Last Modified: Thu, 02 Oct 2025 01:12:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386350e06027ee1ed7d235436ec602d1fb4fe4559ada772989aa7b351f5a99ab`  
		Last Modified: Thu, 02 Oct 2025 01:12:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499daddc15fc9c757ff4867c325b8251f302fa211cb9852e3a7bc4cdf63eb4ac`  
		Last Modified: Wed, 08 Oct 2025 00:11:30 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9418b33176ba557766bd46c56f97b372e87d6cd88e94c0faf205488ee779d0`  
		Last Modified: Wed, 08 Oct 2025 00:11:31 GMT  
		Size: 14.1 MB (14075920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab90999b50e44bb5729c795a0499207b5d1a6552c6b9f95b5af228847d2b9d01`  
		Last Modified: Wed, 08 Oct 2025 00:11:31 GMT  
		Size: 196.5 KB (196476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:d56f36ffe4fbc108dfacfe73747c2e10ead07e3f6a96a7bde0f725a878c9dfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb4f4ddc481798e1e77b9bda05b06155e82b29e9e02987a4957fc67daf11db6`

```dockerfile
```

-	Layers:
	-	`sha256:8e371dc625d8c4e37f0ed48a8851efbdec3a146bb5f3cbd872835b6449762c66`  
		Last Modified: Wed, 08 Oct 2025 02:39:12 GMT  
		Size: 3.4 MB (3352008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e37e54af3c88f266f1539d5cd1e3cb1f098c423cb12f0d8c084e15a697a3330`  
		Last Modified: Wed, 08 Oct 2025 02:39:13 GMT  
		Size: 24.3 KB (24276 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:081a5df7f5abd26fdd6981a968dd3f4aeebd4940f06e01e59345bc04cc6e0264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108881669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c219fc015ff1f5ab3faa5301c2771b3889f30a65506a67a468829b179a084c21`
-	Default Command: `["catalina.sh","run"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 20:03:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 20:03:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_VERSION=11.0.12
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_SHA512=85f8cfec9b1cdb9c7484b416c6e00cd7acb89c45e30090563b5d8f9c83c7e734bc9f5d32e110af129c5ea7d11f5632097c3e5230fe027e0219a9b0f52f42efac
# Tue, 07 Oct 2025 20:03:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 20:03:28 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 20:03:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61ea3d0cc515835574128a1f4508ce3cd84046c84f5adfdd31329471a200f56`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 46.5 MB (46481685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b517f5a2189728afd33be6639f2a5e5c4b8aee4303360f7de0b50358dae34`  
		Last Modified: Thu, 02 Oct 2025 01:17:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d1b0ab5bd79a9fc3c444d3bad8851b0a3692b7066fdf6e1f0d7b2e6e709d54`  
		Last Modified: Thu, 02 Oct 2025 01:17:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9c611eef0948eca729762a6300a8fd7d00724db2e89dd8633e1fb9dcac3541`  
		Last Modified: Wed, 08 Oct 2025 00:13:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f858fab0419046f07195c78972598992b5bc2aa2974fa70014b1fcc3bc0229a`  
		Last Modified: Wed, 08 Oct 2025 00:13:06 GMT  
		Size: 14.1 MB (14104008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b76c8a68d01842cd9aef6d2a24ba8dc95b75d115769ebec7ac818c7209301`  
		Last Modified: Wed, 08 Oct 2025 00:13:05 GMT  
		Size: 225.4 KB (225396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:1108e95df288b468a1e3d282252b3ec56f5b034cbaba426a5287c88b297525df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d89e4dcb52039f91ce276314e7e3e6d4762a430770f2e75c2d7a5f56ff4eddc`

```dockerfile
```

-	Layers:
	-	`sha256:a0d8f87fe8087e6832c9ace99e4dc6183649e18c9b5bb2e7e2716fe0661c36cf`  
		Last Modified: Wed, 08 Oct 2025 02:39:18 GMT  
		Size: 3.4 MB (3350172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b019970c577615194a7a96a634cd44c451b1206f5d4ad787c7084ddec4a1fe0`  
		Last Modified: Wed, 08 Oct 2025 02:39:19 GMT  
		Size: 24.3 KB (24340 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:b77351a33a498ec7e610a977a41132c4ffd16143c0c9615d6a57a7edf6887caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116940117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28e864c9faa99a78e5903da51dd76508c05abc5c80759854858c50a205418ef`
-	Default Command: `["catalina.sh","run"]`

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
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 20:03:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 20:03:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_VERSION=11.0.12
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_SHA512=85f8cfec9b1cdb9c7484b416c6e00cd7acb89c45e30090563b5d8f9c83c7e734bc9f5d32e110af129c5ea7d11f5632097c3e5230fe027e0219a9b0f52f42efac
# Tue, 07 Oct 2025 20:03:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 20:03:28 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 20:03:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9acb17607aec02fd5fd93f2fde25243ef3044bcb4e30ef1e561b8b40c746b40`  
		Last Modified: Thu, 02 Oct 2025 01:21:01 GMT  
		Size: 21.4 MB (21437493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b5b51365acd431050e5c9aa8a28fc16968d9ebc74c387a66c020ea8e3de67`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 46.8 MB (46826188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c02052496692df552217e8081affcddb529a5fd7ebba3efc33ece04f21f577`  
		Last Modified: Thu, 02 Oct 2025 01:33:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2ef71696dc21cb9f56e6908c946c107e46b427b97d9068bd3cf79eb1712f48`  
		Last Modified: Thu, 02 Oct 2025 01:33:54 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d8606b061898e406ed16afea3eb2d42569f47030b279a0d23b740705f55bbb`  
		Last Modified: Thu, 02 Oct 2025 13:24:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aeb5bd8e0327fc2d66aa907cb1e331058e781587f6c024b15debe155cb1f367`  
		Last Modified: Wed, 08 Oct 2025 00:25:29 GMT  
		Size: 14.1 MB (14113393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef047a2a941f048ff0386ba630458bbf2b20d6ca8c19418aaa200c83da91a27`  
		Last Modified: Wed, 08 Oct 2025 00:25:28 GMT  
		Size: 256.9 KB (256853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:accd42f15a4b93c65cc658bbf8e37cc8afed5b5a7da1ec43ac7eb48951422a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33be5bb0c30952cf928d1fb7d73e35b401610845048c87e4ad34bfbe1f8b7e1a`

```dockerfile
```

-	Layers:
	-	`sha256:5480b12dbaa218367582ab4fd9b1a6d1b6b4f6fde7f3653d53d056ec08c69a90`  
		Last Modified: Wed, 08 Oct 2025 02:39:24 GMT  
		Size: 3.4 MB (3353729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b65436c25f6933b536b929460cc07de776566ca43833aae5c2df2ddb1dbab365`  
		Last Modified: Wed, 08 Oct 2025 02:39:25 GMT  
		Size: 24.2 KB (24190 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:2281e4747659d4890d40bc5c5a315b79f6bc55347a89b74a0092195289437a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109407804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e4f5cd3d3f0cd59f133f9da24f57e54914e412185a12eb668c7be03fcf0168`
-	Default Command: `["catalina.sh","run"]`

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
ADD file:13e2355f84c9f5f1ba6aa2fa1db4359cbe23312f7b2905fc8b976899a09fdfef in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 20:03:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 20:03:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_VERSION=11.0.12
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_SHA512=85f8cfec9b1cdb9c7484b416c6e00cd7acb89c45e30090563b5d8f9c83c7e734bc9f5d32e110af129c5ea7d11f5632097c3e5230fe027e0219a9b0f52f42efac
# Tue, 07 Oct 2025 20:03:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 20:03:28 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 20:03:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2d699e6bd7ed3cc40f40b8118f763dc4303b0e97b911de163cabf78f19b5d434`  
		Last Modified: Thu, 02 Oct 2025 23:21:18 GMT  
		Size: 31.0 MB (30950446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c968878eef99dc549f1ba1b1045b0f5e0b9fd8a5906a80b6d2dbf8a197890f50`  
		Last Modified: Fri, 03 Oct 2025 19:37:02 GMT  
		Size: 20.0 MB (19973992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6931bbf7f95305f7237a842814ac5d12a641aa1bddf4c8431788f996b345b51c`  
		Last Modified: Fri, 03 Oct 2025 19:37:05 GMT  
		Size: 44.0 MB (43966016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7923ee616005c441d532d5b3960a52aaa36ff1c206df24fba941b142c7eb6`  
		Last Modified: Fri, 03 Oct 2025 19:37:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45031549139eaf4fd579de0e60830fad9d498e504790625816da8e7666ed2137`  
		Last Modified: Fri, 03 Oct 2025 19:37:00 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f4f71bc4adaa56c3f988eeb10f46bca68a67a746c31292eb17144aefcd861d`  
		Last Modified: Tue, 07 Oct 2025 12:38:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf11f3d9f6e9377b30631331f35892fabcfc35ab5dafb8a562974ed517459c`  
		Last Modified: Wed, 08 Oct 2025 13:09:09 GMT  
		Size: 14.3 MB (14286440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a51499869dbed52caafda7a5cfa735dde92abcdfa74a9adc4af28f50784e01`  
		Last Modified: Wed, 08 Oct 2025 13:09:07 GMT  
		Size: 228.3 KB (228268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:04cd58fd4ad5c20649af87705e6e64f1a12861f776c5a87867a0ed52e9a3d23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3365921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa846f170f7280ed7d3e2ed2ff6bbe2590dfd5b4acfd3b02ae8d60f00ec966f`

```dockerfile
```

-	Layers:
	-	`sha256:4186b1be4347bb0777fe45b43a49bb7f1bdd9fcb68f5d7376dc224afb939a3d8`  
		Last Modified: Wed, 08 Oct 2025 14:31:14 GMT  
		Size: 3.3 MB (3341731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfd2934dc55339159ff02fcc39d4db47cc332f3f9141463d96276d4f064a618`  
		Last Modified: Wed, 08 Oct 2025 14:31:15 GMT  
		Size: 24.2 KB (24190 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:6357f5451ca728b1f62bfbab781b0363918632964c9cfbd318b96ab897e75b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107901729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6379e87936c22f1bdf7090e966d6a96e7b350aab72794cddaa9a780894f1031`
-	Default Command: `["catalina.sh","run"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 20:03:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 20:03:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_VERSION=11.0.12
# Tue, 07 Oct 2025 20:03:28 GMT
ENV TOMCAT_SHA512=85f8cfec9b1cdb9c7484b416c6e00cd7acb89c45e30090563b5d8f9c83c7e734bc9f5d32e110af129c5ea7d11f5632097c3e5230fe027e0219a9b0f52f42efac
# Tue, 07 Oct 2025 20:03:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 20:03:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 20:03:28 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 20:03:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e9a7df0c6e08fd0434347bd07ecdade7cc5d006c086084ec4347cd24546ee1a5`  
		Last Modified: Tue, 30 Sep 2025 17:14:38 GMT  
		Size: 29.9 MB (29906146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaa0051061f5de859a26823f4e2384fefb5551991c28fdc8246e7416429647e`  
		Last Modified: Thu, 02 Oct 2025 01:16:00 GMT  
		Size: 19.7 MB (19677624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9563c759967dcdb735c9735ab336d95dbd967e023ad1427910faa2a93900328`  
		Last Modified: Thu, 02 Oct 2025 01:21:01 GMT  
		Size: 44.0 MB (43974092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7f018e7da616beeb3b2f899dc20b638d9a691c197c3cb62324bd917d951ee1`  
		Last Modified: Thu, 02 Oct 2025 01:20:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a825f36c7a20161f0806405c387b048e1654349e70b725c3ec443dc8c8a3fe7e`  
		Last Modified: Thu, 02 Oct 2025 01:20:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9086df3894acf2d171ac2bf0a8a36015f353e3e2d61f67ef9b76faad90e5d43`  
		Last Modified: Thu, 02 Oct 2025 05:37:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b639facf154d54bf70e1e73bf938e21a3a0d7e5a0f26da8616646ad5bbd594`  
		Last Modified: Wed, 08 Oct 2025 00:12:32 GMT  
		Size: 14.1 MB (14108391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf54e97b7c006478a32e48635ff91cb78b4ee6dd6e5713c93c8f967c4685e92b`  
		Last Modified: Wed, 08 Oct 2025 00:12:16 GMT  
		Size: 232.8 KB (232833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:9a49a62e9ca0ee905a9b0f41f5cd8f06ce537493243e55cb9350f3a5814b2fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3375887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a1eda35ebea5a8fc2c0b913241de6628689e43ef33a043a3d0777ceff1ebdd`

```dockerfile
```

-	Layers:
	-	`sha256:b827ddec71c27e76ea77f3cf7ca41aefb02debca7ffaa5fe025cf804fb103651`  
		Last Modified: Wed, 08 Oct 2025 02:39:33 GMT  
		Size: 3.4 MB (3351803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce3126ed88f320a1e95b548231e88ee92d4d8c3bb7aafcf1ab04a8f652e59cab`  
		Last Modified: Wed, 08 Oct 2025 02:39:33 GMT  
		Size: 24.1 KB (24084 bytes)  
		MIME: application/vnd.in-toto+json
