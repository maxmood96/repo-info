## `ibmjava:8-sdk-alpine`

```console
$ docker pull ibmjava@sha256:0fefb063330e81d20356ef52afeaa07aba64bbad383cf84eeb93d12ac911599b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:fa6a1e35a5f90f5810b85a0fed77b7ad300d0800232a9be52e5bf854aa40f8cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174868204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83370a97033a93b706ccc7ef9614747d18233ad3ac25a09d0c8db018f062a20`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:52:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Apr 2021 22:52:22 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 14 Apr 2021 22:52:39 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 19 May 2021 19:24:09 GMT
ENV JAVA_VERSION=1.8.0_sr6fp30
# Wed, 19 May 2021 19:28:45 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='afd31dea9c65fdfef664ac93140115f7c0746445bbe24fc7c62891236d28689d';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='763acaa61abc4e58b6c910b909b4d7ca2459ca1d4cc17d15cab328db94bf4ae7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d5dfe0aebd5f6bf09797aad1962f7feb3950546ac6e67174cd66447d00daf576';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='b5faf5cf5d5cfeb0dbb390059a56f4e5da3a902604d3f821104879f18c78ffb6';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='663c68478b7888b3455838c4fcd4cc9d1e09c8b55ec5dd1eb7eba786df9cee46';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 19 May 2021 19:28:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2473651455a528e12a77a3f77634a9edcf271c6673a5d553738621ea93c7f661`  
		Last Modified: Wed, 14 Apr 2021 22:54:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a476c88f89042a64d394f56be791c17d185be12546f3f0be1966502a0643c`  
		Last Modified: Wed, 14 Apr 2021 22:55:01 GMT  
		Size: 5.5 MB (5539744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cf7ef807ba2797ceee0e0fc82fd6cc3af1d5250f230b7bbc6adf6e00686b92`  
		Last Modified: Wed, 19 May 2021 19:31:26 GMT  
		Size: 166.5 MB (166527354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
