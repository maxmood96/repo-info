## `tomcat:11-jre17-temurin-noble`

```console
$ docker pull tomcat@sha256:0aeb6e9477c6cdc909c993a55bb953796b5d8f3745ca24c2817d2756a6e83cac
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

### `tomcat:11-jre17-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:2926e8ed0bd34d77d7eeed72af36f4f50bded8979d3b4c1f2b714cf1244622c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108712754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c64e0f5f505d0c7fec418543470c582997261e36905d5a254286430a31e9e53`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:56 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 00:13:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 May 2026 00:13:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 00:13:01 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 May 2026 00:13:01 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 May 2026 00:13:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 00:13:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 00:13:01 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 May 2026 00:13:01 GMT
ENV TOMCAT_VERSION=11.0.22
# Wed, 06 May 2026 00:13:01 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Wed, 06 May 2026 00:13:01 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 May 2026 00:13:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 00:13:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 May 2026 00:13:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 00:13:06 GMT
ENTRYPOINT []
# Wed, 06 May 2026 00:13:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f2a026f4e857e6710d7371079214474f83b2a72af7243a5be77a97b2f7f5ec`  
		Last Modified: Wed, 15 Apr 2026 20:34:12 GMT  
		Size: 17.0 MB (16983429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220fbdf6ba711172c65f46573fb8ae25fa235a06039daf1c9e8ac635285fb9cb`  
		Last Modified: Wed, 15 Apr 2026 20:34:13 GMT  
		Size: 47.4 MB (47434831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8c1cd79a1e9cbb0d2f65b7542a9e9817b0659fd9c6e6ca5376208775e31416`  
		Last Modified: Wed, 15 Apr 2026 20:34:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094e86219be8ad2c0ff540151faa5cf78418e7062517cb774dfc01885b395a0`  
		Last Modified: Wed, 15 Apr 2026 20:34:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2dc00d7cf557fee955774ebdb2a83aa04bc0c805d700bf5ce35a1ea0a33821`  
		Last Modified: Wed, 06 May 2026 00:13:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24280c97ccd02946716260887b977deb65838ef64500d8e09df89ebe0f24d3c`  
		Last Modified: Wed, 06 May 2026 00:13:15 GMT  
		Size: 14.3 MB (14334144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746ff2a0ad49ddf55278e7475cf12dd8700e8d779d33616ad5dd18ff35d0a58b`  
		Last Modified: Wed, 06 May 2026 00:13:14 GMT  
		Size: 224.7 KB (224727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:19c9697af51cedc9f8db1b1fd143de01873a9b53b512c27c275fd6c2f47bc6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c275f6fb48c5e67b86b5dbaec48f0b7d7cb36640d35a9b61488d31aafa87f74`

```dockerfile
```

-	Layers:
	-	`sha256:487031dc5eba34a3963fff3e6574a242cfd667b0150d289672cf5a54d5c50c85`  
		Last Modified: Wed, 06 May 2026 00:13:14 GMT  
		Size: 3.3 MB (3349392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcfe23a25dc64bd37a62def3714f0527d2000d9855593e50d730050482118db2`  
		Last Modified: Wed, 06 May 2026 00:13:14 GMT  
		Size: 24.0 KB (24041 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:9bf847ee0877b15b8666bc6f3947293206bc3d2d0e441ac73a64ed3a6b3812a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102719424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e0d033ea9b3a5a75c855fe94c74b383041b7db65607543e235ad5ceaa65944`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:32:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:32:33 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 00:10:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 May 2026 00:10:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 00:10:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 May 2026 00:10:58 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 May 2026 00:10:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 00:10:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 00:10:58 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 May 2026 00:10:58 GMT
ENV TOMCAT_VERSION=11.0.22
# Wed, 06 May 2026 00:10:58 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Wed, 06 May 2026 00:10:59 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 May 2026 00:11:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 00:11:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 May 2026 00:11:07 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 00:11:07 GMT
ENTRYPOINT []
# Wed, 06 May 2026 00:11:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd1a12c436b8c8176eceae36cf99726296a8f3fd0963367cb1aa9233f3d476`  
		Last Modified: Wed, 15 Apr 2026 20:33:07 GMT  
		Size: 16.3 MB (16309756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd149db0ee0cc0e7d9029179ff3c0503fbedaa507cc2e3b9fc23e9ac8b3fa0af`  
		Last Modified: Wed, 15 Apr 2026 20:34:33 GMT  
		Size: 45.0 MB (45044433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8472949dcee4e56f580671a1ee5468d57689bf50d0d090b5f436805cbc38e5c5`  
		Last Modified: Wed, 15 Apr 2026 20:34:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc898f1ae2b45a9ffab5672cd0580372ecd24e4a2878d38df8948a0b871411`  
		Last Modified: Wed, 15 Apr 2026 20:34:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f501c33b49dd81767572edb0dd555e025212512869afc2f08c9820c671600`  
		Last Modified: Wed, 06 May 2026 00:11:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d411cd878f1d73a594f2732f3397035dadcd0f200438e018e3043de24d035`  
		Last Modified: Wed, 06 May 2026 00:11:15 GMT  
		Size: 14.3 MB (14306612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a237a004e4c1ed2ca107cbc382c2fdff5b4ab7912ec03bf7e00994a12b12ce9f`  
		Last Modified: Wed, 06 May 2026 00:11:15 GMT  
		Size: 196.3 KB (196289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:993748675091804704ab7cf71aa37e6df9a207f51b3f3a1917316330ed1f553f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a8bcec1eb24a4bc80efe19e0735039be041ceee70f9b82488b51b7b2dff2bf`

```dockerfile
```

-	Layers:
	-	`sha256:ea31e73024e2bd2c43317090f741db68ec6e418ab8abfb8a630ae5777ba74672`  
		Last Modified: Wed, 06 May 2026 00:11:15 GMT  
		Size: 3.4 MB (3351796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47291dac276699b770374a52304771809bcb841db7421bae72b6255b1dd234ca`  
		Last Modified: Wed, 06 May 2026 00:11:15 GMT  
		Size: 24.2 KB (24231 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:313e09e50541ef7852d0b9766b08c13bb62c80fcc9dfafa10badf5aa9068fd5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107358458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1dd63018b1fd2a89a333cb213a0a6edf0d8e6d4d250574bec770aa676c761c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:03 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 00:13:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 May 2026 00:13:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 00:13:20 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 May 2026 00:13:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 May 2026 00:13:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 00:13:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 00:13:21 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 May 2026 00:13:21 GMT
ENV TOMCAT_VERSION=11.0.22
# Wed, 06 May 2026 00:13:21 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Wed, 06 May 2026 00:13:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 May 2026 00:13:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 00:13:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 May 2026 00:13:31 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 00:13:31 GMT
ENTRYPOINT []
# Wed, 06 May 2026 00:13:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05498ca84c34f7a91e3e695646db9b00c8acd41836f3ed4561193dbf7daca54`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 17.0 MB (16996261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf808475c74724ef30e1327e0aee1183fe00af6431bbfe3a03dc45bef6a982f`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 46.9 MB (46922138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7290fbca45383216175d6032c9b32fc43206a736f84c41398fc9b0f259f0994`  
		Last Modified: Wed, 15 Apr 2026 20:34:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a396ac8cf6a493c6091fdfa8a3c0b507fa9bc9efcfdcf26d1098e627f47fdcff`  
		Last Modified: Wed, 06 May 2026 00:13:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf962b782572e74396bfc0fb85a7130c98a646b0deacf1102244efac3c0eef96`  
		Last Modified: Wed, 06 May 2026 00:13:40 GMT  
		Size: 14.3 MB (14336337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9806ff527a4bc34fb3b7766cfa152372e123e1a020d25d4a31fbe01912c758ad`  
		Last Modified: Wed, 06 May 2026 00:13:39 GMT  
		Size: 225.3 KB (225292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:4eb8a5152c700cd9789cdfa378e836c21b998ddc20d220e96d6f00ab822965ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08417739a21304c690ebcd095dc405d6fe1b250811f52ac8ff9b9fe253b169a`

```dockerfile
```

-	Layers:
	-	`sha256:a72160ef74c6d4cbfd4c6b3d51e735968a8fea503b01c8e167d3b6ea60232e40`  
		Last Modified: Wed, 06 May 2026 00:13:39 GMT  
		Size: 3.3 MB (3349960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568c2245997c856ff9afecf3fed9773232df8d8f4dfa43ef600d349d7add5123`  
		Last Modified: Wed, 06 May 2026 00:13:39 GMT  
		Size: 24.3 KB (24297 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:059768037b4f21f6bab1f7b777c412309e83dc0ef159b5bec925a7f7acb343aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115069794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd4232dd5e486e86c3dff5f1f6fcf166155c8919d2c65c50140b9523def37bf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:12:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:12:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:12:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 01:11:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 May 2026 01:11:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 01:11:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 May 2026 01:11:24 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 May 2026 01:11:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 01:11:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 01:11:24 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 May 2026 01:11:24 GMT
ENV TOMCAT_VERSION=11.0.22
# Wed, 06 May 2026 01:11:24 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Wed, 06 May 2026 01:11:25 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 May 2026 01:11:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 01:11:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 May 2026 01:11:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 01:11:39 GMT
ENTRYPOINT []
# Wed, 06 May 2026 01:11:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13718497a6adee31aa098ce2c85aca5feeb60aa6f13ee0ac169b2a181311f2cd`  
		Last Modified: Wed, 15 Apr 2026 21:13:20 GMT  
		Size: 18.8 MB (18813307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2decdee82476d2d5f2a613ac0c43803df1e6a2015ba9eee219fb2b1da395ba57`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47332020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925130925f5f968231b25d0be5197a21705e6bd8671cfe5cd4ca2626112cad42`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1f759bac23388caf3bfbb563b6e9c3e45cd081ff0ec4a04e3d69d2f386970e`  
		Last Modified: Wed, 06 May 2026 01:12:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e1bd599568ea554f96dd0908c65795aa4b6d1ee33a36afbf4f4311019509b2`  
		Last Modified: Wed, 06 May 2026 01:12:01 GMT  
		Size: 14.4 MB (14350914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359ba32d39ae6e0bf254406b2d288bab21aa22620193cdae6002d0e7d009a150`  
		Last Modified: Wed, 06 May 2026 01:12:01 GMT  
		Size: 256.7 KB (256733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:97cab66563c831ad710e1981124d2e410db034dba47d858526afeac6b001cdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75ffb74c7bbf9491c2376c030db67083b36ee0b88cdbb0897ae082f4e347198`

```dockerfile
```

-	Layers:
	-	`sha256:027e91f93ecfcd1bc59b7bb239e913fe356092dd1419a8fa3468956efb2b142c`  
		Last Modified: Wed, 06 May 2026 01:12:01 GMT  
		Size: 3.4 MB (3353517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9af727ffbae9619fdc9e5cc35d17bac8d11c1c2fa8fb204d930e340152436a`  
		Last Modified: Wed, 06 May 2026 01:12:00 GMT  
		Size: 24.1 KB (24147 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:d12798ee05e09741e7725baf234568f292a593d14cd0e85e992c1f9d6e665dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109597053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8abee46aa5a32ca635aabca944754e4e6365426f75caa14a34c9648c0ed14`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 16:54:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 16:54:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 16:54:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Apr 2026 16:54:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 16:54:04 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 16 Apr 2026 16:54:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 16 Apr 2026 16:54:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 16 Apr 2026 16:54:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 16 Apr 2026 16:54:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 15:47:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 May 2026 15:47:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 15:47:25 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 May 2026 15:47:25 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 May 2026 15:47:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 15:47:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 15:47:25 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 May 2026 15:47:25 GMT
ENV TOMCAT_VERSION=11.0.22
# Wed, 06 May 2026 15:47:25 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Wed, 06 May 2026 15:47:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 May 2026 15:48:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 15:48:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 May 2026 15:48:18 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 15:48:18 GMT
ENTRYPOINT []
# Wed, 06 May 2026 15:48:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0390b1a9899a52673c5b8052b6d71338c516171daccb3d007ddf3a109f2a31`  
		Last Modified: Thu, 16 Apr 2026 16:56:46 GMT  
		Size: 17.9 MB (17872647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001532fc00ba3fd5ea28685a46b17399c478b909da82087a2a06ba777cc21dfb`  
		Last Modified: Thu, 16 Apr 2026 16:56:50 GMT  
		Size: 46.0 MB (46007377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51038c9b085138d5fef0541614c4a499d0536c2a8a509862356053689244c612`  
		Last Modified: Thu, 16 Apr 2026 16:56:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84cb654d1732ec9b6b794dfcb53f7003c0cf0d55ebf5f59f92c0a55cd5adcbc`  
		Last Modified: Thu, 16 Apr 2026 16:56:40 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca75405960442e9a99b378864457d65d457f216aebc87ecbdd4aa1053d00bcd`  
		Last Modified: Wed, 06 May 2026 15:49:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12f9adc5f3a912b8fcf03a13b2faa80ef7badf55740aba69c7d796667b5e052`  
		Last Modified: Wed, 06 May 2026 15:50:00 GMT  
		Size: 14.5 MB (14521075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb62565ecd2af1d5fdc8ccfd6e1a976690a06933eccc351f06c64e491d94e27a`  
		Last Modified: Wed, 06 May 2026 15:49:57 GMT  
		Size: 228.0 KB (227982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:129cf56d987783ca582412e7c8be66f9d58afaf192b877199a638915b872d810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3365666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ed85635771c24bf157828a634e3f5ab21f054ff233819e274c7082d54d4ca6`

```dockerfile
```

-	Layers:
	-	`sha256:b8284208b422ac69f5d3b5208e9ada139bce9c061e479c246b3e8348cfc7b9a2`  
		Last Modified: Wed, 06 May 2026 15:49:58 GMT  
		Size: 3.3 MB (3341519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8c347bf16a74acd5868d3e242c59dd61df882e3d65205f46afa9a6c832f62a`  
		Last Modified: Wed, 06 May 2026 15:49:57 GMT  
		Size: 24.1 KB (24147 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:727f48384dc9139c2b45755d42a6a1707bf1360ff25c8587c0c01787ed1af618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106479564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8ea00317442b3760dac1168d536731ff59279e6a9f2e6b0988a107bde936c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 01:17:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 May 2026 01:17:47 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 01:17:47 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 May 2026 01:17:47 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 May 2026 01:17:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 01:17:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 May 2026 01:17:47 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 May 2026 01:17:47 GMT
ENV TOMCAT_VERSION=11.0.22
# Wed, 06 May 2026 01:17:47 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Wed, 06 May 2026 01:17:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 May 2026 01:17:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 01:17:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 May 2026 01:17:52 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 01:17:52 GMT
ENTRYPOINT []
# Wed, 06 May 2026 01:17:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a3498cd625b1c7f2fe4f65685d4036d3cad9b92fdc3a7c30d047b0511431d`  
		Last Modified: Wed, 15 Apr 2026 20:44:43 GMT  
		Size: 17.6 MB (17579116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25db138fd0977b0b77232c829a48effbfe36e9fba90f12720aa6836b42bd244`  
		Last Modified: Wed, 15 Apr 2026 20:45:25 GMT  
		Size: 44.4 MB (44409571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995587062a6ec3124249b97651c304171dd5fc7569374d93304f016b167f8490`  
		Last Modified: Wed, 15 Apr 2026 20:45:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85857433d525793f70ecd9928002af0a5433cb29c9a82024561e7b07ef801fa`  
		Last Modified: Wed, 15 Apr 2026 20:45:24 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f240945cca96d69c9d0db13c48e6a15bae0943bd5a215904c7b5152a8181b2b`  
		Last Modified: Wed, 06 May 2026 01:18:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9067feb9c8bc235db9596b8aa044a9bcd8a65408f1cb6018976b6eeedcf49f0d`  
		Last Modified: Wed, 06 May 2026 01:18:16 GMT  
		Size: 14.3 MB (14343075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eae4b3766732b28e54744f2be6cc99759decc1452dd2500bed5221a5ae960ad`  
		Last Modified: Wed, 06 May 2026 01:18:15 GMT  
		Size: 233.0 KB (233009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:991a835b90bbce721f591e251db41e959c6dc5160dbe0d93e47fd3ea21ab5040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3375632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744c8eeea1fd110b2bd6ac342f12ad23886c3585d8f73f1829bebc4e18b190d8`

```dockerfile
```

-	Layers:
	-	`sha256:35271253b737d87282b24cdf2427240e148c7ea18b33d623be688c43d01840b4`  
		Last Modified: Wed, 06 May 2026 01:18:15 GMT  
		Size: 3.4 MB (3351591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed1d0202c3f18f56dbe883566ff9d2dbc9052414bee9ee6d1e3a894dd894782`  
		Last Modified: Wed, 06 May 2026 01:18:15 GMT  
		Size: 24.0 KB (24041 bytes)  
		MIME: application/vnd.in-toto+json
