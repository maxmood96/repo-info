## `tomcat:jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:b6bad0b735012226e0e887222ed30a6e0baf3e3c7c6c739f83e35d1c2e682d2b
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

### `tomcat:jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:2ceb9f86114a55b73d5d20ae0a65e20b93dea45a57029b004cb078a9f9df81aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107086763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab592a47b84fca7d40b7cf8dd216e00ddb47e5e11603dab219f4403412f83362`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:18:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:18:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:18:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:18:14 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:18:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:18:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:18:14 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:18:14 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:18:14 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:18:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:18:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:18:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:18:21 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:18:21 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:18:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabf0c4438e2613c495d680a046e02808ced16df84bd9647a11f7c584625d4a1`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b40c59e949b7304682e700d3538e2356cee2db22a6979780388ea75578e76a`  
		Last Modified: Sat, 08 Nov 2025 19:18:37 GMT  
		Size: 14.1 MB (14112227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8208c09516c5d8d580dc43075f05b74b81d75157bcf1881c5a0f4224fda14e01`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 229.6 KB (229604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:5260cf34d1ae73cb3f49cb9a7a06ed55ef0fc740157294b5773ff964a6d6fd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3963317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a9872a1a13953c2087fc4cf2dacc5761555321c25a07a0e32d89eb411f6bc1`

```dockerfile
```

-	Layers:
	-	`sha256:fd329f17faa7a5be37cbbc6474cf9864863ae59f3ae6c65702b9cfdef4c3b06d`  
		Last Modified: Sat, 08 Nov 2025 21:38:41 GMT  
		Size: 3.9 MB (3941769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf38325343aa93f620d08bc7908fb8a69e865e362b12a49ad90d1f624236ad5`  
		Last Modified: Sat, 08 Nov 2025 21:38:41 GMT  
		Size: 21.5 KB (21548 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:050200a58d2bec85b43382c29bf17b3c780c0b5dbdd132649e2774579c6a2008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101550667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae696d27135f5f41ce8ae5a313de3bd9bdc3d90ca0baa42b328582bf99df7ad`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:33 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:36 GMT
ADD file:7939f961de8cf091ed251aa1d8e432c16ec7506130ed39a1db4028efdad8fbfe in / 
# Wed, 01 Oct 2025 07:06:36 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:25 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:56:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:56:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:56:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:56:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:16:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:16:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:16:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:16:26 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:16:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:16:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:16:26 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:16:26 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:16:26 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:16:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:16:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:16:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:16:35 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:16:35 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:16:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:33392950d914bf1e16e980fc0bbcec6367a2d2b8ecbd726dc5fc65b4c96ce79f`  
		Last Modified: Wed, 01 Oct 2025 18:17:15 GMT  
		Size: 26.6 MB (26643435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1345e0b53413e99f889c26d5ec17e483aedeef73cf90f7586033224325438fc`  
		Last Modified: Sat, 08 Nov 2025 17:53:05 GMT  
		Size: 15.9 MB (15889483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fe97ed48ae2b98ef0d4fbf1f5de459c12f31e50bb8d11d0b15aa5688aef408`  
		Last Modified: Sat, 08 Nov 2025 17:56:27 GMT  
		Size: 44.7 MB (44723983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000893011f6cb759e44d937042f81e5f23c3f17378b7da321861c214afc7e81f`  
		Last Modified: Sat, 08 Nov 2025 17:56:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d48d3d2407dd98c2b710dc3b7b04c796f870c40aca83dd153b179c608c9f35`  
		Last Modified: Sat, 08 Nov 2025 17:56:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f196c3278a125ef13ef36990dc60938f723c9a3a29fe84b8bb42ab844737e6b`  
		Last Modified: Sat, 08 Nov 2025 19:17:07 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dcb5d29aadcca09fd6cf5c63bb95f452dc370f9234300fc552cfd364006969`  
		Last Modified: Sat, 08 Nov 2025 19:17:09 GMT  
		Size: 14.1 MB (14088788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43419120bba0916ef3d6d8745301297100244e76ff3279d346244080c18d3e8e`  
		Last Modified: Sat, 08 Nov 2025 19:17:07 GMT  
		Size: 202.3 KB (202334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:2b38f4eb8323ac7402b3cd0f7431357831e5ff1f955b206764a08670c1d558e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d45c85ce1c362c9b8a77bc9569068af8458c222d028ff6e678f44b21c1f93c9`

```dockerfile
```

-	Layers:
	-	`sha256:10fc371b4a67b5977bab49cff18198f8279cfda2f35b2ce94118544b9a063e69`  
		Last Modified: Sat, 08 Nov 2025 21:38:45 GMT  
		Size: 3.9 MB (3944112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a4e3499a455a72a4dd34e6521dab14138e6f9fe3d7e050ec6785b0a1b57f04`  
		Last Modified: Sat, 08 Nov 2025 21:38:46 GMT  
		Size: 21.7 KB (21676 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:bdb2cb394215cb9ba0db23a2ccc3e815b985723cfe8d2baa1fab4c6a74d8278d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104335118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706389d45caa62de975eb8374cc7583718de5ade52b5c1c87539d015f43f2e4e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:17:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:17:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:17:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:17:14 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:17:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:17:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:17:14 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:17:14 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:17:14 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:17:15 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:17:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:17:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:17:23 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:17:23 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:17:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b4ef68d752406edc2f7253c01aa2481db51f4904395a518e86993369dd2e9`  
		Last Modified: Sat, 08 Nov 2025 19:17:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb10046ded196077c656e57606a4946a7257681cd59b0d2a4bf4fe066745f7`  
		Last Modified: Sat, 08 Nov 2025 19:17:39 GMT  
		Size: 14.1 MB (14116050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c36927928d4667c956abbfc2d7ae3219b726f02989aaad5ca36ba088c1421d`  
		Last Modified: Sat, 08 Nov 2025 19:17:38 GMT  
		Size: 228.7 KB (228696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:28206448db7f3d73c044ba2952045bce3d64c96a95141a13b3ec29544bb38436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3963158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2980a61126238ca975727fd7b177275811fab45390dacd45041a0f2a0e7f183`

```dockerfile
```

-	Layers:
	-	`sha256:8ceab3e1dc54ad3efd1b89a22b029165fa518a42219d8375dd57a1ca86098450`  
		Last Modified: Sat, 08 Nov 2025 21:38:50 GMT  
		Size: 3.9 MB (3941450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b0150dfe6015d9cd161cda7518026b427b92366df541adfc48ffa0fe3d0aff`  
		Last Modified: Sat, 08 Nov 2025 21:38:51 GMT  
		Size: 21.7 KB (21708 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6236ddbe329228a78dedf9131ceb697683ef39a10e6560f8bccf6315ccb3f144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113340354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f121c4bfaa9ffe040489598d19213c660367ad42d93ec7876d1148dc3083b39`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:17:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:17:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:17:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:17:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:17:59 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:15:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:15:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:15:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:15:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 22:14:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 22:14:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 22:14:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 22:14:06 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 22:14:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:14:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:14:06 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 22:14:06 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 22:14:06 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 22:14:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 22:14:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 22:14:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 22:14:15 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 22:14:15 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 22:14:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0104670d5e6da865b4b88cd9bc61191ca43fd2ed27ab1483145fb0f36d46b694`  
		Last Modified: Sat, 08 Nov 2025 18:16:26 GMT  
		Size: 46.9 MB (46881233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8d2d4364d266318229f93a7df9d0933e2e24afe844e7e7d2b138d750b18bf`  
		Last Modified: Sat, 08 Nov 2025 18:16:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c76616592bb95c3807991245131992a94dc98152c99c7fa4347459ac97341d`  
		Last Modified: Sat, 08 Nov 2025 18:16:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db9513f1288436bcb3a3918cea1f546f9fac71ddc99e15bec00c04fcae5d108`  
		Last Modified: Sat, 08 Nov 2025 22:15:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69db66522af7436ecb7bd4cd6864944ded23d9352af624820f2ca23c0fcb337`  
		Last Modified: Sat, 08 Nov 2025 22:15:05 GMT  
		Size: 14.1 MB (14126972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17b4e0e179f1b494a3f8b44e5c2c3007b76362e16b6d9c0616cc9ee176e71e`  
		Last Modified: Sat, 08 Nov 2025 22:15:03 GMT  
		Size: 259.0 KB (259040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4e4fcd12aa44d4a9f8cc22495e9e1da1dcc7b1afe61cd55d82499132c6686ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9aeddfd344fd95a158323db4a5fc28d33c4e7f2fa2291ccbecbde76b6466bb`

```dockerfile
```

-	Layers:
	-	`sha256:72380f3eefdcce955dad84ae8ad07b94e1d49dc98e3256c4c8789b88136caf5f`  
		Last Modified: Sun, 09 Nov 2025 00:32:10 GMT  
		Size: 3.9 MB (3945863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08592c80ff0d5b2c90b680d51972b4884fe44998255f5a7a13c10f098e3443c`  
		Last Modified: Sun, 09 Nov 2025 00:32:10 GMT  
		Size: 21.6 KB (21605 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:30c4a75930a0d3a41e3b870b11886fa3b923b01cf3fa38fcd0b76a8851df529d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102533977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e297f79f2aaaf669592ce846e0e0e7e9cbd1599d1c3a9eb61829f9415d4275c5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 20:57:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 20:57:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:57:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 20:57:43 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 20:57:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 20:57:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 20:57:43 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 20:57:43 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 20:57:43 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 20:57:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 20:57:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 20:57:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 20:57:49 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 20:57:49 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 20:57:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625d63bdf6c125a342be6db5902411b8a367f28e03bf7dced87adfe9dcf1e34a`  
		Last Modified: Sat, 08 Nov 2025 20:58:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431a5cc6470190e2396de7dc72c6d47bb086a74517eea95c5a1f551da93593b`  
		Last Modified: Sat, 08 Nov 2025 20:58:13 GMT  
		Size: 14.1 MB (14116696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c16392d1c96bb511b3b27c655b586c34099772e0dd12e210c580dde535d05a`  
		Last Modified: Sat, 08 Nov 2025 20:58:13 GMT  
		Size: 230.8 KB (230800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:dce4d8892b62304fd9430d4dd4c438ec96c1001e964da650edb083511befcc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2d746b83d229107004cd4b8a9c4df475d8508636bb9213c2cfce1896595c0e`

```dockerfile
```

-	Layers:
	-	`sha256:5fdac44d7867223ff253f0125912fba14eb3d4766d512dd80dcd53f3781d3aa9`  
		Last Modified: Sat, 08 Nov 2025 21:38:58 GMT  
		Size: 3.9 MB (3943360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35818bcc3fe25b93062bcd103e62152bdc4feb823507de9973eac5995347ef8`  
		Last Modified: Sat, 08 Nov 2025 21:38:59 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json
