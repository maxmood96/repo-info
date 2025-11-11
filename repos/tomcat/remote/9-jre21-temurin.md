## `tomcat:9-jre21-temurin`

```console
$ docker pull tomcat@sha256:7dce3ef42cad3bc8c0d201b47040d08042e838a05b670314dfa6dae798244cc3
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

### `tomcat:9-jre21-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:2be42fd6fac6c88444ec6a1dba5eee4097f663d4f8fdab25a303830811e425d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113633413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f3c218f0ba377356fba9fea73564ce45d3dc56da4d69899283779b61109015`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:55 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:27 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:27 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:27 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:27 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:34 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab3da5da257e46e9d6b1be6e6312cf99ab2fd30b3369ea1e6e8133c3ec67afc`  
		Last Modified: Sat, 08 Nov 2025 18:00:24 GMT  
		Size: 17.0 MB (16972258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8908794a351cbc23988c2d21157ab97f0e7f9caf3b6ca7652c35ae100381a897`  
		Last Modified: Sat, 08 Nov 2025 18:00:40 GMT  
		Size: 53.0 MB (52978720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8db6d83f4b1e909438cff1d916e4c634deba5e4c3b141c6d0d5cce163272729`  
		Last Modified: Sat, 08 Nov 2025 18:00:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3096c0eb2bbc9ac33b0cdb8552433f874659010096eb476cdd53f1aae60a3`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0901b900c8978b59af02435423327f6a534ccb8c7845cbb29a5384dae163`  
		Last Modified: Mon, 10 Nov 2025 19:12:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e29527bdb49f8e4d3192c26dd3297bb4d9ac814704f1b1b036a4ba01451aaf4`  
		Last Modified: Mon, 10 Nov 2025 19:12:50 GMT  
		Size: 13.7 MB (13731885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6aa5b7b37424c8544ae0ad15e87c1d8684332e0cc97ddc07de0f48dd8ff41c`  
		Last Modified: Mon, 10 Nov 2025 19:12:48 GMT  
		Size: 224.8 KB (224760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:1806e2324b96acbebb88738b6b8b166df1bb1e5ed33fc3d94270d19bbe4e22e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3370077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de079ef3361a205d80c08112a1ea4219a2b56b6de5fd7cf0bf5f1dc12173c371`

```dockerfile
```

-	Layers:
	-	`sha256:7b64c50541a902399dcf781e21841a3b58c47822d9d9c7764224477f70c8a509`  
		Last Modified: Mon, 10 Nov 2025 21:47:22 GMT  
		Size: 3.3 MB (3346984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f42352bf8c5b27ce596145647f5e695709a124f252dbc5956b5bdf0507cb9c0`  
		Last Modified: Mon, 10 Nov 2025 21:47:23 GMT  
		Size: 23.1 KB (23093 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:df4f309c4e96c60ab9a6402436271eb72c1f562e20a05e92008730595d80245f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111967803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75c77193925671c6be068c2997926f52b1407c8150c570b1056802c47031155`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:18 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:07 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:07 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:07 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:07 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:08 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:16 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:16 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd064525dab7d3e6a55ac027c2378ea84880cb2c28cc9692d7b0bfae184d80f`  
		Last Modified: Sat, 08 Nov 2025 17:59:52 GMT  
		Size: 17.0 MB (16989345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95a28c73a7a10d2a43ad3961af1797f94b61b01ca4afe942add55b8c51928e`  
		Last Modified: Sat, 08 Nov 2025 17:59:55 GMT  
		Size: 52.1 MB (52148610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebad9b5655dfd4ccb31f9926a948528eb1eed13f62472b96d104bf32b00f8b7`  
		Last Modified: Sat, 08 Nov 2025 17:59:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c83d3140bc0663488b5277b96f30f09c76765775b653007c9573825d31d1e`  
		Last Modified: Sat, 08 Nov 2025 17:59:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012cc5cc465ced5bee967b61ef27207544c0a37a7056a698c094ed5f8a1009a5`  
		Last Modified: Mon, 10 Nov 2025 19:12:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0398f4ea24ec4ddf68db767754812138c8a076d6389db635e64583b8ff0892b0`  
		Last Modified: Mon, 10 Nov 2025 19:12:30 GMT  
		Size: 13.7 MB (13740116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a3d5ae19ab2e0477503829b7793fa5d5a65608c33707b49a31437e8bb2ba40`  
		Last Modified: Mon, 10 Nov 2025 19:12:28 GMT  
		Size: 225.4 KB (225378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:5349d522a701cbbae573ae18d12910578f16fb528253280c577cdc53452da7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3370828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d596321c77a68a1bffb6399ca75ffbb651a477ee13556c86892ba804c5396a`

```dockerfile
```

-	Layers:
	-	`sha256:7f72521b1d5ce0cc6d36521415ce118b84b400576856c74a793b2ecabd80fb7b`  
		Last Modified: Mon, 10 Nov 2025 21:47:28 GMT  
		Size: 3.3 MB (3347516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:707bea940aa5fc56a1407e8ffbbc0008ba0e00ad1d84139fe66dfec850dfa4d1`  
		Last Modified: Mon, 10 Nov 2025 21:47:29 GMT  
		Size: 23.3 KB (23312 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:b607a394fd2301e0927a1049d16c5074a8ba74b0b7ec3f0a799c0e32edce1351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120127816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1f4cea009e0d6dbfa6d1cc69939efc02f838fbd6a2d1c2b3c56eb420f17a85`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:25:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:25:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:25:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:25:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 22:11:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 22:11:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 22:11:55 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 22:11:56 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 22:11:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:11:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:11:56 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 22:11:56 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 22:11:56 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 21:20:58 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 21:21:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:21:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 21:21:08 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 21:21:08 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 21:21:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c3c84c9145d6e39b87361420c42775001b0a5d2bff0b29876f0b582e69bdbf`  
		Last Modified: Sat, 08 Nov 2025 17:54:48 GMT  
		Size: 18.8 MB (18814703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d1e85429a1b5aa90ad6f69412429b1bd9fc173b47d7b1a18825e0abe15777e`  
		Last Modified: Sat, 08 Nov 2025 18:26:39 GMT  
		Size: 53.0 MB (52985531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544a4e3fd29e30694619adf17ca3e5db38fab9fef32bcddb99bcc11432b28601`  
		Last Modified: Sat, 08 Nov 2025 18:26:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541eac08f476eb9598a98f02fff07486a7343f9ceef7c40d6e568543a260b22`  
		Last Modified: Sat, 08 Nov 2025 18:26:27 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1584a60bc161b0d42bb22f072d4c015b438e3a43c8b782e0ac7cc148115396`  
		Last Modified: Sat, 08 Nov 2025 22:12:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37883fd1bcd32b87eb4577c041337bd417d2e517df81c3b7a9478ee4afb0c7b3`  
		Last Modified: Mon, 10 Nov 2025 21:21:35 GMT  
		Size: 13.8 MB (13764732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a9a0d154214ab6042aaee9e78c2b179f776e9e4b87d4be2e020dea69a00a4`  
		Last Modified: Mon, 10 Nov 2025 21:21:34 GMT  
		Size: 256.7 KB (256680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:affd6793f9be7d07d8cd078bf3f5459ea6c75120b1bd92451c352b1f79d2cddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b8db47a01edc29c8e1341522118c906d0cd614886d81ea18c3770c997ea6b0`

```dockerfile
```

-	Layers:
	-	`sha256:156ebdeef22f91d951ccde550d21ca8c1c194bf84728cc6b6f5597327bcd4b0b`  
		Last Modified: Mon, 10 Nov 2025 21:47:33 GMT  
		Size: 3.4 MB (3351091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638c0acde75e778069ffb70bc16f00b931cbc73c165c89bc50b85e06be003437`  
		Last Modified: Mon, 10 Nov 2025 21:47:34 GMT  
		Size: 23.2 KB (23180 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:c2ebf0057eb684efe17c522706b42700d3ff413944cabff3735eb8003ad4cf81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115805218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc6cf9aeb61472754b68d8d48abadde0d7a051190d26bc5e3a83277c3640ebb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:48:30 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:48:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:48:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:48:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:49:22 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Wed, 01 Oct 2025 13:49:27 GMT
CMD ["/bin/bash"]
# Sun, 09 Nov 2025 21:55:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 09 Nov 2025 21:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 09 Nov 2025 21:55:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 09 Nov 2025 21:55:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Nov 2025 21:55:38 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sun, 09 Nov 2025 22:05:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 09 Nov 2025 22:05:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 09 Nov 2025 22:05:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 09 Nov 2025 22:05:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 05:16:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 05:16:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 05:16:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 05:16:51 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 05:16:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 05:16:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 05:16:51 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 05:16:51 GMT
ENV TOMCAT_VERSION=9.0.111
# Mon, 10 Nov 2025 05:16:51 GMT
ENV TOMCAT_SHA512=2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba
# Mon, 10 Nov 2025 05:35:10 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 05:35:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 05:35:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 05:35:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 05:35:55 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 05:35:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f168f32147322448b62f52061211b5e8d09d625fa544b55b31e5531645eb05a`  
		Last Modified: Sun, 09 Nov 2025 21:58:38 GMT  
		Size: 17.9 MB (17864334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33fb7855f09fe4f3923f030acb9ccaadd503dee15f4b3532ec753a867f4c249`  
		Last Modified: Sun, 09 Nov 2025 22:08:12 GMT  
		Size: 52.5 MB (52524121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c6ab41e357027f5eb2e4f68b92ee639c71ba6eff65996998f7e40d5e56f6c5`  
		Last Modified: Sun, 09 Nov 2025 22:08:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81644f9096133b71f864db5d2e4f8a342490ae4ece3dafaac67f83a30fbd7ca`  
		Last Modified: Sun, 09 Nov 2025 22:08:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c8082382db060e6c8de08d444ffe616de2b51718cde9dbd4d309ad913e664e`  
		Last Modified: Mon, 10 Nov 2025 05:19:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19ada71157dfa0fb441e8530c95291891bc68fe0e00deb3fe12fda92f4a8590`  
		Last Modified: Mon, 10 Nov 2025 05:37:47 GMT  
		Size: 14.2 MB (14233993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7871cd151a9f58ded664cc266ba35d85d2cc31aeac29207e8258b329e48354e9`  
		Last Modified: Mon, 10 Nov 2025 05:37:46 GMT  
		Size: 228.7 KB (228745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:f29e8a3a3d0ed59e2bdd1acdf94d76ca3951d4bc134ccf4a920a2f95ec2f9d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3362274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd677f98a88d3e0287ad055cb1f21a73c922f6dbdf96b5275a3bf243c3954b15`

```dockerfile
```

-	Layers:
	-	`sha256:16ef8248af48ccc3de990bc5b0f74de465177392f468849bb1be882af9b41582`  
		Last Modified: Mon, 10 Nov 2025 06:33:44 GMT  
		Size: 3.3 MB (3339093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36569201aa18cfa0055fa62fa65335c75feb4a7a4aaa8911e9491b4a040e1d1`  
		Last Modified: Mon, 10 Nov 2025 06:33:45 GMT  
		Size: 23.2 KB (23181 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:2846a9c8e60dbeb6147b9191c6a5e2dfc13e2e227cd585fffb45927f7e2b73c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110984783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acae6e45b6a12db6abdb0718934fd78c1b2ce3f10bdf90a22d6089525ae024a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:05 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:07 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 01 Oct 2025 13:02:07 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:22 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:12:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:12:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:12:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:12:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 21:28:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 21:28:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:28:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 21:28:22 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 21:28:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 21:28:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 21:28:22 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 21:28:22 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 21:28:22 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 23:28:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 23:28:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 23:28:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 23:28:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 23:28:55 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 23:28:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c39bab3c353e0b04d65b92f35e87c17654f9b33dfd7b7ec5b40d471bbee22e9`  
		Last Modified: Sat, 08 Nov 2025 17:54:14 GMT  
		Size: 17.6 MB (17580941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6402797e850dad1270fcc331d5c751d8b06c4f107bc52fb44c5dcf489452bb7e`  
		Last Modified: Sat, 08 Nov 2025 18:12:46 GMT  
		Size: 49.5 MB (49521894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3888de4d2a4176ac35e9ebf1546b9c2126a25ce5c85c526452a932c80ae5863d`  
		Last Modified: Sat, 08 Nov 2025 18:12:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec87eb59b13be8bc5fc51f77e89437a21d3f2e0702ac86b04b0aca5ff75bc72`  
		Last Modified: Sat, 08 Nov 2025 18:12:41 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c473ac11da34492a7aa6f5821c2d3dfe28e383768f22647373debb5119f42b1`  
		Last Modified: Sat, 08 Nov 2025 21:28:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1d41dbc3f84dc31aa974c34715765495e8267a2189233efeeb50fff1c6c89c`  
		Last Modified: Mon, 10 Nov 2025 23:29:15 GMT  
		Size: 13.7 MB (13740384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84daca4d94d8db5588ce01170e1ae367a77aa8399b10039e1c763a4448e2a6ae`  
		Last Modified: Mon, 10 Nov 2025 23:29:14 GMT  
		Size: 232.8 KB (232771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:2983b658c1bc8f1ceb00b15949fb89a325ce460948c1cbeeebcafedf35470b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df107cef9436c1bbb198e60a782e1a2bd6a8484dba5850b01c0343521821e27`

```dockerfile
```

-	Layers:
	-	`sha256:78cf2d3d93c831638f0dd0ea454d3f61984ac7fcadd341be4a94280825c61797`  
		Last Modified: Tue, 11 Nov 2025 00:35:47 GMT  
		Size: 3.3 MB (3349183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f59e10b9e120f384b890208046628db95727a775e25194aa711c38c7057566e`  
		Last Modified: Tue, 11 Nov 2025 00:35:47 GMT  
		Size: 23.1 KB (23093 bytes)  
		MIME: application/vnd.in-toto+json
