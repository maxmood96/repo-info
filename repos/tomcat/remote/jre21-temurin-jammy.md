## `tomcat:jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:ccbe46c30dd6f0153200da327d744ccfd0eea1d6a792be4541026bd5e1c9d46b
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
$ docker pull tomcat@sha256:197b03d078c0c575cc2a4498e858dfe09e7531e4b12b0d895dc365ae50a062b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113439731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04008bdfab63b173781f8068b3aaea6cb126a3824db40af4b2a6f2b2888fcef`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:32:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Apr 2026 22:32:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:32:55 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 15 Apr 2026 22:32:55 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Apr 2026 22:32:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:32:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:32:55 GMT
ENV TOMCAT_MAJOR=11
# Wed, 15 Apr 2026 22:32:55 GMT
ENV TOMCAT_VERSION=11.0.21
# Wed, 15 Apr 2026 22:32:55 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Wed, 15 Apr 2026 22:32:56 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 15 Apr 2026 22:33:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:33:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 15 Apr 2026 22:33:04 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:33:04 GMT
ENTRYPOINT []
# Wed, 15 Apr 2026 22:33:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e434fc527435d14ec923b0acc9953dacb6ec1bd892d7d48eb54eb7a312aa0f5b`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 53.0 MB (52985647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf851d0cdffee253ce46e5cdf9a5c19c21be33fa5231efb26464aa3846ec0f`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ed9e099432789068ce1d3578eeff3f3c7b7db69e22b254afc8941073a1cfd`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc22756636d18b832eb76c824f99edbfe3ca9e9a83f19230ca2aadafd699f57`  
		Last Modified: Wed, 15 Apr 2026 22:33:12 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80249aa4294d93b366fe5f275b5f347c2d3e0bbefffcbceb41a97b05989fb5a4`  
		Last Modified: Wed, 15 Apr 2026 22:33:13 GMT  
		Size: 14.3 MB (14334353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84fe5632b23578fa34744c4ce0511182315eb69601ff53d483e0833ebc4fb85`  
		Last Modified: Wed, 15 Apr 2026 22:33:12 GMT  
		Size: 229.7 KB (229736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:5b5ef75873c9933781f176f3e5101e91a7b2dac8ca0ef258aaf12ae19b2fa0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36c34d0fe8cc2b66546a466dc10b88c2f5ec8da5633ee9187cf954f723935d3`

```dockerfile
```

-	Layers:
	-	`sha256:3d9e751442ae281fd576d30335276efee1ae8ff49c3004f43da6c7d2ba3c18cb`  
		Last Modified: Wed, 15 Apr 2026 22:33:12 GMT  
		Size: 3.9 MB (3942767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bc793c81a55fd33b6fd68a27f4464b36f626dc603617aff67bb076a953e54f3`  
		Last Modified: Wed, 15 Apr 2026 22:33:12 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:8bca294cf6812a7ec4add0574349068857fef4ab709d6d0cfff5de9042b42947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110403379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39420e4d5cd10657700ecf207c61994ce61c0d73f6c13f86f0d3bfcb56fe1fe7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:41:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Apr 2026 22:41:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:41:25 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 15 Apr 2026 22:41:25 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Apr 2026 22:41:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:41:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:41:25 GMT
ENV TOMCAT_MAJOR=11
# Wed, 15 Apr 2026 22:41:25 GMT
ENV TOMCAT_VERSION=11.0.21
# Wed, 15 Apr 2026 22:41:25 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Wed, 15 Apr 2026 22:41:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 15 Apr 2026 22:41:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:41:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 15 Apr 2026 22:41:34 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:41:34 GMT
ENTRYPOINT []
# Wed, 15 Apr 2026 22:41:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9976ad46810a0a1b423803f447753b429b04144c676b1d429a09e94303e03d1b`  
		Last Modified: Wed, 15 Apr 2026 20:34:43 GMT  
		Size: 16.1 MB (16075150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471cc4701b229f4446be5d8c981bd3d0eeb429de8c98c2bd5869d49f549d8e4d`  
		Last Modified: Wed, 15 Apr 2026 20:34:48 GMT  
		Size: 52.2 MB (52155611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df963689a6ce26de9c84e4dc05e2f0a2086bdc9709bd12098f0a1f50ddd4485`  
		Last Modified: Wed, 15 Apr 2026 20:34:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58e1d661ef05644b20d264beb4376aab10dc6ab7dfd0fa292caf433a1b564d6`  
		Last Modified: Wed, 15 Apr 2026 20:34:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48521c4705fb83cb48152fd0ae1c70f41d91e523fedf4c09652bc69eb910f0ed`  
		Last Modified: Wed, 15 Apr 2026 22:41:44 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1579737c7d2c9fb210a0092fe377905e0bd33d285ad10b42785134ffaef57d`  
		Last Modified: Wed, 15 Apr 2026 22:41:44 GMT  
		Size: 14.3 MB (14334747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9579cde7bc1ce647f748d3b200bc5e420486a87aff23d9b6b2a38a799726db59`  
		Last Modified: Wed, 15 Apr 2026 22:41:44 GMT  
		Size: 228.7 KB (228688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3a9a85245b2e68499e88f1504fc900d1d8eda6ef9fdce233381ace9bbf0126f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec7356726c55fa0c73facd953488736ecdd2297f4ca8a7a7fd11da270d36874`

```dockerfile
```

-	Layers:
	-	`sha256:973487a29c24a02387dbbb9eecd2845778f9173d90b71677fc5622f81095763e`  
		Last Modified: Wed, 15 Apr 2026 22:41:44 GMT  
		Size: 3.9 MB (3942448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae81fc03c517733ca770ad7944683f900b4da44e0abaec3fb0a0c8a4c6547932`  
		Last Modified: Wed, 15 Apr 2026 22:41:44 GMT  
		Size: 21.7 KB (21705 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:1f937dfba6aaea90964f165c4f4bf95e131dbef5d1eb9e362e5255b141da4711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119854772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840fd2a2697b42132ee41dbab5fa9c6a52b80ecb5096b5fae8e5716a162c5ef9`
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
ENV TOMCAT_MAJOR=11
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_VERSION=11.0.21
# Wed, 01 Apr 2026 22:11:16 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Mon, 06 Apr 2026 19:09:45 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Apr 2026 19:09:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 19:09:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Apr 2026 19:09:53 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Apr 2026 19:09:53 GMT
ENTRYPOINT []
# Mon, 06 Apr 2026 19:09:53 GMT
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
	-	`sha256:91ab1d95424f84c32cf5da628c219b3f53cde129ea70469469ce95699922281d`  
		Last Modified: Mon, 06 Apr 2026 19:10:09 GMT  
		Size: 14.3 MB (14348067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98c821ba82543a958fb06005323c0aa3a01631347c350192a929b45527c2472`  
		Last Modified: Mon, 06 Apr 2026 19:10:09 GMT  
		Size: 259.2 KB (259199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:37d84805cc9c8b8b1220449cded27a011e1bd4fc113ea0c690a044297482b146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777863588a523c1201140ae33a36240e56a596e28143f4fb8abe71307cb3efc1`

```dockerfile
```

-	Layers:
	-	`sha256:e1577874dcffbee9fea54cc0fcc1fc26017d8960f658ea392744c4c2476ef317`  
		Last Modified: Mon, 06 Apr 2026 19:10:09 GMT  
		Size: 3.9 MB (3946861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c60744af3f78b48009cf7aaafff823f5878714fe86209415254eb5a52ecb4c5`  
		Last Modified: Mon, 06 Apr 2026 19:10:08 GMT  
		Size: 21.6 KB (21603 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:c168e309d0d2615b23d649b56bc9988c306738f177119b59ab79a694b35db808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108463342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c8e0d3d546dfa75310ec349ad2aa440dcfeb0928cecd2ebadc4aeff5a0ad49`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:04 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:46:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:46:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:46:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:46:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 01:23:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 16 Apr 2026 01:23:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 01:23:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 16 Apr 2026 01:23:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 16 Apr 2026 01:23:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 16 Apr 2026 01:23:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 16 Apr 2026 01:23:27 GMT
ENV TOMCAT_MAJOR=11
# Thu, 16 Apr 2026 01:23:27 GMT
ENV TOMCAT_VERSION=11.0.21
# Thu, 16 Apr 2026 01:23:27 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Thu, 16 Apr 2026 01:23:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 16 Apr 2026 01:23:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 01:23:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 16 Apr 2026 01:23:33 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 16 Apr 2026 01:23:33 GMT
ENTRYPOINT []
# Thu, 16 Apr 2026 01:23:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcb54377fdd395a9a5653d000164548b21b31b11ea73a57fb207b8cf12e0d51`  
		Last Modified: Wed, 15 Apr 2026 20:44:37 GMT  
		Size: 16.2 MB (16150488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2526fc67504b9cd766ce67e2659059aaa401a05c510bf78d9bcfcfe68c8a349b`  
		Last Modified: Wed, 15 Apr 2026 20:46:32 GMT  
		Size: 49.5 MB (49540916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491125d5186618e1f9b2e725f2af6bec01ba47b3911f5beeac7e0fef4e20874b`  
		Last Modified: Wed, 15 Apr 2026 20:46:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5ca14cea1d3e1902a61aa225b935a1e5651668925e2b2af61b47ce042e3bc1`  
		Last Modified: Wed, 15 Apr 2026 20:46:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a642d2389f14290d1688a038fdb49703831e5568dde215da30bb0a6e14f13`  
		Last Modified: Thu, 16 Apr 2026 01:23:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3298ba4c1a768e70533ac78c9807cd12642e4b7763927dfdad8be6b07f84eb2d`  
		Last Modified: Thu, 16 Apr 2026 01:23:48 GMT  
		Size: 14.3 MB (14336047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed192060d1105ac8807c968c940d984573b9d8919aa5f1eda6a230dda0f51b19`  
		Last Modified: Thu, 16 Apr 2026 01:23:48 GMT  
		Size: 230.9 KB (230948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:9a9c4afac89658409dde6818cb6a7d71432c2c1ce6c1eec356b4093835962a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e824ab92a8f42e83bee7bdde3bac8b731a625df4c0db6b5044fa2eb94b332b`

```dockerfile
```

-	Layers:
	-	`sha256:4533e63b4608f52ac87db6d8eebef15b483a859f40f2040fbe64a36b5ea01a3a`  
		Last Modified: Thu, 16 Apr 2026 01:23:47 GMT  
		Size: 3.9 MB (3944358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64914313cac35aeef9dbdead099908c4590752da14e4584d293bb96d6f8dbcd8`  
		Last Modified: Thu, 16 Apr 2026 01:23:47 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json
