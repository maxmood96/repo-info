## `tomcat:11-jre25-temurin-noble`

```console
$ docker pull tomcat@sha256:716fc3c343c39814caf6670f8b209e88249232a3a60cf7e68c74df903ac6e0e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:11-jre25-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:6663ceacd0c73f3ea20f8fad3dde9f64eb16ddaa7feb7d38cfc5c34e7b518d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124320958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c39fbe573fededfbd755a58b91f5cbdf3eec569d03b08e081651499dd95e27d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3ec1d5906104fb273821a5865235b673fcd2b55674c5aee68d15b429fdc7837c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 26 Sep 2025 16:59:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Sep 2025 16:59:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 16:59:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Sep 2025 16:59:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_MAJOR=11
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_VERSION=11.0.11
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_SHA512=a26b2269530fd2fc834e9b1544962f6524cf87925de43b05ad050e66b5eaa76a4ad754a2c5fc4f851baf75a0ea1b0ed8f51082300393a4c35d8c2da0d7c535bd
# Fri, 26 Sep 2025 16:59:31 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 26 Sep 2025 16:59:31 GMT
ENTRYPOINT []
# Fri, 26 Sep 2025 16:59:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b86f52d93f39a9cd7948b111170ca364b8983d59785511e8b8fd26d9c04adfd`  
		Last Modified: Thu, 25 Sep 2025 21:23:48 GMT  
		Size: 17.6 MB (17571783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847777cef2a1ff0a2ffef5b55f78a65f985269154fecd0dd396e054e70ade242`  
		Last Modified: Thu, 25 Sep 2025 21:23:50 GMT  
		Size: 62.7 MB (62713800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82534876c02903f6c1f497a5ad54196c388773c65bc845cda9014829db43344b`  
		Last Modified: Thu, 25 Sep 2025 21:23:46 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d927d233f6e92c36685600a80df2aec723a9a0626e0a47cfbc8f620545687192`  
		Last Modified: Fri, 26 Sep 2025 23:10:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86321dbf3d6c5a437db8fa5f20213d42b0ed6f003c12347b8b591bdd50d97793`  
		Last Modified: Fri, 26 Sep 2025 23:11:01 GMT  
		Size: 14.1 MB (14101657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d4ffb29cb58aa1d1f12e62be1c2fda3f1aa794da0be2fbf02c9353b3816fda`  
		Last Modified: Fri, 26 Sep 2025 23:10:59 GMT  
		Size: 207.8 KB (207752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:b3ee1b29356287c3cddfca7bdc3652089a7ce90ec8ee84faac21a6a38ed12ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac4050f47856afb2ed5b2bc78f84e429af9944659bddf473f20bf00aa2e4f9e`

```dockerfile
```

-	Layers:
	-	`sha256:f17c78b34dbec22d9e0eb3440afbe4d758edf70cbade3d77a09659c253e37758`  
		Last Modified: Sat, 27 Sep 2025 02:31:43 GMT  
		Size: 3.1 MB (3130082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f5a0e27cea39d41e3940092dfedaa4b588d1bebbc88bdcedaaa88b22bc43684`  
		Last Modified: Sat, 27 Sep 2025 02:31:44 GMT  
		Size: 24.1 KB (24064 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre25-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:95c3b75ad164ac9ac766179796da9881eb8596d24b7f6571637ece77109a2a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122163076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c18eb777713a261acfd59b735f7d106b3ec1993dd806ca0c336240901050b1e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3ec1d5906104fb273821a5865235b673fcd2b55674c5aee68d15b429fdc7837c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 26 Sep 2025 16:59:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Sep 2025 16:59:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 16:59:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Sep 2025 16:59:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_MAJOR=11
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_VERSION=11.0.11
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_SHA512=a26b2269530fd2fc834e9b1544962f6524cf87925de43b05ad050e66b5eaa76a4ad754a2c5fc4f851baf75a0ea1b0ed8f51082300393a4c35d8c2da0d7c535bd
# Fri, 26 Sep 2025 16:59:31 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 26 Sep 2025 16:59:31 GMT
ENTRYPOINT []
# Fri, 26 Sep 2025 16:59:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1632307dd4f034f428853e000721b56eeff937cd6ed46d1222a71cbd4f1daa17`  
		Last Modified: Thu, 25 Sep 2025 22:10:28 GMT  
		Size: 17.3 MB (17333675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469690150ae8fc62b121f0b93649f30c4bd4682c06925527570e3e89ed072a1b`  
		Last Modified: Thu, 25 Sep 2025 22:10:32 GMT  
		Size: 61.7 MB (61655869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82534876c02903f6c1f497a5ad54196c388773c65bc845cda9014829db43344b`  
		Last Modified: Thu, 25 Sep 2025 21:23:46 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1122f8b52608a1ee5b0d75df503c37d2997a77311fa3b57d8d174ae1a71a1ba`  
		Last Modified: Fri, 26 Sep 2025 23:10:57 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ba1c2900910eec4b1bb24a7fd84d56e735c97feda85a1cda9e64f293299c1b`  
		Last Modified: Fri, 26 Sep 2025 23:10:58 GMT  
		Size: 14.1 MB (14102274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d278053c0893e1f0ef57e3700720bef863824877f8745eb0c5d0a9d1a5ad2cac`  
		Last Modified: Fri, 26 Sep 2025 23:10:57 GMT  
		Size: 207.4 KB (207425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:047593fc743aab0eab665899297ccb10ed4004786442fc886421df0f67e7785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e900004679a4c2a8a69dee540f7c5c394ec8be9cfda6e4a96514d857d801be00`

```dockerfile
```

-	Layers:
	-	`sha256:9e2d845306c48ce4b7762bcc9c1b196e27c8321b627438599bbae087a5b37afd`  
		Last Modified: Sat, 27 Sep 2025 02:31:48 GMT  
		Size: 3.1 MB (3130628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4cfcb2c4bdbc8a6bbf52f9efa111b2a3dbce88e61a04c98378193e295810ded`  
		Last Modified: Sat, 27 Sep 2025 02:31:49 GMT  
		Size: 24.3 KB (24320 bytes)  
		MIME: application/vnd.in-toto+json
