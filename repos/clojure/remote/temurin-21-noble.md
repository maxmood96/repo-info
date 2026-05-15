## `clojure:temurin-21-noble`

```console
$ docker pull clojure@sha256:c3614e72b9b5524a1d4aa2ec744bb2a5dfca1f2c476a054b931a13236ee8ab3b
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

### `clojure:temurin-21-noble` - linux; amd64

```console
$ docker pull clojure@sha256:fe1aaa28dadf8a678bc2b0d8197c4d31572ae64aa4c0c67909bf4b2217732ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266088671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8a03e3653f7e16335b0064595170709f30a126fe5887ac329bbb08edbd6cd8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Thu, 07 May 2026 23:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:55 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:00:03 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:35:54 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:54 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 14 May 2026 23:36:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117face21d4999b98333e39f0370ceccc72ca68ac796e6637469537582d5a61f`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 23.0 MB (22966995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510ce46061a4b99d147c0b3deedae89dcd096b6c3e74b533cb783d18f9bab2d6`  
		Last Modified: Fri, 08 May 2026 00:00:25 GMT  
		Size: 158.2 MB (158171738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725f3390c4115f24528fbb7be27b2f2b4fc47a10c12ea80ca4d6bbd632155e54`  
		Last Modified: Fri, 08 May 2026 00:00:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78dd6a47528af4f12330b07b6f941bbd217e6278e89ba9875a41a50def41fa`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d81f79f1a47e9b2f2f86c6d81249690450b447a827eb20b025f639e7df44e4`  
		Last Modified: Thu, 14 May 2026 23:36:21 GMT  
		Size: 55.2 MB (55213480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e8678388db911b74d6188b1e41c032667b052bbcc1376e1d7515d589c59f08`  
		Last Modified: Thu, 14 May 2026 23:36:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc533af91c3946fc8b4b61c2cb697296ce06896ddd56aa2ec6be2236e77b831`  
		Last Modified: Thu, 14 May 2026 23:36:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:c4fe7ce458481f4a727b41514b9804ecf22798e1be0ed119d7c3314c59eb84bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a7edc4e0cc6c0950501266c8d9067d29e8bcbb85140e8e00e9aa38f90205f3`

```dockerfile
```

-	Layers:
	-	`sha256:d3ecabe6264ef42deced62dfb8265769c12e8eb1b20d2961763841350281d328`  
		Last Modified: Thu, 14 May 2026 23:36:20 GMT  
		Size: 5.9 MB (5910968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f4841799db16e0bd7c7f0c1fc12c52b8a5527232a69e5a9c41e3ff9db1931f`  
		Last Modified: Thu, 14 May 2026 23:36:20 GMT  
		Size: 15.5 KB (15545 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:49e0f7fd54d221fe55d49d03184f7dc7e11445f29b66a0276962f5a889be6c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264685005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026ff4162f78526f22a89f68a2630fb26a80e15a0226e1c40ec82f86ec086612`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Thu, 07 May 2026 23:59:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:34 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:42 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:35:52 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:52 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 14 May 2026 23:36:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fa2a514a5307491f5de1145b4702ac1bbd0e4e8c13ab659b3326714f6ec4b3`  
		Last Modified: Fri, 08 May 2026 00:00:00 GMT  
		Size: 24.2 MB (24172696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce21ee5c0e78f9798c236abe913341fbf00efbf30ffc203c0d0882e4a39d6f9c`  
		Last Modified: Fri, 08 May 2026 00:00:04 GMT  
		Size: 156.5 MB (156473515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774b8a7e68a4d73adc475392932ee24fa0bffa64087021207a11e6dad3d0043`  
		Last Modified: Thu, 07 May 2026 23:59:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6c40c3516540503092334eba702c60474cf1e29c9c196eef302b94935ce434`  
		Last Modified: Thu, 07 May 2026 23:59:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60da96f5c9080f29e18f7587b3d95b2830e397446f56c991dc87679a9ec57137`  
		Last Modified: Thu, 14 May 2026 23:36:26 GMT  
		Size: 55.2 MB (55159523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b17c9a0ab6ced277157450c9c04e3c8e5856e4b64aed26985477e59aa8c5e8`  
		Last Modified: Thu, 14 May 2026 23:36:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41c69e086dc1cd850fdaaed2ff9f7b23b6e9cf45e43444a88183de9abccb0c3`  
		Last Modified: Thu, 14 May 2026 23:36:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:522bb83489ff25ef1368bd6788a61b9a09e958465f0b422267c664b26ae80620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fe70c6fdbf80a4598acc701ea5fe4691f1a4f79f3b5d6b4cbcf766babbbb9f`

```dockerfile
```

-	Layers:
	-	`sha256:ce1919d052f1cb919ace4aaf87027ce4f891673d2ee3200a4406e90fd4e7dc97`  
		Last Modified: Thu, 14 May 2026 23:36:25 GMT  
		Size: 6.0 MB (6048582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf95f789709173e7c699f68da74e8a80a5ce35c84168b96bcfe923e1de17206`  
		Last Modified: Thu, 14 May 2026 23:36:24 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:fb660762fc9592261cf0700ed57e592e9b61206e21ad6b5e41b57ac62fa1dc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277268095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431ed0b44949759b9afe0c80d184878d85d5d8804691d6d59e508b9f21da0800`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Wed, 15 Apr 2026 21:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:18:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:18:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:18:06 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:10:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:10:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:10:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:10:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:10:12 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:48:52 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:48:52 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:49:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 14 May 2026 23:49:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:49:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:49:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:49:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053e955f9e814add024b501a8f341ea40f458696ac7204b476dfa5a6086a32ec`  
		Last Modified: Wed, 15 Apr 2026 21:19:07 GMT  
		Size: 24.1 MB (24093352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23b9cce7abffcfcd9e08b905a55d1ff723d3972330c2caae990e0bb15e1a25f`  
		Last Modified: Fri, 08 May 2026 00:10:48 GMT  
		Size: 158.3 MB (158345862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957bdcd4c8d936e7298416ae4670437e1bd6d55dc002d6a748f08e27165091a3`  
		Last Modified: Fri, 08 May 2026 00:10:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa610556d07325dce3c80a698fc38d67882cbeb6339c3467e40e235f37fc42`  
		Last Modified: Fri, 08 May 2026 00:10:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916e3d7171db1e0fb1400c52ee5405637cab4c8c5f3ba50b49d4adba291846c`  
		Last Modified: Thu, 14 May 2026 23:50:02 GMT  
		Size: 60.5 MB (60511215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c7be62fb09390bda559a8db28e23b427f693b8143e7c7badd8c3ecdf7ad943`  
		Last Modified: Thu, 14 May 2026 23:49:59 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4eee17b93169e6c7560cccc840f1dcd6ecad1e9450509d18f56178a29c9e072`  
		Last Modified: Thu, 14 May 2026 23:49:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:8f1a138688f68742c080e68da76c1cecf93b7df2a46b1ab9d3b5793df205dcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5977407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04896c75e5589ad4a636844658f5afa4b5801f234e4461eabd5914b9696b0a6`

```dockerfile
```

-	Layers:
	-	`sha256:d4bb194dd8a23407018460e2814e80c72cb4434c1dbc13c303a4f1ecd032e87b`  
		Last Modified: Thu, 14 May 2026 23:50:00 GMT  
		Size: 6.0 MB (5961824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f893650d9879341aeae9eb4147a1064274b1001c1bb9fb4781f42500d61cfa9`  
		Last Modified: Thu, 14 May 2026 23:49:59 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-noble` - linux; s390x

```console
$ docker pull clojure@sha256:ae039305fb4b899401b1aef0c6f8cfb1f30f925773e51fbe4a3065120867b7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (255995912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb9f4727364d7a01a929b884c0e7ba2ab1f9d7b5ca0eab138f0cb151559985b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Fri, 08 May 2026 00:04:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:04:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:04:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:04:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:04:08 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:04:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:04:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:04:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:04:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:04:14 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:36:38 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:38 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 14 May 2026 23:37:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118eef6e5957b1aba811386b0b98175bba1b072f039fb886ff13f6a20ba0c45c`  
		Last Modified: Fri, 08 May 2026 00:04:40 GMT  
		Size: 22.1 MB (22130438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786ae644fd0e3af8f1495ba5170a43957709e10fc793b71b8d492bc5e78bd41`  
		Last Modified: Fri, 08 May 2026 00:04:43 GMT  
		Size: 147.4 MB (147398938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f5b76ec2d7c176890095ce021aad312c1c1b39e55a5e2da3821d8182a2ca`  
		Last Modified: Fri, 08 May 2026 00:04:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf33398f9906debb3129bd88100995a1c1cc7c7ed8b42aad3d24a012eaa03a54`  
		Last Modified: Fri, 08 May 2026 00:04:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0345b45822e32aba56129e8595c799a95c2f1f165ace815fb480939926bca032`  
		Last Modified: Thu, 14 May 2026 23:37:39 GMT  
		Size: 56.6 MB (56550905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064615e6adf144218bdc8782c40ed6b323f3feced68f9208328173b695c92750`  
		Last Modified: Thu, 14 May 2026 23:37:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a13cb055e1b5140e0968639f9324fe0dd15d037a285b8b1f4e904ff5ae8a38`  
		Last Modified: Thu, 14 May 2026 23:37:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:d26c4d072c72bb4687eb572ed478cb3fa9b0a078bca26a2b8fb5b005015f15c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5871860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d863ff2dae293bbdaed6f12745cb1bfdabe525c70020f70dd1a50d1284d91`

```dockerfile
```

-	Layers:
	-	`sha256:711febc32c7c900328d9a15929ff65c6725dd3579c6fb23495bb267dae97f172`  
		Last Modified: Thu, 14 May 2026 23:37:37 GMT  
		Size: 5.9 MB (5856315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60bafbe354ff4f89d5fe5ca74c11490b0e9709199e25bc4db210b9863fbea83`  
		Last Modified: Thu, 14 May 2026 23:37:37 GMT  
		Size: 15.5 KB (15545 bytes)  
		MIME: application/vnd.in-toto+json
