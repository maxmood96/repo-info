## `tomcat:jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:50a40e5a2aaa6d36875bfa85da105a5fb057821163b512794ec4eac7c14a7783
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
$ docker pull tomcat@sha256:f40321dfed77281c51e6589435541db295316680c0fd1842258930be01bbbe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109981454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744dde12a3a273e9e2cbf16768546d35f32555b35d52368c37272aa222945a35`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 17:34:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 17:34:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 17:34:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 17:34:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 12 Jul 2024 17:34:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 17:34:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
WORKDIR /usr/local/tomcat
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 12 Jul 2024 17:34:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 12 Jul 2024 17:34:49 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_MAJOR=10
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_VERSION=10.1.26
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_SHA512=0a62e55c1ff9f8f04d7aff938764eac46c289eda888abf43de74a82ceb7d879e94a36ea3e5e46186bc231f07871fcc4c58f11e026f51d4487a473badb21e9355
# Fri, 12 Jul 2024 17:34:49 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT []
# Fri, 12 Jul 2024 17:34:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcac2a60c8a6f89a0f9c541976baee59b0f7760d2e0436ff0b3e28073ed3487`  
		Last Modified: Tue, 23 Jul 2024 01:11:15 GMT  
		Size: 53.5 MB (53513754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04efe3dc9eb87c507252d441b92889ed5200bda63aa14d4db53e2e43a1f663`  
		Last Modified: Tue, 23 Jul 2024 01:11:08 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22715d4e4b06cf2d6e38b45f390b8d34110ed3b239c609bf69d95c30e69149cc`  
		Last Modified: Tue, 23 Jul 2024 01:11:08 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff92f23f9638dc19d64b05b3c59d8e78ff400ee6a077e8324bbf680786effb9`  
		Last Modified: Tue, 23 Jul 2024 03:03:50 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fdaf7cf2a6865f52081e8c1ffcbe172056ca3a7d4455219e829419ce9c64dd`  
		Last Modified: Tue, 23 Jul 2024 03:03:51 GMT  
		Size: 12.9 MB (12937134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13400539395ba94e1efdcbd738017df5376ca3989105190a30fd9b095d0953e2`  
		Last Modified: Tue, 23 Jul 2024 03:03:51 GMT  
		Size: 217.8 KB (217836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:000c1b53c31b903780b229281a9b72b4c792718c47183291ec1e7eea2fce3e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651965eba9a190b1011a2f9f855b5475dc71e103081e068b39652dfc11a2a9e5`

```dockerfile
```

-	Layers:
	-	`sha256:9c01608e7955a3b63bc8c784f4795a090cdad4b01ec9010b017317c03c38849e`  
		Last Modified: Tue, 23 Jul 2024 03:03:51 GMT  
		Size: 3.5 MB (3532947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9602c06c63ccbadaaf36c37c67de67a8a24318a815d949d8c62fa8d1a57aeb5`  
		Last Modified: Tue, 23 Jul 2024 03:03:50 GMT  
		Size: 24.6 KB (24574 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:50a761b8eedd152fd839d09a12ce0976bcd41b03f6c28973a41c6c0c1a671ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (107012042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1f88e720019afe78843dbdf0d63dd72f5e01fb3439cdb3fda594d39d28e6c5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 17:34:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 17:34:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 17:34:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 17:34:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 12 Jul 2024 17:34:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 17:34:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
WORKDIR /usr/local/tomcat
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 12 Jul 2024 17:34:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 12 Jul 2024 17:34:49 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_MAJOR=10
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_VERSION=10.1.26
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_SHA512=0a62e55c1ff9f8f04d7aff938764eac46c289eda888abf43de74a82ceb7d879e94a36ea3e5e46186bc231f07871fcc4c58f11e026f51d4487a473badb21e9355
# Fri, 12 Jul 2024 17:34:49 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT []
# Fri, 12 Jul 2024 17:34:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aecf5753adadd0693c04a6292d2440325b410fbd3e991d5cda098b52a42a3c8`  
		Last Modified: Tue, 23 Jul 2024 04:16:15 GMT  
		Size: 52.6 MB (52641370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5698ce9633c7de7c15b903b6daa1ca880225ba96158d8693d05504a610c6b528`  
		Last Modified: Tue, 23 Jul 2024 04:16:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d24ede5177b85c3e92e2496f0c18937cef5eed6d8c8fc1ca78b12cac2f77c8`  
		Last Modified: Tue, 23 Jul 2024 04:16:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e670d52a382c5657011e2f21bcd40f92ef22411d4365664b6742b6a580e9bb80`  
		Last Modified: Wed, 24 Jul 2024 18:03:32 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbede007dea44844170ec7e1a45069883d91f70bea55929181225d663d172ceb`  
		Last Modified: Wed, 24 Jul 2024 18:04:00 GMT  
		Size: 12.9 MB (12937952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d4a11da715ce8a2b3b763c620315277634539472d3047b64a1bfed78659d7`  
		Last Modified: Wed, 24 Jul 2024 18:04:00 GMT  
		Size: 216.8 KB (216827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:65e16b65e261c686b56dde6688e0121fb07a5303cf5f6898c50d0e25b355bef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9f918031ddf8bcb156b8faaf6398b50568447b3d605e36b370ba9cd3b39220`

```dockerfile
```

-	Layers:
	-	`sha256:90bcaa2ba8661ac00d6683a5715de1d4113f297b86672759ae0c68fa619bff48`  
		Last Modified: Wed, 24 Jul 2024 18:04:00 GMT  
		Size: 3.5 MB (3533335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c41fd2200c0392c19a754b96a43984d0bd7e5dec4a00a30d3e551d8338bb9036`  
		Last Modified: Wed, 24 Jul 2024 18:03:59 GMT  
		Size: 25.3 KB (25334 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:dc9cc47b0be9602300069c26cb8860e7a7153cbb332cb45911520c040a6ae176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116042846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbd1a4df6b2ec87680cb128fc77b64557ec591e959c5289a73f34f9e916fd26`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 17:34:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 12 Jul 2024 17:34:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 17:34:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
WORKDIR /usr/local/tomcat
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 12 Jul 2024 17:34:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 12 Jul 2024 17:34:49 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_MAJOR=10
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_VERSION=10.1.26
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_SHA512=0a62e55c1ff9f8f04d7aff938764eac46c289eda888abf43de74a82ceb7d879e94a36ea3e5e46186bc231f07871fcc4c58f11e026f51d4487a473badb21e9355
# Fri, 12 Jul 2024 17:34:49 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT []
# Fri, 12 Jul 2024 17:34:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702f9087d30dc482e203456fc23911476da9e8831f6836fefefd9c8c262cc3e`  
		Last Modified: Tue, 02 Jul 2024 05:06:37 GMT  
		Size: 53.5 MB (53538142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c57f2ef768e52a23740f79ac68b7f0640871761642412dab03407842287e718`  
		Last Modified: Tue, 02 Jul 2024 05:06:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d070f95330bd18c45b7847bfa55e6a8ec1833b40a10b0663ed5912c50b1b26`  
		Last Modified: Tue, 02 Jul 2024 05:06:29 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8a1422eb22c17604b6ef47d627a9398822713d396b5d7a6a9c7f5d70c21b69`  
		Last Modified: Wed, 03 Jul 2024 16:58:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f545ae7b349189f0818d181bb935b2f9dfa712cc3a11ea756178c4ed9d3250`  
		Last Modified: Fri, 12 Jul 2024 22:58:30 GMT  
		Size: 13.0 MB (12950659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f0925284322930bccb3b48fe8532d2111bd9065207dd546b7d848086a50af7`  
		Last Modified: Fri, 12 Jul 2024 22:58:30 GMT  
		Size: 249.8 KB (249753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0c20f066e630edab5c1853532e4910e11df98c953fb21cdfd9b1e7daa50a853e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee1ec4866c8e0c0c4b6bbfc5cff14159ae8a10159d8cb2b6cb7550eb347fe04`

```dockerfile
```

-	Layers:
	-	`sha256:a079a85b041a4f1a32eeca8d601b227415195441a58a16b82c66c2b8a45cbdc3`  
		Last Modified: Fri, 12 Jul 2024 22:58:30 GMT  
		Size: 3.5 MB (3505540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:466604e1a5ffee556f6ac8995baf8471f91ce13b1b96fc3514cf7b9fdfe1483b`  
		Last Modified: Fri, 12 Jul 2024 22:58:29 GMT  
		Size: 24.7 KB (24692 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:e20ac838bf5d2848690694df1f0722f587dd722e6c297c37ad9e917a61e202b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104423259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d472233298ae4a857128628fcf4e840a559ead30eea60630d866f62b022641ee`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 17:34:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 17:34:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 17:34:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 17:34:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 12 Jul 2024 17:34:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 17:34:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
WORKDIR /usr/local/tomcat
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 12 Jul 2024 17:34:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 12 Jul 2024 17:34:49 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_MAJOR=10
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_VERSION=10.1.26
# Fri, 12 Jul 2024 17:34:49 GMT
ENV TOMCAT_SHA512=0a62e55c1ff9f8f04d7aff938764eac46c289eda888abf43de74a82ceb7d879e94a36ea3e5e46186bc231f07871fcc4c58f11e026f51d4487a473badb21e9355
# Fri, 12 Jul 2024 17:34:49 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT []
# Fri, 12 Jul 2024 17:34:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eaa70dc31cdad42121b062dd92b14960ba0a992a5bedede9795f6d11bf4a38`  
		Last Modified: Tue, 02 Jul 2024 03:54:48 GMT  
		Size: 13.0 MB (12954922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec92b6a2be0d15eabde554357a220ffafedde720e7b4534d283070a82435ccf0`  
		Last Modified: Tue, 23 Jul 2024 02:45:24 GMT  
		Size: 49.7 MB (49669531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f70991318334da0b7743660016407ef8a1d5cb49383ccbc0b9b98274aaee675`  
		Last Modified: Tue, 23 Jul 2024 02:45:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9d599c4ebc8e5ecfd1e8553f4f0257393d08cba9be21a755415ec38b9cc34c`  
		Last Modified: Tue, 23 Jul 2024 02:45:17 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd93e0e060a658215d0fdf63265a9accc04e971f6e80335fc3fe66f2ce7f475`  
		Last Modified: Wed, 24 Jul 2024 19:47:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ca39619e69c103266fa4628cc96931aaa30f06c868b4ec019a6bb24132e547`  
		Last Modified: Wed, 24 Jul 2024 19:48:49 GMT  
		Size: 12.9 MB (12940204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f876f119537404fbffe4203d773b77ea4b9697c3ced6ee201ff9b2b4e997832`  
		Last Modified: Wed, 24 Jul 2024 19:48:49 GMT  
		Size: 219.3 KB (219334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b9988e0986063fae733b1955158ef258a6de5c57ce90ad45dd5a4781308ab688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008e7b34072eaf8ae2a89325b5800ffa9a2acbe8e7ab5471d259feb97355ef10`

```dockerfile
```

-	Layers:
	-	`sha256:e54dad36196c26ec4cd99b5259467645eb855080969b85457019d3d94ce26ec4`  
		Last Modified: Wed, 24 Jul 2024 19:48:49 GMT  
		Size: 3.5 MB (3534063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5204735968a6a6a29d8ac9cb0b5f5bcf71752629ab845256bf0dee25eb1d16c`  
		Last Modified: Wed, 24 Jul 2024 19:48:48 GMT  
		Size: 24.6 KB (24599 bytes)  
		MIME: application/vnd.in-toto+json
