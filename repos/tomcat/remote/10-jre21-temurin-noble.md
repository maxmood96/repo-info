## `tomcat:10-jre21-temurin-noble`

```console
$ docker pull tomcat@sha256:f683307f4625b2435dab5b9f650a28f2737b92f1fee39b8a4e5704adf257751d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:10-jre21-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:54ff927183cb88adc39f975f85fce7ae7a6cd8cd4ebd4e549b79d80ea1a4a087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113979883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5003ca218519f3b90346a4baaf5d6fa8ddcf763c520990a482a3a439194a69`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 14:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 14:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_VERSION=10.1.47
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_SHA512=fdaaefb63a8b7150b3e065a19730a7ac14d7c835c33a273245dfe428ff5e8d7bbff18e590de843c40e2196ba54b894d4a17330ce6c1f53f93fe98c8f5310b2f5
# Tue, 07 Oct 2025 14:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 14:03:19 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 14:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f38e2e092670ef283f8cef3be87ca664b534a953c460e93cfc9ffeebbc8224`  
		Last Modified: Thu, 09 Oct 2025 21:13:36 GMT  
		Size: 17.0 MB (16971757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c474f64746d27f2879d262f6299fbbf510deb0689105ba567ba62c6760583d3`  
		Last Modified: Thu, 09 Oct 2025 21:14:09 GMT  
		Size: 53.0 MB (52968909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e9704d175f236f24573f3263c46c98ce312c06751ec7feb8aa18adda6c39e`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2326993b9fe603f4efecedec459c92a6f5cbddca94dc55593db837055ac2e4e8`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aacf5f64022600a03fb136afde92d6802d5f609c8e0374ed46ff2ab8df20987`  
		Last Modified: Thu, 09 Oct 2025 22:48:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfdd3c2eeff8b42ffa950791fbd422a590219e7af6ff73d7f601deb8f9277ef`  
		Last Modified: Thu, 09 Oct 2025 22:48:18 GMT  
		Size: 14.1 MB (14088698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aff5f7a045155cb540fdd83ab21d422cb41160dd136e6b901eae57ca4a5ee3a`  
		Last Modified: Thu, 09 Oct 2025 22:48:17 GMT  
		Size: 224.7 KB (224729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:e138cd68d2489e5e7a78093d464e581f90f5ab2d3c0a2b8b85bc80a5f17729ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5494a52649044aec4aaafb637e28a9f1bbd70452f423ec09f50f474e707ad82d`

```dockerfile
```

-	Layers:
	-	`sha256:df785699eaeaf699abf307fa85725df348dd58e463d5e9f45c96f09f155caa02`  
		Last Modified: Fri, 10 Oct 2025 05:30:19 GMT  
		Size: 3.4 MB (3351174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f245f308ff896d0a6782ba6004150b36768f88cccc69aa51d9b8d0dc8fa5966`  
		Last Modified: Fri, 10 Oct 2025 05:30:20 GMT  
		Size: 23.1 KB (23149 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:f61ba1f86ace2717c4eda2a54df12503a264b87ace70e9691174865a0eafa6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112319368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f6be8f5d1a2ed0e039bb202fbb8c64da97a2efb3bde2a7a6a6ba1f13de028e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 14:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 14:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_VERSION=10.1.47
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_SHA512=fdaaefb63a8b7150b3e065a19730a7ac14d7c835c33a273245dfe428ff5e8d7bbff18e590de843c40e2196ba54b894d4a17330ce6c1f53f93fe98c8f5310b2f5
# Tue, 07 Oct 2025 14:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 14:03:19 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 14:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf670432170ff54aa7d7fec54b27ad51dc4b767bc00a3178b28176173ef130c`  
		Last Modified: Thu, 09 Oct 2025 21:14:24 GMT  
		Size: 17.0 MB (16989173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d3072b7ee41b26a0c52ffc0714ce586e836d00c7f9936e7f5c4219d8993682`  
		Last Modified: Thu, 09 Oct 2025 21:15:03 GMT  
		Size: 52.1 MB (52148484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd18b9ed8f5e6430b2e5b01ce34688a7c375b5a5ab76ed710e24a610e354cc1e`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452d8b8a38c043118d3c800c54e6273302aa0642a20b0df0f628b8d0e8866ce`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb8b10add49cb56b0618566b02ca0efb0758d3083646cd43f6cf9b32d749583`  
		Last Modified: Thu, 09 Oct 2025 22:51:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95082d2bacc17a6bcc66970aa0e3ea6d9d2daf22d491a63e7b29f710d58d06bc`  
		Last Modified: Thu, 09 Oct 2025 23:13:01 GMT  
		Size: 14.1 MB (14091992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02913cd637cdc1691f5a6ff7e5d4d63fa13aad5f95241ffe6b2fca14eb7c378`  
		Last Modified: Thu, 09 Oct 2025 22:52:00 GMT  
		Size: 225.4 KB (225365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:2d61415770142c4d2896b52572e86a1f76f02ccb674d8043077656409dc991a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3375075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e66056cb2c4c43df0b1a7a686dc12448f108b27ac304616c1766507d0cb223`

```dockerfile
```

-	Layers:
	-	`sha256:5f8b8b8be971c22d2aa56808dbd008d3b47d117b039de05dce669b1212a74e8c`  
		Last Modified: Fri, 10 Oct 2025 05:30:24 GMT  
		Size: 3.4 MB (3351706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5599f44333966dc8cc1dff30dfdcfcc247215414d9558c28d30704a9a4fc8b7d`  
		Last Modified: Fri, 10 Oct 2025 05:30:24 GMT  
		Size: 23.4 KB (23369 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:8aa9e1b94eb57221bded937dfa6f68e8f935e967785a72b1b13e2c2129dc47cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120478103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f60932c8d7adf03c34b2e94193374503c04d0eaf0f9ed213e5e5d166c3cd879`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 14:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 14:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_VERSION=10.1.47
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_SHA512=fdaaefb63a8b7150b3e065a19730a7ac14d7c835c33a273245dfe428ff5e8d7bbff18e590de843c40e2196ba54b894d4a17330ce6c1f53f93fe98c8f5310b2f5
# Tue, 07 Oct 2025 14:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 14:03:19 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 14:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8140b6802a26c7a0bead435aebae86d7674662b20259d072bc0bec540e3606a`  
		Last Modified: Thu, 09 Oct 2025 21:16:28 GMT  
		Size: 18.8 MB (18814785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef75afc9a8ebb8bd90828afa217b7916d2f86fdc78d84d9052a1aacdf27ec4b`  
		Last Modified: Thu, 09 Oct 2025 21:19:09 GMT  
		Size: 53.0 MB (52994817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a364d4ee4cd8448091024a65c4c43bc21b7d63c76a800599583f919042d68c35`  
		Last Modified: Thu, 09 Oct 2025 21:19:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e8018793dd12ba2eb4550d3e43adf769660dfdb860abb447a67c1f4bffe6dc`  
		Last Modified: Thu, 09 Oct 2025 21:19:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02168793b3ae51c3a041e7c36e85703e2e373d5a650b3c2b4817543271a06337`  
		Last Modified: Fri, 10 Oct 2025 08:42:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799aef8dce80f6f002def1f17ce70df09c4a51d765331bbe887230aa87aad954`  
		Last Modified: Fri, 10 Oct 2025 08:45:11 GMT  
		Size: 14.1 MB (14105671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5062160223d409fc6126ca61a9109db9660ae757ff82ffe40539e454bda22d`  
		Last Modified: Fri, 10 Oct 2025 08:45:08 GMT  
		Size: 256.7 KB (256661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:c06f0d0ec84cb572fd9910b436557096d23b02e0cde01a903d2ac8162350cf32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3378518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9a68ed2bc0bf16b889bf9ebe9d9f6d4aa9798a960cf63d082c11653870c42d`

```dockerfile
```

-	Layers:
	-	`sha256:902b7410f650be08359e21e7cb2bf42959e3d8b27cf5d8ebf617d13bd19756b7`  
		Last Modified: Fri, 10 Oct 2025 11:29:07 GMT  
		Size: 3.4 MB (3355281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e824f0b7546fb81b7758b7e8df6aba16899784eeae0f26bf2b90567a9b80dca`  
		Last Modified: Fri, 10 Oct 2025 11:29:08 GMT  
		Size: 23.2 KB (23237 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:b9e61ad6fa1681c672868aa406726306dc4136ecee4fa22c6645c26f8abd664d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116150070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a06a7a9aa96d7ca6f7339cbbbd88b23ba1879f7469ffbb893d99725234bd654`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:13e2355f84c9f5f1ba6aa2fa1db4359cbe23312f7b2905fc8b976899a09fdfef in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 14:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 14:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_VERSION=10.1.47
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_SHA512=fdaaefb63a8b7150b3e065a19730a7ac14d7c835c33a273245dfe428ff5e8d7bbff18e590de843c40e2196ba54b894d4a17330ce6c1f53f93fe98c8f5310b2f5
# Tue, 07 Oct 2025 14:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 14:03:19 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 14:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2d699e6bd7ed3cc40f40b8118f763dc4303b0e97b911de163cabf78f19b5d434`  
		Last Modified: Thu, 02 Oct 2025 23:21:18 GMT  
		Size: 31.0 MB (30950446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c968878eef99dc549f1ba1b1045b0f5e0b9fd8a5906a80b6d2dbf8a197890f50`  
		Last Modified: Fri, 03 Oct 2025 19:37:02 GMT  
		Size: 20.0 MB (19973992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bd089c38d4fe75d2f7740a64daf6d568ec413730b8deb98aafb9d48a0c4824`  
		Last Modified: Fri, 03 Oct 2025 19:46:04 GMT  
		Size: 50.7 MB (50720802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd61fa1afe6e1b1ef4a6c9030a4ceb799b3fa4171666a5b3bc8b81c8e735f792`  
		Last Modified: Fri, 03 Oct 2025 19:46:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4562de9443302a99d5e68fe406b244a6561146fd84ec79585f3663b73904b68`  
		Last Modified: Fri, 03 Oct 2025 19:46:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b26e3bfaa5a2506084ca96935361231546c677dc3073ecf5b4c1e5e7b31de`  
		Last Modified: Tue, 07 Oct 2025 12:49:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8c40e9a29fce369e5d1db523839f5d126a39daf237406b2da7ed2dfb10aaf`  
		Last Modified: Wed, 08 Oct 2025 12:48:34 GMT  
		Size: 14.3 MB (14273968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0d0e08fb9a67e8a1287d180fc3dab053a8cea8130703c5e68897375e8b2fb5`  
		Last Modified: Wed, 08 Oct 2025 12:48:30 GMT  
		Size: 228.2 KB (228219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:431bb41240bb2147c8f07c75ca73893d6a0847816985a309ef7d53f185d496a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3366520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe2d63a85a15e69d57a6282b31311196682c23f8b1516c9eccdcf37fba143fe`

```dockerfile
```

-	Layers:
	-	`sha256:92407e18dd150271e8bba54be0bc1c4122a9ee008211c97a5e2ecad18efc2606`  
		Last Modified: Wed, 08 Oct 2025 14:29:00 GMT  
		Size: 3.3 MB (3343283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb97f50407300869897650a7a57043af568ff7a9768e1f6332d5604110ef84f`  
		Last Modified: Wed, 08 Oct 2025 14:29:01 GMT  
		Size: 23.2 KB (23237 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:4e9c28d420b32128573d447cf5f4cbcff0a9871456b060b112ab13bfbbf05e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111329913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec2646a2e4ec834f42f394569a7e86c9d6657df1a3371f4b1d934d3348ebfca`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Oct 2025 14:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 14:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_VERSION=10.1.47
# Tue, 07 Oct 2025 14:03:19 GMT
ENV TOMCAT_SHA512=fdaaefb63a8b7150b3e065a19730a7ac14d7c835c33a273245dfe428ff5e8d7bbff18e590de843c40e2196ba54b894d4a17330ce6c1f53f93fe98c8f5310b2f5
# Tue, 07 Oct 2025 14:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Oct 2025 14:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Oct 2025 14:03:19 GMT
ENTRYPOINT []
# Tue, 07 Oct 2025 14:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabd01e6819aeac2f63cff823f48fd76bc7d79e15d01db865388e99659200e56`  
		Last Modified: Thu, 09 Oct 2025 21:11:03 GMT  
		Size: 17.6 MB (17580766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adb3a0395b2f142197dbed56132fd32b81a5412b86fba6635a5c2a3d52f5b35`  
		Last Modified: Thu, 09 Oct 2025 21:15:07 GMT  
		Size: 49.5 MB (49507306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994e349dc26716765c18123a1afe35154dc41a42980b380811d998d1fccab7d`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052dc0d5069685926780974e4c16a48da1ad8e760614f991e98d260844156d`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72aae98b62c8abdc6c95d4adbc67ec773749c2472dd7d1241fb879b39fb249`  
		Last Modified: Fri, 10 Oct 2025 05:27:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a442b2230dab6a965a227bef745cc2b77611d56b0c75d59adf550941b4cb6d6`  
		Last Modified: Fri, 10 Oct 2025 05:29:22 GMT  
		Size: 14.1 MB (14100305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d3f0a3a0efab3875dadb838de7c09631ceadedf632c93236918425ff7c2952`  
		Last Modified: Fri, 10 Oct 2025 05:29:21 GMT  
		Size: 232.7 KB (232739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:670e74202c68f30c960c7c1b0fa5e3ca12313e8759ffaec77dc6deae206adeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e8971c620db85522aea733de2ba03d9ad636eb123389b49d5001b7ae6c86b8`

```dockerfile
```

-	Layers:
	-	`sha256:642e445ecd65e19b4e24d06fe4d758296af74e1e95cab661411a69e8e8ee5ee6`  
		Last Modified: Fri, 10 Oct 2025 08:29:16 GMT  
		Size: 3.4 MB (3353373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d6511b37770dbde9247d973e9f6b993b959777509b3800d3f04d93cae5adaa`  
		Last Modified: Fri, 10 Oct 2025 08:29:18 GMT  
		Size: 23.1 KB (23148 bytes)  
		MIME: application/vnd.in-toto+json
