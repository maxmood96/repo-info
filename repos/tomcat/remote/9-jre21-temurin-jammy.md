## `tomcat:9-jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:3c662414686d713ad283e68d782afc07113e17f3577c953fa0cd20b61ac1e17f
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

### `tomcat:9-jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:aa4964d10c27e32fb2f3eba60c5c2291fccde76e522b0a596803e760d63f24c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112932603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ee57775ec83fdd660015c82a1ad23e1bcfb2d5126028796c2cbc966ee9b55b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:11:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:10 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:10 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:10 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:10 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:10 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:18 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:18 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedbe7a7f974cd5e22a8bfde6806ab9362ef702fffc0f695deb267c3d5559917`  
		Last Modified: Wed, 01 Apr 2026 20:10:19 GMT  
		Size: 16.1 MB (16149364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804ba6bff73469147f6fae7c7fe225f067d6300d746c73b601d11ec86aadc95`  
		Last Modified: Wed, 01 Apr 2026 20:10:43 GMT  
		Size: 53.0 MB (52985551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37362c6be30a6b98c5fb295f72f8dc6d7e244f517ac8cdedbfd8ddbfc35f483d`  
		Last Modified: Wed, 01 Apr 2026 20:10:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4344daae9c653e41df744ff6dc2031ac59062111661991fff8856f0791bdea`  
		Last Modified: Wed, 01 Apr 2026 20:10:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e5f2ad41b201641c1d78cb0d33d65cb783012f12d0aa5f2bb3c886073c7c3c`  
		Last Modified: Fri, 03 Apr 2026 18:11:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144604f18f7cc2638bd4c4d1c0b68ca026d43038ff5601f54dbcacc44578c55`  
		Last Modified: Fri, 03 Apr 2026 18:11:27 GMT  
		Size: 13.8 MB (13828892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13814f8136cd2ed7b0a0e63c8bc0e8211468a53d578d66533520bf1886c47c0d`  
		Last Modified: Fri, 03 Apr 2026 18:11:27 GMT  
		Size: 229.7 KB (229739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3a9354934fbd7ed6c07d96e9bf8eb4e783c15492e161118a29e28b88f907c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699bbd7546c2f013e0dbf256862f405d506eb2369693310fa82a733134dc08dd`

```dockerfile
```

-	Layers:
	-	`sha256:3dbb43f3e2baa6f4b69be6f30c14fae34255606d2d2c2c6553153e34186e6fb4`  
		Last Modified: Fri, 03 Apr 2026 18:11:27 GMT  
		Size: 3.9 MB (3939777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f46b4a6f3bd0e4d17b40bbcab44168645f01ab5630f1724919eb8c158504d8db`  
		Last Modified: Fri, 03 Apr 2026 18:11:26 GMT  
		Size: 21.2 KB (21213 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:cf9a9c5f87623189de34a2ebb5642eebb0e77086bc2f28dcf878c4daeba38fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109903220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2116f5b7d36d84e45e2f5c7a96f8e6508ab29d3cbecd3f1e4fd17878dccb37`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:48 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:11:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:37 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:37 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:37 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:37 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:37 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:37 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:37 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:45 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:45 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:45 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963beb3bb70b2cebe7d47d994eafcdb017e7b54e6384c981571029519a38ea81`  
		Last Modified: Wed, 01 Apr 2026 20:11:06 GMT  
		Size: 16.1 MB (16073461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd019c3adabdec1621320404cbcbf8000084b66cd60b8f5838a2d1e6f42702f`  
		Last Modified: Wed, 01 Apr 2026 20:11:09 GMT  
		Size: 52.2 MB (52155647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa479ab8defbc52e300a4fedcb30c0e90cd6c53ff7f31a0855de60e65ffb7d`  
		Last Modified: Wed, 01 Apr 2026 20:11:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d407e998bf208d5b7a1aeb7f7ee16ecc1d4a6dd5b119948e88ef59763bcc83d1`  
		Last Modified: Wed, 01 Apr 2026 20:11:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1de1333d23a8e816af075c26fa9303cf107c1698acb16e7635e66c0ee6a525c`  
		Last Modified: Fri, 03 Apr 2026 18:11:55 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052ab1bba37fd8a1643d779462bd682b80564dc4f68bbef2fddc112017f21f17`  
		Last Modified: Fri, 03 Apr 2026 18:11:55 GMT  
		Size: 13.8 MB (13835834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ea3d3f8696167d4d224b4d4be09b6abd1c1669d1fd746b1e904adb646bfdc`  
		Last Modified: Fri, 03 Apr 2026 18:11:55 GMT  
		Size: 228.7 KB (228693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b6cb9596540936c0ba3f8e79d30ed76a7cb17ca73af780f6873ac5cddd4151b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941d5577d2284e4c54c5cd3d4f908eef85b2ec6c21980f3f1555d7166e5a11ba`

```dockerfile
```

-	Layers:
	-	`sha256:649b6f6237054da73de9dcde120c5fb7778ceee4661461c445b7049f3c0f86f0`  
		Last Modified: Fri, 03 Apr 2026 18:11:55 GMT  
		Size: 3.9 MB (3939446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950babaf2583781abfe4993bfc2e142e8950af23d797fad4f10d0b9a51ccad30`  
		Last Modified: Fri, 03 Apr 2026 18:11:55 GMT  
		Size: 21.4 KB (21361 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:fcda5dee571679920e76f5ba2bf2e695923d1639f632cc522e1c39077b2d0344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119360047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202f6c3ad20881e2151f4c30a3b844964bf77b2e86ade09d19ebd5bff9a3016e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:20:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:20:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:25:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:25:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:25:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:25:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 22:11:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2026 22:11:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 22:11:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 01 Apr 2026 22:11:16 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:11:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_MAJOR=9
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_VERSION=9.0.117
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:14:25 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:14:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:14:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:14:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:14:34 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:14:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e568bb13a59c072b3af8c406e7b451459d28a2bdf653f96393ea9610f7d09959`  
		Last Modified: Wed, 01 Apr 2026 20:21:27 GMT  
		Size: 17.6 MB (17622524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75b0f5db868730b25bbd0273a39f17da8826d39dd60b93eff19ad535326b86f`  
		Last Modified: Wed, 01 Apr 2026 20:26:05 GMT  
		Size: 53.0 MB (52972676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a059848b258bda15b7bf160d777ae51347cf9fa832001e7831ef5cb8e3f889`  
		Last Modified: Wed, 01 Apr 2026 20:26:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9873189c2e6f2903da55f7c84aa95ebd358d738b7a77047ecf6e695cdcd73f`  
		Last Modified: Wed, 01 Apr 2026 20:26:04 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34616904fac3f1ca3b01fd31fc6fbb59aa5422ffcc0b3b300f3db9da5531525`  
		Last Modified: Wed, 01 Apr 2026 22:11:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e79c50631e7f068cdb27dfa864fb7fc166ba43ceb9a63b26136531e0ae8978`  
		Last Modified: Fri, 03 Apr 2026 18:14:59 GMT  
		Size: 13.9 MB (13853336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767d060ab51e56f0ff40b553785ea3106d65a50bbcfc1b72f6187d7e80c253c`  
		Last Modified: Fri, 03 Apr 2026 18:14:59 GMT  
		Size: 259.2 KB (259205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7efe4758e5cb96b425668c45f755126a217b950a0b44e572a38c8d653e46d054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28361d9a2d070622345e00bf4888e50204eaccc6b9796e7d80497a2f9f7238b`

```dockerfile
```

-	Layers:
	-	`sha256:6297e1ff81eb82fcc1c1386d4fa2ad37d1d772b4d6dc191ca8f9d94f2d225e90`  
		Last Modified: Fri, 03 Apr 2026 18:14:59 GMT  
		Size: 3.9 MB (3943865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1997167f5aa815c9b4d170a4862e0730f8a65f81f21d80b36a95b758f74b4b`  
		Last Modified: Fri, 03 Apr 2026 18:14:59 GMT  
		Size: 21.3 KB (21265 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:c6460c109b722ea93dfb63b6c5181f8e341faa86b52ae0a9f5f0bd4fa5a573a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107947730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0eb759cada637b85e661106f289e694df8aa0077a2c3846db256ac588c727e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:08:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:08:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:08:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:08:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:08:48 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:12:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:12:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:12:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:12:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 22:46:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2026 22:46:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 22:46:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 01 Apr 2026 22:46:28 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2026 22:46:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:46:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:46:28 GMT
ENV TOMCAT_MAJOR=9
# Wed, 01 Apr 2026 22:46:28 GMT
ENV TOMCAT_VERSION=9.0.117
# Wed, 01 Apr 2026 22:46:28 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:10:38 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:10:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:10:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:10:41 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:10:41 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:10:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61594cb5a2469e67362dd6ac0dbccf92b89f433e8186d9f63201da426862ed3`  
		Last Modified: Wed, 01 Apr 2026 20:09:10 GMT  
		Size: 16.1 MB (16149500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de0722acac48023af60b31f1400a4568acb67787669e863ec1524800b202b24`  
		Last Modified: Wed, 01 Apr 2026 20:13:13 GMT  
		Size: 49.5 MB (49540952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede059f97736c8bcc51e072ea5fec2e46117fe9d7309f36e641124c9074abd67`  
		Last Modified: Wed, 01 Apr 2026 20:13:12 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d188b69c19f4c1dd330ef462967c312f40bc7283d2724603784faeb5501db9`  
		Last Modified: Wed, 01 Apr 2026 20:13:12 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377f1e140f2d3641620b4583fe99483727afaca615e5d1505d001d821837ef6`  
		Last Modified: Wed, 01 Apr 2026 22:48:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e635bdba583005486a5507229adb307f796ae43ed388538c2afd4c90e9b470`  
		Last Modified: Fri, 03 Apr 2026 18:10:55 GMT  
		Size: 13.8 MB (13820956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcc4d15b99e6f4570d893c7f70b2721e4e615045afff44508cd8fac1ca7c3d`  
		Last Modified: Fri, 03 Apr 2026 18:10:55 GMT  
		Size: 231.0 KB (230953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:903137b0aaa65f57cc54834bef07f0d34aa88a8797b4b5c084b27cfcf3a51b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96be2e4db79de44b54609d9fb8775a233b9e53c68dfd62853868c79b28cb89fb`

```dockerfile
```

-	Layers:
	-	`sha256:60499a6fb58b50ad032a34505c15e96672a687a05dc64f26e248aed87903d3c0`  
		Last Modified: Fri, 03 Apr 2026 18:10:55 GMT  
		Size: 3.9 MB (3941368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e179ce6f0a8b7840a3733e947a73bd5480bd46ad5c7f6bac07ba6dab05e360`  
		Last Modified: Fri, 03 Apr 2026 18:10:55 GMT  
		Size: 21.2 KB (21213 bytes)  
		MIME: application/vnd.in-toto+json
