## `tomcat:10-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:7fd2bc89745bc1d6e97f30d3478791610c9d749ad9a64665f7a1080bed986b33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:10-jre11-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:17b57b94237148e6cb5d0c782faac62e61e1fe1f77058aefa928bf86e9b38f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107078855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd27332e2ec9a4d4aca7fad084492df5490bff41b17c46d3a5b33b1c37bf34ff`
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
# Thu, 15 Jan 2026 22:19:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:13 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:27:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 02:27:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:27:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 02:27:43 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 02:27:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:27:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:27:43 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Jan 2026 02:27:43 GMT
ENV TOMCAT_VERSION=10.1.50
# Fri, 16 Jan 2026 02:27:43 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Fri, 16 Jan 2026 02:27:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 02:27:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:27:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 02:27:53 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 02:27:53 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 02:27:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f72bbf49e53cd7abbf0a1938937550baad6a61278e830b27dc7ac0b1237056`  
		Last Modified: Thu, 15 Jan 2026 22:19:37 GMT  
		Size: 16.1 MB (16147450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52334a3339e5917bdaae310909a684a6d33f493ac029ad7bbb3d4d45bdf6a2d7`  
		Last Modified: Thu, 15 Jan 2026 22:19:28 GMT  
		Size: 46.9 MB (46883643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbb3186e79f54c1c8bc93b2e4ac17c88d0719c0662caf3c8f5fee1e4068afb8`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d704164306ad1ff78584a292668f38506a0e6ff418351bfd0e4678c81a02bfb`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b68c2a9e41c14d048d6e431ed9fe0d134b817191677b9a7e6bdfc45dd6f2b56`  
		Last Modified: Fri, 16 Jan 2026 02:28:03 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc3f368ab1878eb9d6f443bac3141eaf2debe4770c9d9acd86c326a41b5937`  
		Last Modified: Fri, 16 Jan 2026 02:28:03 GMT  
		Size: 14.3 MB (14278772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74e2872e3607aa4a2eabc7f9f90cb472522f0c49ca5def274250bb486dec28a`  
		Last Modified: Fri, 16 Jan 2026 02:28:03 GMT  
		Size: 229.7 KB (229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b87e1586c508f58b9d2a2e7f8f7fd0f98e735d7a9bb777566f8b2ae4045eeb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdaaf58ece69c853601c16abe757f137e5e0eccc073f7a617d3861270d403228`

```dockerfile
```

-	Layers:
	-	`sha256:29fd056f3c67f66951a3e64131abb57df88ed268293f05ef7c86b32a9763e9f9`  
		Last Modified: Fri, 16 Jan 2026 02:28:03 GMT  
		Size: 4.0 MB (3953059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed6e6bcaec8841ccb7821c92aa567d36c7832da4230eca1ed979c306304492d`  
		Last Modified: Fri, 16 Jan 2026 02:28:03 GMT  
		Size: 21.2 KB (21220 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:9d93212835f00bf4f359d85071b0bb0bed8484e7535e22022481aa0d9de7d88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102040259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87092e6c916daacb0e849bf4be021735cf2978dcd2d3a6d097b025872a2e01a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:02:38 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:02:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:02:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:02:38 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:02:42 GMT
ADD file:c6e8dc9cf610f17d4ed912b48dc43aef299146d67e62f2248ccd0e2cca210a77 in / 
# Fri, 09 Jan 2026 07:02:42 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:10:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:10:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:10:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:10:21 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:10:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:10:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:10:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:10:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:33:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Jan 2026 23:33:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:33:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 15 Jan 2026 23:33:40 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Jan 2026 23:33:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:33:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:33:40 GMT
ENV TOMCAT_MAJOR=10
# Thu, 15 Jan 2026 23:33:40 GMT
ENV TOMCAT_VERSION=10.1.50
# Thu, 15 Jan 2026 23:33:40 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Thu, 15 Jan 2026 23:33:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 15 Jan 2026 23:33:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:33:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 15 Jan 2026 23:33:47 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:33:47 GMT
ENTRYPOINT []
# Thu, 15 Jan 2026 23:33:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:83d1a597d0ed11bf60c1ab8ef65516448b87de3790f14ee8336174b7f9a56d82`  
		Last Modified: Thu, 15 Jan 2026 02:42:29 GMT  
		Size: 26.6 MB (26643402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dbfe0e4a3e1b55426985b0e755d33abe06266bf8cd68733654fa59e5e27c75`  
		Last Modified: Thu, 15 Jan 2026 22:10:48 GMT  
		Size: 15.9 MB (15890632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30468d2c90f924c1a9519afa4b9ca96ecfaf94c54580d548352fc47832c9bfdc`  
		Last Modified: Thu, 15 Jan 2026 22:10:38 GMT  
		Size: 45.0 MB (45046779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8a0937243e305f098425ab4fed456d847c7a20a93270b126a59dc736076e7e`  
		Last Modified: Thu, 15 Jan 2026 22:10:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf8ae01510bc04c2d4b113e5d1d1f1d6ff5462d99e73c27e10411cad69ac781`  
		Last Modified: Thu, 15 Jan 2026 22:10:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac54aa970a5634f5d1ab8c1613ee1165b15ea699a96d8ac1985b32d492e9004`  
		Last Modified: Thu, 15 Jan 2026 23:34:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7de3f78028882a7a784374a5e0c8fa9d42c91b95837029c5186c6e986f6e8d`  
		Last Modified: Thu, 15 Jan 2026 23:34:05 GMT  
		Size: 14.3 MB (14254434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3f06bdaf45b68c5522f6e136e360a5c48c7500ac207c2dfbd96e498f92e23d`  
		Last Modified: Thu, 15 Jan 2026 23:34:01 GMT  
		Size: 202.4 KB (202372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7ad0052f81b3af3c13551c3cc9b43dd3331a989ca6ebd761503df6c77a01d51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110430b9f27545f5df7af5b482264a54ce7108de9a98ab0c4206c529bad2bdbb`

```dockerfile
```

-	Layers:
	-	`sha256:9faaaeada7ea76d47d0481ced0e2a1805850b4f7751c681a1f67da3f93a9f262`  
		Last Modified: Thu, 15 Jan 2026 23:33:55 GMT  
		Size: 4.0 MB (3956657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f0d9be85cfe0a1080eb63737dab32c5961dcb5d398c42b590ef199bd35749e`  
		Last Modified: Fri, 16 Jan 2026 00:33:24 GMT  
		Size: 21.3 KB (21339 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2f8d3b0d93a2205d1612712ca028e988a638beb56ed5683fbd854137c56d7b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103183019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce3b9b78a8f133061a6b2c02596b914f1a46e998a7ab9fee14934545159c3c5`
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
# Thu, 15 Jan 2026 22:19:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:05 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:44:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 02:44:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:44:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 02:44:03 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 02:44:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:44:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:44:03 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Jan 2026 02:44:03 GMT
ENV TOMCAT_VERSION=10.1.50
# Fri, 16 Jan 2026 02:44:03 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Fri, 16 Jan 2026 02:44:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 02:44:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:44:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 02:44:12 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 02:44:12 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 02:44:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e7c78b270fc977bd807e23019ea3b57ca39734f8ba060d62ef10d6f99e9d0c`  
		Last Modified: Thu, 15 Jan 2026 22:19:29 GMT  
		Size: 16.1 MB (16065931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729da86244bc5e1a1e48c9acd85dc2d7a5f2456ae786c69f178857b683ec59f`  
		Last Modified: Thu, 15 Jan 2026 22:19:32 GMT  
		Size: 45.2 MB (45220556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dff9cf0162ae7bc52165e6958c57d5974c45f73dc204dfff761910068efcd1`  
		Last Modified: Thu, 15 Jan 2026 22:19:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb954ce4c40c8ba7cb4d1b301537c9468fbdb35dc33337742e5163bb52cb3c0f`  
		Last Modified: Thu, 15 Jan 2026 22:19:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953ec49566bdea6c1a19e070bfe8a1d205b9f25bc27203d75852f92972c0dd91`  
		Last Modified: Fri, 16 Jan 2026 02:44:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7fb765ba2eb6d39f52f4fd95dead0da5b95e36affe8355531d9c047ced7dc0`  
		Last Modified: Fri, 16 Jan 2026 02:44:21 GMT  
		Size: 14.3 MB (14281731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b60dd2e9e0826da6a53a690c0a443b4a79f28d7c941cc9f2bb07c1c332bd2d7`  
		Last Modified: Fri, 16 Jan 2026 02:44:27 GMT  
		Size: 228.7 KB (228660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:8082857463513cdcdbab2767e309ad75e7b4b3cbe637cb69af59b796a47012b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c062e1fbb7a81c09d7e834241ad51dceb213f0fd0ded9728b5897916e51a0b`

```dockerfile
```

-	Layers:
	-	`sha256:c879fea656d54236a62582958847a32897003a39001b916ffea965fb661b89dc`  
		Last Modified: Fri, 16 Jan 2026 03:31:46 GMT  
		Size: 4.0 MB (3953346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d309c91e48a8667da72e5bcf943c7f7fce6cd53836941e2ed101a50db72c3f`  
		Last Modified: Fri, 16 Jan 2026 03:31:47 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:8f20f402956d81fbe60b4f1df63bf253949050970068fa579eb0f330270e19ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108912129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e44f9a2ca71269da6f280127ac2bf1f89ea6909a451c4f7284fc50b45b1ff2e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:13:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:13:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:13:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:13:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 04:59:23 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 04:59:23 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 04:59:23 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 04:59:24 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 04:59:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 04:59:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 04:59:24 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Jan 2026 04:59:24 GMT
ENV TOMCAT_VERSION=10.1.50
# Fri, 16 Jan 2026 04:59:24 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Fri, 16 Jan 2026 04:59:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 04:59:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 04:59:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 04:59:36 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 04:59:36 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 04:59:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:53 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b293ecafd630063bcb5186267efa589f780b852b7f4ae4f6161fc21b368d64`  
		Last Modified: Thu, 15 Jan 2026 22:13:44 GMT  
		Size: 42.3 MB (42290561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4efca18364173dfd2388d2503fc6932286ff0d015e2f28b9e09194042f4b1e`  
		Last Modified: Thu, 15 Jan 2026 22:13:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262e22cdecd7e1c54b3ecf1d2ca9016d4abcf373561c9bbab60a3823ccf7129e`  
		Last Modified: Thu, 15 Jan 2026 22:13:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74194f2c1623aebd3a07f5aee04d5d6369e55d3038acd7f8847dc452400e3999`  
		Last Modified: Fri, 16 Jan 2026 05:00:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a430cd669b0a57b122baec43c966411437ea275ad5e221fdea38871a4a785b`  
		Last Modified: Fri, 16 Jan 2026 05:00:12 GMT  
		Size: 14.3 MB (14293658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f560928114e02220b1b822aaaefa225647156d7228448c2259438ec508eac383`  
		Last Modified: Fri, 16 Jan 2026 05:00:21 GMT  
		Size: 259.1 KB (259105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d131be643391dbad5636d27bc8b1713bbc95db41f3be50545b682de4ad758d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c8240f50d1b61ce5389631a1f3039856a8982a090076e927db4a0341c2683f`

```dockerfile
```

-	Layers:
	-	`sha256:b934c4ff45db605c37efdd4a1c62cb8f91e3ce40efb785ccb6f669d4aa26da12`  
		Last Modified: Fri, 16 Jan 2026 06:28:59 GMT  
		Size: 4.0 MB (3957153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d7f7bb25751a95836e014dcf026af11f54c64b102da4afe844b31abcf85da3`  
		Last Modified: Fri, 16 Jan 2026 05:00:11 GMT  
		Size: 21.3 KB (21273 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:04f90a17fbff428304899fad6bf32711a1dad8a0ab86c73b63febf3163add788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99547276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41046d8675eec3311926f08e778ed0e2330fa14a75448ee2deb93b6a4261008b`
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
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:07:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:07:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:07:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:07:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:55:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Jan 2026 23:55:52 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:55:52 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 15 Jan 2026 23:55:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Jan 2026 23:55:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:55:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:55:52 GMT
ENV TOMCAT_MAJOR=10
# Thu, 15 Jan 2026 23:55:52 GMT
ENV TOMCAT_VERSION=10.1.50
# Thu, 15 Jan 2026 23:55:52 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Thu, 15 Jan 2026 23:55:53 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 15 Jan 2026 23:55:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:55:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 15 Jan 2026 23:55:56 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:55:56 GMT
ENTRYPOINT []
# Thu, 15 Jan 2026 23:55:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5756fabaef1b7457ab960f2aa94d20ec15c3df6ec7fef1bc4fcc286452731bf8`  
		Last Modified: Thu, 15 Jan 2026 22:08:22 GMT  
		Size: 40.9 MB (40880653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93407051451d97f5b77b799507f6e56cf6e8af23ee883a6ff564cf52afcdf1`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db9d6aa879ded96abfcbf210b06cb8e8df22a13e843c05d8bf2fc6099a54903`  
		Last Modified: Thu, 15 Jan 2026 22:08:17 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e701c137d8a8c9af1d2637179ffe93c0bf8f0377b5a1edf72dd11537f98e7f`  
		Last Modified: Thu, 15 Jan 2026 23:56:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aac488e732e865421ea44841e67875dfe1e65f97cf807fcf5325e8e14ef73d`  
		Last Modified: Thu, 15 Jan 2026 23:56:12 GMT  
		Size: 14.3 MB (14283691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffc158fe568de523e26ed4627bf785c31b6f583c453d793c33778a49b51b6f`  
		Last Modified: Thu, 15 Jan 2026 23:56:11 GMT  
		Size: 230.8 KB (230791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0067c3eb2534ca2726ca8fb9486c43ada45a9c33a0a5dae12c0a58e230779b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215f9e053cfe42888805e4edda9a0634d9c063780c1557b47458e7dd2d7603f`

```dockerfile
```

-	Layers:
	-	`sha256:f17e9bb595ccd64ddd28d5c8d8bfb165566bdb38a03bd0a92b33581364040e2e`  
		Last Modified: Thu, 15 Jan 2026 23:56:11 GMT  
		Size: 4.0 MB (3954656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca2bf409f332e3a763c7e518139469f5410d3eab77fbc81265038ada84179324`  
		Last Modified: Fri, 16 Jan 2026 00:33:40 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json
