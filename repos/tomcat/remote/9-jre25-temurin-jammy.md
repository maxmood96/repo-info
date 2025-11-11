## `tomcat:9-jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:1cb5e0b9f829213242a7cb1ce85aff3c021b31a4646a7a04f744f9eab5b2d129
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

### `tomcat:9-jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:d30f4c97a0eabf806cc887d82a6650e0c10591971ab4a0f8699b53551e0b0843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117617834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a1778a3a0b5f2a79e0b2b752c73293eea70aa0ffd47db49ef7da12f86ac8d0`
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
# Sat, 08 Nov 2025 18:00:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:32 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:13 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:13 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:13 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:13 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:13 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:20 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:20 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6510df90aaf6ceaf3f951fc7d64e89b65b9b64143fd6e6f2f9f1f676545ef58`  
		Last Modified: Sat, 08 Nov 2025 18:01:16 GMT  
		Size: 11.4 MB (11404548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2228750769407eb28fa51d649bb3f5510864a02c1b7032180851726ce478f674`  
		Last Modified: Sat, 08 Nov 2025 18:01:29 GMT  
		Size: 62.7 MB (62687787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c996064fc0386a5d3a1a3d9fa56ee380b6e1bc2b989942f6a8528480102d2fe`  
		Last Modified: Sat, 08 Nov 2025 18:01:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5179777ced81a00f8b7c061ccad0488406ee9d58c2ba338ebe7bebfb7470e793`  
		Last Modified: Mon, 10 Nov 2025 19:12:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ec0a1853d93e13f2d27485131213ef860c19e63424592a0bd85bbaf106fbdf`  
		Last Modified: Mon, 10 Nov 2025 19:12:34 GMT  
		Size: 13.8 MB (13772731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb233dff11f97634f70bfdb7b9f82b49c4313fd3a8cdfea9bffcf820afec40dd`  
		Last Modified: Mon, 10 Nov 2025 19:12:32 GMT  
		Size: 213.4 KB (213433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:afb20be6355a01866d1c884d575189c53c8098281e88f4bb6d6a36c3786dcf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341948fb12f0a8658cb27db43fd17a75eb4fc6fa0c11d383298d04adfd2c31a9`

```dockerfile
```

-	Layers:
	-	`sha256:1876595acc3033bbaa5371df90eee6143e69d2472ea5303dad2f5adc6683465e`  
		Last Modified: Mon, 10 Nov 2025 21:48:02 GMT  
		Size: 3.7 MB (3704983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e9d73dfffc1e9eb2696d5dba4c0a5d9e1d5beb5a963c8f60a92f0455cb65f20`  
		Last Modified: Mon, 10 Nov 2025 21:48:03 GMT  
		Size: 21.2 KB (21202 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b1f19c725ce48b506bbb602a0037f26b5e61f6f4fcd8dc021e6860eea4260f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114373230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e58b114fa6aea479a06fbc05c08aee5d06405aa3ceb919730b3f7d9b3c06d6a`
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
# Sat, 08 Nov 2025 18:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:02 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:06 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:06 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:06 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:06 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:13 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990beddf5e4b01af9c65b599641437c6ef7ac83d823f2d3b2f2327dbc8a6059`  
		Last Modified: Sat, 08 Nov 2025 18:00:45 GMT  
		Size: 11.4 MB (11357747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86e09fcb6ff39a6c4b94c1dafbba559fb4d24acb5c8e74cd5a39210562e6db7`  
		Last Modified: Sat, 08 Nov 2025 18:00:48 GMT  
		Size: 61.6 MB (61638741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae07793e0e1ee544d90107dbaec35e20c92afc4156d29b01c572d3a5a7e404b`  
		Last Modified: Sat, 08 Nov 2025 18:00:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed738f49ad71f63b4d3bec3facf7be2bfb93a7ecabd3706845427b4b0d3f311`  
		Last Modified: Mon, 10 Nov 2025 19:12:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397c137780bbe282b9509bcea3c986e157b7085d4f53c6bb9e8ff23d696fed99`  
		Last Modified: Mon, 10 Nov 2025 19:12:29 GMT  
		Size: 13.8 MB (13778556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a7915c3e93393686ef8ab5f9e3131adab9a8d4a40abe50f6b4015d9f492702`  
		Last Modified: Mon, 10 Nov 2025 19:12:27 GMT  
		Size: 212.6 KB (212563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6ba53138e9147a6d27cddad55d94f8bdfe99efd3e8b013e3eb9c95a5f9d9603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c87f22b1c3969dbb12f70497ab192b116acfca5e1c8b731d58dffb0781468f`

```dockerfile
```

-	Layers:
	-	`sha256:208409df01cf3923c5c3c3eb8dc7809b3dfa2026ff62e4a5d789e2e11c6ac332`  
		Last Modified: Mon, 10 Nov 2025 21:48:08 GMT  
		Size: 3.7 MB (3704634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ab00afb5fe50c0a31d722203c4a10def179bdc26002d6025ee2ffea58128a0`  
		Last Modified: Mon, 10 Nov 2025 21:48:09 GMT  
		Size: 21.3 KB (21349 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:c56937abee34e292c8613736e680819eb4948cf28120c4d7bb3a01effd943edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122508557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1709f894f8494a1ac0b87c825af2bad0edecb946bf17fdc27d11ac0b3d51c7d`
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
# Sat, 08 Nov 2025 18:33:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:33:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:33:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:33:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:33:29 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:33:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:33:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:33:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:33:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 22:10:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 22:10:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 22:10:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 22:10:50 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 22:10:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:10:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:10:50 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 22:10:50 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 22:10:50 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 21:20:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 21:20:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:20:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 21:20:25 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 21:20:25 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 21:20:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05a419dbbdae4c74ce8cbea20f33b711554ca281ea5b632c3cbf7fed8d819f4`  
		Last Modified: Sat, 08 Nov 2025 18:34:32 GMT  
		Size: 11.9 MB (11893670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efacde85c6a9be3b7e0b804b464c7e4f0160319d2406c6114a8cbde0e096cec9`  
		Last Modified: Sat, 08 Nov 2025 18:34:34 GMT  
		Size: 62.1 MB (62123046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db4f445e55d6ead60bf318ddd25e4ca7e4425be6b9f26330912f1e66c3aaf26`  
		Last Modified: Sat, 08 Nov 2025 18:34:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4502b6af0a831da3fa12abdd640b138a274f9a2acb7deeda30a7d1a4f1cee23`  
		Last Modified: Sat, 08 Nov 2025 22:11:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cf97284415802782fd2992c14ab3acb99744e33710ee242df3f8c24b5fae6f`  
		Last Modified: Mon, 10 Nov 2025 21:20:51 GMT  
		Size: 13.8 MB (13799419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dc2f5f0bb4c143fe0f932dcfaa47539aaa1db848bd8583c87f3f02c791867a`  
		Last Modified: Mon, 10 Nov 2025 21:20:49 GMT  
		Size: 243.1 KB (243115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:66ee010977dd92c431249545ad282a36bb19a319ab23dce42ee17fa3f71c5105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e830dd0303e591ab9dce65fd4275c88444bbf2b054050a8be7259ce8cc0f108`

```dockerfile
```

-	Layers:
	-	`sha256:f98c0cf8dd90b6341e4687dfabb236c64c87f18d06c20b835724c2a33f820e69`  
		Last Modified: Mon, 10 Nov 2025 21:48:13 GMT  
		Size: 3.7 MB (3708323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7446844b12478ac3decdc0569ce226976392bfbbcd383b963973814d73c278`  
		Last Modified: Mon, 10 Nov 2025 21:48:13 GMT  
		Size: 21.3 KB (21253 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:24575c250e552e2a24aa791dfc5e9c4f3439e2cf8020d82847605edd8a086d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113797225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196246193b90414274b18006a8bcd91859e3248098b7d8646d8d541a6e5eff97`
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
# Sat, 08 Nov 2025 18:17:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:17:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:17:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:17:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:17:56 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:18:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:18:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:18:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:18:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 21:27:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 21:27:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:27:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 21:27:31 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 21:27:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 21:27:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 21:27:31 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 21:27:31 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 21:27:31 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 23:28:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 23:28:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 23:28:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 23:28:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 23:28:13 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 23:28:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5224ee9f1eda0ee26a6b72e8ef1534e70542038a9b3622af533a5010050bd007`  
		Last Modified: Sat, 08 Nov 2025 18:18:49 GMT  
		Size: 11.5 MB (11497447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020ebcd5925b1404168463882e031fbd63d36dedb9fffd13627e7ce2ca4ec960`  
		Last Modified: Sat, 08 Nov 2025 18:18:49 GMT  
		Size: 60.3 MB (60310260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d0d5477cee9470b2961c247786f5e5ed28cc7024f5647c18206e991ce657aa`  
		Last Modified: Sat, 08 Nov 2025 18:18:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b5d88d3b7b135a50a73e2b920d2a3ca957b67a345075168cd1c16d5c73febb`  
		Last Modified: Sat, 08 Nov 2025 21:27:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c934f114932e71d93ad04f4906d45495f7e40a9aa22093206d0f92be58c3d8`  
		Last Modified: Mon, 10 Nov 2025 23:28:37 GMT  
		Size: 13.8 MB (13768970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaf59adfbad84ee86fa59caa0358daa562c8bebb589a8025505251d09ffe79e`  
		Last Modified: Mon, 10 Nov 2025 23:28:36 GMT  
		Size: 214.6 KB (214618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:f2a8cf427af168219fd63fdddee2a3875c237936b54f737bb9a53362b8ef1255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdc62ab835148afcf00c4f42d919813d48fe8f0ecb6f11266c423e1368e06e9`

```dockerfile
```

-	Layers:
	-	`sha256:48339303a2c3023870c99744fa7cc6c1f049409b9791c5a355ac907be70b016f`  
		Last Modified: Tue, 11 Nov 2025 00:36:13 GMT  
		Size: 3.7 MB (3705968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980f72af1e6d818ba81c30a9a4ec8bd53415029c2cec76c7e82ca34dbfd9dd43`  
		Last Modified: Tue, 11 Nov 2025 00:36:14 GMT  
		Size: 21.2 KB (21202 bytes)  
		MIME: application/vnd.in-toto+json
