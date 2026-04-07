## `clojure:temurin-11-tools-deps-1.12.4.1618-noble`

```console
$ docker pull clojure@sha256:1830e8aa163b2b3d544e9bed7f4c7e40972bbc9b7c62143f2edb2964445fecc5
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
$ docker pull clojure@sha256:0c9e04d0b5efe5c62978dd0ce889b5f7b066e4035fe8dca29b49fd2cad5769e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247694487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd989b9a06fea453defbe12e52fc2c91af1fb870e050dfa3bd977c40a68cee3b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:36 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 07 Apr 2026 01:51:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:51:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:51:43 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 03:13:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:13:56 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 03:14:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:14:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b8205a7f54e5e07f983b04fa097bc66871456a6dce9e39f9d67c12bea02a19`  
		Last Modified: Tue, 07 Apr 2026 01:51:59 GMT  
		Size: 17.0 MB (16983584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9fd154034df3a181ea45c6747976a66b7d291d091bc5b8024cf9d9fba0dfc8`  
		Last Modified: Tue, 07 Apr 2026 01:52:02 GMT  
		Size: 145.8 MB (145819399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512b2237d8ef417956fc23edb0c480ef2b903ed160de6daf18d73e2bf0e4bebf`  
		Last Modified: Tue, 07 Apr 2026 01:51:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d4139f1af20e46863c7ed02e7e81234536ea4c5d23ca4f5fa8d8bf53c70e10`  
		Last Modified: Tue, 07 Apr 2026 01:51:58 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f93505fbbe8af58e1e995b94439b4141ca7468a5fe2c0beebf72457433f0cf`  
		Last Modified: Tue, 07 Apr 2026 03:14:29 GMT  
		Size: 55.2 MB (55154957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5e341f6d9c567016b40334b1e67192fbbdb67f8666f67d6816eb9f08223af5`  
		Last Modified: Tue, 07 Apr 2026 03:14:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:b3858dd4b1cbf8648d1c098b1ad99ec2ac14cd50202c229c6530ef7aae1b915c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1f05c972abd2b03378b5dd110f65f87b8ffab1e73a6943ffeda6ec79459b0d`

```dockerfile
```

-	Layers:
	-	`sha256:946be60d2109799fae9b88a56c5c31849daf7d891c7bf71fac1bf518457006c7`  
		Last Modified: Tue, 07 Apr 2026 03:14:27 GMT  
		Size: 5.8 MB (5775513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb4683980e49878d860d3591ffb24d5bdd728474e77fdd2aa0b4c6098ae4b44`  
		Last Modified: Tue, 07 Apr 2026 03:14:27 GMT  
		Size: 14.2 KB (14191 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:09bb663dd1ec2328692b44c112c1735c917821d504970f21a4a8473ec49702ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243488765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df147d11be0ec7578764e42b229d45b6c2aee236c31537ed323f6574efe7ea4d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:53 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 07 Apr 2026 01:54:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:55:00 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 03:24:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:24:42 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 03:25:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:25:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2198206947f45bb622b27a53d2b539eb3183e604dc967d6460858f154e001e04`  
		Last Modified: Tue, 07 Apr 2026 01:55:17 GMT  
		Size: 17.0 MB (16996221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e367798191faf034264f5134128f989d7255510209adca9be9294666694d9fc`  
		Last Modified: Tue, 07 Apr 2026 01:55:20 GMT  
		Size: 142.5 MB (142513602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2775b62842c2f8e2bbae6790a5c9ceefbe01b9ffe41a5065f66f8c4d0282bb8b`  
		Last Modified: Tue, 07 Apr 2026 01:55:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2250a891790b16484887e97a864b09f25d8a1205ca0a43dc2fade3e325af7`  
		Last Modified: Tue, 07 Apr 2026 01:55:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc0a9cb655480f06c31ec6d9d20a46d734f5208011ecb74cf8a51ec0f97e946`  
		Last Modified: Tue, 07 Apr 2026 03:25:18 GMT  
		Size: 55.1 MB (55101780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a719c725dc943c91ca05c2d499d1a776583abd910a0967ab566b8e3cfcc4ed3b`  
		Last Modified: Tue, 07 Apr 2026 03:25:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:c9cb67010bdf28d8d0820590542d987b0d313e17225b6424ec55c4d979cea85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8f046ee7e13b0443639f78460d70aa04f995e0eac3d7ff50e1506ebf550885`

```dockerfile
```

-	Layers:
	-	`sha256:87f5878b36134602ad283fbd14bd1cc822bc2ce41e44cbde68f3a4818470cd1b`  
		Last Modified: Tue, 07 Apr 2026 03:25:16 GMT  
		Size: 5.8 MB (5782719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21a02dfbbd0a15a8863d45571f9550c7ed84860df035fd839c9df8dc12ccecc`  
		Last Modified: Tue, 07 Apr 2026 03:25:16 GMT  
		Size: 14.3 KB (14306 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:0eb2f4c1c7d7005eadaf6834879a466552a50a9c99668ab6267c5ea96a167539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245913600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f1f813ec3cfc9ca57204938358ebde3d906720c0ef782041ac85e8447da7b3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:29:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:29:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:29:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:29:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:29:49 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Mar 2026 08:31:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:31:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:31:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:31:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 08:31:06 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 18:17:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:17:17 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:22:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 18:22:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:22:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c602d6d5b3bff268e7b1f1815099c69255c8fca8953f0d22e169ed8acd2c409c`  
		Last Modified: Tue, 17 Mar 2026 08:30:26 GMT  
		Size: 18.8 MB (18813047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ded87fc84e78541b310e12b114a5b0e8d3f9ecd276b768acf3f06f9d1617d8`  
		Last Modified: Tue, 17 Mar 2026 08:31:48 GMT  
		Size: 133.0 MB (133004271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2ce04d9b6cfba06e611c0632ffb3c9a8035d84d07f4cce2fef3788f2573a6`  
		Last Modified: Tue, 17 Mar 2026 08:31:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8c3b7c60c462232368e702a32d1aa3fc185c931c52b0e3822ca0930b153544`  
		Last Modified: Tue, 17 Mar 2026 08:31:45 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e3572f148021523ef86bd1c36c54da90ecf6989a3dd07f14faf2465a1dcfc9`  
		Last Modified: Tue, 17 Mar 2026 18:22:58 GMT  
		Size: 59.8 MB (59783140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99a63a4e14ccd462a9754a7ea0e1a7a2ffdbb469692f8f8d5ea2971a9e2ca44`  
		Last Modified: Tue, 17 Mar 2026 18:22:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:755fb69d4935719bca05f530758c508c332e08cba3c182769611ac32dfcaf8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2777cffed1565122da272f503f6b4edbe88061206c894c90ef085c091431e9dd`

```dockerfile
```

-	Layers:
	-	`sha256:b3a7f285e3ffd39367b13c4b00448510dfea03cb4ab183987a2a91a8905ee50e`  
		Last Modified: Tue, 17 Mar 2026 18:22:56 GMT  
		Size: 5.8 MB (5780143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4555be162ab9d82e213829e5c25278dce7a43b22223d3b250d9885d8b08a98`  
		Last Modified: Tue, 17 Mar 2026 18:22:56 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; s390x

```console
$ docker pull clojure@sha256:0c3952573981bc74115bf7c2761826c912397e552c6f0f04401111dd01d6a503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230578399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1650712fbbfa9fa8520aabcee001ce7665027cb2d56d87c0661b2861e6accc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:09:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:09:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:09:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:09:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:23 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 07 Apr 2026 03:09:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 03:09:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 03:09:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:28 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:39:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:39:16 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:41:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 05:41:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:41:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafd1916c5cba31aaa22e1e52aa83c9c76d6979e0d05bbd0bccbd399520dd951`  
		Last Modified: Tue, 07 Apr 2026 03:09:52 GMT  
		Size: 17.6 MB (17579082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b6b54faf1d0b905618d6c72981d0b30b7342ea2dde4805dc122eff6b8174b`  
		Last Modified: Tue, 07 Apr 2026 03:09:54 GMT  
		Size: 126.6 MB (126566100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b4944bffc81c057fa6031b471300cb088996165b8c0ae0219dde861cab1abb`  
		Last Modified: Tue, 07 Apr 2026 03:09:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69899eb0c6daeaca16e7d61f72a2166b79ad0def7c9347df5ee9c033b2b7d5`  
		Last Modified: Tue, 07 Apr 2026 03:09:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80e7d1f6f67e5f8d9d7ecf08f3fc408d4b480b7743ff089333587b4d4775fa6`  
		Last Modified: Tue, 07 Apr 2026 05:41:32 GMT  
		Size: 56.5 MB (56518289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f9c37b18ea8d2a624103ccb481bc92d7d0bd6d556333ce54b4be9d9227c1e`  
		Last Modified: Tue, 07 Apr 2026 05:41:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:d37d1ef57fce1edd7d817122c13f478e00a9654e61e1b1544ebf0617c40bc2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5787044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000b7fa152ede1501a611a794067eac32c72139bf45e1cc6755ac93d6cb9985b`

```dockerfile
```

-	Layers:
	-	`sha256:073f21a4ec4d3c3bc1f39e0d8d9ceb180d8955f29df5a59514cecac9fd606d67`  
		Last Modified: Tue, 07 Apr 2026 05:41:31 GMT  
		Size: 5.8 MB (5772853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9341518daaab3829f5597eb8f4345d0776a2ca206d0f1088c5dc3bff3e6ba618`  
		Last Modified: Tue, 07 Apr 2026 05:41:30 GMT  
		Size: 14.2 KB (14191 bytes)  
		MIME: application/vnd.in-toto+json
