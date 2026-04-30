## `clojure:temurin-11-tools-deps-1.12.4.1618-noble`

```console
$ docker pull clojure@sha256:8d08425fe01550356d8f4fa96b78e30f7da35df238ff74d43a4bfce93d75c077
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; amd64

```console
$ docker pull clojure@sha256:549afeab24e2d4581f8e73fe4465f7f1569f09b3454ee0e13350706955f262c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247798420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e60e007e7095a447101a6dc126a71f0b37e445f8bb275abbb20ce35bcc0d24c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
# Wed, 29 Apr 2026 22:45:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:04 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:45:11 GMT
CMD ["jshell"]
# Wed, 29 Apr 2026 23:15:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:10 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 29 Apr 2026 23:15:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aae374073e904edc01d2f9292c7922d131564c2ec03c7829ba6d7b18b257acf`  
		Last Modified: Wed, 29 Apr 2026 22:45:28 GMT  
		Size: 17.0 MB (16983520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999ae1941941dca10afdeab5a6dee7fd30cfee197b7624ae043b80e1091bee4e`  
		Last Modified: Wed, 29 Apr 2026 22:45:32 GMT  
		Size: 145.9 MB (145895033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d44a9a5e9c37b4b23227163ec6e698a672f53152d8bea8c07252255a8a9350`  
		Last Modified: Wed, 29 Apr 2026 22:45:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97505cf6119c72cd9319720d774fcbb74028c6e8858e6c5da45fd3a44ae59f81`  
		Last Modified: Wed, 29 Apr 2026 22:45:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4039c41dcdc6cfb68ed91ac3fad528116057a1678ce3300a442cd24dfcb7210c`  
		Last Modified: Wed, 29 Apr 2026 23:15:38 GMT  
		Size: 55.2 MB (55183799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05077d310726805d85cf067990854858f3872d7e4aebe081c9e2627294470700`  
		Last Modified: Wed, 29 Apr 2026 23:15:37 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:b14a1079695324c12f21f86f41c30058f3e6354b72774cdb3b7b0aaac33e2666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72860a8604a77f8aa8e7da101f6bc3144d1aa7f536a984b359a7e49a096d4966`

```dockerfile
```

-	Layers:
	-	`sha256:2aaf08ad314828b51d534dff39caeba6133965ba48db959502743c754d795c7d`  
		Last Modified: Wed, 29 Apr 2026 23:15:37 GMT  
		Size: 5.8 MB (5776951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faf9523538d5ddc5e76374815e79607d293213dcc823756d95af8033f8e1ff07`  
		Last Modified: Wed, 29 Apr 2026 23:15:37 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2b70b58efbb67cf9d335b5940a7a9dbd90f3d584d0c11bac6f53df2e387555a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243589941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49b7770a27f03fee236b499fb6603da8ca8029acef8ead08eb9cc9922fae72a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
# Wed, 29 Apr 2026 22:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:44:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:44:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:44:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:44:29 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:44:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:44:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:44:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:44:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:44:37 GMT
CMD ["jshell"]
# Wed, 29 Apr 2026 23:14:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:14:14 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 29 Apr 2026 23:15:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ed88568ade3d38ce7a4e9d7db04f62ed58fcc05613cda79757e2f6048ba04`  
		Last Modified: Wed, 29 Apr 2026 22:44:54 GMT  
		Size: 17.0 MB (16996212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714faa0a9aeda111c15c069b94ee97656f02d41bf80662902cfcb9b90f292ba4`  
		Last Modified: Wed, 29 Apr 2026 22:44:58 GMT  
		Size: 142.6 MB (142590522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3245a328f975ccdb30f7457480916bf5fc04847685e4b90959cd46e47c225a80`  
		Last Modified: Wed, 29 Apr 2026 22:44:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49da1ae99239d05da2927ae08b888490d348a7274597bd0c50cc688b20359ded`  
		Last Modified: Wed, 29 Apr 2026 22:44:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eaac3b6183f46ccb5420e6436f4300dbb54a5606dec95cc89cc459becbc4fc`  
		Last Modified: Wed, 29 Apr 2026 23:15:20 GMT  
		Size: 55.1 MB (55124332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf4a0acf0f8630ea0b19d8a6c49fbacdf2bc2193e74894dfd5ec8440fd78af`  
		Last Modified: Wed, 29 Apr 2026 23:15:18 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:fd58d51d3635a136ebd3f2dd831f424a20862b4dfa372591005b6f8eae82c052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5798465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdf547356a8e274178e5508f0d09676d8066a8e606677180fbcd9bf59fafd64`

```dockerfile
```

-	Layers:
	-	`sha256:adab99aa316051e357234849d4905f7a2f7b66783b9e8d4ac4a05a6b66188ffa`  
		Last Modified: Wed, 29 Apr 2026 23:15:18 GMT  
		Size: 5.8 MB (5784157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:591bd2862ec921969eec910d466744f56e9b27ace39e4f3e8b6d52c58485fedd`  
		Last Modified: Wed, 29 Apr 2026 23:15:18 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:fcd5ffa5e13e898a7296453dfb4324ef7b3f5bef1ea3cfb231b379dc90fbf168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245919196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d867539330fb5d8eda7cc0b21f58b1fda0b132544ab788cfd84e1d9e3fe5ecdf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 21:15:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:15:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:15:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:15:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:15:37 GMT
CMD ["jshell"]
# Thu, 16 Apr 2026 02:41:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:41:00 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:46:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 16 Apr 2026 02:46:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:46:18 GMT
CMD ["clj"]
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
	-	`sha256:13e6d27d6213cbcf3ad98189ecd1637a3352d6613a6cbc6bc2ae299ba97403b0`  
		Last Modified: Wed, 15 Apr 2026 21:16:18 GMT  
		Size: 133.0 MB (133004805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8fdbc23e7600c67f69257086df388953e624b8375745b1e759f5a3c14cd22d`  
		Last Modified: Wed, 15 Apr 2026 21:16:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59078c7d1c4b7fa9f9cca0e00b180c88531bbc38947269e03c5bf1913507759`  
		Last Modified: Wed, 15 Apr 2026 21:16:15 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1df867617f4b67bef1e8381badf8e94a13bd32124ee70f5ea216c13308cbb6`  
		Last Modified: Thu, 16 Apr 2026 02:46:51 GMT  
		Size: 59.8 MB (59783822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d0cf8289c24755531e137e3b7f0975bbe2291ad7a7c72569d6fcac205cbd57`  
		Last Modified: Thu, 16 Apr 2026 02:46:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:82e10930268f02cdff2de94db68f517e591ff06c9e65b0e37acea84988b5d281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc241949e07442ec627a54b1974ead3117e16f988605c37251c0c299824547f1`

```dockerfile
```

-	Layers:
	-	`sha256:204ef1aa99085cabe987725e1651687769eced9e91d7f64a7f00b7a629434b65`  
		Last Modified: Thu, 16 Apr 2026 02:46:49 GMT  
		Size: 5.8 MB (5780143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f173c443a9e8a93e2bdaac0492a1ea863d7110cc2883bf4fd6382e5241c85da`  
		Last Modified: Thu, 16 Apr 2026 02:46:49 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; s390x

```console
$ docker pull clojure@sha256:0e5660eab8a7cd20873589f2fee05579e46ea81c2daf4494df97b130d00a2e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230678408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25db4aef8f288c4c886a904814d3abe88f3b7638d24d6f313e46f5127e710297`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
# Wed, 29 Apr 2026 22:42:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:42:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:42:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:42:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:42:50 GMT
CMD ["jshell"]
# Wed, 29 Apr 2026 23:15:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:11 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 29 Apr 2026 23:15:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:28 GMT
CMD ["clj"]
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
	-	`sha256:0ef965a4a0b0c71b28aa2044116369b7311b3195121f17456fb6de0fb5e60818`  
		Last Modified: Wed, 29 Apr 2026 22:43:15 GMT  
		Size: 126.7 MB (126662744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03b0c44fb975cc61e445ce5116a6206d7888a14e2f0427118d1f5c8523734d1`  
		Last Modified: Wed, 29 Apr 2026 22:43:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcd567fda8aa28aea61e97101d6ed13cc425a81d115f18827bb0b1a1f1c2a06`  
		Last Modified: Wed, 29 Apr 2026 22:43:12 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57060d2a40ffc92b853ee91441ffe854c007c617ecaf4ab06178c033ce5bd1b`  
		Last Modified: Wed, 29 Apr 2026 23:15:50 GMT  
		Size: 56.5 MB (56521312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb4cd9384c77818993c33a69dc83c605aae29d625d385b4a0ee6efacd246de1`  
		Last Modified: Wed, 29 Apr 2026 23:15:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:2208fbff25cce518fdb0850cf484e8cb7b5f357415217c49b87d3f6f387a705e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5788482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7637d9b93ea8a4399c553729a31732bedea6bf4fd36f8575dac24a616a000b89`

```dockerfile
```

-	Layers:
	-	`sha256:f295567e5bb6f6c3c20711d477c507680f9f69c7518ab66ccce9d429242a6b44`  
		Last Modified: Wed, 29 Apr 2026 23:15:49 GMT  
		Size: 5.8 MB (5774291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:605e75fabbe828317e288ff3340a4fb632d7052625ed76e3c4973ce4aa3c05e1`  
		Last Modified: Wed, 29 Apr 2026 23:15:48 GMT  
		Size: 14.2 KB (14191 bytes)  
		MIME: application/vnd.in-toto+json
