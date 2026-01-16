## `tomcat:11-jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:33f7125e82f333f9661116aa7e721b688ecedb5026fb9f7dd9fc0d8e4481a77c
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

### `tomcat:11-jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:42c33ae063ad5bca29789dd4c73155f8901833987ea2183fda98bb857d7c5545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113184599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2032410aa972fdcf78afa13346d26c44226df9fe9093b88e1eb4d62084a7ba0a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:10 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:26:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 02:26:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:26:13 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 02:26:13 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 02:26:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:26:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:26:13 GMT
ENV TOMCAT_MAJOR=11
# Fri, 16 Jan 2026 02:26:13 GMT
ENV TOMCAT_VERSION=11.0.15
# Fri, 16 Jan 2026 02:26:13 GMT
ENV TOMCAT_SHA512=876beac5138cf8277f30fe8f6b519fcdd0bfe3d8ca3d20f734cab0f83e9b2e83de9395ee71052c2604f29f700d9646eddaeec72da5807a2d7edea3936096c742
# Fri, 16 Jan 2026 02:26:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 02:26:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:26:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 02:26:20 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 02:26:20 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 02:26:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c302597d98839a67b2d0eb53131fa4ef7965592afa8c476b8a799849d09954c`  
		Last Modified: Thu, 15 Jan 2026 22:20:36 GMT  
		Size: 16.1 MB (16147367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b8601c1ef3ef81eb5c67cd33025b6798a46aa1e38c5c216c3f27dc893757c`  
		Last Modified: Thu, 15 Jan 2026 22:20:38 GMT  
		Size: 53.0 MB (52978517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa93b68716d37237a828ea6838f2d363ff8db2cebb0701b5a6cc553c1e28a37`  
		Last Modified: Thu, 15 Jan 2026 22:20:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce36aff9df917fee409541f259e7bf51507339b25d86a0bb2eebd24e393aaa4b`  
		Last Modified: Thu, 15 Jan 2026 22:20:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62be411abd8c7f52a9dd861abdd8bad13571ff68a9dba4aebd92b4b86252b8ab`  
		Last Modified: Fri, 16 Jan 2026 02:26:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eefc2bfec2e01d39cc157ad87575ec1ed61c92dbed7f18d3ba8558d20889bf`  
		Last Modified: Fri, 16 Jan 2026 02:26:34 GMT  
		Size: 14.3 MB (14289697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b8f7c5ee075bd09818773a5bde9db7ad79f9bca8d5b2bed3ac61a0abed08e5`  
		Last Modified: Fri, 16 Jan 2026 02:26:37 GMT  
		Size: 229.7 KB (229709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6be0ff00fbba5ccb9b4f5cae329a4d6ebf5be824c63aa477fe2ce50e5e9ee36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3616dfad96d2cd1b03bf6a3c8782953d16427ab6117dac7a1646c6364909db`

```dockerfile
```

-	Layers:
	-	`sha256:8b5a6d88e971b06b2aec2f9997a5bc0512601d75405b1e318b78a16a8b6e7020`  
		Last Modified: Fri, 16 Jan 2026 03:38:19 GMT  
		Size: 3.9 MB (3942765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8180c61641139f16a3c01c77d8d5b966bd3a81bdd07f348113366021a42a68`  
		Last Modified: Fri, 16 Jan 2026 03:38:19 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:d3845ded7893e0d0f097a3991512a0e1c12c8506d3a963d5f1f8ef2b6bc71bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110120289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d13d594ecb2242bb1cd463f32f5750e0a8421d185c31ba65b3b78fc6e40b4b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:42:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 02:42:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:42:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 02:42:26 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 02:42:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:42:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:42:26 GMT
ENV TOMCAT_MAJOR=11
# Fri, 16 Jan 2026 02:42:26 GMT
ENV TOMCAT_VERSION=11.0.15
# Fri, 16 Jan 2026 02:42:26 GMT
ENV TOMCAT_SHA512=876beac5138cf8277f30fe8f6b519fcdd0bfe3d8ca3d20f734cab0f83e9b2e83de9395ee71052c2604f29f700d9646eddaeec72da5807a2d7edea3936096c742
# Fri, 16 Jan 2026 02:42:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 02:42:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:42:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 02:42:33 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 02:42:33 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 02:42:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:14 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a219d36f811564c72bb7a6d0857ab0c8d89d075c294126c2b2a475008aa7a9f9`  
		Last Modified: Thu, 15 Jan 2026 22:21:05 GMT  
		Size: 52.1 MB (52148571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e1d55d5d40f3e93a56f24f668a26eea6fa6e5356a993c4e45d8e9953b76df9`  
		Last Modified: Thu, 15 Jan 2026 22:20:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999485e2399b87c1520ab9bc7b8571ffae8afc8ca4ae4945f41f8c3a95c1cf2d`  
		Last Modified: Thu, 15 Jan 2026 22:20:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2fa9d0399c4cf4f9284bdfb8d2c6243c94f8bc2f85ef970199839f5579039e`  
		Last Modified: Fri, 16 Jan 2026 02:42:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a7df4ab33de754f594c627d42eca6fed1c666c3508233ea6e09c6c3de7e3ec`  
		Last Modified: Fri, 16 Jan 2026 02:42:52 GMT  
		Size: 14.3 MB (14291294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac90c2750ed97585d1809c138edecb7751b6ff69042413649e54a9256d476ab`  
		Last Modified: Fri, 16 Jan 2026 02:42:51 GMT  
		Size: 228.6 KB (228627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4741ef1af6bec7e57b1ca3e34e3ab5b5ca1516b4b7d6de0acd2e0864912b5b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0e90bce95a37afa66e27f763e9771764e340eb6fbe3f36a13c5c185d4c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:509f75ded325c2a56ea3760097786ef3fb38f5a0c6adbb4a06e76a06e8bc3dc3`  
		Last Modified: Fri, 16 Jan 2026 03:38:25 GMT  
		Size: 3.9 MB (3942446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d08b67a428262042cc9b51f98cb96700f69f0f263a84d21f66cc9766af295d2`  
		Last Modified: Fri, 16 Jan 2026 03:38:26 GMT  
		Size: 21.7 KB (21704 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:872852fdc330710967cd6b9d6a345bfeda4765c5ac2612e517446c55b2de57a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119626008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09eb18e7654a5ffb85b7f666596b8edf3285ed8d86d61f3eb33a52b567585a17`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:28:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:28:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:28:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 21:59:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 21:59:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:59:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 21:59:01 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 21:59:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:59:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:59:01 GMT
ENV TOMCAT_MAJOR=11
# Mon, 08 Dec 2025 21:59:01 GMT
ENV TOMCAT_VERSION=11.0.15
# Mon, 08 Dec 2025 21:59:01 GMT
ENV TOMCAT_SHA512=876beac5138cf8277f30fe8f6b519fcdd0bfe3d8ca3d20f734cab0f83e9b2e83de9395ee71052c2604f29f700d9646eddaeec72da5807a2d7edea3936096c742
# Mon, 08 Dec 2025 21:59:02 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 21:59:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:59:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 21:59:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:59:13 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 21:59:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7981811f07ac9eb3c9a58776fcd918efc4e1b55f3918ffca403a7cdb419d26d`  
		Last Modified: Tue, 13 Jan 2026 03:00:11 GMT  
		Size: 53.0 MB (52985377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604ced66345def7cb398c82a62cef8238b9618bf05090c9e9b7cb42b06f342b`  
		Last Modified: Tue, 13 Jan 2026 03:00:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f48406d6a19b8080d4ef1c51d90387e0b1221722e879c7a9c35f676c263cb64`  
		Last Modified: Tue, 13 Jan 2026 03:00:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd754ecd032318ef5ca6e02d754ea4c284198719f3688eb2704dd4787ec39a0f`  
		Last Modified: Mon, 08 Dec 2025 21:59:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86240ed9b427543e76764a64a99f2999bbd4e5878a58734ae1277ccfd82c2cf4`  
		Last Modified: Mon, 08 Dec 2025 21:59:40 GMT  
		Size: 14.3 MB (14308187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5a75f6f0937c2299f7eff27ab403f6ef4997698dc9315cef2521469eb322b6`  
		Last Modified: Mon, 08 Dec 2025 21:59:39 GMT  
		Size: 259.2 KB (259224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0ce29b1f0e79d39e747265c12cea64a2d16ae7bc9b82e4cb4380159f9db55996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1536008bd8fa4e55bc7e6eceae8298cfcf51a47e91ac2f773d99be5a5a1db7`

```dockerfile
```

-	Layers:
	-	`sha256:6c9e71cc8e82a4b7e4cf526fd873d8723eff93210f432dabd2830db277d09439`  
		Last Modified: Tue, 09 Dec 2025 00:38:16 GMT  
		Size: 3.9 MB (3946847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c239580b0a2d7da3fa2e2f78f27a09f0ba4751394b16b8e8652aa5de975c648`  
		Last Modified: Tue, 09 Dec 2025 00:38:17 GMT  
		Size: 21.6 KB (21601 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:d3696df78132e14e54a8d15382c6f395d3ea5496f6eb82c205bb759ee5dae424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108201934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8f84eff0cc45ec20e3c28da2bab0cb3b3ae2dad05a6c1e3da652b4d2b52433`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:06:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:06:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:06:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:06:25 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:09:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:53:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Jan 2026 23:53:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:53:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 15 Jan 2026 23:53:45 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Jan 2026 23:53:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:53:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:53:45 GMT
ENV TOMCAT_MAJOR=11
# Thu, 15 Jan 2026 23:53:45 GMT
ENV TOMCAT_VERSION=11.0.15
# Thu, 15 Jan 2026 23:53:45 GMT
ENV TOMCAT_SHA512=876beac5138cf8277f30fe8f6b519fcdd0bfe3d8ca3d20f734cab0f83e9b2e83de9395ee71052c2604f29f700d9646eddaeec72da5807a2d7edea3936096c742
# Thu, 15 Jan 2026 23:53:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 15 Jan 2026 23:53:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:53:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 15 Jan 2026 23:53:49 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:53:49 GMT
ENTRYPOINT []
# Thu, 15 Jan 2026 23:53:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817c28fd1674e902e8c2258dd5597f668d610e64feba2532604bc61a8e4ba2fd`  
		Last Modified: Thu, 15 Jan 2026 22:07:14 GMT  
		Size: 16.1 MB (16146443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93b5ce375928373ab6b1091166a97d3f16205cd7f00b39f3b27c03968c27642`  
		Last Modified: Thu, 15 Jan 2026 22:10:34 GMT  
		Size: 49.5 MB (49521850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7864b99467bfa2de329397dce5563f929731779e2cb0ebc27d35175b3cbb55`  
		Last Modified: Thu, 15 Jan 2026 22:10:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf8ae01510bc04c2d4b113e5d1d1f1d6ff5462d99e73c27e10411cad69ac781`  
		Last Modified: Thu, 15 Jan 2026 22:10:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc08edb9763290c180ad2e036fbb7dee05efcbd01607775954acd2de134477f9`  
		Last Modified: Thu, 15 Jan 2026 23:54:07 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c5dc77046d382b63d6922540de3f70ba54347d29cd3a96f6aa994724bfec0e`  
		Last Modified: Thu, 15 Jan 2026 23:54:09 GMT  
		Size: 14.3 MB (14297103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebbe2e53486b37a25003447e4008434dac719ae3eb2e4e0358a54d5e028cc4`  
		Last Modified: Thu, 15 Jan 2026 23:54:07 GMT  
		Size: 230.8 KB (230759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:5fe7e85448f4418d27a3ff60cd419b344ec580b03a4500528f2167e234cfa656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad741439e89e34425cc6098a851459eb2bd11c7503a723188644c6ea3488e08`

```dockerfile
```

-	Layers:
	-	`sha256:be61c13c8aa84304d2aa46e3b5356afce67ff45a14efafda194914fc316d7307`  
		Last Modified: Fri, 16 Jan 2026 00:37:39 GMT  
		Size: 3.9 MB (3944356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c26882ec2b64b82608c37e8989d48a27afadcd629404335bcd7c6546ed82e4`  
		Last Modified: Fri, 16 Jan 2026 00:37:40 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json
