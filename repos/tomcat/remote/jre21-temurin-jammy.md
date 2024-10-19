## `tomcat:jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:2d81949ba34fa31b2934734d3530b9c43b7aef9215faf34bcb1f13039badf717
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
$ docker pull tomcat@sha256:47f53da6b05c75b66f6386e4288fa705dc8405436397958db1f8e1a53fc0ffe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109686931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6f79261dc9a72ca6dc7bfe81baa532a49b0467e9c0644ec4d4c45d31c89e66`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_VERSION=11.0.0
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_SHA512=f23c533f257725cd673eb39423459799b6647e6fa9dc14a0b252cb7186935870a36a657741f72578935a4b52330e128e15372fb6bb678a7fd26ae942710a1f1e
# Wed, 09 Oct 2024 17:36:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:36:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23567824ed1341bd9ba3c91e9c2416b1c4958ab60015df479d966c50b6a71189`  
		Last Modified: Sat, 19 Oct 2024 02:06:43 GMT  
		Size: 12.9 MB (12887678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b6a306e80f054db34c66fb38d6cc2fbf19c9d8eb513b17beb1262e9119b239`  
		Last Modified: Sat, 19 Oct 2024 02:06:44 GMT  
		Size: 53.5 MB (53513700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00bc82ff765b9e46184c9ef416b7fdab9461e51d046b732ade43b8f8d52986`  
		Last Modified: Sat, 19 Oct 2024 02:06:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225e711672e48572d7d8c0c3841d2b77311eb19e52d949e18efabb32815888e4`  
		Last Modified: Sat, 19 Oct 2024 02:06:41 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ca804c417935f93982015b816c4bf9c713392839a5f277c112dc83ae6a0680`  
		Last Modified: Sat, 19 Oct 2024 03:57:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9573e5a51678558430cdb0b504d42504e54cf7c228de303a9a2d5d5cbd30072d`  
		Last Modified: Sat, 19 Oct 2024 03:57:48 GMT  
		Size: 13.5 MB (13529399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456a76bcad99bd9ef7ee27799651a7648304fbb316ec8170e65d9caee3bed2f8`  
		Last Modified: Sat, 19 Oct 2024 03:57:47 GMT  
		Size: 218.0 KB (217998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:aab405c3959e00066afec0e17e2d3a47f3d2e29eb36dcde6f80895d9a2e54278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3649238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd76485711af5c42848c5dabf1e6c230f17bc873d1a12a048c0cb4611380561`

```dockerfile
```

-	Layers:
	-	`sha256:42c93c7b3f4040866e5533037ab00e83f30c1a8698aed28bb1168a11228bf07f`  
		Last Modified: Sat, 19 Oct 2024 03:57:47 GMT  
		Size: 3.6 MB (3627149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a400f825a6bee3cc73446d6a2b6f8d94fbcdd77a7592901a95947e1860ec5e22`  
		Last Modified: Sat, 19 Oct 2024 03:57:47 GMT  
		Size: 22.1 KB (22089 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9424b2c9e9b57545e2220fd8b1e33f2a0c12ccc8467378de9fa311ec01ce3c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106578308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61434f5b05a80431dcd9097e612b3301fe0a4a8524e6e24c34fcfbecc2c5ce7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_VERSION=11.0.0
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_SHA512=f23c533f257725cd673eb39423459799b6647e6fa9dc14a0b252cb7186935870a36a657741f72578935a4b52330e128e15372fb6bb678a7fd26ae942710a1f1e
# Wed, 09 Oct 2024 17:36:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:36:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dece6d062dc0723f97a73605fb14fdb50c21ad91f9182d5756336b6456a39f`  
		Last Modified: Sat, 19 Oct 2024 05:27:13 GMT  
		Size: 12.8 MB (12828465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97bc277b093b97eaa03bfa71fb19594219faa0e4eec43a3151163ff1fbbe92`  
		Last Modified: Sat, 19 Oct 2024 05:41:08 GMT  
		Size: 52.6 MB (52641677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c0822cb48eaf4a596fe34b9ce78b967d25071c410531d74c6b29087f49f3e7`  
		Last Modified: Sat, 19 Oct 2024 05:41:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93780580828e40fc0fa6ba28f56fee1b471816aa6d50d34e379d2d88b3a2f47d`  
		Last Modified: Sat, 19 Oct 2024 05:41:05 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c6f912a526b07297b5eff212c6ae2286493f882a9b231283e11bc728383d17`  
		Last Modified: Sat, 19 Oct 2024 21:01:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8e743d130b0591605671f56565f33ce85aced0ba36b6477ddf89d134df9d70`  
		Last Modified: Sat, 19 Oct 2024 21:01:28 GMT  
		Size: 13.5 MB (13530446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccd2617cbb4bc2d943a93f8b70f58acce3fc8948b0e226829d5fa27ae18b9a5`  
		Last Modified: Sat, 19 Oct 2024 21:01:28 GMT  
		Size: 216.9 KB (216921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c42f22da2fef24d98d59decfb5b9e746d64b83824c708cab182a8709ce21732d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3649072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b989d0283096522dc59b5c72d38952933b689af6dcc8db195430bcfa59a37b`

```dockerfile
```

-	Layers:
	-	`sha256:d4732e43cae5bb1f09720352cb0a7788bc19faf944963e22434272d6da48348d`  
		Last Modified: Sat, 19 Oct 2024 21:01:28 GMT  
		Size: 3.6 MB (3626822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f8856538cd6924750627ada57fd2e2e001e1248c4f71ec1e53ec9f73f66e74`  
		Last Modified: Sat, 19 Oct 2024 21:01:28 GMT  
		Size: 22.2 KB (22250 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:1a7e39a231cb18a4ce660e1dc764ac42a1f8650135c6d1a1d9d6764e9f72d70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115541803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b23e1513867866e5b6ce0d53845e1e72d543df30de31a2ce1f97c7d33f04c9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_VERSION=11.0.0
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_SHA512=f23c533f257725cd673eb39423459799b6647e6fa9dc14a0b252cb7186935870a36a657741f72578935a4b52330e128e15372fb6bb678a7fd26ae942710a1f1e
# Wed, 09 Oct 2024 17:36:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:36:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b215e70428c4748ef34966c9edda654fb7f223d14068d026d7741eabb1a719`  
		Last Modified: Sat, 19 Oct 2024 04:18:39 GMT  
		Size: 13.7 MB (13725185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6a1163c730d9a4cb20438d4e799e2353d2afed812c0159dfcc82707379f4c7`  
		Last Modified: Sat, 19 Oct 2024 04:39:58 GMT  
		Size: 53.6 MB (53573566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80343f39e348ab971a62846915e8c3ba3932219be650ebf653b4e9b757619e62`  
		Last Modified: Sat, 19 Oct 2024 04:39:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6749b48d61ca4e5d3c6d8e37fd76ed709f0524368e70f4a511aea9892b8e792`  
		Last Modified: Sat, 19 Oct 2024 04:39:56 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75faa72b11586cb2673239f7012e209dfa2cb24daecd683f2f011f7f8baefefc`  
		Last Modified: Sat, 19 Oct 2024 19:46:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9550278672c8c6cf2dbef2873269f0eae4e4f9dd457744ae175ab4b740558242`  
		Last Modified: Sat, 19 Oct 2024 19:46:23 GMT  
		Size: 13.5 MB (13543997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63090f3e392c188ea79d70f664fe02e8e56143c29bd70bca52a0e256866d63c`  
		Last Modified: Sat, 19 Oct 2024 19:46:23 GMT  
		Size: 248.3 KB (248342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7d0441fdcc9aae122d4b395a38a7432050209572f484834aaaf2c979239a444d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3653197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158ff19e08a1d8f8e3b6cebe3799b08dea1d1a0d0c9d25455ab34fe2ad082f51`

```dockerfile
```

-	Layers:
	-	`sha256:16bb5e39e401eb3d9ed2b8cf6aa02f62aed4e69bd7cca5c367c48b0ffd430af2`  
		Last Modified: Sat, 19 Oct 2024 19:46:23 GMT  
		Size: 3.6 MB (3631049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff10e3296e7f889d471685b57aab2f4847ab8bc87a232889e80831e42ba6bbd2`  
		Last Modified: Sat, 19 Oct 2024 19:46:22 GMT  
		Size: 22.1 KB (22148 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:7863d2cbfe8f5a0b36fb7300957f712eccab4814a174b54cca19336052c6e22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104396509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8469ea896a364156933e321f442b91c9a470c61bd0b5d54cc3dc13b03f4e0c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:36:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:36:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:36:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_VERSION=11.0.0
# Wed, 09 Oct 2024 17:36:46 GMT
ENV TOMCAT_SHA512=f23c533f257725cd673eb39423459799b6647e6fa9dc14a0b252cb7186935870a36a657741f72578935a4b52330e128e15372fb6bb678a7fd26ae942710a1f1e
# Wed, 09 Oct 2024 17:36:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:36:46 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:36:46 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:36:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930446b1bcd01fe732ccd6c0777d5a5556f080ae138efc45b08957e86a30da0d`  
		Last Modified: Sat, 19 Oct 2024 03:55:21 GMT  
		Size: 13.0 MB (12970024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f74b8fc4cc56b6306b6dfcabe22b04d2bb68f27a44dce4caeef54ac242caff6`  
		Last Modified: Sat, 19 Oct 2024 04:09:07 GMT  
		Size: 49.7 MB (49669474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2848e9eb3eb625bedf1cf0847f8ed99a437972eff5058482598d2d0bb7f9c0`  
		Last Modified: Sat, 19 Oct 2024 04:09:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5805bd3747b04a9037c36b8e337eb1a8aca0cc88d53e9563eda8fb597fb9b5a0`  
		Last Modified: Sat, 19 Oct 2024 04:09:07 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58650734e044b20cd59e75d9c711b2f9552e20df73855b71ef7c484185d22319`  
		Last Modified: Sat, 19 Oct 2024 16:10:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f38de937ba2241620f649c94c2009dda4f5e1be8097f91585d42de137fbaed`  
		Last Modified: Sat, 19 Oct 2024 16:10:41 GMT  
		Size: 13.5 MB (13533477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7611652255f490bd28e391e975e2c774be75b60fe7ee0596b5cd41b92de2a8f1`  
		Last Modified: Sat, 19 Oct 2024 16:10:41 GMT  
		Size: 219.6 KB (219588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d06e7ae67736906fd62ff28d70e4888f7c3a98556af4df84b103a4d4d2af3636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3650839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dac7aa62d5177920a9386932ee98adf7bd12a79cc146f8973c372d3883993d`

```dockerfile
```

-	Layers:
	-	`sha256:7d747d911db8f460718bb665128cf2d3f0419e7a207a55b85db9ddb4146df88b`  
		Last Modified: Sat, 19 Oct 2024 16:10:41 GMT  
		Size: 3.6 MB (3628749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3faa4795e0a5c7e3c74448fe7689115b644725d05283faf9e1e3d0a15e8b1298`  
		Last Modified: Sat, 19 Oct 2024 16:10:40 GMT  
		Size: 22.1 KB (22090 bytes)  
		MIME: application/vnd.in-toto+json
