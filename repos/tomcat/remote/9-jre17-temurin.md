## `tomcat:9-jre17-temurin`

```console
$ docker pull tomcat@sha256:c3805f98af01598a2b1f2e03f93fa5ac32cc8b8b5151021701b7f5e4cb22cdad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:9-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:163e232737bb6c116fa5ecabe140bde687fbaf98a8e898008cefd0300609e26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108142238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15449df4b8fdfd5ff0c65179daea2461215aec4d26932a063c42fd4bdb09f57b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:19:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:19:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:19:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:19:58 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:20:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:57:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:57:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:57:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:57:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:57:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:57:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:57:07 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 21:57:07 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 21:57:07 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 21:57:11 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:57:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:57:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:57:20 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:57:20 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:57:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e61c1c7634c5cdff204406872254c592ce58045e1dbe190f3b0909e2ef28d30`  
		Last Modified: Tue, 17 Feb 2026 20:20:14 GMT  
		Size: 17.0 MB (16980681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d73e22a56245290442c468a1acdf5344791228f3a2ca6a3c3eadc95fcf78e`  
		Last Modified: Tue, 17 Feb 2026 20:20:15 GMT  
		Size: 47.4 MB (47434783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cbb3f549f16e820ceb68c09055edbb06364740ecefa58833bd97565acc85fd`  
		Last Modified: Tue, 17 Feb 2026 20:20:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61892f0e6a40d1489bc9c8c303b00d33b25e2290f56d541b9e003a433a1c2c1`  
		Last Modified: Tue, 17 Feb 2026 20:20:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090639185e8ca9ae4649464203263d99a328bd7987ab1a9e3ce39dde1c563109`  
		Last Modified: Tue, 17 Feb 2026 21:57:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47d66af200876f8ae7083845a796dd369a9a43b897ffd1e6bb0e91662b2ae21`  
		Last Modified: Tue, 17 Feb 2026 21:57:32 GMT  
		Size: 13.8 MB (13771684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1214184f8dac89e0b7f124815a7807cc9d4f088d6ab61e8d7ef0e6613f5cb86d`  
		Last Modified: Tue, 17 Feb 2026 21:57:32 GMT  
		Size: 224.8 KB (224835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:9bb322d80fb180891aae48565951841dc163747be25853d705f8f82fdc2ac5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3368850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f674539c0a6f62278a7870c8ddce8bcd6f46d4653b917ef03957acf8f608adb`

```dockerfile
```

-	Layers:
	-	`sha256:525710363e0d35321b9dc0b6f160fd25fd532a6a1e48283fafb78bfee35bfd70`  
		Last Modified: Tue, 17 Feb 2026 21:57:32 GMT  
		Size: 3.3 MB (3345758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6f8fa55719a25070f9e108a0298801ac4bbcf8dfea0a4f2de0dcd2ab486720`  
		Last Modified: Tue, 17 Feb 2026 21:57:31 GMT  
		Size: 23.1 KB (23092 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:bbd1921061a4a4c82e0683bfb3f12d1520a5296817218b5f3db001c941035849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102111244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9155ba6334a2c91844e759c04d138834df80e18fce137d2a7a6c0ffd6ddae30`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 16:51:23 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:51:27 GMT
ADD file:9633092e110ed5475e9e31841bcc6e288ca09c116e102d75694089f384f549b3 in / 
# Tue, 10 Feb 2026 16:51:28 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:11:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:11:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:11:52 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:12:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:12:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:12:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:43:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:43:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:43:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:43:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:43:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:43:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 21:43:42 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 21:43:42 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 21:43:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:43:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:43:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:43:50 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:43:50 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:43:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:dd135084b7c993802b7c1ba97d192c201727ddf710812c361d5441cb729f5c20`  
		Last Modified: Tue, 10 Feb 2026 17:41:49 GMT  
		Size: 26.9 MB (26855457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef9bea89ab62b13598603be1200b7256437427d102522de5524653d0a3c568`  
		Last Modified: Tue, 17 Feb 2026 20:12:15 GMT  
		Size: 16.3 MB (16308084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d219ad0cae478f69edada796883d080ef54f48bdd60ba42615de8453d3255aa`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 45.0 MB (45044557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebe964b9955e8249855a3b0f92673c5ae780dce60417bc1fd28e4281cf929ae`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d63b4ef3e8ade1a87276a6b87ba57bed9859de8eff24e890d18620ccf354b`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa11b54dc6bb6c57e9bee4cd0140cdab37f038cee12f89a23d3d53490bbb635b`  
		Last Modified: Tue, 17 Feb 2026 21:43:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39779ded9f7cebad3817ef7d379c5f4ea0d684e21b82eb2082413277a17fb03`  
		Last Modified: Tue, 17 Feb 2026 21:43:59 GMT  
		Size: 13.7 MB (13704269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99327094abe97d88c5f741c6f62c46bdb2c1903209b1e2639ef168006b6e30b2`  
		Last Modified: Tue, 17 Feb 2026 21:43:58 GMT  
		Size: 196.2 KB (196235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:99b70afd752c0594600bfe6c042d65216e0d4bf7b0984c69c4d44da5b4936f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3371399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb5c6a35e872dc839750cb034457d835878f40b8b42b5ab54df82b31b4fe3d3`

```dockerfile
```

-	Layers:
	-	`sha256:b8626435f6e50a48761ad1de3ac4e202cfc1cf14ee9f8134bd43ca13780173b3`  
		Last Modified: Tue, 17 Feb 2026 21:43:58 GMT  
		Size: 3.3 MB (3348138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40a647814b3a107f98a029461e8d90da45830906491836931dbeaeb29ec1e7e`  
		Last Modified: Tue, 17 Feb 2026 21:43:58 GMT  
		Size: 23.3 KB (23261 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:d5fd4fe09a13530762de620ebc6a611a607919f1039790e9d9010aa26aac0609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108290898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da462b865db5d6bf796eebfd382b3581bea35c7870453ff2b91eec91f6b8e27`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:54 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Mar 2026 01:24:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 03:30:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Mar 2026 03:30:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:30:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Mar 2026 03:30:27 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Mar 2026 03:30:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:30:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:30:27 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Mar 2026 03:30:27 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Mar 2026 03:30:27 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Mar 2026 03:30:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Mar 2026 03:30:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:30:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Mar 2026 03:30:40 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Mar 2026 03:30:40 GMT
ENTRYPOINT []
# Tue, 17 Mar 2026 03:30:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135b685185570494910edd394b8134172c97bab64cfef4134685bc7a7adf965`  
		Last Modified: Tue, 17 Mar 2026 01:24:08 GMT  
		Size: 17.0 MB (16996055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2cd9590e5d48e6a3302ddc079709cd642f78e0609ee70084045d54b69f1cd8`  
		Last Modified: Tue, 17 Mar 2026 01:24:31 GMT  
		Size: 46.9 MB (46922135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7c1c52c3ce02cf734adb29eb7a2c7d950c8a89652378cf9ec8eac5a321fa90`  
		Last Modified: Tue, 17 Mar 2026 01:24:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7483a7f867de37bbf4a1c948255b63498ac2c0520ec35a0d753e382658eb1b`  
		Last Modified: Tue, 17 Mar 2026 01:24:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2c9c6eba59d7794200309f4ff1b317bced10ca9ab217f9ec2f2e9bf0b38e8c`  
		Last Modified: Tue, 17 Mar 2026 03:30:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae0595f396001caa27f8f9cbcda79ccf7cbce5b110782e43f6ccfba6693a72d`  
		Last Modified: Tue, 17 Mar 2026 03:30:49 GMT  
		Size: 13.8 MB (13780850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9cd2a2653a1e1739f76c38f3e0f55f67e43df13c869bf2c0e002b5e4b764dc`  
		Last Modified: Tue, 17 Mar 2026 03:30:49 GMT  
		Size: 1.7 MB (1719506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:d2dab62eb09e4dbdc5b371884f182a43a60d84650828beb2c9990da8e10094e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3369633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a5e5d0a4846142274aff9b65c3906c87160bdf0d633db3c1e3723b6ebe04b7`

```dockerfile
```

-	Layers:
	-	`sha256:f7be75381dace4d6239b8b0fb67ceb4a5771b4190079c0c27ac746ca20fce102`  
		Last Modified: Tue, 17 Mar 2026 03:30:49 GMT  
		Size: 3.3 MB (3346318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6b0cdb9d6e8f47db37683f00849d0c7b597c1a6c41d9331ab4fe004e308553a`  
		Last Modified: Tue, 17 Mar 2026 03:30:49 GMT  
		Size: 23.3 KB (23315 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:9d0b8bcf2939bfdf543b4bc12223845d2dc105725b925c02a76a95f61ae078d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114520958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da4994c891cf274110d21dea3fd895084579d2d1365e7df38c6df10f0568f23`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:13:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:13:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:13:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:13:51 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 01:05:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 18 Feb 2026 01:05:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 01:05:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 18 Feb 2026 01:05:35 GMT
WORKDIR /usr/local/tomcat
# Wed, 18 Feb 2026 01:05:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:05:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:05:35 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 Feb 2026 01:05:35 GMT
ENV TOMCAT_VERSION=9.0.115
# Wed, 18 Feb 2026 01:05:35 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Wed, 18 Feb 2026 01:13:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 18 Feb 2026 01:13:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 01:13:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 18 Feb 2026 01:13:24 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 18 Feb 2026 01:13:24 GMT
ENTRYPOINT []
# Wed, 18 Feb 2026 01:13:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7c72ff62beb3fa7ef85f29d31b133f9c93f5b3be5679ac7a733c7736000812`  
		Last Modified: Tue, 17 Feb 2026 20:14:29 GMT  
		Size: 18.8 MB (18815050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cc03ef4958f22d7a21c3bb735d6283d69d0ca978b76c8bfbdfbcd0f4af92d6`  
		Last Modified: Tue, 17 Feb 2026 20:20:29 GMT  
		Size: 47.3 MB (47332074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306aa7e18b4737442b707149648e27299adad29d4aa82176f86ea657c6ff690c`  
		Last Modified: Tue, 17 Feb 2026 20:20:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ad53a07c1aff7bd7917b14f09743e87d2f48f377af1c63429f5391b97c141`  
		Last Modified: Tue, 17 Feb 2026 20:20:27 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5481aa83e094591601e40d1d2f19d38df5a3b84f8f5a083ad96f8970afdbbb`  
		Last Modified: Wed, 18 Feb 2026 01:06:07 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9a3290ab697c9e7b4da81d44dc7da4046a80b40bc928ab608a8ee408e2bfd6`  
		Last Modified: Wed, 18 Feb 2026 01:13:48 GMT  
		Size: 13.8 MB (13807650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43820c56f453ba67c690fd8082e9cd6079054dbafd9c93591b1a5c10352de6b5`  
		Last Modified: Wed, 18 Feb 2026 01:13:47 GMT  
		Size: 256.6 KB (256635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:3043ca9856c39a6dfd732d6a0dcae8b5fd23d99c513bf876f741e434f6f19250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254408918fb08c243564349487f3126dd720e1f18a2688a3dfa2de405d1d2fca`

```dockerfile
```

-	Layers:
	-	`sha256:745a656997fe1f2ddf72a3eed1558ebbc38bbb11a84922b9311a2f68ab9cf995`  
		Last Modified: Wed, 18 Feb 2026 01:13:48 GMT  
		Size: 3.3 MB (3349865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de7a0ec3f58d6f34bcb786afc08184387bc208802d3d14d84303e59302a0f24f`  
		Last Modified: Wed, 18 Feb 2026 01:13:47 GMT  
		Size: 23.2 KB (23180 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:c26ba60eb43cd35ff138ee906d8e510dfe2248b55f9f6dff1f9a06ce11e497a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109343492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97374aad5ec110898ab3e0cb57f58faec9ded74a8c09e73b919ef1beb38b75c3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 17:33:09 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:33:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 17:33:55 GMT
ADD file:b4821892707dbb5cc8e8eb3b4e757edc2d124db81fcdedfc3b244dcb5c1fa6c0 in / 
# Tue, 10 Feb 2026 17:34:00 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 00:04:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 00:04:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 00:04:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 00:04:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 00:04:02 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 18 Feb 2026 00:04:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Feb 2026 00:04:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 00:04:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 00:04:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 12:49:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 18 Feb 2026 12:49:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 12:49:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 18 Feb 2026 12:49:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 18 Feb 2026 12:49:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 12:49:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 12:49:06 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 Feb 2026 12:49:06 GMT
ENV TOMCAT_VERSION=9.0.115
# Wed, 18 Feb 2026 12:49:06 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Wed, 18 Feb 2026 13:07:31 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 18 Feb 2026 13:08:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 13:08:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 18 Feb 2026 13:08:22 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 18 Feb 2026 13:08:22 GMT
ENTRYPOINT []
# Wed, 18 Feb 2026 13:08:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f2683d5e2cbe038b4f1178e139d507e705e0a3a566f8b9c89bf3484f426119af`  
		Last Modified: Tue, 10 Feb 2026 17:42:05 GMT  
		Size: 31.0 MB (30954431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c3712d635153aaa7be4b1830d8686d2050b5e7e814867311ab3448a2028a9`  
		Last Modified: Wed, 18 Feb 2026 00:07:30 GMT  
		Size: 17.9 MB (17865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f4c3e7bd3e21557cda13bb0bba4da46b9a05547266b7d0190495d108bd4756`  
		Last Modified: Wed, 18 Feb 2026 00:07:34 GMT  
		Size: 46.0 MB (46007467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a4a96d5699deacaa0e94a27bbdfb0da81f1e3d19d6fd26005a46cf25f4d17a`  
		Last Modified: Wed, 18 Feb 2026 00:07:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcee2480c97768954ae515a2f889c8ee892e48963f2ad9fea3e559a017ca624`  
		Last Modified: Wed, 18 Feb 2026 00:07:24 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae3977f0db8c3e704fbf55406eb4c4cffc885ec3ad6d67e47664746eff71a85`  
		Last Modified: Wed, 18 Feb 2026 12:51:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c9bef09a8035974a5a636894169069f7e63321c0590927e04f01789e2bcf62`  
		Last Modified: Wed, 18 Feb 2026 13:10:03 GMT  
		Size: 14.3 MB (14285892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64093941e76aa38486b8ef377577acfe622ee1cc745e515a509ad56e78f2957`  
		Last Modified: Wed, 18 Feb 2026 13:10:00 GMT  
		Size: 227.9 KB (227875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:43d8d9d4580722bb5bb8a50e404af438448cde1872a461a0f925c5cd59b69c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6dd88a9cea8be05ea01735dee4e96276ae724a494e194b5a839f35c291eb39`

```dockerfile
```

-	Layers:
	-	`sha256:3978cee51370fce916f900ae7ed414e81ee21e6e3918fac3f65a77d206ff5c37`  
		Last Modified: Wed, 18 Feb 2026 13:10:01 GMT  
		Size: 3.3 MB (3337867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fc8003a9c355906764aea674d40189a1c55e60cdb415397234af14669809c9`  
		Last Modified: Wed, 18 Feb 2026 13:10:00 GMT  
		Size: 23.2 KB (23181 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:40fae3eaf7bbe8ac07d92f8a1b9b13605b0dc6589787c283f577cda015fcbbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105918706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59940f9f3dd5a64e452e29e6ffc4b48d02e284a168f622829081e8624a3c0b6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:13:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:13:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:13:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:13:47 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:13:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:13:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:13:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:13:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 22:44:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 22:44:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:44:59 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 22:45:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 22:45:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:45:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:45:00 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 22:45:00 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 22:45:00 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 22:47:20 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 22:47:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:47:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 22:47:27 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 22:47:27 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 22:47:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a428c7288420c3859cdedb624dc0d9eb5cfe511d7b19ec62d1604bdf1e861593`  
		Last Modified: Tue, 17 Feb 2026 20:14:20 GMT  
		Size: 17.6 MB (17581531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d7ed2d0be93eb66970292f7e04c09bbd95fe0667928e37fef5b2a8b823f06c`  
		Last Modified: Tue, 17 Feb 2026 20:14:20 GMT  
		Size: 44.4 MB (44409458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dd71842a718cfb695da1f3b614f724f588a6d698d2f77f012de8fb952d8e7a`  
		Last Modified: Tue, 17 Feb 2026 20:14:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790b6d2f071d336175caa0e62e59bff28a496e8a66257968cca40ee5333666c`  
		Last Modified: Tue, 17 Feb 2026 20:14:19 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a11182bdfb31dd66fc7c19b2d3c629676be84ef307fda76ea5f106c18fe4f0c`  
		Last Modified: Tue, 17 Feb 2026 22:45:28 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5207748821dbb4e178c487e3ddd7fbdbaf0b9a6ee637305562992895cf6e262`  
		Last Modified: Tue, 17 Feb 2026 22:47:58 GMT  
		Size: 13.8 MB (13782222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d096ac16e79aa27ee022c53a19995ce9f92f8daa86a6f145b6f71aa4450ee83`  
		Last Modified: Tue, 17 Feb 2026 22:47:57 GMT  
		Size: 233.1 KB (233068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:9bd76ee000ebf21564e1a2cd5ab6f0662192d2b5fd7b46a23ceae665629df6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3371050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec6191c01c1302e52338048451c1924b0537bca2ed2055d34c081d831640f9c`

```dockerfile
```

-	Layers:
	-	`sha256:d3f0f874051b9416b2fdf041544417b3fe7fd8cc706ca808725650eaea146512`  
		Last Modified: Tue, 17 Feb 2026 22:47:57 GMT  
		Size: 3.3 MB (3347957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11788ce01b39c2b9d824db285334fb88f6bdcc22db05e3f720feca33ffc28f4`  
		Last Modified: Tue, 17 Feb 2026 22:47:57 GMT  
		Size: 23.1 KB (23093 bytes)  
		MIME: application/vnd.in-toto+json
