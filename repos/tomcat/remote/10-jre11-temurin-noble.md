## `tomcat:10-jre11-temurin-noble`

```console
$ docker pull tomcat@sha256:bf1b6c3b455aab03935280c4dd92cecb1e0e8c52263a6a423aa3a637a4012279
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

### `tomcat:10-jre11-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:30a41a627857b6b6a7a3bd5d9c5c245686646ada4baa895778f501d295299fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108598711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0222fa241e12e059716e32ffd40d2fdde2562e79062ee2de75b7e0c157f04ef1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:38:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:38:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:38:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:38:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:38:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:38:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:38:26 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:38:26 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:38:26 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:38:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:38:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:38:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:38:30 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:38:30 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:38:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf23ab6a8436ea4cc30c42c9eced3d7a9a42b066275648f8f1fbb0208b18c8fc`  
		Last Modified: Wed, 29 Apr 2026 22:45:34 GMT  
		Size: 17.0 MB (16983441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a14539c3f6df146437a21e07161e034b17f23dbe26ca23f9476c502b4c11df`  
		Last Modified: Wed, 29 Apr 2026 22:45:35 GMT  
		Size: 47.3 MB (47344091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288fd19c92924e5275f173c7e37ab77f791d263774ab4012d94aea4a7e017433`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50069af557289dad3f81803ec84242ee38d92cc0440cca83f780e8ba4d498e4f`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41311244edf0c08bf1a464bf699d81bda9b27e39ef4be4d14e19d34103e082d5`  
		Last Modified: Tue, 12 May 2026 23:38:38 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21690816e4b33f2909d221954292c702ba23fc8e01bfb9a58fcf5cbcc96b85bb`  
		Last Modified: Tue, 12 May 2026 23:38:38 GMT  
		Size: 14.3 MB (14310813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5653b2da8949f86b08cf73109ac05111a078cbf38490be519a859756773a7`  
		Last Modified: Tue, 12 May 2026 23:38:38 GMT  
		Size: 224.7 KB (224743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:6d81864c09d1dfe3adf6cf45f2b9bd900862e438f6477b5d70b44fcad8b4703b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3384692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fec8be0e2ad5efef43b34b98035db90047fa134776f95ccec0582a6fd6dec41`

```dockerfile
```

-	Layers:
	-	`sha256:188fbcc1ff1bfe928bff4e03b662a6513609d109a3be431db6e63de5634ce20d`  
		Last Modified: Tue, 12 May 2026 23:38:38 GMT  
		Size: 3.4 MB (3361580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a9a4253acc28d306de3935bdb06125a0f256fbed9801f52ced64f3ef1781fc`  
		Last Modified: Tue, 12 May 2026 23:38:37 GMT  
		Size: 23.1 KB (23112 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:8ea0f8222f90ca7cdd0e1153425e14dfd35137b7f119adb2432c067d8b9d1103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103104802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf75d92cbfe0b8027675e5b763c5bc843a292eaf0719de243b0d8cea50f27317`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:32:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:32:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:32:53 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:32:53 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:32:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:32:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:32:53 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:32:53 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:32:53 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:32:54 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:33:02 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:33:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:33:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:33:03 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:33:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3dcebaf2b2fcd539a30bc10bd91bbc7ef20caf11f1c358662e4ed783f9f102`  
		Last Modified: Wed, 29 Apr 2026 22:46:06 GMT  
		Size: 16.3 MB (16309684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f053e6426c790097075d4ca7bfd3ab90c6a6e96cdbbccf290cdb2a94445589`  
		Last Modified: Wed, 29 Apr 2026 22:46:07 GMT  
		Size: 45.5 MB (45452102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea68a1289a7d5d8edf9eded1c36c22635133ba55845322243cb20a0b0cdcdfd`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34376f25195e52a2212871c8527277aa3bcd48be13afd35392696de749a7a56`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2de0f4dc774caf63cdb1ad74adf58efca49ce3a995734a44bde6317362861f`  
		Last Modified: Tue, 12 May 2026 23:33:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f4b5440ba51ce2c3d3c8824ba0c514052f99fc01ca981688c0953d035b7d2f`  
		Last Modified: Tue, 12 May 2026 23:33:11 GMT  
		Size: 14.3 MB (14284217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdd9fb3071aba4241b2b274f56214362ce8e33b6e5fec8d81c6163352e458b5`  
		Last Modified: Tue, 12 May 2026 23:33:11 GMT  
		Size: 196.5 KB (196464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:24346e24c5da7d1716081f45816315f45aa938afb40713d3f1244e2e8a76eaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186d4d79f3bb57ec2c6f4b64d82ffb83d6573bae7a4ee617071ffbcf7b7e9043`

```dockerfile
```

-	Layers:
	-	`sha256:5a5403b20c9166f83f2a4d93488c11407f8dd2d0432901d0b40c129a15b213cc`  
		Last Modified: Tue, 12 May 2026 23:33:11 GMT  
		Size: 3.4 MB (3365223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c532534dfed5cddf9702451b06632702c32be8942d061545691416e467b464`  
		Last Modified: Tue, 12 May 2026 23:33:11 GMT  
		Size: 23.3 KB (23280 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:049153c59ff6ba8398e4899ba7af6b444ea239359cf10bb37c7278e60aa15e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106075346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065f6edadfa6ba85a8a19ea10777f173fb7ece670e05fe788e291c15cfbd417b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:38:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:38:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:38:04 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:38:04 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:38:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:38:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:38:04 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:38:04 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:38:04 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:38:04 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:38:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:38:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:38:14 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:38:14 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:38:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340297f35e2c376c99270f2485ce4edd3c92de46a0bbef95a9bce7a944b35238`  
		Last Modified: Wed, 29 Apr 2026 22:45:59 GMT  
		Size: 17.0 MB (16996253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a8f9d2e0cdee350d3ed81afb01002bf9e394770886cecaed65f94e9470854`  
		Last Modified: Wed, 29 Apr 2026 22:46:00 GMT  
		Size: 45.7 MB (45660771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8b082d384d013a651b9a297183b301e82f6a59914d0873722ee08ae517b26e`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08b5a1d9756317e6e8d13806e18cd14d78e5909594672612e96f2e3669b4f15`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493aa5207362534bdd0dfac1652655ebe93c6ed0b5e78401e3b6c0d394cc9cdf`  
		Last Modified: Tue, 12 May 2026 23:38:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a5d22d4dd273dfe7abd9f395ee68e2ac63aa41e0ac6c8c5de57dfd8b1a6b56`  
		Last Modified: Tue, 12 May 2026 23:38:23 GMT  
		Size: 14.3 MB (14314602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dfb6d7df794bb17b6ec143337a4dc71b940f33e1b0159095194ce2cc21c72c`  
		Last Modified: Tue, 12 May 2026 23:38:22 GMT  
		Size: 225.3 KB (225291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:610d1d1799a33f0df8c5a14b18427c3534d18990de87289a6fa1ccd26bab031c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3386062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03567bbba0d1e252034307ca8439156104e18c3b100e86459ac04a5256397153`

```dockerfile
```

-	Layers:
	-	`sha256:91bbb243cfbb691500fe7a4c1eeb4e7e1f804a739312f92b2350682d174acaf7`  
		Last Modified: Tue, 12 May 2026 23:38:22 GMT  
		Size: 3.4 MB (3362730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e89bbbcf142adce6529eb90fab83fcc4a7c142f2c31fecad7a15adaf0801bf1`  
		Last Modified: Tue, 12 May 2026 23:38:22 GMT  
		Size: 23.3 KB (23332 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:caa29bda26e8bccdae35f4d2f30e8618064851f85b1cce36ade5717c26510e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110529797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a411d961406eeecce2a8329299cc944c8b274eeff53b905f0e436c87628681bb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:12:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:12:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:12:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 01:22:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 01:22:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 01:22:58 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:50:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:50:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:50:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:50:22 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:50:22 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:50:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13718497a6adee31aa098ce2c85aca5feeb60aa6f13ee0ac169b2a181311f2cd`  
		Last Modified: Wed, 15 Apr 2026 21:13:20 GMT  
		Size: 18.8 MB (18813307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cb69b760c692aaca637d1f978ca71a27e8f712772ebee4f24d36075f9e119`  
		Last Modified: Wed, 29 Apr 2026 22:46:19 GMT  
		Size: 42.8 MB (42813437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f006dbd4d35f9dc4139ef666a81408417cd773080cdf49bb5876a1228c7a0`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105aa809cab5140e7f62bdbab1c9624ce547772bb7b5e7b61d334457d61a3b`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ac7edd53aaec8649090cca5b03990f58f860ea148a5da89d274fb41c41609`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74146c19d1ec8b2332ab16e01a62d0b2b1da7a847f0787c7da1456413578b802`  
		Last Modified: Tue, 12 May 2026 23:50:40 GMT  
		Size: 14.3 MB (14329566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0910a6944c8d2554660f330e8cad39d4195396b275efdd94f3473cdac2050db4`  
		Last Modified: Tue, 12 May 2026 23:50:40 GMT  
		Size: 256.7 KB (256667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:acb16a2cef756ea6fb94a01b5eba6e8e45673f8cc19104d156bb6a3ed51044e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22c28d18ec8204840a72f77dc1ceaef9caa1f0debf54aad12720b37d90122b6`

```dockerfile
```

-	Layers:
	-	`sha256:a86670dc5d0b7f6cbf6ba4e4ace6a827deee96047fdf6be7ebb4bbaeb79a2ee3`  
		Last Modified: Tue, 12 May 2026 23:50:40 GMT  
		Size: 3.4 MB (3365693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:275e698ab78ead03675d2a8e126ea5cee92e3cb336f8b558b325f65c5e2cc391`  
		Last Modified: Tue, 12 May 2026 23:50:40 GMT  
		Size: 23.2 KB (23200 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:76aa627bd709bcafcb1d93c2c225acb0f736a741d2b26cde28ce3b828b9cea29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103405324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b9b14e1d73cafda2f5afea05901ce6b00bf6cf049eec9d4b679774866309fd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:52:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:52:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:52:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_MAJOR=10
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_VERSION=10.1.55
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:43:04 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:43:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:43:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:43:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:43:19 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:43:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a3498cd625b1c7f2fe4f65685d4036d3cad9b92fdc3a7c30d047b0511431d`  
		Last Modified: Wed, 15 Apr 2026 20:44:43 GMT  
		Size: 17.6 MB (17579116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb83646d8cec7253c91045c8e0b103abc33d9faba0838653791cc13cfd2131d`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 41.4 MB (41358769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d1ad21b5f4affc0bdf817bc13bc1b05c5e24c5728fc980722be40acf096d52`  
		Last Modified: Wed, 29 Apr 2026 22:43:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a0630eea6b0c3f15ae53ad6c9f09b28ec02d6d14461bd65f1672e3066b8b8`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef363bd4cee4e70ac0af7fd7af4b7e52eeba57c7a34b82803d8b38577887af9c`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9405ec510ba729dd50c07ca4167286b4d6a1a8f61182f5143f0e502881dd6871`  
		Last Modified: Tue, 12 May 2026 23:43:45 GMT  
		Size: 14.3 MB (14319674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ef5ebf3ae77b3eba43c87c2f0f3df391d99eff99be85d6de8997819742de5`  
		Last Modified: Tue, 12 May 2026 23:43:44 GMT  
		Size: 233.0 KB (232975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:46831588aab50ec7867b3975705de5a332624d47f0f1a9e107364d0f13345c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3386897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9837870d9f5c0ae35f86947e120fdb2f9bb1f2c5a48116e15f8331ba4ed209ea`

```dockerfile
```

-	Layers:
	-	`sha256:65d0730f6893313070c21a73f5c3b091a0697326805d1ec3b920857993bdbd98`  
		Last Modified: Tue, 12 May 2026 23:43:44 GMT  
		Size: 3.4 MB (3363785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c986b774920dbab334487d758a343a00336f1aba26f05f970ef049e28b025817`  
		Last Modified: Tue, 12 May 2026 23:43:44 GMT  
		Size: 23.1 KB (23112 bytes)  
		MIME: application/vnd.in-toto+json
