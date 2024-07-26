## `tomcat:jre17-temurin`

```console
$ docker pull tomcat@sha256:7b67ba924866f4de3b09aa168a77456726598dd947c313427243270017d49896
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

### `tomcat:jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:5a5af80b0a01288af72d7ca2eda11deb1b08d69ad97c0254059184c21586da5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103748311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bf3b63f3436fe7011aa998bb67c8621dbac2a7cc508a0c106a54f001d730f7`
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6398c3721538bd8622ff98a27b2a746ee39009329d907fb51d4fa9d6d8b8eeb`  
		Last Modified: Thu, 25 Jul 2024 20:08:42 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217a379205404a554d1f5331709aeb8f5c44f22e2d713160f4ea32bc738e32a2`  
		Last Modified: Thu, 25 Jul 2024 20:08:43 GMT  
		Size: 12.9 MB (12937162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a98e2715be075dc795b6f8ec5bb83ad222959b250097323c6bfb9d41ce8dc2`  
		Last Modified: Thu, 25 Jul 2024 20:08:42 GMT  
		Size: 217.8 KB (217823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:7b5e687d62b53cd083765e7b13a27e47b35e403f493b0ca633aa46fa64199517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a5b03ce571e6d9762865543e39a7ff8ba7912458e1aee8cbfcf1a74c16590c`

```dockerfile
```

-	Layers:
	-	`sha256:31eda98e0664c3abf0299950311f8dbdbb304e520351536dffd6c7da283bd2c0`  
		Last Modified: Thu, 25 Jul 2024 20:08:42 GMT  
		Size: 3.5 MB (3532943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be756d9b37cdb8923f6c33a10fa17990f12f8b3a95fba9cea31f5e49d251b212`  
		Last Modified: Thu, 25 Jul 2024 20:08:43 GMT  
		Size: 24.6 KB (24578 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:dfb85e7bbbd0903c14abefa7e7d5f3296c4be3097c4b175ea0160eb721150f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98045142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1547624e54c406e3e85fa62bf36b5ed84242e6d0337c9fddd2265e6425e24f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a19afd6824ec92d0dc0c87f846a2dee26a1132e6aa125aee604683db3e3a56`  
		Last Modified: Tue, 23 Jul 2024 03:18:36 GMT  
		Size: 44.9 MB (44944593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e95f385aa63517fa26c24d9a8f8a15f7feae4d7c42425411cadc98adb73bf4e`  
		Last Modified: Tue, 23 Jul 2024 03:18:28 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0484280a520269e7fbbb3c0f5ba3542505bf0771b364d9a577b63757570033b1`  
		Last Modified: Thu, 25 Jul 2024 18:03:26 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66de3d9064c9ac596026dfc2c1fed4ab1a3087723160bc15f03f3bf64b5f0e0`  
		Last Modified: Thu, 25 Jul 2024 20:35:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705af490002c3857f638c1e6434e1c6ee7d88661068d0c689b0482b70a63582e`  
		Last Modified: Thu, 25 Jul 2024 20:35:58 GMT  
		Size: 12.9 MB (12910446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e547bb923f76a21884f2b47dadab5f81bc9081b536402730df71defd929769`  
		Last Modified: Thu, 25 Jul 2024 20:35:58 GMT  
		Size: 190.9 KB (190894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:3efc61df2ac4cede68c483a7d834bd4dd8a7745606990481f2b25bc539da083d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4bc605a835b592360f7590610e5bbabf25efef836f32e91d772b2300146c9f0`

```dockerfile
```

-	Layers:
	-	`sha256:c6c5f33f0591be4f746e91e4c8d27964f2e52c066c13166cc1cec67702d6f7e0`  
		Last Modified: Thu, 25 Jul 2024 20:35:58 GMT  
		Size: 3.5 MB (3534238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:681e4d714f4e58132c89dcd5b3bc980c41f21acae7b9d24463ff5f9141e5632b`  
		Last Modified: Thu, 25 Jul 2024 20:35:58 GMT  
		Size: 24.8 KB (24784 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:bbb87725b2ccafbd84e3aad8173314cb4571bbf181f8234356b444c10e52a8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101116949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb387753346b7cd7bcdbd5a9831a8cc7f81fd5f8ecb1499dd37bfa723158348`
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bdf074211340aa0bb9e65f26324e0e9f0596e54d686991659e80e2234ac9cd`  
		Last Modified: Wed, 24 Jul 2024 18:04:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13d9fdb66e60a2b37d3292696d925129d485bfcc74650d1ca23dd2758ea092d`  
		Last Modified: Wed, 24 Jul 2024 18:04:28 GMT  
		Size: 12.9 MB (12937877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb1148dfe86dab3022af918dcd285c350b27030500fb32725de39c9f8b399c4`  
		Last Modified: Wed, 24 Jul 2024 18:04:27 GMT  
		Size: 216.8 KB (216816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:e4115214365711a105e45a022b1479c29f270d3121c80216b0a6e05e74e3505b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f84b31252b727c2b6cd2658783c0b6efca34417eb794171bced13635533ca1f`

```dockerfile
```

-	Layers:
	-	`sha256:8688d789548c93ede62c978f6eb3969247c5bf1286553a61d8a82955e4c0ebb2`  
		Last Modified: Wed, 24 Jul 2024 18:04:27 GMT  
		Size: 3.5 MB (3533331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9718f7191ccac7d911e03a16a25488a3766dd4b236b8bb3605f85645a46480`  
		Last Modified: Wed, 24 Jul 2024 18:04:27 GMT  
		Size: 25.3 KB (25335 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:a7a972591bebe50c50e28fd4410ae27132549612ce39e01f5d945ea5f01289fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109621175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cdd3d67ad2eaa2add16c9baea3778b4d4473913c82ad314a9627229539594c`
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
# Fri, 12 Jul 2024 17:34:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 17:34:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 17:34:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb31ba8991bd13ec24ef7b7bda39efcdd774e50b2bd85287b28c64f84c5d8e7f`  
		Last Modified: Fri, 26 Jul 2024 00:07:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e927733b14f2389ec308d1e455d565b486f951aedbe51f84038a35c950207bae`  
		Last Modified: Fri, 26 Jul 2024 00:07:21 GMT  
		Size: 13.0 MB (12950141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a5dfb97c8f2a0ebe90c4c2208824c6a3049a594a5ac0f37e464828660c038b`  
		Last Modified: Fri, 26 Jul 2024 00:07:21 GMT  
		Size: 249.6 KB (249632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:c604559c6247afacfad5b20b05128f69289693a1e6fd11660770f87465dedf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485458ffb7ff1544369da298ffdafb6e88d4872d17868674f74ca17450920349`

```dockerfile
```

-	Layers:
	-	`sha256:2edf220c45e9fbd0a270538cc22470692d82c8272835449b055e61a9361d1e10`  
		Last Modified: Fri, 26 Jul 2024 00:07:21 GMT  
		Size: 3.5 MB (3537510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:005370d84dd221cb17775f86a80159d87306487cdadce354d237c3d92fe2b7be`  
		Last Modified: Fri, 26 Jul 2024 00:07:20 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:070a343ca461e7445ac7e7ad00eb152f7aa0974f5200a75f1a7e4d9e7489ff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98618138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd432d5d615dfffc501f74f0b9f32419630353c7b62d360ac2092c759a6cf12`
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 17:34:49 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:cc2daba858b3a1c053285ff07cbbbc4a61154a3259ca12a1050495c78b2f497f`  
		Last Modified: Tue, 23 Jul 2024 02:43:54 GMT  
		Size: 43.9 MB (43864232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da80df5ffcb165f8c3f70c45e38e83dd4b4b34c5f3787f6d3de600abd0725ad8`  
		Last Modified: Tue, 23 Jul 2024 02:43:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea8ff02a44909bdabb4629a754a68b565a55896426ec6260d76aced4c7397c9`  
		Last Modified: Thu, 25 Jul 2024 17:48:53 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d789fc47b1f63804186ef85562d14d2cf0cd91bc82d5bf985fed23b962030158`  
		Last Modified: Thu, 25 Jul 2024 20:18:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695106065275989ffe06a76c3fb5823ebf19871fc7d049170d62842be13e1d0e`  
		Last Modified: Thu, 25 Jul 2024 20:18:01 GMT  
		Size: 12.9 MB (12939989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a480e37c98be2f64b520262b8d0568b606fbfb8d9822f2a01eaaa143d7e2a4a`  
		Last Modified: Thu, 25 Jul 2024 20:18:00 GMT  
		Size: 219.3 KB (219296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:faab2947bd494bf1d6cca46be72310f9a09b0962f40b2a80f4c0f59000c33620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebf122c14923a730be7178b601579cb4757d4df7002ce19db8d467b061186cb`

```dockerfile
```

-	Layers:
	-	`sha256:a71f14e711b0fb4be81b2e066185d483236a1246a4e31ad8be6996617311ffdb`  
		Last Modified: Thu, 25 Jul 2024 20:18:00 GMT  
		Size: 3.5 MB (3534065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528afe95aede3c35c04d2b06c31d3306bb35ea82d271c66075ef64367ecbb10e`  
		Last Modified: Thu, 25 Jul 2024 20:18:00 GMT  
		Size: 24.6 KB (24602 bytes)  
		MIME: application/vnd.in-toto+json
