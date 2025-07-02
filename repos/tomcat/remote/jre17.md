## `tomcat:jre17`

```console
$ docker pull tomcat@sha256:95c37b7c3962f9660e856bdbb95cdf810f888068efed7b7623ff9026a90bd98a
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

### `tomcat:jre17` - linux; amd64

```console
$ docker pull tomcat@sha256:74e10031c6e34973823b83962f7de8d363e3a3504047ff1301925af9fa272a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107931638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638f60273fb2f6816027706e9bf6f2f8d7526e887c3376ef34eab12275b94737`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Jun 2025 08:03:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 08:03:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_MAJOR=11
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_VERSION=11.0.8
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_SHA512=82a7a2e686da1fbafdd76c863d0bd1435bcd7e58d507ad353c43e364522eb3284d2dc3552388a5ca389e48afed863885886572edc13ba40ff0a13e339fca251f
# Mon, 09 Jun 2025 08:03:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Jun 2025 08:03:35 GMT
ENTRYPOINT []
# Mon, 09 Jun 2025 08:03:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581a991e8c51d03f64a485816990ee75102d04d913b17e674d8be968acdd235e`  
		Last Modified: Wed, 02 Jul 2025 03:10:16 GMT  
		Size: 17.0 MB (16969556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536501ff28ab077f36e7e2c74363b808b164edadef3ff3e502e1cfb66ce4f5df`  
		Last Modified: Wed, 02 Jul 2025 03:10:18 GMT  
		Size: 47.0 MB (46958453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e7e0c10bb5cead1e2f11045b8ec7c638b60a6772ace5b44751e90ba197cefc`  
		Last Modified: Wed, 02 Jul 2025 03:10:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc3ac322a39aaf1330c5a33929c23fde13800e4bd4b0a5676618db9eb460b3f`  
		Last Modified: Wed, 02 Jul 2025 03:10:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b18f8c1a2bd5c427d0e3f53cd2e037d768ff6d82a688a84c78152e54b26d9`  
		Last Modified: Wed, 02 Jul 2025 05:12:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d187914f954ada11600a6eeb733eadc3569d5b4094899972b638368ff5d28b6`  
		Last Modified: Wed, 02 Jul 2025 05:12:21 GMT  
		Size: 14.1 MB (14058015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7329073ff5610f28f98598da91119cdb5bd532370a41120b5a333129f4cb0c34`  
		Last Modified: Wed, 02 Jul 2025 05:12:19 GMT  
		Size: 224.6 KB (224603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:1caeedea07426cb7d83bc50e42c666c91632be644140f81d67cfb55aa8880063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe7536a7d29a868dc050acf22548efdb9ed3e9472ab76ccbedfcebc110894d5`

```dockerfile
```

-	Layers:
	-	`sha256:a002e6c386fd32f96b0de12363ce5ac29bf3384e82e643733065aca2eb5357f0`  
		Last Modified: Wed, 02 Jul 2025 08:33:23 GMT  
		Size: 3.3 MB (3349512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ed624e055d2e0ab5214dd5641e0ec19c127fca784cf98bf7a4529fff89306f0`  
		Last Modified: Wed, 02 Jul 2025 08:33:24 GMT  
		Size: 24.1 KB (24075 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:04e0d81e34a950f64e9e33647e5c482ad7c5e55f90d909d7b110aaec657c1194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102010362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35c5c34441cb22e8752868d6bc1ec63cef06c93df09a08031176fbd8aaf7f45`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:88b7ca184cec1707b10b6b543ddfa7abfcacc2605cdd5919877294ff5290aa3e in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Jun 2025 08:03:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 08:03:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_MAJOR=11
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_VERSION=11.0.8
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_SHA512=82a7a2e686da1fbafdd76c863d0bd1435bcd7e58d507ad353c43e364522eb3284d2dc3552388a5ca389e48afed863885886572edc13ba40ff0a13e339fca251f
# Mon, 09 Jun 2025 08:03:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Jun 2025 08:03:35 GMT
ENTRYPOINT []
# Mon, 09 Jun 2025 08:03:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:149362fdfa6e6a5d9f009b896da3be3172c395ba2287b57d4969f3f46e573055`  
		Last Modified: Fri, 20 Jun 2025 10:02:42 GMT  
		Size: 26.8 MB (26844462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87008fd131e34e3e3f4ffd352cf8db54b0e89603b6dc942d3c4f194b46bdfc32`  
		Last Modified: Wed, 02 Jul 2025 10:26:30 GMT  
		Size: 16.3 MB (16304975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea95a2b504993fbb5490ed6c22bd36389f7d39a04051a8563a03d95749466eb`  
		Last Modified: Wed, 02 Jul 2025 10:33:22 GMT  
		Size: 44.6 MB (44627701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c032501c322f08c300f065e7695386c009d16cbac547b42e66194ac6bf1a215`  
		Last Modified: Wed, 02 Jul 2025 10:33:19 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c24f659c97c51b71a1c06678d99d61a5646c47758bc5f31ad0f96872667085`  
		Last Modified: Wed, 02 Jul 2025 10:33:19 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fe4bbda6d3e6d643003f52d7f1b5e1a4df6d33db24c4aa509fa91343015d8e`  
		Last Modified: Wed, 02 Jul 2025 12:28:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3982fd2343efb16dbd312d9674150f6d885475c3b11d72cb3b5153a78577d3b`  
		Last Modified: Wed, 02 Jul 2025 12:28:42 GMT  
		Size: 14.0 MB (14034397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173cb24d9d24f29500068a6d717d3de64933ddd1589f9d6f3f6dab11170259b2`  
		Last Modified: Wed, 02 Jul 2025 12:28:38 GMT  
		Size: 196.2 KB (196185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:c75f314d43eceb979686211054e9e483ed6afdcbe9c7c117d8f4ca0968655bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f6d50aeabecd43f520c7ef4320ab50d6cf3c08fdbfcca19d83e055b6476d36`

```dockerfile
```

-	Layers:
	-	`sha256:22479b26711159125f6e9b8b66f859f52c1e4073b2402566d5c2b455b5db7843`  
		Last Modified: Wed, 02 Jul 2025 14:32:32 GMT  
		Size: 3.4 MB (3351916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21a0d270364b696ed4325717c5d0d754e6c80afa120bf1a2937e64504db8eaaf`  
		Last Modified: Wed, 02 Jul 2025 14:32:33 GMT  
		Size: 24.3 KB (24263 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2056080ff0e1afff76d880029ac8fff0d911578235aca40fc62d751fb202abf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106605153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949f764b8166d682d72283bfc7657d7f64ed1a474e960dc26f4bd62916872095`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Jun 2025 08:03:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 08:03:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_MAJOR=11
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_VERSION=11.0.8
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_SHA512=82a7a2e686da1fbafdd76c863d0bd1435bcd7e58d507ad353c43e364522eb3284d2dc3552388a5ca389e48afed863885886572edc13ba40ff0a13e339fca251f
# Mon, 09 Jun 2025 08:03:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Jun 2025 08:03:35 GMT
ENTRYPOINT []
# Mon, 09 Jun 2025 08:03:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb5cdde15082c2c264c46bd2f1aa0a8ad43d7590dd7374853ce1748ae4259a4`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 17.0 MB (16988306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cf1c06f50de6ec97f12f6099906a5c09940adce66d3f85fa8964651550fac9`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 46.5 MB (46474392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3790f5e56d3199420b90752ae9fadccdd125189d2a723774568fcf8eef87c768`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01de15c36901dba78b0f48401a6a9259b9f51b7b9cd784ea65342e6033b6d45e`  
		Last Modified: Tue, 03 Jun 2025 13:30:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2616310a8dce00df43ca1776615c3daf4333d4566c044ef017b19804c401285a`  
		Last Modified: Tue, 03 Jun 2025 14:06:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a348390da81cd9bc51c107ba0a6b37988b772c6bcd37a44f76ead8fce8a4d1f`  
		Last Modified: Mon, 09 Jun 2025 23:21:06 GMT  
		Size: 14.1 MB (14062672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ce07a632eafd9a8faa4fe18199715d40be32c02a9911eb7482244c3d1dea42`  
		Last Modified: Mon, 09 Jun 2025 23:21:05 GMT  
		Size: 225.2 KB (225241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:aefddb6a3babf0dc69f0ae903451a10d529acfc6be7eee88c53a6c057e9907f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a8fc1b46976a2799df92f8613d4c1da1ed1d1e734f2cd8f896b8b0149d3bea`

```dockerfile
```

-	Layers:
	-	`sha256:84f6726b8caec2dc6e075664a35e490ebcfa98be69a8b5781681f61e53f03d1e`  
		Last Modified: Tue, 10 Jun 2025 02:30:10 GMT  
		Size: 3.4 MB (3350080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e163fad99624f1b2903991619398c4b8da133e28d643660c9d838ddce896c7d9`  
		Last Modified: Tue, 10 Jun 2025 02:30:11 GMT  
		Size: 24.3 KB (24330 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; ppc64le

```console
$ docker pull tomcat@sha256:99deb90582e948e02045f8841f68b67238117a0bbce8e6325f85dbaadc566d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114246711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cd93b7ddf42ec70bb7b7a8f7e317236700b623b6687f4ef85e3f135f9292a4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Jun 2025 08:03:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 08:03:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_MAJOR=11
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_VERSION=11.0.8
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_SHA512=82a7a2e686da1fbafdd76c863d0bd1435bcd7e58d507ad353c43e364522eb3284d2dc3552388a5ca389e48afed863885886572edc13ba40ff0a13e339fca251f
# Mon, 09 Jun 2025 08:03:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Jun 2025 08:03:35 GMT
ENTRYPOINT []
# Mon, 09 Jun 2025 08:03:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2357cdb0b572402f44522ed5512cbdd3414537099dc31df3241d54f1a1546d`  
		Last Modified: Tue, 03 Jun 2025 14:27:57 GMT  
		Size: 18.8 MB (18817014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5bd2201e944c801ef56c4c9802868d78e0374b4dc80ae4088271452b6681c8`  
		Last Modified: Tue, 03 Jun 2025 14:30:08 GMT  
		Size: 46.8 MB (46770313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f10dfc3c9223f697db93dd5c74547105a43784822fb2559eecfe5650308153`  
		Last Modified: Tue, 03 Jun 2025 14:29:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12d94570a381d42261c0a613b2006ee1fb323bd86d408aa4edfc27a7a7b5ffd`  
		Last Modified: Tue, 03 Jun 2025 14:29:57 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d74ef753db9d47f32bf6c49d1550126367e0f7f5223e590cb555fc8005daba`  
		Last Modified: Wed, 04 Jun 2025 01:05:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b188ceef2d965a517e15960af0274e43cac2bc6bfc8b9ac3aa6c0e276295c9d8`  
		Last Modified: Mon, 09 Jun 2025 23:11:10 GMT  
		Size: 14.1 MB (14075142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0467fad80dcbbbf6ed70a28aa7bfd56f8dd5c47fb7c3ad5adcfb5799576936`  
		Last Modified: Mon, 09 Jun 2025 23:11:09 GMT  
		Size: 256.4 KB (256390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:24eeed5ea2f4c517cbcc510b1ab492c7775bef12f882da011aa3bcc05a017d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18640f6a262c7d5b5a0b59cffca7377f5c8b22ff7600779bc73807662ea4face`

```dockerfile
```

-	Layers:
	-	`sha256:66da5c10d9df575adb3dded50595a7c66587a0f98ffb6b481a20e510d15e44f0`  
		Last Modified: Tue, 10 Jun 2025 02:30:15 GMT  
		Size: 3.4 MB (3353637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a504e3357736085c37a4477145a618914470a69a26e88c57920000024697a39`  
		Last Modified: Tue, 10 Jun 2025 02:30:16 GMT  
		Size: 24.2 KB (24180 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; riscv64

```console
$ docker pull tomcat@sha256:1ed6ecf7ecf908b07e48bd95f418d9c66dd8550bc0d8a3929f2a7199cfaa0fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107220391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc966cf6898af568ce6d1523163e5bee0a21c8afb5ea4227f0a6bce8463cff6b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:202c5a7a84e813495c089800398f2ba18952221717db2c10e042ce4179ee6fc0 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Jun 2025 08:03:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 08:03:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_MAJOR=11
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_VERSION=11.0.8
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_SHA512=82a7a2e686da1fbafdd76c863d0bd1435bcd7e58d507ad353c43e364522eb3284d2dc3552388a5ca389e48afed863885886572edc13ba40ff0a13e339fca251f
# Mon, 09 Jun 2025 08:03:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Jun 2025 08:03:35 GMT
ENTRYPOINT []
# Mon, 09 Jun 2025 08:03:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4ccdff8fdb11e14b8e0dab6804aeebce5855635c68b20f199dcf0efcd9b4c462`  
		Last Modified: Wed, 02 Jul 2025 01:17:14 GMT  
		Size: 31.0 MB (30951024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b112a889acb1550129c19c10a637af9d1912567df5d0ca30859202a60544b8`  
		Last Modified: Wed, 02 Jul 2025 03:35:12 GMT  
		Size: 17.9 MB (17863019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3e3a154d91cdf2ee8cf43400acf17758ba59b939289d59adb82905428f3001`  
		Last Modified: Wed, 02 Jul 2025 03:35:13 GMT  
		Size: 43.9 MB (43931373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f802f14f85b371449d2594a51a06873460822c8ab5e3b2a6c4338fdcbdef3d`  
		Last Modified: Wed, 02 Jul 2025 03:35:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffe2789d3c3a636b9931c2f89476a685aa837cbfa52d2eea9dfe2f16d3553a`  
		Last Modified: Wed, 02 Jul 2025 03:35:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d9c28d7e29421e85ce34006c701be9073613f318dc695d8634ccee29d85cd9`  
		Last Modified: Wed, 02 Jul 2025 11:22:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4a009e65198aab905b6f50047dc2ab1574a038a97f58edcd45038333b0f711`  
		Last Modified: Wed, 02 Jul 2025 11:22:28 GMT  
		Size: 14.2 MB (14244452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fbbfd11dd4670e12c709450eee29a66837ab311c05e7f5a00996cf918a4040`  
		Last Modified: Wed, 02 Jul 2025 11:22:25 GMT  
		Size: 227.9 KB (227878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:494e9cc38d4de867501c5398fc886917cf69556ca51b6b810d111f0a9ab9d0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3365820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7896eb8d6d8371f6f606113d9865cbe46e8da02cd29ac539fd9d3888a6e69a0`

```dockerfile
```

-	Layers:
	-	`sha256:f1a56e49b17e50f99ee2f8dd04023d802b7c6fcef307a722aeebacf34eaf0f3f`  
		Last Modified: Wed, 02 Jul 2025 14:32:44 GMT  
		Size: 3.3 MB (3341639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45123ca9f29ea6c545f930e3a65b1b84a30352a4a74c3e77d0e7a859c1b97161`  
		Last Modified: Wed, 02 Jul 2025 14:32:45 GMT  
		Size: 24.2 KB (24181 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; s390x

```console
$ docker pull tomcat@sha256:e4f23fadd7d93c20b9cfa31fe68d2af40b1c835a0ac790a9e574cf7d52d37c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105772834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bd5296b72811f2ea97db68afb3ebf529f0e85a5fcd76ae70f726da5b07c865`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='392d179be0f9fde0b74aeb1f308be8324c2aa8c970a5c5ea456993fcbb7aa798';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Jun 2025 08:03:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 08:03:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_MAJOR=11
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_VERSION=11.0.8
# Mon, 09 Jun 2025 08:03:35 GMT
ENV TOMCAT_SHA512=82a7a2e686da1fbafdd76c863d0bd1435bcd7e58d507ad353c43e364522eb3284d2dc3552388a5ca389e48afed863885886572edc13ba40ff0a13e339fca251f
# Mon, 09 Jun 2025 08:03:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 09 Jun 2025 08:03:35 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Jun 2025 08:03:35 GMT
ENTRYPOINT []
# Mon, 09 Jun 2025 08:03:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376d0f4302e30b01c4235de8a3d72897ca97f7a056bf7655f826977caaf40fa8`  
		Last Modified: Wed, 02 Jul 2025 04:17:12 GMT  
		Size: 17.6 MB (17582256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06961d922aec9238e114636afa9ad7e2d4609fdf1939a1718fe4d26fc99224`  
		Last Modified: Wed, 02 Jul 2025 04:21:24 GMT  
		Size: 44.0 MB (43961160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc58c82551316fbad214defa165b7c68c4e3c3061ee2fdd1654b0f6b22538cc`  
		Last Modified: Wed, 02 Jul 2025 04:21:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317f8fa98acb09b8d5a9dc3bf95cccf9c3d0f5b92303de9044b0d7bf7083e7a0`  
		Last Modified: Wed, 02 Jul 2025 04:21:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b4752a766d01c1c0dfe1a41eff8649b054a3c5aa68f120e037f913986579b9`  
		Last Modified: Wed, 02 Jul 2025 07:21:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b5b382d59bcb630f1aa0dbb89b6e57324c191174297dd896ca10ba8bd9dca`  
		Last Modified: Wed, 02 Jul 2025 07:21:03 GMT  
		Size: 14.1 MB (14068627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25422af04cdbfe37999960a6551420a99c57b2e7c490bc6ba3746585d9494b26`  
		Last Modified: Wed, 02 Jul 2025 07:21:04 GMT  
		Size: 232.5 KB (232515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:e99ae31c2f94602091dd13bb19227adafc20c49bea8ba79f731cc9e052213d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3375785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c05e6f0836a5f853e743863c7fc54ca76680e8b6580dfffed85fe4148c74b76`

```dockerfile
```

-	Layers:
	-	`sha256:528d51d131ead140885b21b51de800eb8fa2c4c5249e6ea64b635096e6e6a787`  
		Last Modified: Wed, 02 Jul 2025 08:33:45 GMT  
		Size: 3.4 MB (3351711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5b7e474ec42213758e54207e9c45ae668c6ef8426a6af880a3c4c5d0f74e35`  
		Last Modified: Wed, 02 Jul 2025 08:33:46 GMT  
		Size: 24.1 KB (24074 bytes)  
		MIME: application/vnd.in-toto+json
