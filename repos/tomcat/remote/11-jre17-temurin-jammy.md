## `tomcat:11-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:4027b78c69d7c49d2f5326b341757549ea79d87a9e58cdfe169f48663096c455
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

### `tomcat:11-jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:0cf5ee052541f4a3a3379c451abffa1a4a037019c9c861cc6dd60f06ae4a6c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106718429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a074f6a3569d5bd6308cc062ff95b0b9fa90f041364608f367e15659f7d6bd5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_VERSION=11.0.6
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_SHA512=ecff1b6a3128cb8dd8169237176eef6e3554c3bf694c50e70065abe71bc209fc2431097b859c84b626d87212d6b62fa3e1e9a3e1d1447b62aa657e62461c2260
# Wed, 09 Apr 2025 14:03:29 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 14:03:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97781601768cddddc35e23ddf38633ea2e4a0a4ae0a8f59f11856fffbd8a3bad`  
		Last Modified: Wed, 23 Apr 2025 16:31:54 GMT  
		Size: 16.1 MB (16146029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa68485484727aa6d5321f078fb21840fd2a8bdd598f4f8a3e1672a95317733e`  
		Last Modified: Wed, 23 Apr 2025 16:31:56 GMT  
		Size: 47.0 MB (46958421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85f04a42eb69d25f9b02e9a1c46559467f5274b45bb338cd0809534deef05e`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0137fea4bef4dc4ff919d973a8ae36f29edacba15f7b5129ebe177983d665fe0`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68152ff5e4c683e4da8e9e517b136d95aeb50de5df3e553d4a4a2445862cb86`  
		Last Modified: Wed, 23 Apr 2025 18:46:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166fb88b5e232216faf128a97babcd8809dbd6bb443f57bf928abfe84580f259`  
		Last Modified: Wed, 23 Apr 2025 18:46:10 GMT  
		Size: 13.8 MB (13849309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172599f47d9a5340a44be24d05a490771ccb65bbfa13d9aca9b4a36b1ceecd25`  
		Last Modified: Wed, 23 Apr 2025 18:46:10 GMT  
		Size: 229.7 KB (229662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:e8ae2f35159f927f4b335afb7d360657b635104b8bf0d2891d1ae7976c62dacd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3791325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5442d17ca5b18602b5d9a9eae1bd87f7e267bd40acce2847a0944969e89a2c1`

```dockerfile
```

-	Layers:
	-	`sha256:3315d3ade3622ed23b97a4dd4f8305cb55d063e0a051615f4bf63bdaa1c6b5fb`  
		Last Modified: Wed, 23 Apr 2025 18:46:10 GMT  
		Size: 3.8 MB (3769742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2e158a1e914e2d6ce737314ca39aac185cce2cbf606b5519f3192268b3431e7`  
		Last Modified: Wed, 23 Apr 2025 18:46:09 GMT  
		Size: 21.6 KB (21583 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:cc5a43ee07f8972da434a238980897fcaa22bebd63b8a3a94bac8631bf5932b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101185168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affc03542ece369a3950403c72eebe9d6c508226c6835df1ab3905806d63394a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:22 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:25 GMT
ADD file:b27bdc0157c0d964026ea411ed5874766d804b491dfc3d5ac10188c76746bbb0 in / 
# Mon, 07 Apr 2025 07:27:25 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_VERSION=11.0.6
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_SHA512=ecff1b6a3128cb8dd8169237176eef6e3554c3bf694c50e70065abe71bc209fc2431097b859c84b626d87212d6b62fa3e1e9a3e1d1447b62aa657e62461c2260
# Wed, 09 Apr 2025 14:03:29 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 14:03:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f3e10eb95482b14d0f5a969fafb71afd541d5efd38890d551e27c957ed3ae84e`  
		Last Modified: Mon, 07 Apr 2025 08:26:39 GMT  
		Size: 26.6 MB (26640334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c38f06e215a1fbf49c830181d7341b1b395e52f4245dca30239c9be2d76548`  
		Last Modified: Wed, 09 Apr 2025 11:39:21 GMT  
		Size: 15.9 MB (15890794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedef9d8601d037c6607d99a42f0074fb33d5936766b4cba4384087acf9c9f7a`  
		Last Modified: Wed, 23 Apr 2025 17:10:21 GMT  
		Size: 44.6 MB (44627656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ffd34696417d30d06adaad92a0a6345ea000af5359ebb6c389b065973ad49d`  
		Last Modified: Wed, 23 Apr 2025 17:10:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bb9098917e0dac7fe23336870a868df7315d8879450e70ccd49f0f6bf0ea9f`  
		Last Modified: Wed, 23 Apr 2025 17:10:19 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbb960bc31f5f73eb1d2a95433a50bfff05eef7e12d249fab77d6cca6ef321d`  
		Last Modified: Wed, 23 Apr 2025 18:58:31 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f434bd99964cc8df013efbc441699cf9d0c5932eb058aee0642d8a82ab03d8b`  
		Last Modified: Wed, 23 Apr 2025 18:58:40 GMT  
		Size: 13.8 MB (13821408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0f21c589bb3198aaf119185fe0ecde9691306b5cf846e34382c0763173f6ad`  
		Last Modified: Wed, 23 Apr 2025 18:58:32 GMT  
		Size: 202.3 KB (202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7a7734796c81779be0145156f54d6e7d0522a2de56e4390f35ebb2f115b238a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3793792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5018dfb7d7999830582e7efde01d780ab97bc81e3dd18ad3d7b6f42ef72e24f6`

```dockerfile
```

-	Layers:
	-	`sha256:18b3d0308f224c490771439e05ed5f7d25f553ad91c522b8ac45ccbc0f64fb37`  
		Last Modified: Wed, 23 Apr 2025 18:58:32 GMT  
		Size: 3.8 MB (3772085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b135e82a8eceac834cf5d4d4cfb0b218f5eed84fb2f8e5fbcd714ad77f51af1c`  
		Last Modified: Wed, 23 Apr 2025 18:58:31 GMT  
		Size: 21.7 KB (21707 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:ff2e24e09e2af062854a8837fe51505a7e3ee6af6fe1cd61c5cbc08b83c8589c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (103969835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceece073264cbbbfc6ba5fe6fdee914f51ee78a57825dc4ef2c5d85e5fc594c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_VERSION=11.0.6
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_SHA512=ecff1b6a3128cb8dd8169237176eef6e3554c3bf694c50e70065abe71bc209fc2431097b859c84b626d87212d6b62fa3e1e9a3e1d1447b62aa657e62461c2260
# Wed, 09 Apr 2025 14:03:29 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 14:03:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d988c284109adb0ee08f6d6a95a152f6e364456e1a4853bb6c3ebc58c40f099`  
		Last Modified: Wed, 09 Apr 2025 06:58:01 GMT  
		Size: 16.1 MB (16059566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac488a8321ea959588c227573cf8a20259cc8fde212361febce0a1b0c814dbef`  
		Last Modified: Wed, 23 Apr 2025 16:38:17 GMT  
		Size: 46.5 MB (46474324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1af5cf872e078be1505c0565767eed13113730ec78326847e626469b0b8c663`  
		Last Modified: Wed, 23 Apr 2025 16:38:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88f83d0cfd9bd69d840192dccb1b340da7121b21b5d2c5d41ad894714765f2`  
		Last Modified: Wed, 23 Apr 2025 16:38:15 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8ef5d9284fd4e2672e000ba17570b4ec951ce9a0034ac2b26fb41a33437e2a`  
		Last Modified: Wed, 23 Apr 2025 20:40:23 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6bccf47bc48816b0cdd8bb028e9194a47fa58a56be55397ee4ba12744e803d`  
		Last Modified: Wed, 23 Apr 2025 20:40:24 GMT  
		Size: 13.9 MB (13850427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e61d4c8162158731ed99ed7ca807cc63e4337ad4f6573432814e859900140c`  
		Last Modified: Wed, 23 Apr 2025 20:40:24 GMT  
		Size: 228.6 KB (228643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c2287ca902d1410a6bae29523c6952255c35bd0d68c23afd44f7119cc3691e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3791166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cee7c6c743b9805e190753d9a72938ccb5b91dc2663a9f1f6c011999ac1335e`

```dockerfile
```

-	Layers:
	-	`sha256:5919251482df9ee3e4310863d35fd69ce4921b2996f2c36f579f725b0aefbee1`  
		Last Modified: Wed, 23 Apr 2025 20:40:24 GMT  
		Size: 3.8 MB (3769423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b521be0d7b47cb1cb6466a2068580b8084bba3008cb184d0eb66bad791085514`  
		Last Modified: Wed, 23 Apr 2025 20:40:23 GMT  
		Size: 21.7 KB (21743 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:7abef439d56b7a07da3aba6f28a67dd9d3ad070ab9d04ae6f6ff41dde9f82f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112955786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b4c38352f733d0464d9bee431876bdd2edc5fcf3d6d79a7401e1cd313e4146`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_VERSION=11.0.6
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_SHA512=ecff1b6a3128cb8dd8169237176eef6e3554c3bf694c50e70065abe71bc209fc2431097b859c84b626d87212d6b62fa3e1e9a3e1d1447b62aa657e62461c2260
# Wed, 09 Apr 2025 14:03:29 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 14:03:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c38ec2b4ee36ca93f19596eb065a396e648e65a58e52db4e0886be5ded596`  
		Last Modified: Wed, 09 Apr 2025 04:35:13 GMT  
		Size: 17.6 MB (17617815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3400d5f2e38520c6487762c909ae0af92dd3ef636453c243c27e5b531e5aef`  
		Last Modified: Wed, 23 Apr 2025 16:46:41 GMT  
		Size: 46.8 MB (46769848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69913fe4465cbe95c02bbc2b0d2b5e177748b9b473e31e65f9b26da73727e4e`  
		Last Modified: Wed, 23 Apr 2025 16:46:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d3c21455a5d9e113244f43286c051f57e04caff2e5fc4b16462b0d8e7b4783`  
		Last Modified: Wed, 23 Apr 2025 16:46:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921901be0a708da48730276005ba30540b27c8b39938b5b70c9b146eb7dca693`  
		Last Modified: Wed, 23 Apr 2025 18:36:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858b20b37300a0a6b5e65c1ab0adad28989d9f51c681c50e290f845e35c8ac21`  
		Last Modified: Wed, 23 Apr 2025 18:36:11 GMT  
		Size: 13.9 MB (13863750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5071d2ea841cfda3ebc12a99433ad911f4c4f21699c98473eff896d2e4a931b0`  
		Last Modified: Wed, 23 Apr 2025 18:36:11 GMT  
		Size: 259.0 KB (259033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:12601492e9f4c482a8f2659e9eeebcfd34b4a9e621c7ca116b12bcad174a0499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51672aa9147c491a24c195535a05749d68ff876c168e3f9f66cb96222f3e863b`

```dockerfile
```

-	Layers:
	-	`sha256:b188b20fa4710ae17dfcfd27a7bd7634b34c1573df1252a7bb5b1acf61cf9980`  
		Last Modified: Wed, 23 Apr 2025 18:36:11 GMT  
		Size: 3.8 MB (3773684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3299542539dff6274722cfe3fe7467e848d0a6fa5356999417b0b4a37d2ad03a`  
		Last Modified: Wed, 23 Apr 2025 18:36:10 GMT  
		Size: 21.6 KB (21641 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:b2b21b8626009f298efbb47b2953a1376daaa46fe4d8cb1258396dcdbb9017ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102189582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b279ab10287d13c7b184dbd82a8d4ca902688ccbd6a994e919325d78bc878fe`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:00 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:00 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:02 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Mon, 07 Apr 2025 07:25:02 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 14:03:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 14:03:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_MAJOR=11
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_VERSION=11.0.6
# Wed, 09 Apr 2025 14:03:29 GMT
ENV TOMCAT_SHA512=ecff1b6a3128cb8dd8169237176eef6e3554c3bf694c50e70065abe71bc209fc2431097b859c84b626d87212d6b62fa3e1e9a3e1d1447b62aa657e62461c2260
# Wed, 09 Apr 2025 14:03:29 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 14:03:29 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 14:03:29 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 14:03:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ffac1a60b6cb80417a2deaa826c5568b388878415c01490d46c373b76b9af`  
		Last Modified: Wed, 09 Apr 2025 04:16:19 GMT  
		Size: 16.1 MB (16143553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519af0c38240cf5ea7eabd190f4bb907c7286d25ddf361b362469def9b4cf05`  
		Last Modified: Wed, 23 Apr 2025 16:41:17 GMT  
		Size: 44.0 MB (43960934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c191115a908862638fb921185212d5a25c45f899ea7ebf5d5d7de623e202bf`  
		Last Modified: Wed, 23 Apr 2025 16:41:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c9d1ab01c219fdc662993dc0f57d42d26989e7e8a709570b2e15dee5128f40`  
		Last Modified: Wed, 23 Apr 2025 16:41:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1915922f8d725dadd5c52f6fbba78ee2ea7057dceaa5fbc8759a5390612db074`  
		Last Modified: Wed, 23 Apr 2025 18:12:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9384d1527a9e19c8ee6a4c4fa13107232f51a6859ac4edd4e7604029a491c567`  
		Last Modified: Wed, 23 Apr 2025 18:12:30 GMT  
		Size: 13.9 MB (13851488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0a8463164abacf116ba49209fa419a502b3a72865fb1ad53567350f5a2f5c1`  
		Last Modified: Wed, 23 Apr 2025 18:12:30 GMT  
		Size: 230.8 KB (230846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:156ee3a6e0a954fdafcbc956f1b19acde1d3c2857ebc9f280d8efebbfe9814de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0b3ea2237a043cee4258e6e2ec5bd0551ec5faa144cdbef5df7ba163dffc6a`

```dockerfile
```

-	Layers:
	-	`sha256:8d8422461113bb1f60ba75abf9ed71298e64653b6451b6291b991d8b8740ea17`  
		Last Modified: Wed, 23 Apr 2025 18:12:30 GMT  
		Size: 3.8 MB (3771333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01254c73186e28dfad7cae5e88b9f21e54f55542a1531112f64bd0cedcd74052`  
		Last Modified: Wed, 23 Apr 2025 18:12:30 GMT  
		Size: 21.6 KB (21583 bytes)  
		MIME: application/vnd.in-toto+json
