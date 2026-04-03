## `tomcat:9-jre8-temurin-jammy`

```console
$ docker pull tomcat@sha256:cb9ee93366d5f293c9be81566a55957bcce20c5d2e61ab3f9dd209d3ae1ec6fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `tomcat:9-jre8-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:22517663e498775753cd9ef36bef98c29023d530e1e85ffe974c9d685449d9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102275651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9fe5eb8724a5dccc202cc2428b9cf9c3c421819308eb2f5599b0876d7d9307`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:09:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:09:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:09:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:09:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:09:57 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:09:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:09:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:09:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:09:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:11:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:37 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:37 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:37 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:37 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:37 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:37 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:37 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:45 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:45 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:45 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411d94d78660651982f8ea9396c29f168b475309253aa58800d66bf5d35b43c3`  
		Last Modified: Wed, 01 Apr 2026 20:10:11 GMT  
		Size: 16.1 MB (16149386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903ded3f2e7787a196c167b95e9350307d7ae11c304cb25e811211af6d122e61`  
		Last Modified: Wed, 01 Apr 2026 20:10:12 GMT  
		Size: 42.3 MB (42331727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94107fcdb07671418b9a112d2e3ef304d514331bfabb2b879ae3b0d259b3413c`  
		Last Modified: Wed, 01 Apr 2026 20:10:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60911814702725156de46c13c1365f5e1310e172a3ee3d5294c22a56e9eb50df`  
		Last Modified: Wed, 01 Apr 2026 20:10:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5462f6002162753ddb703aebfeff65198f17acd37405988398caed63e49c2c4`  
		Last Modified: Fri, 03 Apr 2026 18:11:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2999c6ab5ee429210fc071c5ca651b9a80b4f1b36625e22f00f9508c15d6f9fa`  
		Last Modified: Fri, 03 Apr 2026 18:11:54 GMT  
		Size: 13.8 MB (13825785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6987b111cfaf72aaebbd7c9193cecbd4d416d6a453e59b94b7231827d5d41e42`  
		Last Modified: Fri, 03 Apr 2026 18:11:53 GMT  
		Size: 229.7 KB (229727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6322e21da0b92c8bd433780edf9d693198a29b290b52d9e491038425171055be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131090a1bff3f8344da766cecec86f6509496a7f72ed5d697e14a5abe66e1496`

```dockerfile
```

-	Layers:
	-	`sha256:3887470d063f0256ce76b460afd4572005d5481c41bf6ea4a2974575ead65cb8`  
		Last Modified: Fri, 03 Apr 2026 18:11:53 GMT  
		Size: 4.0 MB (3968009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a078eea0cbc904312fbde721080c753ee57cb2aa0ac1eada0ced9844866633a`  
		Last Modified: Fri, 03 Apr 2026 18:11:53 GMT  
		Size: 21.2 KB (21195 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:0bfe700091a2b62a368193da14bc4a5210aa9a75f611e80f0874dceea5bf6290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96463086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef193287060cb986cc524a94d31c58c0f75117529e90b1fd1531bbd138817415`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:eaa1e345a925acc7b826effa9fb4c3dfb4aebe47807533938898d49afe7561cb in / 
# Sun, 22 Mar 2026 18:14:12 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:08:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:08:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:08:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:08:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:08:29 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:08:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:08:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:08:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:08:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:13:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:13:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:13:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:13:50 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:13:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:13:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:13:50 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:13:50 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:13:50 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:13:50 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:13:56 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:13:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:13:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:13:56 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:13:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e7c88f36edd2a67246005d083413bd656459d3b63bab8e6a05a1018c7658daae`  
		Last Modified: Sun, 22 Mar 2026 18:43:39 GMT  
		Size: 26.8 MB (26842286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88633c2d7cc2d76a9d37cfd237103b2a3adfab73bfcf26bc834697fb03606a2c`  
		Last Modified: Wed, 01 Apr 2026 20:08:52 GMT  
		Size: 15.9 MB (15890056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046a13da3ebce1756213113acdc7d17dc6b78a2b9868b52c0adf5f4f843535b`  
		Last Modified: Wed, 01 Apr 2026 20:08:52 GMT  
		Size: 39.8 MB (39768551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003b56c550a2199fc0871f67f0dc9e6a81b6ac6bb727f7bc3742e1d9f7a53a13`  
		Last Modified: Wed, 01 Apr 2026 20:08:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abaf50509bd5bd543f12f674a14758f9c3b3f6aece558256d07ecb0e4ad1e9e`  
		Last Modified: Wed, 01 Apr 2026 20:08:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2fc8bc12eba9102fbd1886939b63a794628172899b1a5ccdc76c16678f0b01`  
		Last Modified: Fri, 03 Apr 2026 18:14:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ddad4397219edcc5f098daf3390d3acbb7b16494877b163764855ca81c2f47`  
		Last Modified: Fri, 03 Apr 2026 18:14:06 GMT  
		Size: 13.8 MB (13756906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab23b8bf0033480909cd2dfd4f097515c00b7ac37ad5fe0c59f46a35b047786`  
		Last Modified: Fri, 03 Apr 2026 18:14:05 GMT  
		Size: 202.7 KB (202674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:39a2d885443f49b0ecabee48f852092aada62aeb08924e724673adbc38d35280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2361044ae81f5b0eb73e0164c129944b4ed372e2806d2c88bb0a90ed0384f40c`

```dockerfile
```

-	Layers:
	-	`sha256:fc3d90a9a4dc00fd00c5151e01eec18c0fbbfb1b9e1834d7ac8b25181184dbeb`  
		Last Modified: Fri, 03 Apr 2026 18:14:05 GMT  
		Size: 4.0 MB (3974027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff29304be43841233eb13d69e9b53ca140fb07495a3e6b40aa8d8f55729720f`  
		Last Modified: Fri, 03 Apr 2026 18:14:05 GMT  
		Size: 21.3 KB (21314 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:c66887c14b49ff4bb72fdbd369cf2a346cb66af54aa9d42360096748137f30a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99035240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb06213fa50d6489cdff2f01ec8c27e286039e0e58aaf48fcd07dcb577ed37`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:15 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:10:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:10:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:11:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:25 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:25 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:25 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:25 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:25 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:34 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e9014f5eb87367d3448681e52c7e826b56cc01711c064f54350ab40885507d`  
		Last Modified: Wed, 01 Apr 2026 20:10:31 GMT  
		Size: 16.1 MB (16073495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840913b96d7ce295d1bd76661ce2b7ad31103d72df68fef5f9e359062dbe423b`  
		Last Modified: Wed, 01 Apr 2026 20:10:31 GMT  
		Size: 41.3 MB (41289519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64a78bc2c872bea616c1ee331e63a747bc4bacc5b6fcc58a6671489f3e61eed`  
		Last Modified: Wed, 01 Apr 2026 20:10:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507fa1c7ebbfaf51a003a36e8bf76f07909e5dcb4eb69c2f8b8036e7b63d13aa`  
		Last Modified: Wed, 01 Apr 2026 20:10:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d37b8b3b775d128306d810bef1b341d1851cd5344fa6450a7cb0a01701d065`  
		Last Modified: Fri, 03 Apr 2026 18:11:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56f5c2d7d9b593108d282c42e46e91266fa1a85ca017c1bc582bc44f6f76a68`  
		Last Modified: Fri, 03 Apr 2026 18:11:43 GMT  
		Size: 13.8 MB (13833950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ed865fc9ee099c7ea159bf92a8e2a83567d76eb0e19d045091d51c9d5d5469`  
		Last Modified: Fri, 03 Apr 2026 18:11:43 GMT  
		Size: 228.7 KB (228721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ebb5150b9f236eed847b9fc886608c049a6e90a3c6b6a29dbafda099f734f274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec61c18581c5477250cc3b8464b1dda45e11fac9157c29ad0e230664736e2fa`

```dockerfile
```

-	Layers:
	-	`sha256:b877fde8717c93de790deab8619a8e4a3ac5acff4878f1f093507d5f3f03f987`  
		Last Modified: Fri, 03 Apr 2026 18:11:43 GMT  
		Size: 4.0 MB (3968370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42deab29960ad26828473511b64f8654f4d9f8c66dfdc7e079994a7a7a0d822`  
		Last Modified: Fri, 03 Apr 2026 18:11:42 GMT  
		Size: 21.3 KB (21342 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:ad71705e5ae107b0702119856ecf83b1fc7dfe2750f8da8ec7fa95569362fd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108108879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea2cc310e4321da2aa1e59341e4988af2312f2f5edb2fc47d2bfe887aa763d5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:20:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:20:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:20:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:20:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:21:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:21:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 22:15:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2026 22:15:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 22:15:12 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 01 Apr 2026 22:15:13 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2026 22:15:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:15:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:15:13 GMT
ENV TOMCAT_MAJOR=9
# Wed, 01 Apr 2026 22:15:13 GMT
ENV TOMCAT_VERSION=9.0.117
# Wed, 01 Apr 2026 22:15:13 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:17:36 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:17:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:17:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:17:46 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:17:46 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:17:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e568bb13a59c072b3af8c406e7b451459d28a2bdf653f96393ea9610f7d09959`  
		Last Modified: Wed, 01 Apr 2026 20:21:27 GMT  
		Size: 17.6 MB (17622524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d5afe00e5afbff2327f1e5ddfe70480d6bdb9f90ad6f92e1a98cf210440d36`  
		Last Modified: Wed, 01 Apr 2026 20:21:27 GMT  
		Size: 41.7 MB (41723583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85ac7af2e315c52c0d13aa1fb591e1afeb6936b7f5ce9f71452bf9a9499e439`  
		Last Modified: Wed, 01 Apr 2026 20:21:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab1587e146eac7857d6b4db8ad86055e9020258b1e33f51f83af77d31866425`  
		Last Modified: Wed, 01 Apr 2026 20:21:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de4aac77203fdb3ed1b1699736ea7fae53da85404d828ff7e5a64bad7af8f69`  
		Last Modified: Wed, 01 Apr 2026 22:15:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5617b61578fe5ff0f3e56e410353ae490bbe0724789b77eaa4ba9933aea27887`  
		Last Modified: Fri, 03 Apr 2026 18:18:12 GMT  
		Size: 13.9 MB (13851294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0638d2657ffbb6b6f97ed1c838ae3fd09f10bdcaabe2e2076810ae8c6f78828`  
		Last Modified: Fri, 03 Apr 2026 18:18:12 GMT  
		Size: 259.2 KB (259207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0225e749fb0cba0379eb7a5869dec3487195fb74745695003cf8624306c8d3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62f12cfc22de51cffb745a94905c0525a9edda43685bf5b958d7f479c31fc61`

```dockerfile
```

-	Layers:
	-	`sha256:835133fd2ad5fa03fb00589f6f90a6cebc81d4648cf25d387e86a1e2bab9eb61`  
		Last Modified: Fri, 03 Apr 2026 18:18:12 GMT  
		Size: 4.0 MB (3972789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e496efda8f70b96b632bb21e70161b26fa0d6c0f43e231e63485c5a52b78865c`  
		Last Modified: Fri, 03 Apr 2026 18:18:11 GMT  
		Size: 21.2 KB (21247 bytes)  
		MIME: application/vnd.in-toto+json
