## `tomcat:jre21-temurin`

```console
$ docker pull tomcat@sha256:4a544c658e8f9d8b05b44e259b45f2a94b3dca7912453d905662c69d2b1778cb
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

### `tomcat:jre21-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:ff9990a07877ca72655efb5c7118446a04c6d3e4bed2b2bf19dad4a946894e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114003823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab8088bda21f708738cebd3da05d28ae233ff8f1a3a12291728e3cf7853d505`
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
# Sat, 08 Nov 2025 19:19:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:19:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:19:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:19:59 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:19:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:59 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:19:59 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:19:59 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:19:59 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:20:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:20:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:20:05 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:20:05 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:20:05 GMT
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
	-	`sha256:ad60a30414621b37a0cf68668de64b920fa4dbf7895f8c3089e02eeed90d2ebc`  
		Last Modified: Sat, 08 Nov 2025 19:20:19 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0379014b0550e2c96941a74461b2f8ae9f80d54aa83f0d563174279e17be4025`  
		Last Modified: Sat, 08 Nov 2025 19:20:20 GMT  
		Size: 14.1 MB (14102276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b7e25a8b65b0bb33267c5df14835d93848ed5cf5fc31fade7166d895a0898`  
		Last Modified: Sat, 08 Nov 2025 19:20:19 GMT  
		Size: 224.8 KB (224779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:b60fb862698676818ab5be75071d56db62402d7e80a951a68635f606b6c8b98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5496b0135b991c4e973200afc000638a28b65de7fb82963bc95001f189523b`

```dockerfile
```

-	Layers:
	-	`sha256:d4d8d3c21a98c7903a635bc34c5d18b29117d24081c3b6267041f5791071a33d`  
		Last Modified: Sat, 08 Nov 2025 21:38:54 GMT  
		Size: 3.4 MB (3352104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c19aa1ed12102da3e4ac393e0b6b8de63efe186f93d41fbc39d490b5a73022`  
		Last Modified: Sat, 08 Nov 2025 21:38:55 GMT  
		Size: 24.0 KB (24041 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:270815ed6abea00d3645cf4f28b986b96bb592563e711139abc8603934e9402b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112331957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215e8d2485a6d35e204818d934c369f933343fd13481b264c3c55f3ada360a1a`
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
# Sat, 08 Nov 2025 19:17:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:17:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:17:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:17:15 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:17:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:17:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:17:15 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:17:15 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:17:15 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:17:15 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:17:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:17:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:17:23 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:17:23 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:17:23 GMT
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
	-	`sha256:621edbbb786928f007704e88b9bb51fafec0029787b3ee4b7968281ac825da55`  
		Last Modified: Sat, 08 Nov 2025 20:15:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561f388bf9560410d1ea3c8efb13344ce27bf0df1d7042a54fa5a0d6bb0e0ace`  
		Last Modified: Sat, 08 Nov 2025 20:15:48 GMT  
		Size: 14.1 MB (14104244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af979cbced55a201a663f94175f2bd2e85aa4d4b0d75556ffa22680db1a10ac9`  
		Last Modified: Sat, 08 Nov 2025 20:15:46 GMT  
		Size: 225.4 KB (225405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:3f05ebda7f3033e31746910a9e5d83cd8407f1e126ed7018cab5fa9b8ee570dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53e935226612509009fed28b55e88aabc052ba08b6e3cb216a5eea0a6e637aa`

```dockerfile
```

-	Layers:
	-	`sha256:c18457915dfe76fcb208571dbc2830c378831c552a7f40004c1a681eac0e467c`  
		Last Modified: Sat, 08 Nov 2025 21:38:59 GMT  
		Size: 3.4 MB (3352672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f53185341b3927c61e25a475e3f1d04fffce1861b13e003c9a136029366b79`  
		Last Modified: Sat, 08 Nov 2025 21:39:00 GMT  
		Size: 24.3 KB (24297 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:033f43e676e03ea9b06883f2c11275a789fa645ea8ed1baf1673b135c6c2aab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120479927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cdda35c4cd5ee75f884ca3a0a0ed366cc7962af6447f30ac03c2e7e8e7b9ad`
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
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 22:11:56 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 22:11:56 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 22:11:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 22:12:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 22:12:11 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 22:12:11 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 22:12:11 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 22:12:11 GMT
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
	-	`sha256:e23d2dfd96916c3d015e6a68e5a656f82c98dd28af0c9319a435e0ce8dbc7e2c`  
		Last Modified: Sat, 08 Nov 2025 22:12:42 GMT  
		Size: 14.1 MB (14116837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f25e753e3bb66891d35eef88947fe0150a73e3582863318243d1862ac98228`  
		Last Modified: Sat, 08 Nov 2025 22:12:41 GMT  
		Size: 256.7 KB (256686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:f1443818171ddcf62e16292602b9dd88bf3cac9a3e4d8ec55aee65cd36c93594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3380376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e564694453c9786921c34b1e54871f28b454468ec9fb2a2a20ea63ba191937a0`

```dockerfile
```

-	Layers:
	-	`sha256:006ee18e7523c7e9f708c882386a06b9808f871711b22cd0110fa7a370fa0366`  
		Last Modified: Sun, 09 Nov 2025 00:32:18 GMT  
		Size: 3.4 MB (3356229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89597c992650ae2ff470af8ebbcc4973d01365feb482208aa3316318423163c8`  
		Last Modified: Sun, 09 Nov 2025 00:32:19 GMT  
		Size: 24.1 KB (24147 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:273ba943b6ef5320fc3dc6fb00c893e19b8906fad7b6c9a569e80c3051e6dab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114052417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f68231137cd497d044398607e6f2fa0ace4ea80941b48afb77110a9f32dba76`
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
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
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
# Mon, 13 Oct 2025 20:03:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Oct 2025 20:03:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 20:03:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Oct 2025 20:03:28 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Oct 2025 20:03:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Oct 2025 20:03:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Oct 2025 20:03:28 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Oct 2025 20:03:28 GMT
ENV TOMCAT_VERSION=11.0.13
# Mon, 13 Oct 2025 20:03:28 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Mon, 13 Oct 2025 20:03:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Oct 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 20:03:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Oct 2025 20:03:28 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Oct 2025 20:03:28 GMT
ENTRYPOINT []
# Mon, 13 Oct 2025 20:03:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69d1272cb3efef1855d997233254d334cd7f6b8b0a0f2ba03e0e9ed69c2dcd2`  
		Last Modified: Wed, 15 Oct 2025 06:48:40 GMT  
		Size: 17.9 MB (17864533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ced9151c88ecf82bbf845d45f469f9ee70b6f5dd8a4306e95ccfc75843fde`  
		Last Modified: Wed, 15 Oct 2025 06:57:48 GMT  
		Size: 50.7 MB (50720838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd923966cfdfb49a0bb326051f16c2ac90a047f5df3ee9b28840e83cc4bf81e7`  
		Last Modified: Wed, 15 Oct 2025 06:57:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161c4db92e0a50950b95c33aa86bf1ee77f68191e00f85fe5c94f687f58ac99`  
		Last Modified: Wed, 15 Oct 2025 06:57:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045c076b50431220ff8355aa12c689cb1a81e54209ecc6cc1c9d3d97fdf3b33b`  
		Last Modified: Thu, 16 Oct 2025 11:15:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fccca8be8a44bd5ba811711d60fe87efec1eb78fb8e48fbfe2c581683a1732`  
		Last Modified: Thu, 16 Oct 2025 11:15:47 GMT  
		Size: 14.3 MB (14284284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41bccd102192904c793ca6eac4a8a2bd2b2cdfbbfd9cbe6e245c8672f05b9f6`  
		Last Modified: Thu, 16 Oct 2025 11:15:46 GMT  
		Size: 228.7 KB (228738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:70d2cfd313140c63641da70c870919923b58922d671396bbc06f7ee2b100a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3368416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99bd22d2b710ea6d8cc68c3be8f07895027324af4bd541e5acf17a3fe738223`

```dockerfile
```

-	Layers:
	-	`sha256:d40fa2d7abc11b1343ee318c515751651923b5ab6181f893b2c7ea4a7763288b`  
		Last Modified: Thu, 16 Oct 2025 14:31:27 GMT  
		Size: 3.3 MB (3344229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173160307f5bf78e35982ea970901be33445d64d365abc1501a9cbc33fc6f45f`  
		Last Modified: Thu, 16 Oct 2025 14:31:27 GMT  
		Size: 24.2 KB (24187 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:5e49833bf494dbc37f412395728b0b55053e79471ca391841984f03cc7f02076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111357752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dca69bef1e71e47b41c0d3b4b9d04fcdc3c94e573c9e15fe9c3479f216f2788`
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
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 21:28:22 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 21:28:22 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 21:28:22 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 21:28:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 21:28:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 21:28:27 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 21:28:27 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 21:28:27 GMT
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
	-	`sha256:e07f47238cea16ab624babff0c49cde57f563bfab506c74c8099e5aee0bc4924`  
		Last Modified: Sat, 08 Nov 2025 21:28:50 GMT  
		Size: 14.1 MB (14113371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114a323e2f41634bb00662a8dc14fb0289af23821bcf3b45f176a82b0df34f3`  
		Last Modified: Sat, 08 Nov 2025 21:28:49 GMT  
		Size: 232.8 KB (232753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:220870ea64cb34b55269fc85801708b8cf32bfc8a033c9f3e79298703fc51392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3378344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4863c0282d79cee4513dd845ff6154ac23fb4a5eba2675c63e7d4964708078d0`

```dockerfile
```

-	Layers:
	-	`sha256:dc3baf8ec0bed55cf627ebdc173910a84ba43c3e3f62672fb4a3d90e627d706f`  
		Last Modified: Sun, 09 Nov 2025 00:32:25 GMT  
		Size: 3.4 MB (3354303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba31d0b11a2d4a8560703bbd53113b2f599d556944b0ac312833586cc300ed0`  
		Last Modified: Sun, 09 Nov 2025 00:32:26 GMT  
		Size: 24.0 KB (24041 bytes)  
		MIME: application/vnd.in-toto+json
