## `tomcat:jre17-temurin`

```console
$ docker pull tomcat@sha256:13519362b3b23c30098788c6d7686062d0fce042c3cdc6edbba17eec7e20eef8
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

### `tomcat:jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:854fd866e67075a54033d974de9e7459dfb51d517405e01fcc59680b9dd2168b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108843583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04ec940e93ff8539ac76e6dffe1f8f317fc9da1a8a2140b5b2284e358ea3ecb`
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
# Thu, 07 May 2026 23:59:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:33 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:59:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:24:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 00:24:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:24:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 00:24:18 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 00:24:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:18 GMT
ENV TOMCAT_MAJOR=11
# Fri, 08 May 2026 00:24:18 GMT
ENV TOMCAT_VERSION=11.0.22
# Fri, 08 May 2026 00:24:18 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Fri, 08 May 2026 00:24:22 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 08 May 2026 00:24:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:24:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 00:24:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:24:27 GMT
ENTRYPOINT []
# Fri, 08 May 2026 00:24:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b419ce69b7492def2771bf179c9ff6e02c56d494802d6ba1a56cffb6ee6b1d0`  
		Last Modified: Thu, 07 May 2026 23:59:47 GMT  
		Size: 17.0 MB (16984056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b915181aaf7c04e2cf1641ec5c26247922173f6dde90793a8d49ceeaaee46edc`  
		Last Modified: Thu, 07 May 2026 23:59:50 GMT  
		Size: 47.6 MB (47565016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb964fafce6eb62a36389e3a01144710c7fc99ebfbaf4bc3a7bb214acb10d8f7`  
		Last Modified: Thu, 07 May 2026 23:59:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b317ba485df97a68cb8e6e60aa4e28bb41e662be5eaf897cf5aa09e315a50e`  
		Last Modified: Thu, 07 May 2026 23:59:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83ec4e04800c2b8f9c26e479257245d5def45468e33d92066527b8d488389dd`  
		Last Modified: Fri, 08 May 2026 00:24:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9859541d3b3e6ca5be8184f5894a4ae242367996bb0378e663ca4278a2c26c1`  
		Last Modified: Fri, 08 May 2026 00:24:36 GMT  
		Size: 14.3 MB (14334142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e6a01764bf2ee3a9995bc51bf0246baaa7f492e56964958a961c3900537c30`  
		Last Modified: Fri, 08 May 2026 00:24:36 GMT  
		Size: 224.7 KB (224745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:048b24fcdf5d6e948a1377bbba8ca47273edc89ad2252f23d9cd48515f031ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0260e0e779692d4268b4921f6535dcdcb522b515281cb4e97771bab741cba1c`

```dockerfile
```

-	Layers:
	-	`sha256:8d52e82f093d999a4f20725f6cf82088596e37de2306335607759bb83cea49da`  
		Last Modified: Fri, 08 May 2026 00:24:36 GMT  
		Size: 3.4 MB (3350019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a80f02e29db3bd5be695e61ba42f6f0a83204711c7a2ab35fbe664a6c0201a6d`  
		Last Modified: Fri, 08 May 2026 00:24:35 GMT  
		Size: 24.0 KB (24044 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:489f998f81eee8cd130d558ec7c32410e1814479cf8f2a7705c09e19eb3a8251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102807922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2ca34d74c3b0c779369a3116d711b49de4ef6f90172f6e0b08a8a65c827871`
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
# Thu, 07 May 2026 23:59:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:48 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:59:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 01:13:36 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 01:13:36 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:13:36 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 01:13:36 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 01:13:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 01:13:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 01:13:36 GMT
ENV TOMCAT_MAJOR=11
# Fri, 08 May 2026 01:13:36 GMT
ENV TOMCAT_VERSION=11.0.22
# Fri, 08 May 2026 01:13:36 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Fri, 08 May 2026 01:13:36 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 08 May 2026 01:13:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 01:13:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 01:13:47 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 01:13:47 GMT
ENTRYPOINT []
# Fri, 08 May 2026 01:13:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e59ea925001651cf30cf1fb3c0e451ba91883f11a386bddc78897aa619ac04`  
		Last Modified: Fri, 08 May 2026 00:00:12 GMT  
		Size: 16.3 MB (16310703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08b5d9f23eb00eb33c26a3a56029aff508baff5aa31fd78637febb6ab220c31`  
		Last Modified: Fri, 08 May 2026 00:00:12 GMT  
		Size: 45.1 MB (45131964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb3d54c2717c18e502a22d72fe6b263f5e12b2cd401ceec5b40a270f8a183a1`  
		Last Modified: Fri, 08 May 2026 00:00:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec7da90fc0b17f089e1a5a4b1f6aba42f7d922ee11faba3d2c730589bf44d58`  
		Last Modified: Fri, 08 May 2026 00:00:12 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5861fe3dc1e356972fbe43c1f5f63c04c2791ede75b331f66bade72c399f12`  
		Last Modified: Fri, 08 May 2026 01:13:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec193ff2ee4ef1331c6816d24a490c0d09bf113889a9b5e5f661eab85687aa`  
		Last Modified: Fri, 08 May 2026 01:13:56 GMT  
		Size: 14.3 MB (14306593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6388cee0a34b4726e870318ef6b272c1e1b5c684b0642b057f221114fd9ec08f`  
		Last Modified: Fri, 08 May 2026 01:13:56 GMT  
		Size: 196.3 KB (196328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:8cae5473cf99c84072c0659b5d4e4df0e114b260a4e8a519333cccd20ef26d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd4051361b3654da0aa85a1eba1d8da0110274e70dc76be66d2899cc7e63028`

```dockerfile
```

-	Layers:
	-	`sha256:be6e4f36da856d875b123186e918335020ea375172c3883abd2b7958f8a7a651`  
		Last Modified: Fri, 08 May 2026 01:13:56 GMT  
		Size: 3.4 MB (3352423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795df458d15e69908ea98f33b94cf77a6b096700b6a595b33bb57bdcb41b1304`  
		Last Modified: Fri, 08 May 2026 01:13:55 GMT  
		Size: 24.2 KB (24236 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:705660e3ca0d7915447c4327c5b883d70c92e5cdbb94efb5e6bfcf65ab7f104c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107487794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e86500bdb4e0a347dd8950a6dda01bfa830c403a61b19611d4a765f991a3c2f`
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
# Thu, 07 May 2026 23:58:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:58:56 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:58:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:58:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:58:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:58:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:24:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 00:24:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:24:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 00:24:19 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 00:24:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:19 GMT
ENV TOMCAT_MAJOR=11
# Fri, 08 May 2026 00:24:19 GMT
ENV TOMCAT_VERSION=11.0.22
# Fri, 08 May 2026 00:24:19 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Fri, 08 May 2026 00:24:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 08 May 2026 00:24:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:24:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 00:24:30 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:24:30 GMT
ENTRYPOINT []
# Fri, 08 May 2026 00:24:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23892ba79f85a72c97e9f6ffd7eee9884b681317a9998d5cd0a6753d77e25979`  
		Last Modified: Thu, 07 May 2026 23:59:11 GMT  
		Size: 17.0 MB (16997481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63287ffff8e6b3a9e9d7060a8d080083dedfa5512352a8415ded0304b8a0ba`  
		Last Modified: Thu, 07 May 2026 23:59:12 GMT  
		Size: 47.1 MB (47050254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582493c6c3c919ffd24e17870811a733953fa5035d34503bc1d73968f107c629`  
		Last Modified: Thu, 07 May 2026 23:59:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2445ed0c0bfb140398df91ee6a3e20a1c1fc8853aeb6ab1a11af4f04d19d87e8`  
		Last Modified: Thu, 07 May 2026 23:59:11 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5985029219c6d0186c8375a9ad1d6bf6bd8a56d851322aa48c2319797d21718`  
		Last Modified: Fri, 08 May 2026 00:24:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79d3f2ef90b977f8475c966242241e90a35eca0a8e53df681211e035436196e`  
		Last Modified: Fri, 08 May 2026 00:24:39 GMT  
		Size: 14.3 MB (14336356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c464d61adcc9446afc40125e25f97e13423b2242d9df8aa850eceaa0a158a5d5`  
		Last Modified: Fri, 08 May 2026 00:24:38 GMT  
		Size: 225.3 KB (225273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:1945f4704a54e9a154de87c695bee688b169b7f8c96b15de337fd4d1fc5ad9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d324ee80b9ea1a9e14c2bcc1d06bc08e274e679259042c8c1ce09ac68cf3b24`

```dockerfile
```

-	Layers:
	-	`sha256:9c7e7064d3ea97a903fe67d5e85e1ffa99453f212e019bf74cfb640982a3aae3`  
		Last Modified: Fri, 08 May 2026 00:24:39 GMT  
		Size: 3.4 MB (3350587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3650d2af5c1ea51a0e4144ea8e1c8d6c161e7268705b46c2c94134b5a2fd2420`  
		Last Modified: Fri, 08 May 2026 00:24:38 GMT  
		Size: 24.3 KB (24300 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6ac54d20bbf5a234cb7395e108e5d178652d24131e9d7f81daa0407a5817b2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115225306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37984aa3aaec7ef8cdcfea0d591978e103f7c315865aae3de1ca38cfffae6ed6`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 00:08:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:08:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:08:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:08:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 01:28:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 01:28:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:28:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 01:28:28 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 01:28:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 01:28:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 01:28:28 GMT
ENV TOMCAT_MAJOR=11
# Fri, 08 May 2026 01:28:28 GMT
ENV TOMCAT_VERSION=11.0.22
# Fri, 08 May 2026 01:28:28 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Fri, 08 May 2026 01:28:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 08 May 2026 01:28:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 01:28:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 01:28:36 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 01:28:36 GMT
ENTRYPOINT []
# Fri, 08 May 2026 01:28:36 GMT
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
	-	`sha256:afa634af861b3827e95aba0a3e58ac57307f481355b23e526e3d9b8251eccd5d`  
		Last Modified: Fri, 08 May 2026 00:08:53 GMT  
		Size: 47.5 MB (47487565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64758edb6b2707e1ad93e4e2f619262f302218d46c1c3b9b9df135424897756`  
		Last Modified: Fri, 08 May 2026 00:08:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96a1b415902c4f2a4f00e7db51f275a89178b567df846420cdf4f26c10e687`  
		Last Modified: Fri, 08 May 2026 00:08:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3032cb67b5d0ad66932f632511ff288885de99d7b7d958b131b4e4645e12997d`  
		Last Modified: Fri, 08 May 2026 01:28:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18101b3b119cb038ec9638d9ff7bfadf4ffa62acf3a602b5a24bc61b61ee8ae9`  
		Last Modified: Fri, 08 May 2026 01:29:05 GMT  
		Size: 14.4 MB (14350916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e8ff1f5bc5a43f7a0118cc462347b4d9266d77a10eeea4d007f15bbea8d03`  
		Last Modified: Fri, 08 May 2026 01:28:58 GMT  
		Size: 256.7 KB (256696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:788d8acab61a15691754ce8aa5cbc3a72fa12ef67863b4379d20c893e2ee8e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3378293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85963536e13dadcb071c557a8631a449904d0732ab0b8f9219596f264ff8da8f`

```dockerfile
```

-	Layers:
	-	`sha256:37ee42a1ae9128be14187e598f00dec87ab88ea218041babd10a7d6ad9dab862`  
		Last Modified: Fri, 08 May 2026 01:28:58 GMT  
		Size: 3.4 MB (3354144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5823e6844894569e2f4523f254829d0d7556680c361d3344c5fe07042b4aab4d`  
		Last Modified: Fri, 08 May 2026 01:28:55 GMT  
		Size: 24.1 KB (24149 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:1e3e7a3cc1b22b3134c6d6bc223d3fe5cd8fe72f28870c531f0a2d009f30540e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109703907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bed52c157094f872d898c03124f6794b9e82d54d18de6a3bfaf2b0a6f7f174`
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
# Sat, 09 May 2026 05:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 05:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 05:31:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 09 May 2026 05:31:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 05:31:45 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Sat, 09 May 2026 05:32:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 09 May 2026 05:32:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 09 May 2026 05:32:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 09 May 2026 05:32:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 14:24:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 14:24:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 14:24:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 14:24:29 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 14:24:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 14:24:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 14:24:29 GMT
ENV TOMCAT_MAJOR=11
# Tue, 12 May 2026 14:24:29 GMT
ENV TOMCAT_VERSION=11.0.22
# Tue, 12 May 2026 14:24:29 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Tue, 12 May 2026 14:24:30 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 14:25:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 14:25:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 14:25:25 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 14:25:25 GMT
ENTRYPOINT []
# Tue, 12 May 2026 14:25:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68a4373f628edc661d7177c5f23899a21c354dc26d25031de0c1290c4e2ea01`  
		Last Modified: Sat, 09 May 2026 05:34:26 GMT  
		Size: 17.9 MB (17875393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde45dc07ffd729ced8e42279de0f6107309543dd0bdc6146a19c9f75ff4a786`  
		Last Modified: Sat, 09 May 2026 05:34:30 GMT  
		Size: 46.1 MB (46111471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d507b7d700249459e8e079ad9c7b940db53f796aba9bab4a3a6b1a50c1063e3`  
		Last Modified: Sat, 09 May 2026 05:34:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9c2a04af7a172212f933295d041519d5279a08b828d60555e4a913eab4f43a`  
		Last Modified: Sat, 09 May 2026 05:34:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d216f6c55ce388d5b62e55daa8061cf3ce95d8640dffb83349c4bdeb1a1ec`  
		Last Modified: Tue, 12 May 2026 14:27:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ced3f46fd0bb763e139f5262886c6c3ae702eebb6e9ae3353e35a88e774e34`  
		Last Modified: Tue, 12 May 2026 14:27:09 GMT  
		Size: 14.5 MB (14521093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cfd5778da4cc807b9790ec74012bd2e83c2d75b52df1046ec7acc39e5139f7`  
		Last Modified: Tue, 12 May 2026 14:27:07 GMT  
		Size: 228.0 KB (227978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:630042c3483426dd41da15876eeda605d527283fa7fd31c1960c33b2394c789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3366296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbbfdcd225cc0beb02f61f292ee552d91bc55b2a287f83292fd81a360ef6cde`

```dockerfile
```

-	Layers:
	-	`sha256:fa7adc9fb2e04182250594cec8c4c434473aeb83c1557573b7116f62278c593c`  
		Last Modified: Tue, 12 May 2026 14:27:07 GMT  
		Size: 3.3 MB (3342146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34ff74ea30bdf0fd9dd32c7d122d018b3ac6beffe0d3cd1ef28802e93a0a5966`  
		Last Modified: Tue, 12 May 2026 14:27:06 GMT  
		Size: 24.1 KB (24150 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:c9e4b3a8bd1444455c5b0dc825dbde6c1ddeb576c393fa21f5f1b5340f0858b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106612384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f5da2290edce1db3ba0cbcbded3ec76047830d1e0a6e00d1b7c0fa35ed893c`
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
# Fri, 08 May 2026 00:03:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:03:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:03:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:03:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:03:23 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 00:03:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:03:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:03:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:03:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 01:12:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 01:12:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:12:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 01:12:35 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 01:12:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 01:12:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 01:12:35 GMT
ENV TOMCAT_MAJOR=11
# Fri, 08 May 2026 01:12:35 GMT
ENV TOMCAT_VERSION=11.0.22
# Fri, 08 May 2026 01:12:35 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Fri, 08 May 2026 01:12:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 08 May 2026 01:12:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 01:12:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 01:12:42 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 01:12:42 GMT
ENTRYPOINT []
# Fri, 08 May 2026 01:12:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff4ebc40e1b77e1f1dfef351dd8a6878a782aa00ac2e0b3a9c07d846226b5d`  
		Last Modified: Fri, 08 May 2026 00:03:44 GMT  
		Size: 17.6 MB (17579819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104004eda82401a938263e4f1db51eb6a96f588c3ea34795635387180cd5ff56`  
		Last Modified: Fri, 08 May 2026 00:03:44 GMT  
		Size: 44.5 MB (44541868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1180b37ae76dd60716d5406d22023bb101e0f6415364c8d9551c5020ce24e6`  
		Last Modified: Fri, 08 May 2026 00:03:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea1acc98c8f04c54bab2bed5bc859756e4401735204449632f79cecd3329296`  
		Last Modified: Fri, 08 May 2026 00:03:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1be0cf37a8bcf469e1ee4dfe12b300c207ab8bebf2cd1de81c47b8e4bf6dde`  
		Last Modified: Fri, 08 May 2026 01:12:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2eba9f0338c688bb8664e33dd88522de6d1045e243a63bb3a84986db6cb342`  
		Last Modified: Fri, 08 May 2026 01:12:57 GMT  
		Size: 14.3 MB (14343041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee742b501f8fd3ab2069a4dd1651e2a51fb2ef7e7798ed77ddd9f3866cfc3f0`  
		Last Modified: Fri, 08 May 2026 01:12:57 GMT  
		Size: 232.9 KB (232864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:fcb3369373d3fdd3e0285b3cba2bc6fa98d11546f9b0201834fded3c9743b1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0941effce6dfec95ab196524795dec049ab3546fcf56f52bf6da1656c1f5b5`

```dockerfile
```

-	Layers:
	-	`sha256:3fa234d21539e40e4faaebb8ed88223fa4a746cb7f93e828609b324fca37e824`  
		Last Modified: Fri, 08 May 2026 01:12:57 GMT  
		Size: 3.4 MB (3352218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e473a258d5f463dca47c5f0ef35f2b31870a60f6165403df91ea8541199df31`  
		Last Modified: Fri, 08 May 2026 01:12:56 GMT  
		Size: 24.0 KB (24044 bytes)  
		MIME: application/vnd.in-toto+json
