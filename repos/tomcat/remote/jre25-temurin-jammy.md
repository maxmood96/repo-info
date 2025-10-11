## `tomcat:jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:adb89d46499e1d0ed8e24bd2563053187e315093f4609ce9350d73d101d11bc2
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

### `tomcat:jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:64719a19eb8b95ae54796706ffb29d71066e6ede85cc0077f2facd6f0e407418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117949672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e210d752c698ee2e5c9e4cc412cf0c17ffac19ca58eeee2a1f90181f040bc8e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 26 Sep 2025 12:51:13 GMT
ARG RELEASE
# Fri, 26 Sep 2025 12:51:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 26 Sep 2025 12:51:13 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebcf6ccb7a25d039036b92d9e7222cd6e561a2e8cc1386a7b5fc5bf53d286d9`  
		Last Modified: Thu, 02 Oct 2025 05:02:59 GMT  
		Size: 11.4 MB (11404481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a39644b82549f4f4c61fc7970481a751067fd2638235a1b6235a3b4f00f0f4`  
		Last Modified: Thu, 02 Oct 2025 05:03:06 GMT  
		Size: 62.7 MB (62683569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7781308d60d7ca0777d5dc30ab1f522ffe43197a6ed0ec7c75aac52d7bd8512`  
		Last Modified: Thu, 02 Oct 2025 05:02:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e45a39fc3dcba8b174e80c0b88376f874c2b92d0b47603f03a60ac3f8761030`  
		Last Modified: Wed, 08 Oct 2025 00:12:07 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e09ea7d6dde9344d6ef6ae595ea9eecc5bb82789b1779583a548190189c336`  
		Last Modified: Wed, 08 Oct 2025 00:12:08 GMT  
		Size: 14.1 MB (14108865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0da4d14b9e5a91b398085c85cb9411b0a4a91c2f3f33c7e292e574559894655`  
		Last Modified: Wed, 08 Oct 2025 00:12:07 GMT  
		Size: 213.4 KB (213424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ad779f5fa3b730cff4d317442a9e9f570e9c57d9339213c6674bd5c88b72f218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30103e05c3eb72b7d7da737afaa9f6def4c2cb826ee3d535e82df6ce03b7ab4`

```dockerfile
```

-	Layers:
	-	`sha256:ad7370995d4ca3007dba961e6754c6173ebb0af0d3ee8225f6b85b85e1ca1e86`  
		Last Modified: Wed, 08 Oct 2025 02:40:39 GMT  
		Size: 3.7 MB (3709473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d623a73f21cb1bd82e428b2e85c1e3df0755978f0119ea8973f36de2d10a49d4`  
		Last Modified: Wed, 08 Oct 2025 02:40:41 GMT  
		Size: 21.6 KB (21568 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:f3a5b5ce025a1cd07e6fdf4f04305b4f06eb78653bc779881d220d78304fe48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114689635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377aadc8765c737ef1449a8d21dfb11acfb5fdc6792d41c14302d6fd39957fbe`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 26 Sep 2025 12:51:13 GMT
ARG RELEASE
# Fri, 26 Sep 2025 12:51:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 26 Sep 2025 12:51:13 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1ea8a206ccae53a6fbf662fd1fdd48aa3e046e77b1b5f0e240e23d123fa230`  
		Last Modified: Thu, 02 Oct 2025 01:19:01 GMT  
		Size: 11.4 MB (11357845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a57cf3aec537870ea7681aba07712bdfcc729c81186b6e2b60f6ac66f088ef`  
		Last Modified: Thu, 02 Oct 2025 01:19:08 GMT  
		Size: 61.6 MB (61620509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7a6ec136d5ae6fbc5cdcfca2ce1c427a35caad88a513dd0cd7408f9b6851ae`  
		Last Modified: Thu, 02 Oct 2025 01:19:00 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cf6231b643a71207a5ff8ccc1fd7dcee7a17ad1be1446a62c11812b132238b`  
		Last Modified: Wed, 08 Oct 2025 00:12:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ec7169aebd043159a146673c9eb8b0f09099c8ed10a7dd484f9a0a4c7f8ef4`  
		Last Modified: Wed, 08 Oct 2025 00:12:29 GMT  
		Size: 14.1 MB (14113124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62f4f5dc297d5f045185d863d4f88c511b3527a5a623496eb2d873f3a5d120f`  
		Last Modified: Wed, 08 Oct 2025 00:12:28 GMT  
		Size: 212.5 KB (212532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3778c09fb73574975e3e85efb560a733f4ebaa8eacff9c305b723aa9983cb632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fa77262cbcdc583476271d7f846e78b73dadaa72fedf4857a327e55d43c5ba`

```dockerfile
```

-	Layers:
	-	`sha256:1cae0e0dda1816264081ee8934281dd119bb73111ad23fa8e4cbb75905faf5d8`  
		Last Modified: Wed, 08 Oct 2025 02:40:45 GMT  
		Size: 3.7 MB (3709136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0112d23a547ef613b6d02bf5d5a4325d401c5d15352c070555a602d4f64108c1`  
		Last Modified: Wed, 08 Oct 2025 02:40:46 GMT  
		Size: 21.7 KB (21728 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:51a2890980cb28e54904f45f5ac07c9ae6f051961796ba352764f1253bad6b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122819643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a428d682f6415f9cc7ea887e5b7c74165823b748f646c40dc3e584ac9e3875ae`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 26 Sep 2025 12:51:13 GMT
ARG RELEASE
# Fri, 26 Sep 2025 12:51:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 26 Sep 2025 12:51:13 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
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
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8580e482ec8bf2452e1b0e076feb03d9307466e9ba7b425525a332191fa270`  
		Last Modified: Thu, 02 Oct 2025 01:45:03 GMT  
		Size: 11.9 MB (11893631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dab9b5c165a5c4137aee9c83f16dd23e5f179b0b1a324ff248667e8249c2e6`  
		Last Modified: Thu, 02 Oct 2025 01:45:07 GMT  
		Size: 62.1 MB (62106869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1876fe81c6618e3060ab79d87e7222127645f7209063f784b56281813f82d0`  
		Last Modified: Thu, 02 Oct 2025 01:45:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba4be073be5aee7dbc3eefcf021c2f109a838c7ecdb89738506ac6df9bd8b19`  
		Last Modified: Thu, 02 Oct 2025 13:21:00 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bd07932e2d4def583112cf2caed32eea1eaaea4b5cb4ae26ffaf0b904205ee`  
		Last Modified: Wed, 08 Oct 2025 00:23:23 GMT  
		Size: 14.1 MB (14126770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c325f1d8e4cb631dd9b21aebf6a3e501790efaf911c211117e8a19c9d06f1775`  
		Last Modified: Wed, 08 Oct 2025 00:23:22 GMT  
		Size: 243.1 KB (243070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:849969bfdde78aeaef718ffb9a1be831d46f5235612b1a75818a33167934a94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1862ac0b3f9526ea078ea17e9b15ed36253b5750f5d09de8b4910d9c34b73c`

```dockerfile
```

-	Layers:
	-	`sha256:f7eee6db5d893fa38b8047604dc29f0a6a7a9128ff87ac2c21c147761dce9cc8`  
		Last Modified: Wed, 08 Oct 2025 02:40:52 GMT  
		Size: 3.7 MB (3712819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc6f47eebe417925bf9da993265e8a3dd97defc0e1e1e6aa3eff080c146f589`  
		Last Modified: Wed, 08 Oct 2025 02:40:53 GMT  
		Size: 21.6 KB (21626 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:cd0c1ccf383c5daebd5c307e22fe4938346343d5b4a28c55d5ed95bcaa226f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114131766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ad7618c1ff666f37a1b32e752b3b1c82ca7025da04134568b3cf448fbbc90b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 26 Sep 2025 12:51:13 GMT
ARG RELEASE
# Fri, 26 Sep 2025 12:51:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 26 Sep 2025 12:51:13 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
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
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f9c414af075ff7ef23535bb6ab5561f3349d5fca171a62d794056506db756b`  
		Last Modified: Thu, 02 Oct 2025 01:27:58 GMT  
		Size: 11.5 MB (11497310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3494382da94a851df411ae7c62f825b189d05d1f42939a876e5e514fbff3bb69`  
		Last Modified: Thu, 02 Oct 2025 01:28:01 GMT  
		Size: 60.3 MB (60297088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4a54020446b8e789a6b1450b750a172027f6a8c278c08b7ab186bf8497bc25`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882e301f262cb37d6130354644909a901d5a07a0035239d5dae927f5253e67ab`  
		Last Modified: Thu, 02 Oct 2025 05:36:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa54049e25e1dbda6cb0baccb2b0fe1aa8bea1835a0fdc0a5dba8f8a408ad18`  
		Last Modified: Wed, 08 Oct 2025 00:10:31 GMT  
		Size: 14.1 MB (14116841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b50aad97aac51a89b5910be5fc274bccfb42035b203b60a7f414179c5214ba0`  
		Last Modified: Wed, 08 Oct 2025 00:10:31 GMT  
		Size: 214.6 KB (214598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d828c49d3e888a446667b66631d17f6ec1783ed55411337646a64a7c1cb7cc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35002d90c2c705519bcddb8a9c1dcce8c82bd9ee9af5ae25f26448941896fddf`

```dockerfile
```

-	Layers:
	-	`sha256:ad47d0a4246df0178190be021e31a9c23fd3b4ef3e1ec62f51cb8f69131fb3d6`  
		Last Modified: Wed, 08 Oct 2025 02:41:00 GMT  
		Size: 3.7 MB (3710458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d831ee9b61c65ec04c24b9a6a4740bf1d174b79b3b5a0371a5b06427e4c470`  
		Last Modified: Wed, 08 Oct 2025 02:41:02 GMT  
		Size: 21.6 KB (21568 bytes)  
		MIME: application/vnd.in-toto+json
