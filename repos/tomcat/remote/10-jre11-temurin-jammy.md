## `tomcat:10-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:4b833380ebd55c0f9a828274c0ab595c5443021bee14c890a051406100f90f7e
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
$ docker pull tomcat@sha256:235348541fdc4ec8216711b86270f76180d90e5bd7c31cd910878a3b02c3cc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107082139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a01805ec0fea85f8a16146c5d98fad30cfec2f383e201ce4a8bb691d107b72c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:21:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 22:18:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 22:18:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:18:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 22:18:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 22:18:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:18:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:18:10 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Dec 2025 22:18:10 GMT
ENV TOMCAT_VERSION=10.1.50
# Mon, 08 Dec 2025 22:18:10 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Mon, 08 Dec 2025 22:18:10 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:18:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:18:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:18:17 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:18:17 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:18:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10875650961bf4063d5186970a8c79ef61cf11ca22d49b715b9d59712e0869b`  
		Last Modified: Tue, 13 Jan 2026 00:55:08 GMT  
		Size: 16.2 MB (16150480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbac7e3957e4a8d62e35315a55b2312a794469ede5d7a5657ca94dafc5046460`  
		Last Modified: Tue, 13 Jan 2026 00:55:11 GMT  
		Size: 46.9 MB (46883794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1842296f300570eaf6566d76ca4c3ffd4e2a68f14c6731abb0e72de720d160e2`  
		Last Modified: Tue, 13 Jan 2026 00:55:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c894d7b18aa773bfedc4eeeea8853069f22d621b48004b4a3b7a8ed8ec7f05`  
		Last Modified: Tue, 13 Jan 2026 00:55:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd9842dacebc4031abb054324adaa7c7a4db570cbd978ccbf0ef72df743cc98`  
		Last Modified: Mon, 08 Dec 2025 22:18:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07a92efd9015de2a4bf71fd87bac09125c1c59e37fbbf6e9308db5b33c58039`  
		Last Modified: Mon, 08 Dec 2025 22:18:30 GMT  
		Size: 14.3 MB (14278765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6de6db9c7682326f788a3da6e739281f73f00dafc4da9bd1e5a9b3de1a868`  
		Last Modified: Mon, 08 Dec 2025 22:18:29 GMT  
		Size: 229.7 KB (229660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d679a07b448cb58d7bd34715b4732ed629dd1e5856626a9178c4f82449375e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52705badbe1ac579664c1a5d346937a8c7735e7242fea137fcc02913033b1ac`

```dockerfile
```

-	Layers:
	-	`sha256:77bdb394affd6596e1af8569dc50c3c6827f09eac743a1d4262bed88360745fa`  
		Last Modified: Tue, 09 Dec 2025 00:32:22 GMT  
		Size: 4.0 MB (3953047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e31bf3b7782e52c26d20dfa0cf2510f9f63786a398a769d8b63afaeab9b9ec`  
		Last Modified: Tue, 09 Dec 2025 00:32:23 GMT  
		Size: 21.2 KB (21221 bytes)  
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
		Last Modified: Thu, 15 Jan 2026 22:10:50 GMT  
		Size: 45.0 MB (45046779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8a0937243e305f098425ab4fed456d847c7a20a93270b126a59dc736076e7e`  
		Last Modified: Thu, 15 Jan 2026 22:10:44 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:33:23 GMT  
		Size: 4.0 MB (3956657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f0d9be85cfe0a1080eb63737dab32c5961dcb5d398c42b590ef199bd35749e`  
		Last Modified: Fri, 16 Jan 2026 00:33:24 GMT  
		Size: 21.3 KB (21339 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:162433387b864be4ec9a0258127082c11fcc1c0a257827440eec35908ddc1dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103184061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb07406907111b1fa0695ab191a5e8790f97401708949e460249f35eb5b16498`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 22:17:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 22:17:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:17:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 22:17:39 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:17:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_VERSION=10.1.50
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Mon, 08 Dec 2025 22:17:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:17:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:17:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:17:49 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:17:49 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:17:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44e93e2f17680350eef250800f885c5ec5b1dfc6fb7c43cf8e92ea04d5a6f0b`  
		Last Modified: Tue, 13 Jan 2026 01:13:11 GMT  
		Size: 16.1 MB (16066283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19091f4ba16e523818b0ab550431bc5f8fc49d93fc4e6859db4e667013122066`  
		Last Modified: Tue, 13 Jan 2026 01:21:50 GMT  
		Size: 45.2 MB (45220811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f0f0689ff41fa833d46b5d2ab229f2ed544e7400dc727dd1c05bf9b01bb9c3`  
		Last Modified: Tue, 13 Jan 2026 01:21:49 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53675a133c6bc8e493090499c6df5a23837a682556eaf29bce46837a8957367`  
		Last Modified: Tue, 13 Jan 2026 01:04:52 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ea06acfef5d0e60cce6d4463eededc93e64807fa7c2e247fd5c61d8be6cfb`  
		Last Modified: Mon, 08 Dec 2025 22:18:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b116e97f0d591ac01aaae9c825146d1c0196c68b52f8d64a1e3bab1c5f5414`  
		Last Modified: Mon, 08 Dec 2025 22:18:04 GMT  
		Size: 14.3 MB (14281741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faae193bbf141c88c7ade62965a8ba388e65f28c8a662770a86ebe4570fc95c`  
		Last Modified: Mon, 08 Dec 2025 22:18:03 GMT  
		Size: 228.7 KB (228706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:bcfaec4865ca3e538a6e3b784870b9be577d1d2881986ab2da2d5e6b688e409d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cac6f9d0021cf234ab6bd9cd5f0bdcab84a6f8c244632fafad7e3455233bd7`

```dockerfile
```

-	Layers:
	-	`sha256:a3dc4f0c0a26801eeda79ad4658500a5a392c77b17dfa73a9b35d5bbb7654f59`  
		Last Modified: Tue, 09 Dec 2025 00:32:35 GMT  
		Size: 4.0 MB (3953334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555dce9b0b573db77450aa9de903d550076b4b35d60192511ab88a6cd04b50ba`  
		Last Modified: Tue, 09 Dec 2025 00:32:35 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:c0508d69bb3cd8b77255a1d86ac4974bc13917b6170fabec13f76bc744dcc6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108916853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b0681a9ad183ab55d55b2a4709c01d90e24c7e430f6d3e2c4541eda3be5720`
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
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:18:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:18:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:18:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:18:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 22:10:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 22:10:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:10:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 22:10:54 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 22:10:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:10:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:10:54 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Dec 2025 22:10:54 GMT
ENV TOMCAT_VERSION=10.1.50
# Mon, 08 Dec 2025 22:10:54 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Mon, 08 Dec 2025 22:21:22 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:21:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:21:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:21:33 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:21:33 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:21:33 GMT
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
	-	`sha256:070882254e1568573e76e7e28ef1d0e22d53995aedd17bde2cc69bf0799664c6`  
		Last Modified: Tue, 13 Jan 2026 10:24:18 GMT  
		Size: 42.3 MB (42290660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa81bb9f3ba6a0fbf291196ca08a13aea3234e6425006d666c9ecc99c3b8c476`  
		Last Modified: Tue, 13 Jan 2026 10:24:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81c2d4d6e204d9269bb0567d23b5e805a7b98db27074014cabc60249be8e92c`  
		Last Modified: Tue, 13 Jan 2026 10:24:12 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8253a82ad3d80c353161b4d289b4f28f93c23b7a63fc913a82df2c97546849`  
		Last Modified: Mon, 08 Dec 2025 22:11:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51772d4e3a1d9a50557c02d0b593fe28c55e2b929cf4cad77c5c979e35c138f4`  
		Last Modified: Mon, 08 Dec 2025 22:22:03 GMT  
		Size: 14.3 MB (14293689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d1427611b04267d982b0ae8785e0cc72fc2e5f733a2c1bb1c73ea94d1dcb96`  
		Last Modified: Mon, 08 Dec 2025 22:22:02 GMT  
		Size: 259.3 KB (259283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:88b0839c6ae3ae7b4846114675d1efe84d8b378a6bc50cf1a6203d56d9229e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26332d0cd3f7fd4c16c5417b97526dd35a91e329186d76a0f250ef1e74150b1`

```dockerfile
```

-	Layers:
	-	`sha256:8ec27bdc72c7002e38b3233bf87b7153012a8767acaecb646169c1dd8855988c`  
		Last Modified: Tue, 09 Dec 2025 00:32:40 GMT  
		Size: 4.0 MB (3957141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8998ec4ba47dcea025403e06fedfda6cdfea87d500682e63e138314b1370644b`  
		Last Modified: Tue, 09 Dec 2025 00:32:41 GMT  
		Size: 21.3 KB (21272 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:a0001b5509c0f8a233df4191de30db6cb579918c391d972e5df53989a37fd4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99549606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d358d3984e35429fa5caa325c78aa09d6e29d91e2ed41e55975c342bc59c2a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:09:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:09:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:09:06 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:09:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:09:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:09:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:09:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 21:11:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:11:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 21:11:03 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 21:11:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:11:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:11:03 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Dec 2025 21:11:03 GMT
ENV TOMCAT_VERSION=10.1.50
# Mon, 08 Dec 2025 21:11:03 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Mon, 08 Dec 2025 22:17:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:17:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:17:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:17:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:17:36 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:17:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Tue, 13 Jan 2026 01:21:19 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de558eecb3d8a4c4982425e8af109373d73dbc0fe2bc177a81bc5ffbc6360f2`  
		Last Modified: Tue, 13 Jan 2026 03:00:26 GMT  
		Size: 16.1 MB (16149741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3094babafc87294d40a592b1bc1ebaa47dd8b57b0bdcb997412d71602fd7d2`  
		Last Modified: Tue, 13 Jan 2026 10:23:31 GMT  
		Size: 40.9 MB (40879389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6bb40ce150a38f3152e286194fbf6acc758b068a31d5e393a5d217a0fd8583`  
		Last Modified: Tue, 13 Jan 2026 10:23:27 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9714157a4f71d2cd64d4a1d5a57a361f8cb6e2ef308f29461704908bee6d03a`  
		Last Modified: Tue, 13 Jan 2026 10:23:37 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7515de1162ec017b977cf6e8fb13288755468aaccdf6f9032d35a099833adfa4`  
		Last Modified: Mon, 08 Dec 2025 21:11:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d7bfa34d8ce31f5f9a53cdd0fd5a3b4620decc10c164dbca06fc5d883b8f3a`  
		Last Modified: Mon, 08 Dec 2025 22:17:55 GMT  
		Size: 14.3 MB (14283685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b3302bd511765b7e7119984c356cab38f686c2c9ef4ba66e21a12da9c419ce`  
		Last Modified: Mon, 08 Dec 2025 22:17:54 GMT  
		Size: 230.9 KB (230862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:49c873726ca3847ca6d1c1c807cf73dde357816cdcfea4b4c43f7b5d0e0cb893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b206f8f590cd5439d894bd2dc9f045ef8137bd8edacb6af127381d329f20d60a`

```dockerfile
```

-	Layers:
	-	`sha256:99e1685bf302d0da19cc3737c5eaa6970e6a0646e297b7497ae0059bf923328a`  
		Last Modified: Tue, 09 Dec 2025 00:32:46 GMT  
		Size: 4.0 MB (3954644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d769a854b280196e737fbafc3c90146366ca745f80ae548c3fc13698337335b5`  
		Last Modified: Tue, 09 Dec 2025 00:32:47 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json
