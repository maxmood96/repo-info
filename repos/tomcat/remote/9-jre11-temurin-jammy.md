## `tomcat:9-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:6070df3e18ccae4fe67435a75faf1e4647b30605fdb8fd8293577261134deabf
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
$ docker pull tomcat@sha256:d5cf0f18b22a7a3e53d80a4fa3009f28e1f993c7078f5d18c141e87fb403a679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106598511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af32335c1737412877cca94efca2e86639b4074cdb7e8bc1375c8c2c2b4dfa82`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 06 Jan 2025 23:11:14 GMT
ARG RELEASE
# Mon, 06 Jan 2025 23:11:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 06 Jan 2025 23:11:14 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2218709e815fb56b0b64c187c009b0c907a7935bc70e1133db22c79cd58e71ee`  
		Last Modified: Tue, 04 Feb 2025 04:39:13 GMT  
		Size: 16.1 MB (16135155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7988bfb5529fb85284fe5b1b20470912746d60c808fa72d6854fa5e964a4753`  
		Last Modified: Tue, 04 Feb 2025 04:39:14 GMT  
		Size: 47.2 MB (47216614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d854889cc3907acabb01aa052b8f112d7bdff0b071fd1b8ab2cdccc59b516167`  
		Last Modified: Tue, 04 Feb 2025 04:39:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf2a4e8b353be69b442f45259691d65ef85a8dd97c02a339a0e128f05088536`  
		Last Modified: Tue, 04 Feb 2025 04:39:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c21a565ecf0c7be4aef176acfa7fc7abea5fc5d24d51c1f093078ec30771fd4`  
		Last Modified: Tue, 04 Feb 2025 06:16:30 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346fe833fb0e62182e9c2aecf134c2deb2ba9539a008d08ae097c9bdbecbd4c9`  
		Last Modified: Tue, 04 Feb 2025 06:16:34 GMT  
		Size: 13.5 MB (13478562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4395ccd98bc088a4f45090ee3133287a5daead7dd4561d7103a9175dc97b24a6`  
		Last Modified: Tue, 04 Feb 2025 06:16:33 GMT  
		Size: 229.6 KB (229596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:be32c62c2d2124937abc9856be507172a8a7b6947dad3040a5cd1181cc38d812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3797330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13272f12efdc00eefc705ab826ff3858b1b9a4a47859c4fd0f053aa34b0a5e19`

```dockerfile
```

-	Layers:
	-	`sha256:ff6d30d2ff5fe517485210d6bb9301a09349f55612c283f0557891ac1edc087b`  
		Last Modified: Tue, 04 Feb 2025 06:16:33 GMT  
		Size: 3.8 MB (3776083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688354aa49baffd843cf2995508ce6e0cccf95acf1a42725de7bf881bfec0dcb`  
		Last Modified: Tue, 04 Feb 2025 06:16:33 GMT  
		Size: 21.2 KB (21247 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:8ac63195c3cc42ea0f16db0d8c80e962ab957e5e7f144d207db125108e6b0c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101472500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d861a02ec8e89ee16a95dd7b8e71ad966d88be2d83633fcd7d9a84b3de729514`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 06 Jan 2025 23:11:14 GMT
ARG RELEASE
# Mon, 06 Jan 2025 23:11:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 06 Jan 2025 23:11:14 GMT
ADD file:7e9e4d557a66a31de2a39930803dbe849ba710af36b4731e9cbc856f55c10018 in / 
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:eeaefd3c974dfe1d5e1b8eb1929496ae7befe434399b37e601701f6d012e3169`  
		Last Modified: Sun, 26 Jan 2025 07:02:14 GMT  
		Size: 26.6 MB (26639267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bc4151aca7aee0d14e2a39ddf8e63d8b5b3ab7cb73799f25458d2cec004ff`  
		Last Modified: Tue, 04 Feb 2025 10:51:37 GMT  
		Size: 15.9 MB (15885582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d961c835285012047aa4b5a7bf4bac002f6c3be9c9a15512709fd68c4b341a`  
		Last Modified: Tue, 04 Feb 2025 10:56:51 GMT  
		Size: 45.3 MB (45330421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9145b8f2fbd7b6632f0615ac515cd03cc31cfbdb0fda2dbee675efb02fb3b48`  
		Last Modified: Tue, 04 Feb 2025 10:56:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e265a5edd3b85ff5d7cc73d878e7ac44751ef45a240c87399613154adad74be`  
		Last Modified: Tue, 04 Feb 2025 10:56:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a40559b12dc867028328e41f6e787d47f3cf07625fd7da9a3474fcbd655c0f2`  
		Last Modified: Wed, 05 Feb 2025 01:31:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023dffc8c75c296318d25571c7899adb6c8108f77e1fffcf2ef8e36ceecc4c0`  
		Last Modified: Wed, 05 Feb 2025 01:33:53 GMT  
		Size: 13.4 MB (13412356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a76a39c3ab5163254a2477c2f437c61b0bb1a55b67e472989501bfb7cc3435`  
		Last Modified: Wed, 05 Feb 2025 01:33:53 GMT  
		Size: 202.2 KB (202230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0f20ad57710b905acfdd95c9c6756d0667c8fc47e061bfc28895dc3a48f9e076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84ce7dad374a74883b0c37ef6fb1896cb8e5cc48a1b3125cb52a6893d031a8d`

```dockerfile
```

-	Layers:
	-	`sha256:d8d8ca58fc06c6497d0273aedc19e58548f69ade81361c3bf3c6143e21995207`  
		Last Modified: Wed, 05 Feb 2025 01:33:53 GMT  
		Size: 3.8 MB (3779681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7654ec0ca6adb285c995beb79ebe38bd4ca0ae68dd7b92df33a3d1f9a103f8e`  
		Last Modified: Wed, 05 Feb 2025 01:33:52 GMT  
		Size: 21.4 KB (21363 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:a84f416914bf7da055352d890d0a6a7d96511e90ac33398f800f3f3a7efe810c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102714775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7154f31801d16fa3a2b9f82a3f064329297ab399989deb91c47b3d3d322edb5b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b812e64bffa2068b9b710d250bf1fed09dca5c6adb9ecfb1f1e14b96bf5ea3`  
		Last Modified: Fri, 31 Jan 2025 01:38:18 GMT  
		Size: 45.6 MB (45576051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ae99645f445adb73411db6b15609a9fdaf69adfbe0138c6831aaf6964304b0`  
		Last Modified: Fri, 31 Jan 2025 01:38:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c103131686f33e620ac801461f57e48ee54452ec90c794080bc2bbef04488c4`  
		Last Modified: Fri, 31 Jan 2025 01:38:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c346fa2cc79becaced3b4b6ed07845792ebccbf3d9ac4e96e3c5eef548577f`  
		Last Modified: Fri, 31 Jan 2025 06:16:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec65a5ecde65af9e2867fa56be63ff966f68ad1b0ba3629acc19b8474ebe2f22`  
		Last Modified: Fri, 31 Jan 2025 06:19:00 GMT  
		Size: 13.5 MB (13487319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362cb83e274e87cbe5518d1f036813e5487951cc55d77a628a747c917c1634e6`  
		Last Modified: Fri, 31 Jan 2025 06:18:59 GMT  
		Size: 228.4 KB (228392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:1e36c0c9385f91a120c6a8a988d065e83f73b6613615a0f55f1898df1235f958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5a36052a1a30bdec115a52203bd2e55061beffc5549f1777d622732e40da48`

```dockerfile
```

-	Layers:
	-	`sha256:aa133485a2cda225b4cdd2c0dc05871a762264a99c0c6e5805ff27b61c3212a1`  
		Last Modified: Fri, 31 Jan 2025 06:18:59 GMT  
		Size: 3.8 MB (3778246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91b7a9d9c0a9116fe42571981c579680bc5c8e1a6d5973e637f29890a952b77`  
		Last Modified: Fri, 31 Jan 2025 06:18:59 GMT  
		Size: 21.4 KB (21395 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:2e6d2dbccd9acb794541c6370d0b3265d7d4dea3cf4f318c3d1a35319f9df062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108533191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d730ec251ece22ed50dd6a5e34b173f0d2e95050fe13dfe91bc85cd19de97d40`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 06 Jan 2025 23:11:14 GMT
ARG RELEASE
# Mon, 06 Jan 2025 23:11:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 06 Jan 2025 23:11:14 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71de2d980599cbec4dab5c3bd7274078312e68d7cc81171b5d8bda1a98eb2403`  
		Last Modified: Tue, 04 Feb 2025 07:32:10 GMT  
		Size: 17.6 MB (17642335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c61bbafcc42be7bb2d7712af69e57ebf7e049fec077b764bd1e3b3c4b7efd9`  
		Last Modified: Tue, 04 Feb 2025 07:38:47 GMT  
		Size: 42.7 MB (42674757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1aacfa886ca57611c33edb531a8314eae2266fb71811fa9124927fc6f74338`  
		Last Modified: Tue, 04 Feb 2025 07:38:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34ba8bb6e72bc5d08ef249d59722b03d476b8ab262e61fecdda5f89aea44d47`  
		Last Modified: Tue, 04 Feb 2025 07:38:43 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e479dd91ee379d05e9db0d32f5705899451501378b9be38c941110b8f53429`  
		Last Modified: Tue, 04 Feb 2025 23:16:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a202842db42a25bf4e1ba084d3216d0fdcc46d5ec386bad4e1ea5cf7ff58c58`  
		Last Modified: Tue, 04 Feb 2025 23:19:55 GMT  
		Size: 13.5 MB (13506621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c0de1245c349218747da058779331256b0b2cec502c57e1910772cf73f77e5`  
		Last Modified: Tue, 04 Feb 2025 23:19:54 GMT  
		Size: 258.9 KB (258898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4d5a70bc1fc0956753762378c31a1ef5d5725f4a027a00ed0ceb60f75e404685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45df17d514bdc7d19f57f6b869ee1428bdf44277119282a0b28ce6d2cb52724`

```dockerfile
```

-	Layers:
	-	`sha256:0f62682501631c1ad28314271c583fe9125ea86c59b84acd129433402c48665d`  
		Last Modified: Tue, 04 Feb 2025 23:19:54 GMT  
		Size: 3.8 MB (3780025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1d683269bd01a8ee378091d2e24a1da0ea32f5109ffe2f79dd0818cb773433`  
		Last Modified: Tue, 04 Feb 2025 23:19:53 GMT  
		Size: 21.3 KB (21299 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:98c98304f7b038db3c5c9a6e6304f1d040db9690d4a188ce128e97420e70e906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98679894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d3b17af3456dc43b4bb29be844d05b5d518ac8d163294a7f59a1b2f158d5d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 06 Jan 2025 23:11:14 GMT
ARG RELEASE
# Mon, 06 Jan 2025 23:11:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 06 Jan 2025 23:11:14 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c64c26afd0885ce3d2d456d35ff90e813c65ee4e2f59dd40604fa8b3e90414`  
		Last Modified: Tue, 04 Feb 2025 07:39:56 GMT  
		Size: 16.1 MB (16132604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a6874e2b5e9af7028473edb4150a2a40b9657fc9bd046807c846d5c59d0de0`  
		Last Modified: Tue, 04 Feb 2025 07:42:33 GMT  
		Size: 40.8 MB (40838283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14c64077029f5a50543b5e9018488c1bb1799b0222b8c32f5302e3c597d398e`  
		Last Modified: Tue, 04 Feb 2025 07:42:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38350f10d88e074ce81806f48a1805f8cb0abccb7954d68dd129939623450310`  
		Last Modified: Tue, 04 Feb 2025 07:42:32 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192e20916e6c482f15d45fa6879b622a5020e032d1751e7c3c32d2395fcbaf4f`  
		Last Modified: Wed, 05 Feb 2025 06:01:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb00616b713651a846f6f24f177296ff13bf13899f593ae1b2897e7af9fc0c4a`  
		Last Modified: Wed, 05 Feb 2025 06:04:33 GMT  
		Size: 13.5 MB (13474688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f97a8199b6183cfd4a9b02dcdc957c1fa5507ed9936dbc9c2c2d62a3eed75a`  
		Last Modified: Wed, 05 Feb 2025 06:04:32 GMT  
		Size: 230.7 KB (230746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:caf75f6e42e4e05023bb94eda478206114734bfaef86c8e4ebd14e5948b80cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3798927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e14ea620a7cdea2e8a7f9cb0ec376d5dd1cc23b0a76308a4d9124a645effd3`

```dockerfile
```

-	Layers:
	-	`sha256:62b4f35ea23365eabb60afdd4ee940e0dffa41ecf0a601aac15be3b73805e3a6`  
		Last Modified: Wed, 05 Feb 2025 06:04:32 GMT  
		Size: 3.8 MB (3777680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21fbbbab58e1afa245cd8303a7445ee0c4c30e8ffc717f2f5a0b130312cddecb`  
		Last Modified: Wed, 05 Feb 2025 06:04:32 GMT  
		Size: 21.2 KB (21247 bytes)  
		MIME: application/vnd.in-toto+json
