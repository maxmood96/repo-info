<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sonarqube`

-	[`sonarqube:8-community`](#sonarqube8-community)
-	[`sonarqube:8-datacenter-app`](#sonarqube8-datacenter-app)
-	[`sonarqube:8-datacenter-search`](#sonarqube8-datacenter-search)
-	[`sonarqube:8-developer`](#sonarqube8-developer)
-	[`sonarqube:8-enterprise`](#sonarqube8-enterprise)
-	[`sonarqube:8.9-community`](#sonarqube89-community)
-	[`sonarqube:8.9-datacenter-app`](#sonarqube89-datacenter-app)
-	[`sonarqube:8.9-datacenter-search`](#sonarqube89-datacenter-search)
-	[`sonarqube:8.9-developer`](#sonarqube89-developer)
-	[`sonarqube:8.9-enterprise`](#sonarqube89-enterprise)
-	[`sonarqube:8.9.7-community`](#sonarqube897-community)
-	[`sonarqube:8.9.7-datacenter-app`](#sonarqube897-datacenter-app)
-	[`sonarqube:8.9.7-datacenter-search`](#sonarqube897-datacenter-search)
-	[`sonarqube:8.9.7-developer`](#sonarqube897-developer)
-	[`sonarqube:8.9.7-enterprise`](#sonarqube897-enterprise)
-	[`sonarqube:9-community`](#sonarqube9-community)
-	[`sonarqube:9-datacenter-app`](#sonarqube9-datacenter-app)
-	[`sonarqube:9-datacenter-search`](#sonarqube9-datacenter-search)
-	[`sonarqube:9-developer`](#sonarqube9-developer)
-	[`sonarqube:9-enterprise`](#sonarqube9-enterprise)
-	[`sonarqube:9.3-community`](#sonarqube93-community)
-	[`sonarqube:9.3-datacenter-app`](#sonarqube93-datacenter-app)
-	[`sonarqube:9.3-datacenter-search`](#sonarqube93-datacenter-search)
-	[`sonarqube:9.3-developer`](#sonarqube93-developer)
-	[`sonarqube:9.3-enterprise`](#sonarqube93-enterprise)
-	[`sonarqube:9.3.0-community`](#sonarqube930-community)
-	[`sonarqube:9.3.0-datacenter-app`](#sonarqube930-datacenter-app)
-	[`sonarqube:9.3.0-datacenter-search`](#sonarqube930-datacenter-search)
-	[`sonarqube:9.3.0-developer`](#sonarqube930-developer)
-	[`sonarqube:9.3.0-enterprise`](#sonarqube930-enterprise)
-	[`sonarqube:community`](#sonarqubecommunity)
-	[`sonarqube:datacenter-app`](#sonarqubedatacenter-app)
-	[`sonarqube:datacenter-search`](#sonarqubedatacenter-search)
-	[`sonarqube:developer`](#sonarqubedeveloper)
-	[`sonarqube:enterprise`](#sonarqubeenterprise)
-	[`sonarqube:latest`](#sonarqubelatest)
-	[`sonarqube:lts`](#sonarqubelts)
-	[`sonarqube:lts-community`](#sonarqubelts-community)
-	[`sonarqube:lts-datacenter-app`](#sonarqubelts-datacenter-app)
-	[`sonarqube:lts-datacenter-search`](#sonarqubelts-datacenter-search)
-	[`sonarqube:lts-developer`](#sonarqubelts-developer)
-	[`sonarqube:lts-enterprise`](#sonarqubelts-enterprise)

## `sonarqube:8-community`

```console
$ docker pull sonarqube@sha256:3b653b6c7a11805e819ea94fe67e4b95c0b50f766f5be548ebd90bdb43fff6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:75f244b4fca55312c79f6190c676f457b3052a9ebcb6d5f53142478a5e1f8829
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326566683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b46b9cb56d7d754da60b33a32985dd218761b9d2a2e2f134b0a7903b9f3288`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:59:17 GMT
ENV JAVA_VERSION=jdk-11.0.11+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 06:59:31 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:33:44 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:33:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:35:05 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:35:06 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:35:06 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:35:06 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:35:06 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:35:07 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702f1610d53e7ccac3c312b37154fd9d24972469f1fe80980ccdd158be2eff4c`  
		Last Modified: Sat, 13 Nov 2021 07:11:54 GMT  
		Size: 7.3 MB (7337383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a52b7bec47bba029903a17677539117787bbc1e52c9788913c140a3cf53b6b`  
		Last Modified: Sat, 05 Feb 2022 05:43:04 GMT  
		Size: 43.3 MB (43332570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83892a2ffd2fbb3fffe6486e4b32eac88408953d43759fd25196795f00cd6321`  
		Last Modified: Sat, 05 Feb 2022 05:43:13 GMT  
		Size: 273.1 MB (273086161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324dfcdb2edc78b818038905e78e02f683944f0dde69c9d9cf034ada9ad776e7`  
		Last Modified: Sat, 05 Feb 2022 05:42:56 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8-datacenter-app`

```console
$ docker pull sonarqube@sha256:95c920adc6048f0a3c39ae926bfebec6f23f12efafcb127872e83cabdb4907b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:0df5bc96d81a64e053702ff43d778b292b07fd7de286efeb55a600234687f746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430103034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e44258f8e8552089834f57e4d5bed7e5df5f8a5c94cf8d0d04c5d7159a5c7af`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:35:20 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:35:20 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:38:45 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:38:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Sat, 05 Feb 2022 05:40:08 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:40:10 GMT
COPY --chown=sonarqube:sonarqubemulti:51df763f101eec590ff619b8aadba3476acd9a155be2557d6807f6fb4f272767 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:40:10 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:40:10 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:40:10 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:40:11 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e944524ce66b3a996779185c982fc8fc26cf1e2bba7e50aa52ba34a02ff37d`  
		Last Modified: Sat, 05 Feb 2022 05:43:38 GMT  
		Size: 43.3 MB (43332592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6a0050f758351b88edf3dfd28c7250d9581e7a4e7175aafc841f97d3bc411`  
		Last Modified: Sat, 05 Feb 2022 05:44:58 GMT  
		Size: 376.6 MB (376622180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02daa2d3b89080d04ebf3ba4e6f02c1c8f7cbf3fc93078932cede362110146bf`  
		Last Modified: Sat, 05 Feb 2022 05:44:37 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8-datacenter-search`

```console
$ docker pull sonarqube@sha256:a83aa5b28d429488a9f3c292ba988f1df28d646469dc8c2f52c0275b5b4ff629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:88dd3aa166afacbbd431c665b98e209ebff6a37b351035d04d9706ddef30f40b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430066979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8cfe589de9b6574fecbb417d568d2f06e77b9d034bf2575ca0b96730f74259`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 13 Nov 2021 07:00:57 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fde6b29df23b6e7ed6e16a237a0f44273fb9e267fdfbd0b3de5add98e55649f6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='ad02656f800fd64c2b090b23ad24a099d9cd1054948ecb0e9851bc39c51c8be8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='37c19c7c2d1cea627b854a475ef1a765d30357d765d20cf3f96590037e79d0f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='f18101fc50aad795a41b4d3bbc591308c83664fd2390bf2bc007fd9b3d531e6c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='144f2c6bcf64faa32016f2474b6c01031be75d25325e9c3097aed6589bc5d548';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:40:23 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:40:24 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:40:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Sat, 05 Feb 2022 05:41:56 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:41:58 GMT
COPY --chown=sonarqube:sonarqubemulti:270da8217279c47ae0242cde83fc983aadec2b66d86bcd0a13541b65a67704f9 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:41:58 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:41:58 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:41:58 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:41:59 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea77b4c123efcbecd260c09cdbb31ed4472aa7acda483242be90971dfaba071`  
		Last Modified: Sat, 13 Nov 2021 07:12:36 GMT  
		Size: 43.3 MB (43298710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5e6028425298498b730a7bc34ef1855f1465d303a5795228db88656d802e83`  
		Last Modified: Sat, 05 Feb 2022 05:45:34 GMT  
		Size: 376.6 MB (376619993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71408ab8bf1a663d5c11a31998a653f2ad27b1e36295444df595322c0e6dfbdb`  
		Last Modified: Sat, 05 Feb 2022 05:45:14 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8-developer`

```console
$ docker pull sonarqube@sha256:c5ff7e0da147ef57bb183a7a34249d0ca2e19a4ba49dcacfde7c7500711b8b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:3eb5a76a633cc03d23ee545fd22e4cc97f5de12c9e1ef1dec41283fdfc82ebc7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (386977347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469256af35d1e318889b06dfceadf6cf3fbce6d091c9d1ce743830c9a75056e9`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:35:20 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:35:20 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:35:21 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:36:53 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:36:54 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:36:54 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:36:54 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:36:54 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:36:55 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e944524ce66b3a996779185c982fc8fc26cf1e2bba7e50aa52ba34a02ff37d`  
		Last Modified: Sat, 05 Feb 2022 05:43:38 GMT  
		Size: 43.3 MB (43332592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904043ebf436bc6ea337ba77470c3f0d322fc0c530006625ddd94d2d59c20237`  
		Last Modified: Sat, 05 Feb 2022 05:43:51 GMT  
		Size: 333.5 MB (333496789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7d30131a7bc857a0ccdc4127d21c45eb9336403b67f20cdf4e86e7111c1275`  
		Last Modified: Sat, 05 Feb 2022 05:43:31 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8-enterprise`

```console
$ docker pull sonarqube@sha256:371c7e7fff5b0b9f11b922671eec0237cd69b71a61837533e190e960a17e91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:61299a79cef33f70c585210270b0ec162bba9f18fc0ff19967ae0e644cc90aee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407657025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4783e9efc1b94bca726d1a1e042f3bb56bb606d90be6980a1b9dd15f12d910`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:37:12 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)           echo "Unsupported arch: ${ARCH}";           exit 1;           ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:37:12 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:37:13 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:37:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:38:34 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:38:35 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:38:35 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:38:35 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:38:36 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:38:36 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb49a30ab388d1b5f1e3511529cfe7e7190688c64fe929730cab7ff68fbf1f32`  
		Last Modified: Sat, 05 Feb 2022 05:44:12 GMT  
		Size: 43.3 MB (43332613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45b85ae5f563b9b4a8ac71ffb96c41bc3de75e9653b14c0e8fd9814befecd86`  
		Last Modified: Sat, 05 Feb 2022 05:44:23 GMT  
		Size: 354.2 MB (354176449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b187c11e1fccf0af942c5fbfb1ce762a1c7cb61e4d9c4b368343a8e9a07c5e4`  
		Last Modified: Sat, 05 Feb 2022 05:44:05 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9-community`

```console
$ docker pull sonarqube@sha256:3b653b6c7a11805e819ea94fe67e4b95c0b50f766f5be548ebd90bdb43fff6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:75f244b4fca55312c79f6190c676f457b3052a9ebcb6d5f53142478a5e1f8829
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326566683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b46b9cb56d7d754da60b33a32985dd218761b9d2a2e2f134b0a7903b9f3288`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:59:17 GMT
ENV JAVA_VERSION=jdk-11.0.11+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 06:59:31 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:33:44 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:33:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:35:05 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:35:06 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:35:06 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:35:06 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:35:06 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:35:07 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702f1610d53e7ccac3c312b37154fd9d24972469f1fe80980ccdd158be2eff4c`  
		Last Modified: Sat, 13 Nov 2021 07:11:54 GMT  
		Size: 7.3 MB (7337383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a52b7bec47bba029903a17677539117787bbc1e52c9788913c140a3cf53b6b`  
		Last Modified: Sat, 05 Feb 2022 05:43:04 GMT  
		Size: 43.3 MB (43332570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83892a2ffd2fbb3fffe6486e4b32eac88408953d43759fd25196795f00cd6321`  
		Last Modified: Sat, 05 Feb 2022 05:43:13 GMT  
		Size: 273.1 MB (273086161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324dfcdb2edc78b818038905e78e02f683944f0dde69c9d9cf034ada9ad776e7`  
		Last Modified: Sat, 05 Feb 2022 05:42:56 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9-datacenter-app`

```console
$ docker pull sonarqube@sha256:95c920adc6048f0a3c39ae926bfebec6f23f12efafcb127872e83cabdb4907b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:0df5bc96d81a64e053702ff43d778b292b07fd7de286efeb55a600234687f746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430103034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e44258f8e8552089834f57e4d5bed7e5df5f8a5c94cf8d0d04c5d7159a5c7af`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:35:20 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:35:20 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:38:45 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:38:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Sat, 05 Feb 2022 05:40:08 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:40:10 GMT
COPY --chown=sonarqube:sonarqubemulti:51df763f101eec590ff619b8aadba3476acd9a155be2557d6807f6fb4f272767 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:40:10 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:40:10 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:40:10 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:40:11 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e944524ce66b3a996779185c982fc8fc26cf1e2bba7e50aa52ba34a02ff37d`  
		Last Modified: Sat, 05 Feb 2022 05:43:38 GMT  
		Size: 43.3 MB (43332592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6a0050f758351b88edf3dfd28c7250d9581e7a4e7175aafc841f97d3bc411`  
		Last Modified: Sat, 05 Feb 2022 05:44:58 GMT  
		Size: 376.6 MB (376622180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02daa2d3b89080d04ebf3ba4e6f02c1c8f7cbf3fc93078932cede362110146bf`  
		Last Modified: Sat, 05 Feb 2022 05:44:37 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9-datacenter-search`

```console
$ docker pull sonarqube@sha256:a83aa5b28d429488a9f3c292ba988f1df28d646469dc8c2f52c0275b5b4ff629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:88dd3aa166afacbbd431c665b98e209ebff6a37b351035d04d9706ddef30f40b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430066979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8cfe589de9b6574fecbb417d568d2f06e77b9d034bf2575ca0b96730f74259`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 13 Nov 2021 07:00:57 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fde6b29df23b6e7ed6e16a237a0f44273fb9e267fdfbd0b3de5add98e55649f6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='ad02656f800fd64c2b090b23ad24a099d9cd1054948ecb0e9851bc39c51c8be8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='37c19c7c2d1cea627b854a475ef1a765d30357d765d20cf3f96590037e79d0f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='f18101fc50aad795a41b4d3bbc591308c83664fd2390bf2bc007fd9b3d531e6c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='144f2c6bcf64faa32016f2474b6c01031be75d25325e9c3097aed6589bc5d548';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:40:23 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:40:24 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:40:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Sat, 05 Feb 2022 05:41:56 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:41:58 GMT
COPY --chown=sonarqube:sonarqubemulti:270da8217279c47ae0242cde83fc983aadec2b66d86bcd0a13541b65a67704f9 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:41:58 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:41:58 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:41:58 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:41:59 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea77b4c123efcbecd260c09cdbb31ed4472aa7acda483242be90971dfaba071`  
		Last Modified: Sat, 13 Nov 2021 07:12:36 GMT  
		Size: 43.3 MB (43298710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5e6028425298498b730a7bc34ef1855f1465d303a5795228db88656d802e83`  
		Last Modified: Sat, 05 Feb 2022 05:45:34 GMT  
		Size: 376.6 MB (376619993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71408ab8bf1a663d5c11a31998a653f2ad27b1e36295444df595322c0e6dfbdb`  
		Last Modified: Sat, 05 Feb 2022 05:45:14 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9-developer`

```console
$ docker pull sonarqube@sha256:c5ff7e0da147ef57bb183a7a34249d0ca2e19a4ba49dcacfde7c7500711b8b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:3eb5a76a633cc03d23ee545fd22e4cc97f5de12c9e1ef1dec41283fdfc82ebc7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (386977347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469256af35d1e318889b06dfceadf6cf3fbce6d091c9d1ce743830c9a75056e9`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:35:20 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:35:20 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:35:21 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:36:53 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:36:54 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:36:54 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:36:54 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:36:54 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:36:55 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e944524ce66b3a996779185c982fc8fc26cf1e2bba7e50aa52ba34a02ff37d`  
		Last Modified: Sat, 05 Feb 2022 05:43:38 GMT  
		Size: 43.3 MB (43332592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904043ebf436bc6ea337ba77470c3f0d322fc0c530006625ddd94d2d59c20237`  
		Last Modified: Sat, 05 Feb 2022 05:43:51 GMT  
		Size: 333.5 MB (333496789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7d30131a7bc857a0ccdc4127d21c45eb9336403b67f20cdf4e86e7111c1275`  
		Last Modified: Sat, 05 Feb 2022 05:43:31 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9-enterprise`

```console
$ docker pull sonarqube@sha256:371c7e7fff5b0b9f11b922671eec0237cd69b71a61837533e190e960a17e91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:61299a79cef33f70c585210270b0ec162bba9f18fc0ff19967ae0e644cc90aee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407657025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4783e9efc1b94bca726d1a1e042f3bb56bb606d90be6980a1b9dd15f12d910`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:37:12 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)           echo "Unsupported arch: ${ARCH}";           exit 1;           ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:37:12 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:37:13 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:37:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:38:34 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:38:35 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:38:35 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:38:35 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:38:36 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:38:36 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb49a30ab388d1b5f1e3511529cfe7e7190688c64fe929730cab7ff68fbf1f32`  
		Last Modified: Sat, 05 Feb 2022 05:44:12 GMT  
		Size: 43.3 MB (43332613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45b85ae5f563b9b4a8ac71ffb96c41bc3de75e9653b14c0e8fd9814befecd86`  
		Last Modified: Sat, 05 Feb 2022 05:44:23 GMT  
		Size: 354.2 MB (354176449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b187c11e1fccf0af942c5fbfb1ce762a1c7cb61e4d9c4b368343a8e9a07c5e4`  
		Last Modified: Sat, 05 Feb 2022 05:44:05 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9.7-community`

```console
$ docker pull sonarqube@sha256:3b653b6c7a11805e819ea94fe67e4b95c0b50f766f5be548ebd90bdb43fff6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9.7-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:75f244b4fca55312c79f6190c676f457b3052a9ebcb6d5f53142478a5e1f8829
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326566683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b46b9cb56d7d754da60b33a32985dd218761b9d2a2e2f134b0a7903b9f3288`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:59:17 GMT
ENV JAVA_VERSION=jdk-11.0.11+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 06:59:31 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:33:44 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:33:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:35:05 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:35:06 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:35:06 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:35:06 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:35:06 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:35:07 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702f1610d53e7ccac3c312b37154fd9d24972469f1fe80980ccdd158be2eff4c`  
		Last Modified: Sat, 13 Nov 2021 07:11:54 GMT  
		Size: 7.3 MB (7337383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a52b7bec47bba029903a17677539117787bbc1e52c9788913c140a3cf53b6b`  
		Last Modified: Sat, 05 Feb 2022 05:43:04 GMT  
		Size: 43.3 MB (43332570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83892a2ffd2fbb3fffe6486e4b32eac88408953d43759fd25196795f00cd6321`  
		Last Modified: Sat, 05 Feb 2022 05:43:13 GMT  
		Size: 273.1 MB (273086161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324dfcdb2edc78b818038905e78e02f683944f0dde69c9d9cf034ada9ad776e7`  
		Last Modified: Sat, 05 Feb 2022 05:42:56 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9.7-datacenter-app`

```console
$ docker pull sonarqube@sha256:95c920adc6048f0a3c39ae926bfebec6f23f12efafcb127872e83cabdb4907b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9.7-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:0df5bc96d81a64e053702ff43d778b292b07fd7de286efeb55a600234687f746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430103034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e44258f8e8552089834f57e4d5bed7e5df5f8a5c94cf8d0d04c5d7159a5c7af`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:35:20 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:35:20 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:38:45 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:38:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Sat, 05 Feb 2022 05:40:08 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:40:10 GMT
COPY --chown=sonarqube:sonarqubemulti:51df763f101eec590ff619b8aadba3476acd9a155be2557d6807f6fb4f272767 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:40:10 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:40:10 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:40:10 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:40:11 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e944524ce66b3a996779185c982fc8fc26cf1e2bba7e50aa52ba34a02ff37d`  
		Last Modified: Sat, 05 Feb 2022 05:43:38 GMT  
		Size: 43.3 MB (43332592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6a0050f758351b88edf3dfd28c7250d9581e7a4e7175aafc841f97d3bc411`  
		Last Modified: Sat, 05 Feb 2022 05:44:58 GMT  
		Size: 376.6 MB (376622180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02daa2d3b89080d04ebf3ba4e6f02c1c8f7cbf3fc93078932cede362110146bf`  
		Last Modified: Sat, 05 Feb 2022 05:44:37 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9.7-datacenter-search`

```console
$ docker pull sonarqube@sha256:a83aa5b28d429488a9f3c292ba988f1df28d646469dc8c2f52c0275b5b4ff629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9.7-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:88dd3aa166afacbbd431c665b98e209ebff6a37b351035d04d9706ddef30f40b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430066979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8cfe589de9b6574fecbb417d568d2f06e77b9d034bf2575ca0b96730f74259`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 13 Nov 2021 07:00:57 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fde6b29df23b6e7ed6e16a237a0f44273fb9e267fdfbd0b3de5add98e55649f6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='ad02656f800fd64c2b090b23ad24a099d9cd1054948ecb0e9851bc39c51c8be8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='37c19c7c2d1cea627b854a475ef1a765d30357d765d20cf3f96590037e79d0f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='f18101fc50aad795a41b4d3bbc591308c83664fd2390bf2bc007fd9b3d531e6c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='144f2c6bcf64faa32016f2474b6c01031be75d25325e9c3097aed6589bc5d548';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:40:23 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:40:24 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:40:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Sat, 05 Feb 2022 05:41:56 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:41:58 GMT
COPY --chown=sonarqube:sonarqubemulti:270da8217279c47ae0242cde83fc983aadec2b66d86bcd0a13541b65a67704f9 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:41:58 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:41:58 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:41:58 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:41:59 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea77b4c123efcbecd260c09cdbb31ed4472aa7acda483242be90971dfaba071`  
		Last Modified: Sat, 13 Nov 2021 07:12:36 GMT  
		Size: 43.3 MB (43298710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5e6028425298498b730a7bc34ef1855f1465d303a5795228db88656d802e83`  
		Last Modified: Sat, 05 Feb 2022 05:45:34 GMT  
		Size: 376.6 MB (376619993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71408ab8bf1a663d5c11a31998a653f2ad27b1e36295444df595322c0e6dfbdb`  
		Last Modified: Sat, 05 Feb 2022 05:45:14 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9.7-developer`

```console
$ docker pull sonarqube@sha256:c5ff7e0da147ef57bb183a7a34249d0ca2e19a4ba49dcacfde7c7500711b8b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9.7-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:3eb5a76a633cc03d23ee545fd22e4cc97f5de12c9e1ef1dec41283fdfc82ebc7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (386977347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469256af35d1e318889b06dfceadf6cf3fbce6d091c9d1ce743830c9a75056e9`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:35:20 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:35:20 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:35:21 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:36:53 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:36:54 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:36:54 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:36:54 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:36:54 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:36:55 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e944524ce66b3a996779185c982fc8fc26cf1e2bba7e50aa52ba34a02ff37d`  
		Last Modified: Sat, 05 Feb 2022 05:43:38 GMT  
		Size: 43.3 MB (43332592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904043ebf436bc6ea337ba77470c3f0d322fc0c530006625ddd94d2d59c20237`  
		Last Modified: Sat, 05 Feb 2022 05:43:51 GMT  
		Size: 333.5 MB (333496789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7d30131a7bc857a0ccdc4127d21c45eb9336403b67f20cdf4e86e7111c1275`  
		Last Modified: Sat, 05 Feb 2022 05:43:31 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.9.7-enterprise`

```console
$ docker pull sonarqube@sha256:371c7e7fff5b0b9f11b922671eec0237cd69b71a61837533e190e960a17e91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:8.9.7-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:61299a79cef33f70c585210270b0ec162bba9f18fc0ff19967ae0e644cc90aee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407657025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4783e9efc1b94bca726d1a1e042f3bb56bb606d90be6980a1b9dd15f12d910`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:37:12 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)           echo "Unsupported arch: ${ARCH}";           exit 1;           ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:37:12 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:37:13 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:37:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:38:34 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:38:35 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:38:35 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:38:35 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:38:36 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:38:36 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb49a30ab388d1b5f1e3511529cfe7e7190688c64fe929730cab7ff68fbf1f32`  
		Last Modified: Sat, 05 Feb 2022 05:44:12 GMT  
		Size: 43.3 MB (43332613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45b85ae5f563b9b4a8ac71ffb96c41bc3de75e9653b14c0e8fd9814befecd86`  
		Last Modified: Sat, 05 Feb 2022 05:44:23 GMT  
		Size: 354.2 MB (354176449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b187c11e1fccf0af942c5fbfb1ce762a1c7cb61e4d9c4b368343a8e9a07c5e4`  
		Last Modified: Sat, 05 Feb 2022 05:44:05 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9-community`

```console
$ docker pull sonarqube@sha256:ac3a1965cabafb8728a14ac572bb0803b5badb2940bcc289f8fa4b697cd0d6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:cc91389eea1b3ace2a4751da5a25c9a241c04c40946c815990cbb74d044ecba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (354038097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4842c584e2d7f4ab5a773a4611490c31b3e94fdc8243bf40636fcf6d1fac6`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:21:41 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:21:42 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:21:43 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:21:43 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:21:43 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:21:43 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:21:43 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57709a8c10d43501a5d92978446ba2160f6c994e94301ad39e24c7e0d9185ba9`  
		Last Modified: Fri, 28 Jan 2022 19:29:42 GMT  
		Size: 351.2 MB (351214002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4b951c4c9e08749189c27d301e626134e2e2af89236dce0d2393d5ab4bd637`  
		Last Modified: Fri, 28 Jan 2022 19:29:21 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9-datacenter-app`

```console
$ docker pull sonarqube@sha256:7fb95cf4ba5730a1b45711a77f2b2c9eaae40b9749f6bfb184c940e733c3384b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:6b5ff2fe884cadb28e461c7051d52dedaa97bef3a48db3384778b827b82966cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.4 MB (481426729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f790c818a306cc9ba40d2cdc4b93a180bdbba05716e53239b467dc0a576cdb93`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:25:14 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:25:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Fri, 28 Jan 2022 19:26:51 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:26:53 GMT
COPY --chown=sonarqube:sonarqubemulti:b3583528dc7e1c8c3d5b50dfbb55820aeec61ed9bbc812d0d58f5c5875189ea8 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:26:53 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:26:54 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:26:54 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:26:54 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:26:54 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f19a906a0d754238480d36f07f385d421354fbfbb442110d4fb832195673904`  
		Last Modified: Fri, 28 Jan 2022 19:31:51 GMT  
		Size: 478.6 MB (478602231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba348a73dc21af1ca6ed8021c0fd552897b1ffc6fa78d454f8b83df9474461`  
		Last Modified: Fri, 28 Jan 2022 19:31:25 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9-datacenter-search`

```console
$ docker pull sonarqube@sha256:05bec06bf3cf533f0efb49179557f7560ed9947cce453693ec17ea92b0c1c1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:ac67f834f0de037a0782ef8c54f35b8a8879474d245af03c4c8ee66c080e9959
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.4 MB (481426694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483e9877c4848f5bb423a10fe1d24f3fd3b919cfebc01d986868c7b54cee54e1`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:25:14 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:27:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Fri, 28 Jan 2022 19:28:42 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:28:44 GMT
COPY --chown=sonarqube:sonarqubemulti:8997cda09b77db3cd2004e36d485c5b54ddd96e9993642921bc6be78ee8af554 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:28:44 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:28:44 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:28:44 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:28:45 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:28:45 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ebe47c8a14630f9f7d8fdb91c0d144c07a81a9e811afe59ea2ba1acda62d7`  
		Last Modified: Fri, 28 Jan 2022 19:32:32 GMT  
		Size: 478.6 MB (478602202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913f41ff247bd9ae8951711aedfc4c83eef4ffcd4e3f854c68e59242eb8cd985`  
		Last Modified: Fri, 28 Jan 2022 19:32:07 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9-developer`

```console
$ docker pull sonarqube@sha256:97abe6db4218bf8ac60a1007e77e8061e2232fb18ed6cce163004365d5d9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:7b13b6b9f1059e80ec996a17b4ea57355798f6f5c7459bb7d6e570d9e1147b99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435354743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5749cee89926682680c73370629bb19b649f068093ef9efd449bc07e4e0a2424`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:21:58 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:21:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:23:30 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:23:32 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:23:32 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:23:33 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:23:33 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:23:33 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:23:33 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12bec25131fb03e5d686f6d855cb107159a7d8944c3f5becf990f77623b7f59`  
		Last Modified: Fri, 28 Jan 2022 19:30:24 GMT  
		Size: 432.5 MB (432530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8117ae5d1d9ff7f4e94ec7ce99a3e564f733ba15aa3ac84beaca8d640e3e658`  
		Last Modified: Fri, 28 Jan 2022 19:30:00 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9-enterprise`

```console
$ docker pull sonarqube@sha256:dc01fa40b2d4d739d5deef71b0556812c21c4bb6e180007eb06d26cf4200a3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:2a0a64a62e8cf4309cb995ad32d28d0c30a1285cb6537e0fcce945c4772276f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.0 MB (458985598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bda9f1462050743f45a5e6151d19509c221f2b9b51b61887e81cfc9c1ee03ce`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:23:36 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:23:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:25:08 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:25:09 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:25:10 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:25:10 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:25:10 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:25:10 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:25:10 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2ac75d8a548e978f75df9d9c24372cceded712b5a71d043a53d8b74bbaa995`  
		Last Modified: Fri, 28 Jan 2022 19:31:05 GMT  
		Size: 456.2 MB (456161506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd70f4f5615f2026f5843b90d6bd528df1648158a6279f4f1ad8dde9dbf2e03d`  
		Last Modified: Fri, 28 Jan 2022 19:30:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3-community`

```console
$ docker pull sonarqube@sha256:ac3a1965cabafb8728a14ac572bb0803b5badb2940bcc289f8fa4b697cd0d6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:cc91389eea1b3ace2a4751da5a25c9a241c04c40946c815990cbb74d044ecba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (354038097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4842c584e2d7f4ab5a773a4611490c31b3e94fdc8243bf40636fcf6d1fac6`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:21:41 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:21:42 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:21:43 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:21:43 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:21:43 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:21:43 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:21:43 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57709a8c10d43501a5d92978446ba2160f6c994e94301ad39e24c7e0d9185ba9`  
		Last Modified: Fri, 28 Jan 2022 19:29:42 GMT  
		Size: 351.2 MB (351214002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4b951c4c9e08749189c27d301e626134e2e2af89236dce0d2393d5ab4bd637`  
		Last Modified: Fri, 28 Jan 2022 19:29:21 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3-datacenter-app`

```console
$ docker pull sonarqube@sha256:7fb95cf4ba5730a1b45711a77f2b2c9eaae40b9749f6bfb184c940e733c3384b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:6b5ff2fe884cadb28e461c7051d52dedaa97bef3a48db3384778b827b82966cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.4 MB (481426729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f790c818a306cc9ba40d2cdc4b93a180bdbba05716e53239b467dc0a576cdb93`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:25:14 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:25:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Fri, 28 Jan 2022 19:26:51 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:26:53 GMT
COPY --chown=sonarqube:sonarqubemulti:b3583528dc7e1c8c3d5b50dfbb55820aeec61ed9bbc812d0d58f5c5875189ea8 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:26:53 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:26:54 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:26:54 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:26:54 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:26:54 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f19a906a0d754238480d36f07f385d421354fbfbb442110d4fb832195673904`  
		Last Modified: Fri, 28 Jan 2022 19:31:51 GMT  
		Size: 478.6 MB (478602231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba348a73dc21af1ca6ed8021c0fd552897b1ffc6fa78d454f8b83df9474461`  
		Last Modified: Fri, 28 Jan 2022 19:31:25 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3-datacenter-search`

```console
$ docker pull sonarqube@sha256:05bec06bf3cf533f0efb49179557f7560ed9947cce453693ec17ea92b0c1c1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:ac67f834f0de037a0782ef8c54f35b8a8879474d245af03c4c8ee66c080e9959
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.4 MB (481426694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483e9877c4848f5bb423a10fe1d24f3fd3b919cfebc01d986868c7b54cee54e1`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:25:14 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:27:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Fri, 28 Jan 2022 19:28:42 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:28:44 GMT
COPY --chown=sonarqube:sonarqubemulti:8997cda09b77db3cd2004e36d485c5b54ddd96e9993642921bc6be78ee8af554 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:28:44 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:28:44 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:28:44 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:28:45 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:28:45 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ebe47c8a14630f9f7d8fdb91c0d144c07a81a9e811afe59ea2ba1acda62d7`  
		Last Modified: Fri, 28 Jan 2022 19:32:32 GMT  
		Size: 478.6 MB (478602202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913f41ff247bd9ae8951711aedfc4c83eef4ffcd4e3f854c68e59242eb8cd985`  
		Last Modified: Fri, 28 Jan 2022 19:32:07 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3-developer`

```console
$ docker pull sonarqube@sha256:97abe6db4218bf8ac60a1007e77e8061e2232fb18ed6cce163004365d5d9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:7b13b6b9f1059e80ec996a17b4ea57355798f6f5c7459bb7d6e570d9e1147b99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435354743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5749cee89926682680c73370629bb19b649f068093ef9efd449bc07e4e0a2424`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:21:58 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:21:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:23:30 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:23:32 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:23:32 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:23:33 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:23:33 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:23:33 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:23:33 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12bec25131fb03e5d686f6d855cb107159a7d8944c3f5becf990f77623b7f59`  
		Last Modified: Fri, 28 Jan 2022 19:30:24 GMT  
		Size: 432.5 MB (432530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8117ae5d1d9ff7f4e94ec7ce99a3e564f733ba15aa3ac84beaca8d640e3e658`  
		Last Modified: Fri, 28 Jan 2022 19:30:00 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3-enterprise`

```console
$ docker pull sonarqube@sha256:dc01fa40b2d4d739d5deef71b0556812c21c4bb6e180007eb06d26cf4200a3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:2a0a64a62e8cf4309cb995ad32d28d0c30a1285cb6537e0fcce945c4772276f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.0 MB (458985598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bda9f1462050743f45a5e6151d19509c221f2b9b51b61887e81cfc9c1ee03ce`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:23:36 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:23:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:25:08 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:25:09 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:25:10 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:25:10 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:25:10 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:25:10 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:25:10 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2ac75d8a548e978f75df9d9c24372cceded712b5a71d043a53d8b74bbaa995`  
		Last Modified: Fri, 28 Jan 2022 19:31:05 GMT  
		Size: 456.2 MB (456161506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd70f4f5615f2026f5843b90d6bd528df1648158a6279f4f1ad8dde9dbf2e03d`  
		Last Modified: Fri, 28 Jan 2022 19:30:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3.0-community`

```console
$ docker pull sonarqube@sha256:ac3a1965cabafb8728a14ac572bb0803b5badb2940bcc289f8fa4b697cd0d6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3.0-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:cc91389eea1b3ace2a4751da5a25c9a241c04c40946c815990cbb74d044ecba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (354038097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4842c584e2d7f4ab5a773a4611490c31b3e94fdc8243bf40636fcf6d1fac6`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:21:41 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:21:42 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:21:43 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:21:43 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:21:43 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:21:43 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:21:43 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57709a8c10d43501a5d92978446ba2160f6c994e94301ad39e24c7e0d9185ba9`  
		Last Modified: Fri, 28 Jan 2022 19:29:42 GMT  
		Size: 351.2 MB (351214002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4b951c4c9e08749189c27d301e626134e2e2af89236dce0d2393d5ab4bd637`  
		Last Modified: Fri, 28 Jan 2022 19:29:21 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3.0-datacenter-app`

```console
$ docker pull sonarqube@sha256:7fb95cf4ba5730a1b45711a77f2b2c9eaae40b9749f6bfb184c940e733c3384b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3.0-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:6b5ff2fe884cadb28e461c7051d52dedaa97bef3a48db3384778b827b82966cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.4 MB (481426729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f790c818a306cc9ba40d2cdc4b93a180bdbba05716e53239b467dc0a576cdb93`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:25:14 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:25:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Fri, 28 Jan 2022 19:26:51 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:26:53 GMT
COPY --chown=sonarqube:sonarqubemulti:b3583528dc7e1c8c3d5b50dfbb55820aeec61ed9bbc812d0d58f5c5875189ea8 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:26:53 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:26:54 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:26:54 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:26:54 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:26:54 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f19a906a0d754238480d36f07f385d421354fbfbb442110d4fb832195673904`  
		Last Modified: Fri, 28 Jan 2022 19:31:51 GMT  
		Size: 478.6 MB (478602231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba348a73dc21af1ca6ed8021c0fd552897b1ffc6fa78d454f8b83df9474461`  
		Last Modified: Fri, 28 Jan 2022 19:31:25 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3.0-datacenter-search`

```console
$ docker pull sonarqube@sha256:05bec06bf3cf533f0efb49179557f7560ed9947cce453693ec17ea92b0c1c1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3.0-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:ac67f834f0de037a0782ef8c54f35b8a8879474d245af03c4c8ee66c080e9959
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.4 MB (481426694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483e9877c4848f5bb423a10fe1d24f3fd3b919cfebc01d986868c7b54cee54e1`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:25:14 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:27:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Fri, 28 Jan 2022 19:28:42 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:28:44 GMT
COPY --chown=sonarqube:sonarqubemulti:8997cda09b77db3cd2004e36d485c5b54ddd96e9993642921bc6be78ee8af554 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:28:44 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:28:44 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:28:44 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:28:45 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:28:45 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ebe47c8a14630f9f7d8fdb91c0d144c07a81a9e811afe59ea2ba1acda62d7`  
		Last Modified: Fri, 28 Jan 2022 19:32:32 GMT  
		Size: 478.6 MB (478602202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913f41ff247bd9ae8951711aedfc4c83eef4ffcd4e3f854c68e59242eb8cd985`  
		Last Modified: Fri, 28 Jan 2022 19:32:07 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3.0-developer`

```console
$ docker pull sonarqube@sha256:97abe6db4218bf8ac60a1007e77e8061e2232fb18ed6cce163004365d5d9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3.0-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:7b13b6b9f1059e80ec996a17b4ea57355798f6f5c7459bb7d6e570d9e1147b99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435354743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5749cee89926682680c73370629bb19b649f068093ef9efd449bc07e4e0a2424`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:21:58 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:21:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:23:30 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:23:32 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:23:32 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:23:33 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:23:33 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:23:33 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:23:33 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12bec25131fb03e5d686f6d855cb107159a7d8944c3f5becf990f77623b7f59`  
		Last Modified: Fri, 28 Jan 2022 19:30:24 GMT  
		Size: 432.5 MB (432530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8117ae5d1d9ff7f4e94ec7ce99a3e564f733ba15aa3ac84beaca8d640e3e658`  
		Last Modified: Fri, 28 Jan 2022 19:30:00 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:9.3.0-enterprise`

```console
$ docker pull sonarqube@sha256:dc01fa40b2d4d739d5deef71b0556812c21c4bb6e180007eb06d26cf4200a3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9.3.0-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:2a0a64a62e8cf4309cb995ad32d28d0c30a1285cb6537e0fcce945c4772276f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.0 MB (458985598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bda9f1462050743f45a5e6151d19509c221f2b9b51b61887e81cfc9c1ee03ce`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:23:36 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:23:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:25:08 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:25:09 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:25:10 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:25:10 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:25:10 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:25:10 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:25:10 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2ac75d8a548e978f75df9d9c24372cceded712b5a71d043a53d8b74bbaa995`  
		Last Modified: Fri, 28 Jan 2022 19:31:05 GMT  
		Size: 456.2 MB (456161506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd70f4f5615f2026f5843b90d6bd528df1648158a6279f4f1ad8dde9dbf2e03d`  
		Last Modified: Fri, 28 Jan 2022 19:30:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:community`

```console
$ docker pull sonarqube@sha256:ac3a1965cabafb8728a14ac572bb0803b5badb2940bcc289f8fa4b697cd0d6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:community` - linux; amd64

```console
$ docker pull sonarqube@sha256:cc91389eea1b3ace2a4751da5a25c9a241c04c40946c815990cbb74d044ecba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (354038097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4842c584e2d7f4ab5a773a4611490c31b3e94fdc8243bf40636fcf6d1fac6`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:21:41 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:21:42 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:21:43 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:21:43 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:21:43 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:21:43 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:21:43 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57709a8c10d43501a5d92978446ba2160f6c994e94301ad39e24c7e0d9185ba9`  
		Last Modified: Fri, 28 Jan 2022 19:29:42 GMT  
		Size: 351.2 MB (351214002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4b951c4c9e08749189c27d301e626134e2e2af89236dce0d2393d5ab4bd637`  
		Last Modified: Fri, 28 Jan 2022 19:29:21 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:datacenter-app`

```console
$ docker pull sonarqube@sha256:7fb95cf4ba5730a1b45711a77f2b2c9eaae40b9749f6bfb184c940e733c3384b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:6b5ff2fe884cadb28e461c7051d52dedaa97bef3a48db3384778b827b82966cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.4 MB (481426729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f790c818a306cc9ba40d2cdc4b93a180bdbba05716e53239b467dc0a576cdb93`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:25:14 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:25:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Fri, 28 Jan 2022 19:26:51 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:26:53 GMT
COPY --chown=sonarqube:sonarqubemulti:b3583528dc7e1c8c3d5b50dfbb55820aeec61ed9bbc812d0d58f5c5875189ea8 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:26:53 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:26:54 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:26:54 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:26:54 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:26:54 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f19a906a0d754238480d36f07f385d421354fbfbb442110d4fb832195673904`  
		Last Modified: Fri, 28 Jan 2022 19:31:51 GMT  
		Size: 478.6 MB (478602231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba348a73dc21af1ca6ed8021c0fd552897b1ffc6fa78d454f8b83df9474461`  
		Last Modified: Fri, 28 Jan 2022 19:31:25 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:datacenter-search`

```console
$ docker pull sonarqube@sha256:05bec06bf3cf533f0efb49179557f7560ed9947cce453693ec17ea92b0c1c1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:ac67f834f0de037a0782ef8c54f35b8a8879474d245af03c4c8ee66c080e9959
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.4 MB (481426694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483e9877c4848f5bb423a10fe1d24f3fd3b919cfebc01d986868c7b54cee54e1`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:25:14 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:27:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Fri, 28 Jan 2022 19:28:42 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:28:44 GMT
COPY --chown=sonarqube:sonarqubemulti:8997cda09b77db3cd2004e36d485c5b54ddd96e9993642921bc6be78ee8af554 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:28:44 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:28:44 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:28:44 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:28:45 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:28:45 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ebe47c8a14630f9f7d8fdb91c0d144c07a81a9e811afe59ea2ba1acda62d7`  
		Last Modified: Fri, 28 Jan 2022 19:32:32 GMT  
		Size: 478.6 MB (478602202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913f41ff247bd9ae8951711aedfc4c83eef4ffcd4e3f854c68e59242eb8cd985`  
		Last Modified: Fri, 28 Jan 2022 19:32:07 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:developer`

```console
$ docker pull sonarqube@sha256:97abe6db4218bf8ac60a1007e77e8061e2232fb18ed6cce163004365d5d9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:7b13b6b9f1059e80ec996a17b4ea57355798f6f5c7459bb7d6e570d9e1147b99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435354743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5749cee89926682680c73370629bb19b649f068093ef9efd449bc07e4e0a2424`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:21:58 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:21:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:23:30 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:23:32 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:23:32 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:23:33 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:23:33 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:23:33 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:23:33 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12bec25131fb03e5d686f6d855cb107159a7d8944c3f5becf990f77623b7f59`  
		Last Modified: Fri, 28 Jan 2022 19:30:24 GMT  
		Size: 432.5 MB (432530650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8117ae5d1d9ff7f4e94ec7ce99a3e564f733ba15aa3ac84beaca8d640e3e658`  
		Last Modified: Fri, 28 Jan 2022 19:30:00 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:enterprise`

```console
$ docker pull sonarqube@sha256:dc01fa40b2d4d739d5deef71b0556812c21c4bb6e180007eb06d26cf4200a3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:2a0a64a62e8cf4309cb995ad32d28d0c30a1285cb6537e0fcce945c4772276f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.0 MB (458985598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bda9f1462050743f45a5e6151d19509c221f2b9b51b61887e81cfc9c1ee03ce`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:23:36 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:23:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:25:08 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:25:09 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:25:10 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:25:10 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:25:10 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:25:10 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:25:10 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2ac75d8a548e978f75df9d9c24372cceded712b5a71d043a53d8b74bbaa995`  
		Last Modified: Fri, 28 Jan 2022 19:31:05 GMT  
		Size: 456.2 MB (456161506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd70f4f5615f2026f5843b90d6bd528df1648158a6279f4f1ad8dde9dbf2e03d`  
		Last Modified: Fri, 28 Jan 2022 19:30:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:latest`

```console
$ docker pull sonarqube@sha256:ac3a1965cabafb8728a14ac572bb0803b5badb2940bcc289f8fa4b697cd0d6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:latest` - linux; amd64

```console
$ docker pull sonarqube@sha256:cc91389eea1b3ace2a4751da5a25c9a241c04c40946c815990cbb74d044ecba1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (354038097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4842c584e2d7f4ab5a773a4611490c31b3e94fdc8243bf40636fcf6d1fac6`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_VERSION=9.3.0.51899
# Fri, 28 Jan 2022 19:20:05 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
# Fri, 28 Jan 2022 19:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.3.0.51899 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 28 Jan 2022 19:21:41 GMT
# ARGS: SONARQUBE_VERSION=9.3.0.51899 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 28 Jan 2022 19:21:42 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 28 Jan 2022 19:21:43 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Jan 2022 19:21:43 GMT
EXPOSE 9000
# Fri, 28 Jan 2022 19:21:43 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jan 2022 19:21:43 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 28 Jan 2022 19:21:43 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57709a8c10d43501a5d92978446ba2160f6c994e94301ad39e24c7e0d9185ba9`  
		Last Modified: Fri, 28 Jan 2022 19:29:42 GMT  
		Size: 351.2 MB (351214002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4b951c4c9e08749189c27d301e626134e2e2af89236dce0d2393d5ab4bd637`  
		Last Modified: Fri, 28 Jan 2022 19:29:21 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:lts`

```console
$ docker pull sonarqube@sha256:3b653b6c7a11805e819ea94fe67e4b95c0b50f766f5be548ebd90bdb43fff6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:lts` - linux; amd64

```console
$ docker pull sonarqube@sha256:75f244b4fca55312c79f6190c676f457b3052a9ebcb6d5f53142478a5e1f8829
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326566683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b46b9cb56d7d754da60b33a32985dd218761b9d2a2e2f134b0a7903b9f3288`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:59:17 GMT
ENV JAVA_VERSION=jdk-11.0.11+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 06:59:31 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:33:44 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:33:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:35:05 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:35:06 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:35:06 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:35:06 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:35:06 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:35:07 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702f1610d53e7ccac3c312b37154fd9d24972469f1fe80980ccdd158be2eff4c`  
		Last Modified: Sat, 13 Nov 2021 07:11:54 GMT  
		Size: 7.3 MB (7337383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a52b7bec47bba029903a17677539117787bbc1e52c9788913c140a3cf53b6b`  
		Last Modified: Sat, 05 Feb 2022 05:43:04 GMT  
		Size: 43.3 MB (43332570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83892a2ffd2fbb3fffe6486e4b32eac88408953d43759fd25196795f00cd6321`  
		Last Modified: Sat, 05 Feb 2022 05:43:13 GMT  
		Size: 273.1 MB (273086161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324dfcdb2edc78b818038905e78e02f683944f0dde69c9d9cf034ada9ad776e7`  
		Last Modified: Sat, 05 Feb 2022 05:42:56 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:lts-community`

```console
$ docker pull sonarqube@sha256:3b653b6c7a11805e819ea94fe67e4b95c0b50f766f5be548ebd90bdb43fff6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:lts-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:75f244b4fca55312c79f6190c676f457b3052a9ebcb6d5f53142478a5e1f8829
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326566683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b46b9cb56d7d754da60b33a32985dd218761b9d2a2e2f134b0a7903b9f3288`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:59:17 GMT
ENV JAVA_VERSION=jdk-11.0.11+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 06:59:31 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:33:44 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:33:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:33:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:35:05 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:35:06 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:35:06 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:35:06 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:35:06 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:35:07 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702f1610d53e7ccac3c312b37154fd9d24972469f1fe80980ccdd158be2eff4c`  
		Last Modified: Sat, 13 Nov 2021 07:11:54 GMT  
		Size: 7.3 MB (7337383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a52b7bec47bba029903a17677539117787bbc1e52c9788913c140a3cf53b6b`  
		Last Modified: Sat, 05 Feb 2022 05:43:04 GMT  
		Size: 43.3 MB (43332570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83892a2ffd2fbb3fffe6486e4b32eac88408953d43759fd25196795f00cd6321`  
		Last Modified: Sat, 05 Feb 2022 05:43:13 GMT  
		Size: 273.1 MB (273086161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324dfcdb2edc78b818038905e78e02f683944f0dde69c9d9cf034ada9ad776e7`  
		Last Modified: Sat, 05 Feb 2022 05:42:56 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:lts-datacenter-app`

```console
$ docker pull sonarqube@sha256:95c920adc6048f0a3c39ae926bfebec6f23f12efafcb127872e83cabdb4907b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:lts-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:0df5bc96d81a64e053702ff43d778b292b07fd7de286efeb55a600234687f746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430103034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e44258f8e8552089834f57e4d5bed7e5df5f8a5c94cf8d0d04c5d7159a5c7af`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:35:20 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:35:20 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:38:45 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:38:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Sat, 05 Feb 2022 05:40:08 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:40:10 GMT
COPY --chown=sonarqube:sonarqubemulti:51df763f101eec590ff619b8aadba3476acd9a155be2557d6807f6fb4f272767 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:40:10 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:40:10 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:40:10 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:40:11 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e944524ce66b3a996779185c982fc8fc26cf1e2bba7e50aa52ba34a02ff37d`  
		Last Modified: Sat, 05 Feb 2022 05:43:38 GMT  
		Size: 43.3 MB (43332592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6a0050f758351b88edf3dfd28c7250d9581e7a4e7175aafc841f97d3bc411`  
		Last Modified: Sat, 05 Feb 2022 05:44:58 GMT  
		Size: 376.6 MB (376622180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02daa2d3b89080d04ebf3ba4e6f02c1c8f7cbf3fc93078932cede362110146bf`  
		Last Modified: Sat, 05 Feb 2022 05:44:37 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:lts-datacenter-search`

```console
$ docker pull sonarqube@sha256:a83aa5b28d429488a9f3c292ba988f1df28d646469dc8c2f52c0275b5b4ff629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:lts-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:88dd3aa166afacbbd431c665b98e209ebff6a37b351035d04d9706ddef30f40b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430066979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8cfe589de9b6574fecbb417d568d2f06e77b9d034bf2575ca0b96730f74259`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 13 Nov 2021 07:00:57 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fde6b29df23b6e7ed6e16a237a0f44273fb9e267fdfbd0b3de5add98e55649f6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='ad02656f800fd64c2b090b23ad24a099d9cd1054948ecb0e9851bc39c51c8be8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='37c19c7c2d1cea627b854a475ef1a765d30357d765d20cf3f96590037e79d0f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='f18101fc50aad795a41b4d3bbc591308c83664fd2390bf2bc007fd9b3d531e6c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='144f2c6bcf64faa32016f2474b6c01031be75d25325e9c3097aed6589bc5d548';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:40:23 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:40:24 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:40:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Sat, 05 Feb 2022 05:41:56 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:41:58 GMT
COPY --chown=sonarqube:sonarqubemulti:270da8217279c47ae0242cde83fc983aadec2b66d86bcd0a13541b65a67704f9 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:41:58 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:41:58 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:41:58 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:41:59 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea77b4c123efcbecd260c09cdbb31ed4472aa7acda483242be90971dfaba071`  
		Last Modified: Sat, 13 Nov 2021 07:12:36 GMT  
		Size: 43.3 MB (43298710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5e6028425298498b730a7bc34ef1855f1465d303a5795228db88656d802e83`  
		Last Modified: Sat, 05 Feb 2022 05:45:34 GMT  
		Size: 376.6 MB (376619993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71408ab8bf1a663d5c11a31998a653f2ad27b1e36295444df595322c0e6dfbdb`  
		Last Modified: Sat, 05 Feb 2022 05:45:14 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:lts-developer`

```console
$ docker pull sonarqube@sha256:c5ff7e0da147ef57bb183a7a34249d0ca2e19a4ba49dcacfde7c7500711b8b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:lts-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:3eb5a76a633cc03d23ee545fd22e4cc97f5de12c9e1ef1dec41283fdfc82ebc7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (386977347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469256af35d1e318889b06dfceadf6cf3fbce6d091c9d1ce743830c9a75056e9`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:35:20 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:35:20 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:35:21 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:36:53 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:36:54 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:36:54 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:36:54 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:36:54 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:36:55 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e944524ce66b3a996779185c982fc8fc26cf1e2bba7e50aa52ba34a02ff37d`  
		Last Modified: Sat, 05 Feb 2022 05:43:38 GMT  
		Size: 43.3 MB (43332592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904043ebf436bc6ea337ba77470c3f0d322fc0c530006625ddd94d2d59c20237`  
		Last Modified: Sat, 05 Feb 2022 05:43:51 GMT  
		Size: 333.5 MB (333496789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7d30131a7bc857a0ccdc4127d21c45eb9336403b67f20cdf4e86e7111c1275`  
		Last Modified: Sat, 05 Feb 2022 05:43:31 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:lts-enterprise`

```console
$ docker pull sonarqube@sha256:371c7e7fff5b0b9f11b922671eec0237cd69b71a61837533e190e960a17e91d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:lts-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:61299a79cef33f70c585210270b0ec162bba9f18fc0ff19967ae0e644cc90aee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407657025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4783e9efc1b94bca726d1a1e042f3bb56bb606d90be6980a1b9dd15f12d910`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:00:40 GMT
ENV JAVA_VERSION=jdk-11.0.10+9 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 13 Nov 2021 07:00:52 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.33-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.2.0-6-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="e33b45e4a10ef26259d6acf8e7b5dd6dc63800641e41eb67fa6588d061f79c1c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-4-x86_64.pkg.tar.xz";     ZLIB_SHA256=43a17987d348e0b395cb6e28d2ece65fb3b5a0fe433714762780d18c0451c149;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -Ls ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --inputfile en_US --charmap UTF-8 "$LANG" || true ;    echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c - ;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c - ;    mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Sat, 05 Feb 2022 05:37:12 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|armv7l)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|x86_64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)           echo "Unsupported arch: ${ARCH}";           exit 1;           ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 05 Feb 2022 05:37:12 GMT
ARG SONARQUBE_VERSION=8.9.7.52159
# Sat, 05 Feb 2022 05:37:13 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.9.7.52159.zip
# Sat, 05 Feb 2022 05:37:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.9.7.52159 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Sat, 05 Feb 2022 05:38:34 GMT
# ARGS: SONARQUBE_VERSION=8.9.7.52159 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.9.7.52159.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Sat, 05 Feb 2022 05:38:35 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Sat, 05 Feb 2022 05:38:35 GMT
WORKDIR /opt/sonarqube
# Sat, 05 Feb 2022 05:38:35 GMT
EXPOSE 9000
# Sat, 05 Feb 2022 05:38:36 GMT
ENTRYPOINT ["bin/run.sh"]
# Sat, 05 Feb 2022 05:38:36 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec4a9b4537fd0fd3ff303f89623d2950ec4fae5a99617894e9f4e6abc24e32`  
		Last Modified: Sat, 13 Nov 2021 07:12:30 GMT  
		Size: 7.3 MB (7337396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb49a30ab388d1b5f1e3511529cfe7e7190688c64fe929730cab7ff68fbf1f32`  
		Last Modified: Sat, 05 Feb 2022 05:44:12 GMT  
		Size: 43.3 MB (43332613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45b85ae5f563b9b4a8ac71ffb96c41bc3de75e9653b14c0e8fd9814befecd86`  
		Last Modified: Sat, 05 Feb 2022 05:44:23 GMT  
		Size: 354.2 MB (354176449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b187c11e1fccf0af942c5fbfb1ce762a1c7cb61e4d9c4b368343a8e9a07c5e4`  
		Last Modified: Sat, 05 Feb 2022 05:44:05 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
