## `tomcat:11-jre17-temurin`

```console
$ docker pull tomcat@sha256:4afe4ecdbc949bf9b6374683e5e0cd1f3a378be5d13bb471ea641592498d26c9
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

### `tomcat:11-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:c5c155c9c7c65a2e6ff9fd1fd7511b9aa99d2fa7c6777279ceda65d7cf71d7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108700592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b63a66b184460d73080bace4e0f4758af91fcb2fe0a807c771f284a82cea7a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 01:51:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:51:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:30:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 03:30:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:30:08 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 03:30:08 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 03:30:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 03:30:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 03:30:08 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Apr 2026 03:30:08 GMT
ENV TOMCAT_VERSION=11.0.21
# Tue, 07 Apr 2026 03:30:08 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Tue, 07 Apr 2026 03:30:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 03:30:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 03:30:17 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 03:30:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e4fcbd92e8a1b5e786e8affcb256095fd3ff1ecdfa8d1a9d371116d4f6cb94`  
		Last Modified: Tue, 07 Apr 2026 01:52:06 GMT  
		Size: 47.4 MB (47434830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23edbf63854f65bae118974a690a2cfdedb8dd50600ee14b0ee94b0ee71d1cd5`  
		Last Modified: Tue, 07 Apr 2026 01:52:04 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e4d6afbca49f23d2d40fd86019a301d0aab9720f45e118b161621009c3c4d`  
		Last Modified: Tue, 07 Apr 2026 01:52:04 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36b520c5f2de3dd8c11617b45ec30a5c2dfa2d58e978969493bc4907a0d38ad`  
		Last Modified: Tue, 07 Apr 2026 03:30:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb4f453e4578551ee0ee0eeeb7a4f8eda94be0bd8ba370b1e48b7c7fa6497c`  
		Last Modified: Tue, 07 Apr 2026 03:30:28 GMT  
		Size: 14.3 MB (14321202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a978cbb8dde5cb2eb7933f1efa31a49036e93b48214bd20b190b424bb07e29`  
		Last Modified: Tue, 07 Apr 2026 03:30:27 GMT  
		Size: 224.9 KB (224888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:8384be122aff67f907172fa6de7a0fe35086d88b0e9e8312d53d443f266a4c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0342a3ff061791bf5d221364252321c2fef50527da5aa01c3412747c20168537`

```dockerfile
```

-	Layers:
	-	`sha256:245d47b622b528816f0f64f499c1a12a17eff8de66e431fd69f2efe3f0794855`  
		Last Modified: Tue, 07 Apr 2026 03:30:27 GMT  
		Size: 3.3 MB (3349392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e85bc9874fc44cb0caf72248ba6881ced6dd95617a4568d350e25933cb50f8c`  
		Last Modified: Tue, 07 Apr 2026 03:30:27 GMT  
		Size: 24.0 KB (24041 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:3152daf8067f0f282efaa87a649872a3d2d60673fb8bfb9cde9cf8aa514deed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102706381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3078f229ffeb560900d6024519e196800c07e03ca8a15a860c3dcd7478908575`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:07:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:07:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:07:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:07:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:07:11 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 02:07:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 02:07:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 02:07:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:07:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:31:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 04:31:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:31:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 04:31:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 04:31:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 04:31:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 04:31:07 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Apr 2026 04:31:07 GMT
ENV TOMCAT_VERSION=11.0.21
# Tue, 07 Apr 2026 04:31:07 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Tue, 07 Apr 2026 04:31:08 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 04:31:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:31:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 04:31:16 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 04:31:16 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 04:31:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263723128edb5869aa4d437c88c9af9ac8f30b6bae9053afbf15f1096f6a63e0`  
		Last Modified: Tue, 07 Apr 2026 02:07:41 GMT  
		Size: 16.3 MB (16309798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdafbdd9aebfbeb385816faa0f9ee089356f2afcdcaef2f2e88e7b45e7157b9`  
		Last Modified: Tue, 07 Apr 2026 02:08:07 GMT  
		Size: 45.0 MB (45044513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b20dcd1b0bd47f6ebf94572c29572b7d6815520f2b76c1a395aab0171feec1d`  
		Last Modified: Tue, 07 Apr 2026 02:08:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e241e7bf9e372f9cba5539ac54d4aa93835ba2cf21ab535125fe594e69979b5d`  
		Last Modified: Tue, 07 Apr 2026 02:08:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073aedde205485240a7b96acce95f2c45f478ce1cf4a0486cb3da9586a2a41e1`  
		Last Modified: Tue, 07 Apr 2026 04:31:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e566ad9144a2a778a3e1cff6d5c0f5dd80a6bc6a5425bf75aee9166d265df4d`  
		Last Modified: Tue, 07 Apr 2026 04:31:25 GMT  
		Size: 14.3 MB (14294755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a0de37e106aa9a76e22b97a42f46752ea985e2560530b00c0ed3e99479076c`  
		Last Modified: Tue, 07 Apr 2026 04:31:24 GMT  
		Size: 196.3 KB (196306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:d1f0ed1f153634d475018ec4bc26eb6529969575d69edfe4afc7569eb9726683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f0bec7606efb53ca66d6c216b6520161b5d60754f5524f5e6de8525bd4e917`

```dockerfile
```

-	Layers:
	-	`sha256:2feb9fdd872d04402ddcb802bf9f7d9633b93f2ebbe1440562d5f13b01e5386c`  
		Last Modified: Tue, 07 Apr 2026 04:31:24 GMT  
		Size: 3.4 MB (3351796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2cc970f66631dd165a159c5f43e02baeaab5e104a3623bbf878ae9e10a67aeb`  
		Last Modified: Tue, 07 Apr 2026 04:31:25 GMT  
		Size: 24.2 KB (24233 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:6c2b09d689f8339255c3dd376a7d10cdf1c0f78a526f93ffc70242509022cbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107345658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae81526316001da2b5a76990fc85bb4cb92405f62b729397443a713d356387c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:55:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:55:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:55:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:55:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:55:20 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 01:55:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 05:10:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 05:10:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:10:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 05:10:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 05:10:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_VERSION=11.0.21
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Tue, 07 Apr 2026 05:10:00 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 05:10:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:10:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 05:10:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 05:10:09 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 05:10:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e85586aa1fa35e95ae04fb035ce7104d8de3322b854535837c497045363902`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 17.0 MB (16996257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811d5a1425210eb40d3475146ae2d8dabec7bbd43a8d8b417ff3f61b37acebf4`  
		Last Modified: Tue, 07 Apr 2026 01:55:38 GMT  
		Size: 46.9 MB (46922123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f49957433200a3df05046a65cc1b48ef9fd6cdf6cda8add64e579d42193f7b`  
		Last Modified: Tue, 07 Apr 2026 01:55:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490b2f0a27efac9de4a539111d5469e8f436c673b208448b2c0a4c8b3f91bce6`  
		Last Modified: Tue, 07 Apr 2026 01:55:36 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290e66fae70e064355142927336d04f15c2d5e4fc2192b3163167c7d6e7a8970`  
		Last Modified: Tue, 07 Apr 2026 05:10:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b496b34f8875dec8cedf435f721cc75dea459f50ccc320141390513f794e2d`  
		Last Modified: Tue, 07 Apr 2026 05:10:19 GMT  
		Size: 14.3 MB (14325274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89d1813c622320ba3e490ab232040e28bd71cb7a422342032571e930b040b15`  
		Last Modified: Tue, 07 Apr 2026 05:10:18 GMT  
		Size: 225.3 KB (225286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:b5d1c5b009e2619ecdfd1c4c71e88c608d692272e31005ef574a11c178f5dff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad4861ec55a08f5773bc5dce6bcae9e88051bdf7f0f354191ba0e1c2f79179b`

```dockerfile
```

-	Layers:
	-	`sha256:c784486ce8273e920ae7f977fcb992f65a0cf7e48a9c7955b8668666d6a455b5`  
		Last Modified: Tue, 07 Apr 2026 05:10:19 GMT  
		Size: 3.3 MB (3349960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fba780611bcf77cf354cc8e8451b70aec76852949ab71130aae9fcf17c6f6b4`  
		Last Modified: Tue, 07 Apr 2026 05:10:18 GMT  
		Size: 24.3 KB (24297 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:af32846c14ebdeffcd137186d41774bc4f1b0ed4a96f734059faf4ec4b7719fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115057581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e569ff20d321875030c028a71112dee4436d978b9be12800d52518b92e069b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 04:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 04:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:26:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 04:26:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:26:01 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 04:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 04:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 04:30:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:30:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 18:38:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 18:38:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 18:38:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 18:38:59 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 18:38:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 18:38:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 18:38:59 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Apr 2026 18:38:59 GMT
ENV TOMCAT_VERSION=11.0.21
# Tue, 07 Apr 2026 18:38:59 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Tue, 07 Apr 2026 18:39:00 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 18:39:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 18:39:11 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 18:39:11 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 18:39:11 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 18:39:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d800c8df15b3edabc2d41fd12584d685162ec3e3407bdd29445e3916467625`  
		Last Modified: Tue, 07 Apr 2026 04:26:41 GMT  
		Size: 18.8 MB (18813117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccf16e2dc1d63068d675224a73c5538bba659b903eae0eb061e0e3af2d984b8`  
		Last Modified: Tue, 07 Apr 2026 04:30:45 GMT  
		Size: 47.3 MB (47331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81850b7fccbccc658bec33dcb88296f7a032ab1ad4bf008f5b3ef3e5b658952`  
		Last Modified: Tue, 07 Apr 2026 04:30:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756a52d36a643c6a802d035428ac5ecb3dfd122ef97eab521a61e470b8ce18`  
		Last Modified: Tue, 07 Apr 2026 04:30:44 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5d89a33af3c00dd70d1f7346d8b31f8dabd01a05856fa1d64f2e4f9752c8dc`  
		Last Modified: Tue, 07 Apr 2026 18:39:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60389ac0e2a14f15c9efa486ee093ca38787456ab0a91771dbc5de480f1e925`  
		Last Modified: Tue, 07 Apr 2026 18:39:28 GMT  
		Size: 14.3 MB (14340031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5c9ae6dcbee472412de64ec4bb959dbd7625822356c25f7ce2a6733a8f0904`  
		Last Modified: Tue, 07 Apr 2026 18:39:27 GMT  
		Size: 256.5 KB (256479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:59c852df9b7bab0ff8009d9e5224043d97cda36084030a96ff7f64bd9f0aa7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b1a87ee649f6d050a36301f2b811957679a5e2acfab8f8bae29d79b5f7af75`

```dockerfile
```

-	Layers:
	-	`sha256:2f4965c99e5a062099f2852160c52d86cdc766d08abc2b18dd82be03a2e31a91`  
		Last Modified: Tue, 07 Apr 2026 18:39:27 GMT  
		Size: 3.4 MB (3353517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a08e4ee2c605a6c2563a3c2fc2faaa6b7eadd18b6ce510b5d696fb0097666cc`  
		Last Modified: Tue, 07 Apr 2026 18:39:27 GMT  
		Size: 24.1 KB (24147 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:1041d6570cdae988653ad95f1269387f7a0fb0bdda522e3bda3ec2f02d468810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111693263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc19c8558336ab3dbd9b3dc515f3dce209878eb99b7923139815d4c1b48c68e6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Apr 2026 15:35:32 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:35:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:35:33 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:36:09 GMT
ADD file:59e78909d1b1cd9a524f68d8ff44bb077ea09f4f39da5e046d635b48da9d33bf in / 
# Fri, 03 Apr 2026 15:36:13 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 02:18:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 02:18:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 02:18:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 09 Apr 2026 02:18:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 02:18:26 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 09 Apr 2026 02:18:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 09 Apr 2026 02:18:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 09 Apr 2026 02:18:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 09 Apr 2026 02:18:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 12 Apr 2026 18:33:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 12 Apr 2026 18:33:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:33:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sun, 12 Apr 2026 18:33:03 GMT
WORKDIR /usr/local/tomcat
# Sun, 12 Apr 2026 18:33:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 12 Apr 2026 18:33:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 12 Apr 2026 18:33:03 GMT
ENV TOMCAT_MAJOR=11
# Sun, 12 Apr 2026 18:33:03 GMT
ENV TOMCAT_VERSION=11.0.21
# Sun, 12 Apr 2026 18:33:03 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Sun, 12 Apr 2026 18:33:04 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sun, 12 Apr 2026 18:33:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 12 Apr 2026 18:33:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sun, 12 Apr 2026 18:33:54 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 12 Apr 2026 18:33:54 GMT
ENTRYPOINT []
# Sun, 12 Apr 2026 18:33:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:23ef52cbd4674ce4f8269086177a6a1fc3abbc052567212551b8169743067808`  
		Last Modified: Fri, 03 Apr 2026 15:56:59 GMT  
		Size: 31.0 MB (30963791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faed2562a88c01233c65f8ad9488ca495524525b6ca71ec0ba86bca120f9cac`  
		Last Modified: Thu, 09 Apr 2026 02:21:09 GMT  
		Size: 20.0 MB (19983251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9954bc96a34d28507f7ec2940848c672ea912e594d9091be4b71b09f64c4d83c`  
		Last Modified: Thu, 09 Apr 2026 02:21:13 GMT  
		Size: 46.0 MB (46007424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae89b400e8cfef9d0451b9ff75970ad00ed7ab1b1700f1c67c8fa2299028de0`  
		Last Modified: Thu, 09 Apr 2026 02:21:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfe074b4e9249e940efa694ff322e05d2221e6fa792ab5d3e9a29b24240fd1f`  
		Last Modified: Thu, 09 Apr 2026 02:21:03 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08483efa80a6e867f39be20b42907343b3ebef9fc7e0d76ddc33786859f2470e`  
		Last Modified: Sun, 12 Apr 2026 18:35:34 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be29fdc74b7239700e8677bb6856e6e4346ef8f750be5b05f978d5fd3417bd3c`  
		Last Modified: Sun, 12 Apr 2026 18:35:36 GMT  
		Size: 14.5 MB (14508093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01fab87269f93ad326a6a81ffbd57f42a8eb9a30c8e699f516695e618515f56`  
		Last Modified: Sun, 12 Apr 2026 18:35:34 GMT  
		Size: 228.1 KB (228061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:628818a172dfbf185dbd7e842b1792d5e68b79bf213f6b4d8faff03188a14e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3365666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf12656612f584a8d99f7e8f443721944f791268c5039a8b0615e9e668f50425`

```dockerfile
```

-	Layers:
	-	`sha256:bed91a80d2951033803f7d11dcb3ba286aa0a265ea2e6d7a655c5fd7185b7c3d`  
		Last Modified: Sun, 12 Apr 2026 18:35:35 GMT  
		Size: 3.3 MB (3341519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e8fbec64ef69883e06e8ef3c841ded80d4c00a9f8cd2712e8fa6ec896a65d3`  
		Last Modified: Sun, 12 Apr 2026 18:35:34 GMT  
		Size: 24.1 KB (24147 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:c3c1e45216c5dbcffd0ce81103829619c98aee13ac907887acf4d91745525b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106466607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3f05763022090c78771fe6bf759d87bbe80cc391c67b358bb5141c442a6785`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:09:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:09:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:09:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:09:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:18 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 03:09:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='2c12bc1a94c04702935f61f5d15e4950c1ae3f02936931fcc15affc3d22f5d48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 03:09:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 03:09:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 09:42:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 09:42:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 09:42:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 09:42:24 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 09:42:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 09:42:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 09:42:24 GMT
ENV TOMCAT_MAJOR=11
# Tue, 07 Apr 2026 09:42:24 GMT
ENV TOMCAT_VERSION=11.0.21
# Tue, 07 Apr 2026 09:42:24 GMT
ENV TOMCAT_SHA512=8f490ca1af18b11e718859619e4bdd692a65bf40bc5f03401d991680405f9662488b4f11ce4b060ee6b069087435b099188b035ae74c011987ccbb60447811e4
# Tue, 07 Apr 2026 09:42:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 09:42:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:42:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 09:42:29 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 09:42:29 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 09:42:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237151e8b36130c6bd335ee8e6854730bc9390a14aadc664f2ae372078241d0`  
		Last Modified: Tue, 07 Apr 2026 03:09:37 GMT  
		Size: 17.6 MB (17579008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0570d8ef607fe09596a30cc6cc2e2e42c5729e8be5481a984c34c962818a930c`  
		Last Modified: Tue, 07 Apr 2026 03:09:57 GMT  
		Size: 44.4 MB (44409553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4970fbb3bf619cc0ae66f51d3f72f2ba0c8f7351a90f5161f9118a1847130`  
		Last Modified: Tue, 07 Apr 2026 03:09:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2539910064205421e8454c7c7534d7a5f310bed300166a64e3076d5d3af02421`  
		Last Modified: Tue, 07 Apr 2026 03:09:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b484098f70741aa76f4615ddf457ce33ef473facf8dcb34551cd7ed58f13f3d2`  
		Last Modified: Tue, 07 Apr 2026 09:42:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660479af33e1de4c2f17a010fbbff4637e5d482477ff937d51e7ca239d55d2c`  
		Last Modified: Tue, 07 Apr 2026 09:42:43 GMT  
		Size: 14.3 MB (14330770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf17912ab3d1871033c7b5ed3e3c7b2ca7c072ad277e5026823da1c33a9723a`  
		Last Modified: Tue, 07 Apr 2026 09:42:43 GMT  
		Size: 232.8 KB (232789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:a7ae46a72c7a28bb14144002c8a827f1c97d561fdf13f961e093767828a8f83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3375632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63ee42a042f6d66f3aad92ba1a671b0cfa437027ef5bacfc1d685968500fd4c`

```dockerfile
```

-	Layers:
	-	`sha256:f8c781642c0cf0b042a13130dd08bec0280d16c0d31d122e539af060b8ea0c3e`  
		Last Modified: Tue, 07 Apr 2026 09:42:43 GMT  
		Size: 3.4 MB (3351591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6871d0dcddbd2e06153c07f0e4d7e523ba5e3a5f247b136d92460ea1fbfb0264`  
		Last Modified: Tue, 07 Apr 2026 09:42:43 GMT  
		Size: 24.0 KB (24041 bytes)  
		MIME: application/vnd.in-toto+json
