## `tomcat:jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:3fb91dd338cf85f563beab501ef6b7efa5b5c35990687e14a33712a1ba7a1eb3
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

### `tomcat:jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:46c4748548ff9f90175265672f11a209aaa5f435e31a503d272c48b0061d3c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112601538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bae9e4b51cbab2cd008bb86729be018ed619bfac862f1acf4a6fcc0ef87ab19`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 11:56:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 11:56:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_MAJOR=11
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_VERSION=11.0.4
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_SHA512=1b86558c398086b080f5a2c298b8d55c32d958e0c41782b1bb384d12e8d76f23d54cd98affa177af3d3e6fdc4fd55bdbf7796f5fa5e2ceb6310be0a0fd1acf9a
# Tue, 18 Feb 2025 11:56:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 11:56:33 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 11:56:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b8e353effdf25ad74bbde76a3242135d6d12fe14be177b7108868c3150b48`  
		Last Modified: Tue, 04 Feb 2025 04:40:12 GMT  
		Size: 16.1 MB (16135187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379395aa081f5fd7e867ea654d17431258dab5353139b32bc5fa9c09edb8c19a`  
		Last Modified: Tue, 04 Feb 2025 04:40:12 GMT  
		Size: 52.9 MB (52876031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298e1b6de86675cf06530c6496ec8374d300561fc2cdacf984c524349c6062ae`  
		Last Modified: Tue, 04 Feb 2025 04:40:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea28f6f7f0aa0864f252fa90ca3f85687428d91dd6f829f2ba81dc8719e2e3be`  
		Last Modified: Tue, 04 Feb 2025 04:40:12 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a40ac691dfca46d2e81eb758fe75744d48352ad5b09df51aae61d2f00a724f7`  
		Last Modified: Wed, 19 Feb 2025 02:08:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733ca4137c45989fac865d42cc5bf443a7e8cec5f3d0b25d151b0d49c9d183da`  
		Last Modified: Wed, 19 Feb 2025 02:08:09 GMT  
		Size: 13.8 MB (13822058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcaaba69d5e04aab75093ccbb2b19110162b03c310931d99dae46c1fa09b18`  
		Last Modified: Wed, 19 Feb 2025 02:08:09 GMT  
		Size: 229.7 KB (229677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b181b3e96a0463956770b82f960f1b075e7df6528093e7e28b826f1c0ba206a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3791241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321d0864d5c2ff91932711774a40bcc2125f654930f5146ff8fec0a89f66d6e`

```dockerfile
```

-	Layers:
	-	`sha256:9bfefad8e19b8d7311f77ba6a2bca8b37160e5833cde42f2cd5d0a3930d27159`  
		Last Modified: Wed, 19 Feb 2025 02:08:09 GMT  
		Size: 3.8 MB (3769662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec3972cca926f6daef612b80c789d52b4de7523d756e141089f5308a2fe17a5`  
		Last Modified: Wed, 19 Feb 2025 02:08:09 GMT  
		Size: 21.6 KB (21579 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:8c4b4f03af67faca328b7f5269cf66401bbdc35e34b06d587ef4d827f1873bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109524399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e93a957a93aa44d61ae4455bb094b5fff612f5b90e26f2bff0fd384425c55d0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 11:56:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 11:56:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_MAJOR=11
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_VERSION=11.0.4
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_SHA512=1b86558c398086b080f5a2c298b8d55c32d958e0c41782b1bb384d12e8d76f23d54cd98affa177af3d3e6fdc4fd55bdbf7796f5fa5e2ceb6310be0a0fd1acf9a
# Tue, 18 Feb 2025 11:56:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 11:56:33 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 11:56:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95725c2df89972119cbe127fa685617010a1c1e038ad8fa77f3a2ce55dced587`  
		Last Modified: Tue, 04 Feb 2025 09:25:22 GMT  
		Size: 52.1 MB (52058393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb385b34446c3df21cb4021820b3d3adc4a6c71cdc68b1c961bff59a69117811`  
		Last Modified: Tue, 04 Feb 2025 09:25:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f159f3116700a25149bc46b10b2c56185ebc43fe2b614133fd8a0c0bb25dc991`  
		Last Modified: Tue, 04 Feb 2025 09:25:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704c1e31335e7df2a47128e42aa39c716845023a40968ef71791dc0ed027925d`  
		Last Modified: Wed, 05 Feb 2025 04:43:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ab1e254a6aacd71fac2b40f4ef9e4ef220278517c6bf7d2fb982d0ce23b75`  
		Last Modified: Wed, 19 Feb 2025 01:25:17 GMT  
		Size: 13.8 MB (13823986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d02eab1eb3f97f88e592ac40fe1271a47ee238f142aa929ce19c914ac4874c`  
		Last Modified: Wed, 19 Feb 2025 01:25:16 GMT  
		Size: 228.5 KB (228549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4cf40c2618b5521b01cc2bdce6c82e82cf03a64f7d77255bc597a0bd4f9f710b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3791083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6d6010de2cd7814ccbdce3a916474397d58d4e9b42a639d28963ffc1eed829`

```dockerfile
```

-	Layers:
	-	`sha256:7f1d5520f6c82ac48d5cc48d185799fe73bd86df8aa26c331016bca98ba8b877`  
		Last Modified: Wed, 19 Feb 2025 01:25:16 GMT  
		Size: 3.8 MB (3769343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151048d1d0b49697c5a7a6e9164aec4737d17937abf4af1734ae60867c9520ef`  
		Last Modified: Wed, 19 Feb 2025 01:25:16 GMT  
		Size: 21.7 KB (21740 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:bf66c16a1b66771ceb3cf1191395b6f067706fb1780be1b18e369407c3e0550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119102169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da85a22686f03982eb0af61dd887530147a39c1f0447938d46635aeafcc2657`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 11:56:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 11:56:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_MAJOR=11
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_VERSION=11.0.4
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_SHA512=1b86558c398086b080f5a2c298b8d55c32d958e0c41782b1bb384d12e8d76f23d54cd98affa177af3d3e6fdc4fd55bdbf7796f5fa5e2ceb6310be0a0fd1acf9a
# Tue, 18 Feb 2025 11:56:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 11:56:33 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 11:56:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71de2d980599cbec4dab5c3bd7274078312e68d7cc81171b5d8bda1a98eb2403`  
		Last Modified: Tue, 04 Feb 2025 07:32:10 GMT  
		Size: 17.6 MB (17642335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435fcf10bf81a5ef917029ead19e990e3ff0a4e193038999c648c2631097a48f`  
		Last Modified: Tue, 04 Feb 2025 07:48:19 GMT  
		Size: 52.9 MB (52915069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1afa04b461e33531c028ee10c388148ef95888eaebb52afd7f162cd48d1fff9`  
		Last Modified: Tue, 04 Feb 2025 07:48:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab258ea4c329b5efa03c3fcdd7e6b3f7af187288f825972811b81ea22d0c00bf`  
		Last Modified: Tue, 04 Feb 2025 07:48:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64302daee7499cb7c77b7e9f850ed3835233394c2a2e7cf27e4c5e9aa25f5af7`  
		Last Modified: Tue, 04 Feb 2025 23:10:16 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dd5bbb1bee42c13dc81e59333c7a1dea76b565c0a7c684fe5aa6724899d486`  
		Last Modified: Wed, 19 Feb 2025 02:22:23 GMT  
		Size: 13.8 MB (13835273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585eb5b127574aa0067575730977dffbda2accc96597714c4b81558d14eed51b`  
		Last Modified: Wed, 19 Feb 2025 02:22:23 GMT  
		Size: 258.9 KB (258912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7210820d93b19d4c196d412ccca5a33e80f50c6c98a05036b6eb234d92768c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d048c58b42d524b76d4d10a1ac70aecf80d7defb5e9b362daa48a27a2abcf384`

```dockerfile
```

-	Layers:
	-	`sha256:aea3dbc5e6b5c8ddfc03f19d217a9fa9a05e9609fc95c4d4830be4d2840d75a2`  
		Last Modified: Wed, 19 Feb 2025 02:22:22 GMT  
		Size: 3.8 MB (3773604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d050b24c8113034ae8352ce9504930bb0f52ce7dc6323e083699aa6b10fc490b`  
		Last Modified: Wed, 19 Feb 2025 02:22:22 GMT  
		Size: 21.6 KB (21638 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:ee649cbcca27f768f960fa591a5be032a6c6dc2541495a8880ef3fc6fc359559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107653982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce1143d29196e333af809900bf8e8379c0281b29e1fbc3d45d690aa1b058d1b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:03 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:05 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Sun, 26 Jan 2025 05:32:05 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 11:56:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 11:56:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_MAJOR=11
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_VERSION=11.0.4
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_SHA512=1b86558c398086b080f5a2c298b8d55c32d958e0c41782b1bb384d12e8d76f23d54cd98affa177af3d3e6fdc4fd55bdbf7796f5fa5e2ceb6310be0a0fd1acf9a
# Tue, 18 Feb 2025 11:56:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 11:56:33 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 11:56:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c64c26afd0885ce3d2d456d35ff90e813c65ee4e2f59dd40604fa8b3e90414`  
		Last Modified: Tue, 04 Feb 2025 07:39:56 GMT  
		Size: 16.1 MB (16132604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e748dfd1fa969b853ba3697791f039af4c55a839a5c50e477217176265f1b`  
		Last Modified: Tue, 04 Feb 2025 07:51:22 GMT  
		Size: 49.5 MB (49462943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653884e7c258812fac56cda1ca97c1deafd240ac6d359765356d52bae405c045`  
		Last Modified: Tue, 04 Feb 2025 07:51:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b2b89b98ed384dea007d5383048dcbd69e1889f47389b95507238f8cc2014`  
		Last Modified: Tue, 04 Feb 2025 07:51:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1382cf59890b152f778818b5453406d3b13d148dcffeccb22e855a182252d3f5`  
		Last Modified: Wed, 05 Feb 2025 05:56:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d9d84b4116fc50826f2ef596a324b75512636e7ca6734131a505950a585cf2`  
		Last Modified: Wed, 19 Feb 2025 02:14:07 GMT  
		Size: 13.8 MB (13824142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a88abc3c3cc48606773cb91e70325b9a3ffe5dbf1c653197d48a634a3e46cb`  
		Last Modified: Wed, 19 Feb 2025 02:14:07 GMT  
		Size: 230.7 KB (230719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d8d00e222c991a39e3642e731953388ac5dffc876ee6d66fb3e5e28b8016eafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b6e3cb9805507b7cc987953f761f41d6a5f80d8f795f98ed780c1ddd4a65b0`

```dockerfile
```

-	Layers:
	-	`sha256:b254c59876b191d503b800baa55db542286986d6ebf41f1b59da96c25cccb163`  
		Last Modified: Wed, 19 Feb 2025 02:14:07 GMT  
		Size: 3.8 MB (3771253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd026aab31d12acb3be2d5f612999c96361a20fecbebc83023109c35d4a57db`  
		Last Modified: Wed, 19 Feb 2025 02:14:07 GMT  
		Size: 21.6 KB (21580 bytes)  
		MIME: application/vnd.in-toto+json
