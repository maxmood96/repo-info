## `clojure:temurin-11-tools-deps-noble`

```console
$ docker pull clojure@sha256:ba72bdae33e701f3bc163c2d0f86b9ddee809b31bcb101134c9df6cc4adc5f91
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

### `clojure:temurin-11-tools-deps-noble` - linux; amd64

```console
$ docker pull clojure@sha256:6d3932198b3e3ad6306538c71c969fdf80fe697d1c6f0a7aa6cd7dd4aa2670d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248382075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf35bef9decec6a735e9bd6cb4cfc4528dda8a6b3a3ae15a39113cee870e7327`
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
# Thu, 14 May 2026 23:34:28 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:28 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 14 May 2026 23:34:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:39 GMT
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
	-	`sha256:175373278c643af449f94b46712760edc9f8d31bc22f3e11159b2ecf7b6279c1`  
		Last Modified: Thu, 14 May 2026 23:34:56 GMT  
		Size: 55.8 MB (55767454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271c6dd419b6b23b52dda7baa29a90197571f4086eb91441982502355f4976f0`  
		Last Modified: Thu, 14 May 2026 23:34:54 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:6a7ef9a3486f72369bc2110aada45614343df76b9c7c94314f6215c04605f347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626a3d6f03c5a3da88af74df09674ecca4b088a875b508f3d2b05d263bbef7e1`

```dockerfile
```

-	Layers:
	-	`sha256:12fde9c113e0c1a6fb389301a0067b2d9e3a4d996ca3680cc80eda954e5d2141`  
		Last Modified: Thu, 14 May 2026 23:34:55 GMT  
		Size: 5.8 MB (5776949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a46650d4087539e869bfe41dbbc35ff9969d1d221121b8127b5c687fd1843f`  
		Last Modified: Thu, 14 May 2026 23:34:54 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e4172fba3cf42a4b7adbf05d229764defd5aafa6e8d0ac66a8f3fa735c06a1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244168610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206d93d1825b280b9e033904314002701fecd66e1e3056613f21f8adf97024ac`
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
# Thu, 14 May 2026 23:34:19 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:19 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 14 May 2026 23:34:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:42 GMT
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
	-	`sha256:0e28756eb0ecd8cd14c5f2511797db3ab8f045fa19f09694e326d44edbfc4eb2`  
		Last Modified: Thu, 14 May 2026 23:34:58 GMT  
		Size: 55.7 MB (55703001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed42b7e9a6d4d58092b49366c846f8db8105a6f2adccac1ff92fc891d2ee798`  
		Last Modified: Thu, 14 May 2026 23:34:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:f1f3cd0b81cfc11702841d8100e19b0924daee0a7c54b9dffbb9293cf05ac5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5798463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d886995751f603e9eafae5a2dfe9019fa187e0fb3877ca0084820e3339ca6`

```dockerfile
```

-	Layers:
	-	`sha256:cbc354864e9e817b624f9842166d625b19b56f8ea7b28b9a3c806f3709b296df`  
		Last Modified: Thu, 14 May 2026 23:34:57 GMT  
		Size: 5.8 MB (5784155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc35af1f69030f35074c452acf779fa78c0597ea5214c28b844b491210d21bd`  
		Last Modified: Thu, 14 May 2026 23:34:56 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:124e6777673a72933740ea4876a2d52a4d31705f4a27b0b937ce7d6fb0378b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246760765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6395ab4ac1bc22872d6a0250355ca1e174539b02da6d7930c822215004427231`
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
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:43:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:43:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:43:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:43:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:43:24 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:39:48 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:39:48 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:40:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 14 May 2026 23:40:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:40:18 GMT
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
	-	`sha256:5fbb8143246c70f36b105023da28678c8f97774e64cde3f61ea0b17955dbf0ce`  
		Last Modified: Wed, 29 Apr 2026 22:44:11 GMT  
		Size: 133.1 MB (133122289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e9c6bdbd97e88855dd1ec32bf0ffb119ed132a0688a5b924b6882211884e74`  
		Last Modified: Wed, 29 Apr 2026 22:44:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1e9e32c5c1f0a02f57bc56765ca372c03a79789b4cd818fffe2260d0efd831`  
		Last Modified: Wed, 29 Apr 2026 22:44:07 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dac7577134d9145e6c3553fedde91200cbeeb96e641879ec7ef17ec9c25291`  
		Last Modified: Thu, 14 May 2026 23:40:50 GMT  
		Size: 60.5 MB (60507899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04366b38717aaff98d446e617c6008fe5b17ff1dd26a39a20d27ff9f9e34015d`  
		Last Modified: Thu, 14 May 2026 23:40:48 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:464112f681999d991f7cd4c726dca6f11cd08c927861cd03274727a36661d74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2856b29f5ba66e9f0b927c98666c281256cfa3473a3686563b2dfd580c8289e0`

```dockerfile
```

-	Layers:
	-	`sha256:9eb82aeee5f8bb1db59ae21a3afc95dc038e3cf2f6864f733fab38d08bade23f`  
		Last Modified: Thu, 14 May 2026 23:40:48 GMT  
		Size: 5.8 MB (5781579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1031be4a0268a915e8675b8705421e2b5ddafe047b449d31ba0cf51f30e90b6a`  
		Last Modified: Thu, 14 May 2026 23:40:48 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-noble` - linux; s390x

```console
$ docker pull clojure@sha256:aa2a876e11877824cb114f5b689660a251fe816e837bc96592cf7e60d7253bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231293218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da908a7f405d017befbf9d81a78ce8ba79f5eebd901890dadcaf0291bf4af1bb`
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
# Thu, 14 May 2026 23:33:33 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:33 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 14 May 2026 23:34:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:07 GMT
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
	-	`sha256:e6d69c42fc7c79284e9fff1b43b08888b985470f600b5e0fa4af4526216173f1`  
		Last Modified: Thu, 14 May 2026 23:34:30 GMT  
		Size: 57.1 MB (57136122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240c2c302bed37e1bad5adf8eb0143612fb0c0242a09463d5212d5b79f2d677d`  
		Last Modified: Thu, 14 May 2026 23:34:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:2acb751c0405c4decd0ebc0414f8d2d67cb91a2143816c64f0023ec865584b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5788480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9198bf85980cd0776c82ae95d80bf796a120bb0a9f2cb0fc2928c22441eb980`

```dockerfile
```

-	Layers:
	-	`sha256:5e322069dc396fe5678458566a032b5b650190cf80337f2f09ad0f5d4868b72f`  
		Last Modified: Thu, 14 May 2026 23:34:29 GMT  
		Size: 5.8 MB (5774289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7f9578ffb705da79a783e9cb7a9966c9dfdbdc518d81f084c5c908cad75ef2`  
		Last Modified: Thu, 14 May 2026 23:34:29 GMT  
		Size: 14.2 KB (14191 bytes)  
		MIME: application/vnd.in-toto+json
