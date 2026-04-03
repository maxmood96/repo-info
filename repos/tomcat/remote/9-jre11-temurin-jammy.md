## `tomcat:9-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:5e5d1e58c0e1696d626055b94bd576185d84e3a7b88dc8f4858afffacb76add3
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

### `tomcat:9-jre11-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:22c61d2fd0ec26cfa26f2a54a5fa2c32e97cecc9acb380af9066d66d4d31e9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107249749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2daeb497560d9f2dc5c9a3b3f7a1f98f3e684eec283af6e92a52120303aca0c`
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
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 01 Apr 2026 20:10:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:11:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:32 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:32 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:32 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:32 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:39 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:39 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedbe7a7f974cd5e22a8bfde6806ab9362ef702fffc0f695deb267c3d5559917`  
		Last Modified: Wed, 01 Apr 2026 20:10:19 GMT  
		Size: 16.1 MB (16149364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e5fdc8171e8495e5d230bdb598ef70b1953977f6b35c73b2a6c3f7e69e5e88`  
		Last Modified: Wed, 01 Apr 2026 20:10:19 GMT  
		Size: 47.3 MB (47304979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7e8487d1b298d4f50a6bc0cc17faa53725573152bd99c37acbe9be9d8a618a`  
		Last Modified: Wed, 01 Apr 2026 20:10:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c769fd46c661790d45727fc77e16e982ff770e09a12c857cb8ad1bf5e20d1498`  
		Last Modified: Wed, 01 Apr 2026 20:10:18 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20a60cb6be780e7c4f90c1b1d96980f695c2d578778a1f02ce16d38e66552d4`  
		Last Modified: Fri, 03 Apr 2026 18:11:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782788de781cf9a8aacc0026c4d1c4c24bcde932e14de18a63e68bd0f8c905bb`  
		Last Modified: Fri, 03 Apr 2026 18:11:48 GMT  
		Size: 13.8 MB (13826616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ccc6d5f9a992ee661a8d3ab4838d8e9f5f646c6386e97f45856b4cbd9c76de`  
		Last Modified: Fri, 03 Apr 2026 18:11:48 GMT  
		Size: 229.7 KB (229733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b28c3b91e6e4466f5874003b1634792d2e381cc936135b28ab5992c9c3cacbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7698efc3620b7f4d97838dcaac8a29d6c8342c52f7e9f13e06adf5cc3eb125a4`

```dockerfile
```

-	Layers:
	-	`sha256:af20c3adc2aedd8f8d33637d66a13e276860678f2d8fe4171eb803c94da9056c`  
		Last Modified: Fri, 03 Apr 2026 18:11:48 GMT  
		Size: 4.0 MB (3951643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07e560775105311bff777c5a1333b801db76037a5e27e514091233f0d4bb67d`  
		Last Modified: Fri, 03 Apr 2026 18:11:48 GMT  
		Size: 21.2 KB (21213 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:f7daaaecb2042e40e77e5e73a16d537b33c4bdb9f89af226406d320f48629de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102111448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181c7c853fb971b7133556fbce843b7a44e29e4089ed1c6f8c17f39eb8bae438`
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
# Wed, 01 Apr 2026 20:08:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:08:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:08:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:08:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:08:31 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 01 Apr 2026 20:08:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:08:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:08:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:08:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:10:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:10:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:10:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:10:41 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:56 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:12:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:12:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:12:04 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:12:04 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:12:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e7c88f36edd2a67246005d083413bd656459d3b63bab8e6a05a1018c7658daae`  
		Last Modified: Sun, 22 Mar 2026 18:43:39 GMT  
		Size: 26.8 MB (26842286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c101ab2d24906ba57f07811588d39f3d2bc3bd8387f05863990e8127f502f9a`  
		Last Modified: Wed, 01 Apr 2026 20:08:49 GMT  
		Size: 15.9 MB (15889840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c17dba17d8ed3b008e6c6bc71ca49344853016048d753157a7705a8894aa9ae`  
		Last Modified: Wed, 01 Apr 2026 20:08:50 GMT  
		Size: 45.4 MB (45416530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad07f48ed25f0ac5cb66f5c79bf4f36358a7e0c619db9b8a11e9a3322c85e6f6`  
		Last Modified: Wed, 01 Apr 2026 20:08:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af6217cfc950f325d5385592f3e68fc8b8c23a0fbff8c7cfa7eafd2caa8ad2d`  
		Last Modified: Wed, 01 Apr 2026 20:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d63438b452d8d90635e5664748a304e4eae7fb394b1b4f5f8e19098178d6dd`  
		Last Modified: Fri, 03 Apr 2026 18:10:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1241ac42b670f17b4c94c9b766c170f8b6bebc1320261b46cfa38061f9a8a9b`  
		Last Modified: Fri, 03 Apr 2026 18:12:12 GMT  
		Size: 13.8 MB (13757695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f377f5697223f8cfbddd1a8b64ce40222457572b49af0df276bcea4a1b0753ef`  
		Last Modified: Fri, 03 Apr 2026 18:12:12 GMT  
		Size: 202.5 KB (202454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6bccd68a607a2c828b9803b88cba12b5f8a7919669695ea1786a416a9a03e995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd0b505947435091cf96d1f18ebad951a5c5ea733cca57f9ec4163b6393615e`

```dockerfile
```

-	Layers:
	-	`sha256:4d6cc60302bcd2094438f1f788f38b5c71de4b6999f1c65a96f6dc7efe1f606b`  
		Last Modified: Fri, 03 Apr 2026 18:12:12 GMT  
		Size: 4.0 MB (3955241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d99c5d7be3d2f52af6838ff47d431ce9cfb20af2039b578fa311e79701aaa4`  
		Last Modified: Fri, 03 Apr 2026 18:12:12 GMT  
		Size: 21.3 KB (21333 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:bdc52cd6e3759370234e734988e3eea832157d5c832afbe7cf24b87c7d726537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103369606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91147ad91ed3e361596e474e5f95d1cfc305695342717eef44529fbb1b0fec41`
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
# Wed, 01 Apr 2026 20:10:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:20 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 01 Apr 2026 20:10:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:11:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:15 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:15 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:15 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:15 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:15 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:24 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:24 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ced01b683067d01a3c90dc86777fb9fdcb5e8f69c9558641690ea9c69f7e60`  
		Last Modified: Wed, 01 Apr 2026 20:10:36 GMT  
		Size: 16.1 MB (16073542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ca96112de9c616c6cadc22e35f03440cf3ff5a54207648285466138b8f8275`  
		Last Modified: Wed, 01 Apr 2026 20:10:37 GMT  
		Size: 45.6 MB (45623046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3c68cb5188d0c39d0b7ee425d339091be9e72f53eed4f92e267b988feebe48`  
		Last Modified: Wed, 01 Apr 2026 20:10:35 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995436a9d426cc9dc14f797ac9ebf7ddc8647aa7851217a8e77066a574c2f913`  
		Last Modified: Wed, 01 Apr 2026 20:10:35 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b53409e17e87e53f157dede9c9907a229f62af6a598d059bf31ccc8fa1d6d54`  
		Last Modified: Fri, 03 Apr 2026 18:11:33 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb2e8bba2653738e9185deaa585c4892b9ae1f4c0ace55905fd8406b39dc328`  
		Last Modified: Fri, 03 Apr 2026 18:11:34 GMT  
		Size: 13.8 MB (13834669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ffb6d3f8284c010bfafe1c315dafe5e7508915dee0c9e5cfde4ad4662042c`  
		Last Modified: Fri, 03 Apr 2026 18:11:33 GMT  
		Size: 228.8 KB (228761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:35f2d5750fa918386a2e4eab3c912dccbc00fbfdbadfc44c085bb4e27ffe08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3973291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02551512ed51e5e32082deb37f7221ba39db0034e4ed4b2a2bf847710db336d1`

```dockerfile
```

-	Layers:
	-	`sha256:0d13e8ee45c792b011fdfd75fd2195fbd384ac9185ee8963fae98f6dd22ffc21`  
		Last Modified: Fri, 03 Apr 2026 18:11:33 GMT  
		Size: 4.0 MB (3951930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569c37ae9b196a3f15f90cf0a75c7127e435f9e4066304ba1d1ece323a9acb11`  
		Last Modified: Fri, 03 Apr 2026 18:11:33 GMT  
		Size: 21.4 KB (21361 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:9f6c56ecdc95c9ec722ab339cf2652e45aa516ae78ce812cd65a87fd26be8397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109139935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a29555201d4b6ad8e7a7fac6476cfb2e69f2400351ec7f11dff0e0af8b4f6e7`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 01 Apr 2026 20:21:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:21:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:21:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:21:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 22:13:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2026 22:13:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 22:13:38 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 01 Apr 2026 22:13:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2026 22:13:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:13:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:13:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 01 Apr 2026 22:13:42 GMT
ENV TOMCAT_VERSION=9.0.117
# Wed, 01 Apr 2026 22:13:42 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:16:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:16:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:16:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:16:41 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:16:41 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:16:41 GMT
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
	-	`sha256:d1dba9b6db358d0c8ea9cee84a263326cedb1890f3b92f9d617586a330067d6f`  
		Last Modified: Wed, 01 Apr 2026 20:22:16 GMT  
		Size: 42.8 MB (42753922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb445c563bee675103e92af115f4bc50a879b5bf0d2d2a1f4c4cef83be4fe57`  
		Last Modified: Wed, 01 Apr 2026 20:22:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbf58a2a7db17b02a2300936e5755d53f173550d92c8466debe96bf99fef34`  
		Last Modified: Wed, 01 Apr 2026 20:22:15 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a96084bc7756b654656572f0869333a4be7d67012caf30e864261dfd8b8691`  
		Last Modified: Wed, 01 Apr 2026 22:14:14 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b33a30aa51ae66cdd295444449de2cd103d39e0f4a087ca34daae7e027ec241`  
		Last Modified: Fri, 03 Apr 2026 18:17:01 GMT  
		Size: 13.9 MB (13851942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f902410fd4ab914a4a59504a36323400f7fbce4560e16c2f4a53b0f4678de8a`  
		Last Modified: Fri, 03 Apr 2026 18:17:01 GMT  
		Size: 259.2 KB (259242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6b39f4622075fdadafd7118ad525a04871857c650e19dfcbd4d93d57d302c2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8226406c3b52a267a88aac92e99d78210a778ca99b637122f2ff2278c835b052`

```dockerfile
```

-	Layers:
	-	`sha256:1ebba833649b404a729e5fb608f4a00735fdb645110c8500ed032f3f739a742e`  
		Last Modified: Fri, 03 Apr 2026 18:17:01 GMT  
		Size: 4.0 MB (3955737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95b0ecbad72cada8c0e97f48bf95cdfe3e4589c68c0fe16331b9e0293220d94`  
		Last Modified: Fri, 03 Apr 2026 18:17:00 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:1cf9a812bb5abb731e3c596c34319067fc251c9b8fba0c14ecf40e9832a73e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99716994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83240ea8969b944a621f56ec4e21fc93db21f771a326405c9dc68f1045a5bea5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:08:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:08:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:08:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:08:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:08:48 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 01 Apr 2026 20:08:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:08:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:08:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:08:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:09:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:09:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:09:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:09:54 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:09:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:09:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:09:54 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:09:54 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:09:54 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:20 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:20 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61594cb5a2469e67362dd6ac0dbccf92b89f433e8186d9f63201da426862ed3`  
		Last Modified: Wed, 01 Apr 2026 20:09:10 GMT  
		Size: 16.1 MB (16149500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5050401f4e1c766ad557c81fbb66508e04d50bb536ef9199b83ff4012604581`  
		Last Modified: Wed, 01 Apr 2026 20:09:11 GMT  
		Size: 41.3 MB (41310438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d615835532238585bda87a8bc3aae7e6aebff6b8d283228c6a64931b2db1b6a0`  
		Last Modified: Wed, 01 Apr 2026 20:09:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98639892efde6cd2c01c608614e8f33a3582486896c9f2674a6926be3cbec252`  
		Last Modified: Wed, 01 Apr 2026 20:09:10 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb89b60283bdbc9f2f4a9f364577baf79fcf124c2633006d2f1ddd58d879c709`  
		Last Modified: Fri, 03 Apr 2026 18:10:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c018ad2a9ea9e4f5be39460013aac2359089554b2f2208a546251148636da79`  
		Last Modified: Fri, 03 Apr 2026 18:11:34 GMT  
		Size: 13.8 MB (13820683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf49a80a9064189d4dc9b34c0cb59a39b2a4a77dff8206fcd3744a60d58aa9c`  
		Last Modified: Fri, 03 Apr 2026 18:11:34 GMT  
		Size: 231.0 KB (231001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:e65b5cc1f7bcd5129f1941bf9a43c42baa169fd9abe822fe26a8a0783908239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57947d9968eb456aa242d4658b5e2c5f2a073dc8b50828110ef42a60fce2a018`

```dockerfile
```

-	Layers:
	-	`sha256:941c3b38e4d67770f42ccb3d592b233b50d5b34c27938b78a5697f64b4cfc468`  
		Last Modified: Fri, 03 Apr 2026 18:11:34 GMT  
		Size: 4.0 MB (3953240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d9a48742fd08649d280c1b9ca3264e40f0575a52231b64478312c5d60798d41`  
		Last Modified: Fri, 03 Apr 2026 18:11:34 GMT  
		Size: 21.2 KB (21213 bytes)  
		MIME: application/vnd.in-toto+json
