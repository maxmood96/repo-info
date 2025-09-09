## `tomcat:10-jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:28459af496f8fed032ff7bea15518d3ab06506bc951780941ddb650254d18866
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:10-jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:aae79f416e72cbafbb0c25e44d710f88ce8c888fa783959ba51ed61cc4e3875e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112986593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d09ef700755b1c0008b6e9079d4f3b67f7639d6784fd10f85ae848fe42768b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Sep 2025 14:03:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Sep 2025 14:03:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 14:03:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Sep 2025 14:03:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_VERSION=10.1.45
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_SHA512=2ebff699600c7a11c26e2d166eea3fa4851f894784b87f58555c6f53f4240cec836eef042fc74426959a58d41e68525f015c5f86ca35231b3d19dee07e82abc0
# Mon, 08 Sep 2025 14:03:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Sep 2025 14:03:17 GMT
ENTRYPOINT []
# Mon, 08 Sep 2025 14:03:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04853e34f5a8151c7f20c6027a9364b9233dfe2686ed91def6576890be0c65df`  
		Last Modified: Mon, 01 Sep 2025 23:08:56 GMT  
		Size: 16.2 MB (16150632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f900126b195dacbe382dbd48644d787bc3a578ff2cd19633d92fb038833b3b2d`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 53.0 MB (52968663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f1d4c8a8a52dbb4ae50ee5c9f56237520178681692e173483441961e599a1a`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c11345bebbe56bd80901ef463dbe05ad7adfc57f3c10c13a83bd046b252b4b`  
		Last Modified: Mon, 08 Sep 2025 23:24:03 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03efe8a64fee8ddf19cfbec1c8a3531bf2012a50536966c4f830024acbafa084`  
		Last Modified: Mon, 08 Sep 2025 23:24:10 GMT  
		Size: 14.1 MB (14097987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6d20c8fd5d66ecf6906c40208d9d42116548f1e2b9c617e25e9532af8399db`  
		Last Modified: Mon, 08 Sep 2025 23:26:31 GMT  
		Size: 229.7 KB (229734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:48e405931e638714a8c35b96ec145870f1df1510951dacdc364cead4e37cf7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b685991c9769ebf9a287dbcd7a197982f0b00fd58891d176f8bb7d4a67683bd`

```dockerfile
```

-	Layers:
	-	`sha256:b8f6b5d24e13dc5658224fc4108a991811ee3eaaf3e2990211aa5dc2150a9d74`  
		Last Modified: Mon, 08 Sep 2025 23:30:09 GMT  
		Size: 3.9 MB (3943945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f17985151009b288bed7f96cf1009b9da57b05d6aa278140caabfadbc7f5d61d`  
		Last Modified: Mon, 08 Sep 2025 23:30:10 GMT  
		Size: 21.3 KB (21260 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:8d47af7dd0a6088c707acc7466bc8fd25e31a986c2d4e74cbde822e5035dff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109904921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0144b7766a6de4e88ca719a46f6bd502d57fc7a6bc5fad1d6103f35679c2193`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Sep 2025 14:03:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Sep 2025 14:03:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 14:03:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Sep 2025 14:03:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_VERSION=10.1.45
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_SHA512=2ebff699600c7a11c26e2d166eea3fa4851f894784b87f58555c6f53f4240cec836eef042fc74426959a58d41e68525f015c5f86ca35231b3d19dee07e82abc0
# Mon, 08 Sep 2025 14:03:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Sep 2025 14:03:17 GMT
ENTRYPOINT []
# Mon, 08 Sep 2025 14:03:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4511ef1f8818f22c1b93fbb3e77ebb0b1001005ab33f8e9dd3aff34d0ab1d8ba`  
		Last Modified: Tue, 02 Sep 2025 00:59:41 GMT  
		Size: 16.1 MB (16063768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee350b8550ce6077de2bcaf4cba9f651563a200cedf088752d0d32b90a719ac`  
		Last Modified: Tue, 02 Sep 2025 01:07:01 GMT  
		Size: 52.1 MB (52148282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad5339f3cac439fc50f23f2f5607f1c304eb6ee3b02bfdfbfca85a4736b7558`  
		Last Modified: Tue, 02 Sep 2025 01:06:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed767c847d79314b8696147d5119499010656063e698759024bbe8abafed4f`  
		Last Modified: Tue, 02 Sep 2025 01:06:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2954c1453982403b7ef7c1567f225707f14b9f0bc5151b6a1f5ed9d55b6d3`  
		Last Modified: Tue, 09 Sep 2025 02:56:36 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e958859f35b117dfc07247a4dba168074cb6809b60e3e65164372521a0490c9`  
		Last Modified: Tue, 09 Sep 2025 02:56:39 GMT  
		Size: 14.1 MB (14100015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287e767bddc1a808b100249e324e66cc464f2c0b291804c377eececa7282b44b`  
		Last Modified: Tue, 09 Sep 2025 02:56:36 GMT  
		Size: 228.7 KB (228745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6a4733e29be3b97b5a9dddbf8b6b8d7867facc5b8e812fdc524c67376990de2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb462b447530c72aab73c8c39ab9b02505a9ef1dcf071f0f83fe8b41e8fd1a19`

```dockerfile
```

-	Layers:
	-	`sha256:ce555a2308cd3b212c134e13a1738fc2001883cb3ef95bc9647720eeaf7b9262`  
		Last Modified: Tue, 09 Sep 2025 05:30:20 GMT  
		Size: 3.9 MB (3943614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e60905fb6260603619f074eb70a4267ac1c848623604402d43226e4ee20ca2`  
		Last Modified: Tue, 09 Sep 2025 05:30:20 GMT  
		Size: 21.4 KB (21409 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:c0bb6285cfb33b93b20169082fe6f359bafefbee1e31263b6108ae9caba0872a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119430467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6191347337e5565a35cce29273f4d9d8345da0fbe44f878d6ae28803c9c75517`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 Aug 2025 16:46:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 16:46:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_MAJOR=10
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_VERSION=10.1.44
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Thu, 07 Aug 2025 16:46:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 07 Aug 2025 16:46:24 GMT
ENTRYPOINT []
# Thu, 07 Aug 2025 16:46:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb8a6a11d6a8aa6cb1265b04b48ac3ea54c5e642546199e4ec643364cc84fb`  
		Last Modified: Tue, 02 Sep 2025 00:15:21 GMT  
		Size: 17.6 MB (17624314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f50707cff55d68e366d9b7e0efa24a1b6f016b79111bf86958f7937859a4ffc`  
		Last Modified: Tue, 02 Sep 2025 00:29:23 GMT  
		Size: 53.0 MB (52994820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6021fe73d224dfbd8e712a05c8b5f7f319cdac3d6b4fc4646ed40fd0d55ac22`  
		Last Modified: Tue, 02 Sep 2025 00:29:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd70d93e0de497f196db3f220beba547f685a0ab076dd3e94abc770305a5bd9b`  
		Last Modified: Tue, 02 Sep 2025 00:29:17 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572a2517086870b9723e7aef24ca738d03d71bf95aef09d390ce5d291e20e5a`  
		Last Modified: Tue, 02 Sep 2025 09:54:40 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19af9dbfa3d7b375dd014da41030c23ad6cec5a7fedf86e217c2017a776bb01a`  
		Last Modified: Tue, 02 Sep 2025 09:57:23 GMT  
		Size: 14.1 MB (14106385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966ed34b3ab61897d79766a63c3e123d184dddb685be9bd1d15fd0c76addc42`  
		Last Modified: Tue, 02 Sep 2025 09:57:19 GMT  
		Size: 259.1 KB (259082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:9d8b5a437c6d47c4e2e9e49a0904e763c75aa8d04aaf458f0d356a66770735ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382233e81407ad5874d3dd1a5acfba7b06a5ef12bca0c3de4b20386214215ca6`

```dockerfile
```

-	Layers:
	-	`sha256:0e0e703cd5c2d669910d0e9fc7f30adb37cf98634128f7b14c0124169d845fa7`  
		Last Modified: Tue, 02 Sep 2025 11:29:39 GMT  
		Size: 3.9 MB (3948033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bd1b96bfbe91f157abfcaafbd6d4746ba0f072a9306b7cc624d7aebc7c296aa`  
		Last Modified: Tue, 02 Sep 2025 11:29:40 GMT  
		Size: 21.3 KB (21313 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:5a12f6e112704492ccf164922aa3e85e56434ee722cdbbdfa996e969c2ff5f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107995717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46d9b4f288c131c429c7e9b7e21bb4853bfe292893dd4825eab070616736814`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Sep 2025 14:03:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Sep 2025 14:03:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 14:03:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Sep 2025 14:03:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_VERSION=10.1.45
# Mon, 08 Sep 2025 14:03:17 GMT
ENV TOMCAT_SHA512=2ebff699600c7a11c26e2d166eea3fa4851f894784b87f58555c6f53f4240cec836eef042fc74426959a58d41e68525f015c5f86ca35231b3d19dee07e82abc0
# Mon, 08 Sep 2025 14:03:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Sep 2025 14:03:17 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Sep 2025 14:03:17 GMT
ENTRYPOINT []
# Mon, 08 Sep 2025 14:03:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9a055cccbd579a3774f2095602ffe4afd51473766e809ce2a67b5cfb09608`  
		Last Modified: Mon, 01 Sep 2025 23:11:44 GMT  
		Size: 16.1 MB (16149951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179129c724cd340caa8ca093ce0613c197ca6aca9646d670f1bf88f089c745b0`  
		Last Modified: Mon, 01 Sep 2025 23:20:58 GMT  
		Size: 49.5 MB (49507000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86998506ad314f8ca7142f8989765c1cc1967833ce361aef9f8a7483bee12eb`  
		Last Modified: Mon, 01 Sep 2025 23:20:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f3eeab27a221aad8b2a7a0b14f43e8e7b9e502c77aa9a85ee09be546f43d09`  
		Last Modified: Mon, 01 Sep 2025 23:20:51 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548048a0db6aaaa1420bee0989faa534652ab614fce18296c173c825cd36034d`  
		Last Modified: Tue, 02 Sep 2025 02:44:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35dba6c72c9ae4d3044265dcf3bfa3249314e3f5b9645f5971a7e5c3b94db90`  
		Last Modified: Tue, 09 Sep 2025 17:44:53 GMT  
		Size: 14.1 MB (14101647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249494fb39efdd9ef9028adc9cd17d0233c599b4cc22ff226c624d9368c524e7`  
		Last Modified: Tue, 09 Sep 2025 17:44:42 GMT  
		Size: 230.8 KB (230810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c3529a6adb5623473f490dbc3a10f51a665714b80c75347dd909a3bec5be31d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c6439a7ba98789df2f527f721b709602c1f5deadf87a0ea63cf7b8c5959d89`

```dockerfile
```

-	Layers:
	-	`sha256:f7a3ba151589a860076a45f8eff701f8a6af7a23a951c068a81876abcb0fdd91`  
		Last Modified: Tue, 09 Sep 2025 20:30:16 GMT  
		Size: 3.9 MB (3945536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c922e4fc1cff25a29d7cfa4b752be35163d552507b4160d257f8e64a5dcf01e`  
		Last Modified: Tue, 09 Sep 2025 20:30:17 GMT  
		Size: 21.3 KB (21261 bytes)  
		MIME: application/vnd.in-toto+json
