## `tomcat:jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:f955e68e28095acf1943767929ffc49980d228162c793135c5c12214e2ca4f26
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
$ docker pull tomcat@sha256:95c9840c73c7ac638cf20bcdb6d9302acb1d41f875fc8b62e1cd7e867ca90b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108032662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3498a38c8a7e49c92999e13e3df702c6db07008d3582ea6337ba3e67fd26384e`
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
# Thu, 07 May 2026 23:59:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:40 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:59:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:24:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 00:24:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:24:20 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 00:24:20 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 00:24:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 00:24:20 GMT
ENV TOMCAT_MAJOR=11
# Fri, 08 May 2026 00:24:20 GMT
ENV TOMCAT_VERSION=11.0.22
# Fri, 08 May 2026 00:24:20 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Fri, 08 May 2026 00:24:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 08 May 2026 00:24:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:24:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 00:24:26 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:24:26 GMT
ENTRYPOINT []
# Fri, 08 May 2026 00:24:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e233fa9a2426d781eb3a663f5209668a0f543876fe801ffb333d28a7b018f2`  
		Last Modified: Thu, 07 May 2026 23:59:55 GMT  
		Size: 16.2 MB (16152698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90beff01515b4843e02a005e5aed6983c3b40af0454e41e00a84de716f4fd77`  
		Last Modified: Thu, 07 May 2026 23:59:56 GMT  
		Size: 47.6 MB (47564754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fabe90376bfc1c9d02eb490592776f0251a977e98a5fc8e9525ccde67dc7b0`  
		Last Modified: Thu, 07 May 2026 23:59:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690947699dd57d8e357ab0e8cb9995edfd49ff2450152d2b8788515b5b7096b`  
		Last Modified: Thu, 07 May 2026 23:59:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15dff82d70908b129db561ade239659033b3a9ddd0b97166b34f386948f61c5`  
		Last Modified: Fri, 08 May 2026 00:24:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f5332d576f323b87bec2c19824011e97d30f98fab4e40da57a57fce5a39963`  
		Last Modified: Fri, 08 May 2026 00:24:33 GMT  
		Size: 14.3 MB (14346403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3308954d033d108392bf731eefa946f07d870721675677f1d3a501eeb6cb87`  
		Last Modified: Fri, 08 May 2026 00:24:32 GMT  
		Size: 229.7 KB (229666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:25f4f013a42da9821e50f7b878d305daffc061b830bba2a3130354c97e69787d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3963694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fd127d400c0d27ae4dab1add9cddddb20ca0293e06a2e438b2b71bfd5697f3`

```dockerfile
```

-	Layers:
	-	`sha256:62abdd9515b24c4bf66c10d40dc76d00943d5559c2a4751f1985bd673e4b9161`  
		Last Modified: Fri, 08 May 2026 00:24:32 GMT  
		Size: 3.9 MB (3942146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32c635d5a513c14106d3ec77b3644c73a229e6c6928bf25a3144ee8b1071a76e`  
		Last Modified: Fri, 08 May 2026 00:24:32 GMT  
		Size: 21.5 KB (21548 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:840335f7f177d7ed24c5290143529608886e9a0b2c3885a26c75f64067dd8938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102390148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbe8355ab7e92147160dac37be38a400074322028a99ae60925fbafd0b25ea8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 09 May 2026 04:51:37 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:37 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:41 GMT
ADD file:1699ef25ec41cfa214b8beff2f000963a775084d9ce11ff74fa817bb458c27c3 in / 
# Sat, 09 May 2026 04:51:41 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:12:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:12:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:12:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:12:33 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:12:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:12:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:12:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 22:12:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 15 May 2026 22:12:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 22:12:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 15 May 2026 22:12:57 GMT
WORKDIR /usr/local/tomcat
# Fri, 15 May 2026 22:12:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 15 May 2026 22:12:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 15 May 2026 22:12:57 GMT
ENV TOMCAT_MAJOR=11
# Fri, 15 May 2026 22:12:57 GMT
ENV TOMCAT_VERSION=11.0.22
# Fri, 15 May 2026 22:12:57 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Fri, 15 May 2026 22:12:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 15 May 2026 22:13:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 22:13:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 15 May 2026 22:13:07 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 May 2026 22:13:07 GMT
ENTRYPOINT []
# Fri, 15 May 2026 22:13:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:422dc0f0ec960f769d890f368bdf0a0ba195325ef487f5b07a4d06efaa7b2c41`  
		Last Modified: Sat, 09 May 2026 05:25:04 GMT  
		Size: 26.8 MB (26841796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a370957fdcfa2c046e6c7754b461d8b087266af6c02a9c9ca0d98d509b80b4b`  
		Last Modified: Fri, 15 May 2026 21:12:51 GMT  
		Size: 15.9 MB (15893192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfbaa31c70163c821c1379e60f184f3da1ce9e1c1d9ea9d778e276a5824a11`  
		Last Modified: Fri, 15 May 2026 21:12:52 GMT  
		Size: 45.1 MB (45131884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9340fd70edef252f88faaacec81c28015c5da82e1c48e1a7d201426c2030f9`  
		Last Modified: Fri, 15 May 2026 21:12:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c901da25dae29d074c073d5f908632274ad8b04a228553c9ff87f622e6cb5878`  
		Last Modified: Fri, 15 May 2026 21:12:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db312eb41bcb2bf0b356d317021914d572df56a4d4cafcf2ab72d7a086a17886`  
		Last Modified: Fri, 15 May 2026 22:13:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6cbf9b20fb2a5ed0f79efa8bccdb09590f8691049004b94affa39ca5a3d204`  
		Last Modified: Fri, 15 May 2026 22:13:16 GMT  
		Size: 14.3 MB (14318199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea802cd1c8d3e95e75130b8fe9ca984157a90fb532b4b4434c7eee9bba0a0b19`  
		Last Modified: Fri, 15 May 2026 22:13:16 GMT  
		Size: 202.4 KB (202433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:9d5886a3f861716009614a64fa09acbf3f1a3f4f199963ec07e32b403a147708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b5aa154ade7fb72816352001d23bb7280d9ea1541de48ce59bac2a9e353ed9`

```dockerfile
```

-	Layers:
	-	`sha256:f74a416a5077c47e52ec2ec60baf87550f6c88a133aad67d2587cf499e65c32a`  
		Last Modified: Fri, 15 May 2026 22:13:16 GMT  
		Size: 3.9 MB (3944493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d81e3b77b9793e2db2b2c3f72962a76ecde8b8fdd5b7918fedcde098987177d6`  
		Last Modified: Fri, 15 May 2026 22:13:15 GMT  
		Size: 21.7 KB (21676 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:14854a65235d2d42e2a50a0b47f2b75a93fc39eb8994f2afe20a0beac32386b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105311169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fc25583891b239e73de606cae2aedb9190558ebc5f032b6441810fc2e5087b`
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
# Thu, 07 May 2026 23:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:06 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:59:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:10 GMT
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
# Fri, 08 May 2026 00:24:20 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 08 May 2026 00:24:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:24:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 00:24:29 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 00:24:29 GMT
ENTRYPOINT []
# Fri, 08 May 2026 00:24:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959dacbeeb3d16a92354f9d67deddec1e89003269f4432cfbf8e46286a97fe1`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 16.1 MB (16076177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c594e1edc9977ad3a65e0f725187bd270bfacdf75ebfa13000e465215bac98d3`  
		Last Modified: Thu, 07 May 2026 23:59:27 GMT  
		Size: 47.1 MB (47050262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d5d773bfbc3dc1169cc436b31f0e1debb520687663e282d3fefde0c64ff92`  
		Last Modified: Thu, 07 May 2026 23:59:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771827679748aff6fee75de328131e1e2609e9c1ea12c71728800755bd7437f8`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca434de8807b0e617aa519e38a3c6c2e52bf7b54ae1778c918a7a8200e81eff5`  
		Last Modified: Fri, 08 May 2026 00:24:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333d42d70729c4c1221b70334ae11b06e168d9d7df7889ae5bad3349c8b30771`  
		Last Modified: Fri, 08 May 2026 00:24:38 GMT  
		Size: 14.3 MB (14346834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac440c0ed33799282866424f85962ec2d5d4b4edcbd7d39df8ecc1a45abe8fb6`  
		Last Modified: Fri, 08 May 2026 00:24:38 GMT  
		Size: 228.7 KB (228711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3c7c82327185a45332b0515adf9d15e1d6df66e144fbc3e831f4278d9efb11f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3963535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220db9fd34ebbf3dfeecccbc99c9e71f446acec197e41f32e3b23ea00728c77c`

```dockerfile
```

-	Layers:
	-	`sha256:f3d0f05013cc784d90f01d49ad549e092f6ce3a280b4c40b0c611de561503c3b`  
		Last Modified: Fri, 08 May 2026 00:24:38 GMT  
		Size: 3.9 MB (3941827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528f87d16bb9f916d8b3b8dd6df9a452ee7cfd30b21ee131685fae411f5b0074`  
		Last Modified: Fri, 08 May 2026 00:24:37 GMT  
		Size: 21.7 KB (21708 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:0e2cf7a9ea61f6d34ab3027ddc8ac138cd80590d65e509fa83514ec0238f3f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114379230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4844fe55176589a6a71ec8299a9f4d17a3e7f606781f7dbb3f41a92dc3b867`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 00:08:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:08:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:08:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:08:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 01:29:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 08 May 2026 01:29:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:29:12 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 08 May 2026 01:29:12 GMT
WORKDIR /usr/local/tomcat
# Fri, 08 May 2026 01:29:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 01:29:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 08 May 2026 01:29:12 GMT
ENV TOMCAT_MAJOR=11
# Fri, 08 May 2026 01:29:12 GMT
ENV TOMCAT_VERSION=11.0.22
# Fri, 08 May 2026 01:29:12 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Fri, 08 May 2026 01:29:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 08 May 2026 01:29:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 01:29:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 08 May 2026 01:29:20 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 08 May 2026 01:29:20 GMT
ENTRYPOINT []
# Fri, 08 May 2026 01:29:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63547f1d1a11cf1ca686dfb040571560bc2bb1758e416deef521d6e7ba04e95`  
		Last Modified: Fri, 08 May 2026 00:09:13 GMT  
		Size: 47.5 MB (47487447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45d6f9c4ba053fa7791ab933b4e8f064feab6632b55d9bf0277a1ade6cd7819`  
		Last Modified: Fri, 08 May 2026 00:09:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7880754df2ca5b7d2b60a4ba8e796203260e6c4cb24a0cc583d470917d2341`  
		Last Modified: Fri, 08 May 2026 00:09:12 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5f47e8125c425f4523425932c7aaab667fe6c4c213bbfe0bd80121b0949b90`  
		Last Modified: Fri, 08 May 2026 01:29:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12872ca33c42842384540cb0dfd2cbe44a3d884710444b06509c2027f815845`  
		Last Modified: Fri, 08 May 2026 01:29:35 GMT  
		Size: 14.4 MB (14358156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38686d1e626bef2e9c7d26c8c16172cbd6cca631512c86fba95fbc7c813e19c9`  
		Last Modified: Fri, 08 May 2026 01:29:35 GMT  
		Size: 259.0 KB (259043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:2e6328f5e478446c34c3f7e9861e590aaa3b997b65eaeded7b16063458064309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c528942f0205ab2d435e7b84f1d0fb6956c26293f082afb22f9fc306eb767dd1`

```dockerfile
```

-	Layers:
	-	`sha256:d0623ff195e95ad27e5229b82536da707f70afb84ecd7bf0e82d5f7bc44d4dbb`  
		Last Modified: Fri, 08 May 2026 01:29:35 GMT  
		Size: 3.9 MB (3946240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a7d568015d75ee8b5c9fd75ee60ed2f3704f061bc00b2335b5a2b46963fd06`  
		Last Modified: Fri, 08 May 2026 01:29:35 GMT  
		Size: 21.6 KB (21605 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:c2288f8c78a4f79991cfdc563bbe60a1178da499aff6c61158260f072559792d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103477487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308276f2baee6eb68fb88acd64c56780dfd286f8587bbb644b0df55aa7afe8b4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:13:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:13:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:13:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:13:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:13:54 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:13:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:14:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:14:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:14:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 22:11:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 15 May 2026 22:11:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 22:11:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 15 May 2026 22:11:39 GMT
WORKDIR /usr/local/tomcat
# Fri, 15 May 2026 22:11:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 15 May 2026 22:11:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 15 May 2026 22:11:39 GMT
ENV TOMCAT_MAJOR=11
# Fri, 15 May 2026 22:11:39 GMT
ENV TOMCAT_VERSION=11.0.22
# Fri, 15 May 2026 22:11:39 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Fri, 15 May 2026 22:11:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 15 May 2026 22:11:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 22:11:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 15 May 2026 22:11:43 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 May 2026 22:11:43 GMT
ENTRYPOINT []
# Fri, 15 May 2026 22:11:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb97a9221f0b542a2e021e162ce33d47a57cfd26f54a1c0dbcb6904fc84f0093`  
		Last Modified: Fri, 15 May 2026 21:14:36 GMT  
		Size: 16.2 MB (16151024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d50e31230646ffa8f9dec76eb15cbc010a471af5820bf1f6792fb2824f3ff25`  
		Last Modified: Fri, 15 May 2026 21:14:35 GMT  
		Size: 44.5 MB (44542181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5a10e354f6300409449146a9bef5bc44fb5316820e82a1c8b34c09c732424`  
		Last Modified: Fri, 15 May 2026 21:14:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81126cbe282f3c5290c4b248d2d6cfc5a458c94d88466cd127d0b87ed6d8b89c`  
		Last Modified: Fri, 15 May 2026 21:14:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49049f926c07f6f92e8b3a9c45688c6db1b059d6094532efbeae2815708e407`  
		Last Modified: Fri, 15 May 2026 22:11:57 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e191028fafc0473941c0f4661c288b5a152aaf058789a875d360f8fe6ee3a6`  
		Last Modified: Fri, 15 May 2026 22:11:57 GMT  
		Size: 14.3 MB (14348144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71affe9d03587bb5a6b3df3865aa12180792a01ab7918792b7c1c0eb6c49e80e`  
		Last Modified: Fri, 15 May 2026 22:11:57 GMT  
		Size: 231.2 KB (231187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c4815c66d61fc7cb68443ad512757da63930be837b1528bc8713e2ede9763011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23ab1f61b1b95354c4fe743d57f2a2b13e62a3512fa3b2c06b1010f968e5a81`

```dockerfile
```

-	Layers:
	-	`sha256:165730e098c2533d7d5ae6a43c3e513afa6bb84bbd0123d413a0a403657942d1`  
		Last Modified: Fri, 15 May 2026 22:11:57 GMT  
		Size: 3.9 MB (3943741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7da12a927d82314f786d855b1409fb6eed896aa43076c9545db8e8a5865aa14`  
		Last Modified: Fri, 15 May 2026 22:11:57 GMT  
		Size: 21.5 KB (21548 bytes)  
		MIME: application/vnd.in-toto+json
