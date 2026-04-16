## `clojure:temurin-17-tools-deps-noble`

```console
$ docker pull clojure@sha256:f1dac2081acb29a0cda012b0cb0512d764a9a6ef44922645560b36a2fa9e4d5d
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

### `clojure:temurin-17-tools-deps-noble` - linux; amd64

```console
$ docker pull clojure@sha256:99c9b1659e8d2073c798e3a80d985e83f3e0159221525dfea3046ea056428246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253495411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841b61546c7b147d76bd461c0a9d1f9a7c8a56b9b320e8ef1025efd321f00385`
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
# Wed, 15 Apr 2026 20:33:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:38 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:46 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:04:15 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:15 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 15 Apr 2026 22:04:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dbd4bf6df60adadc649324ed935bca4d910519f68acf374ab030c3c9cb3048`  
		Last Modified: Wed, 15 Apr 2026 20:34:03 GMT  
		Size: 23.0 MB (22965417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f3fd0f1c2176e779aabd80195ebcf9b908f943622f8d916931360b0cbf665b`  
		Last Modified: Wed, 15 Apr 2026 20:34:06 GMT  
		Size: 145.6 MB (145633837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f907e7b2d67743a675319ea202651b65dc9b515430be6018c6fd18bf88461f64`  
		Last Modified: Wed, 15 Apr 2026 20:34:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286cf14499d5b0f1da8709959ce97f11188bd32cbb5b46a0892214ccdfc88861`  
		Last Modified: Wed, 15 Apr 2026 20:34:02 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a73f3bb82d6ae412f9f66efb949f8a3570382911933ea7629aee6bad00a622`  
		Last Modified: Wed, 15 Apr 2026 22:04:44 GMT  
		Size: 55.2 MB (55159692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c56fd210ed260a92edee50612819192db4679d5fa6fb69a69ffd6694245dce1`  
		Last Modified: Wed, 15 Apr 2026 22:04:42 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc84fb8f2211aa0ef7a8b83f452af2aed57f47e259a970754ea293e74ca7107d`  
		Last Modified: Wed, 15 Apr 2026 22:04:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:a2794113ae13733bb3db81aed29610b43639bf41e037c68b734ed048959d39a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddb0d2c9f753e2e8a9c596b42d5a84f252dc32a3b67ec7b90645d02990c19b2`

```dockerfile
```

-	Layers:
	-	`sha256:7a13a303ae2c5f77ead47c2f5975a6701ca0e514bccf4cd677d47704a69bff73`  
		Last Modified: Wed, 15 Apr 2026 22:04:43 GMT  
		Size: 5.9 MB (5907739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce157098c4f12a5fc881b3b0363d6e9b137fcae35185a32b98da909420ea6533`  
		Last Modified: Wed, 15 Apr 2026 22:04:42 GMT  
		Size: 16.2 KB (16228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6a12d4fd71e2baf4d381ce5d41de8c7eb97d6372384923422530f2af88f3103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252598424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849fda5973866810d1deebce270f7e750ba2ed8789bb1e531bd05a875ede90bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Tue, 07 Apr 2026 01:55:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:55:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:55:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:55:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:55:05 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 01:55:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:55:13 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 03:25:15 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:15 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 03:26:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:26:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e985483d507882b395fa9bb8502182df64b567111ba163105e4e78a8d82c722`  
		Last Modified: Tue, 07 Apr 2026 01:55:30 GMT  
		Size: 24.2 MB (24171221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cae6e26c9a9b0d927c08ce6052f557fbaa85c2077ab4a22f51846260528f7`  
		Last Modified: Tue, 07 Apr 2026 01:55:32 GMT  
		Size: 144.4 MB (144444005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8606cc4933ad0b03f2864748c68cfe3334622c4272c911a96572d71f63064`  
		Last Modified: Tue, 07 Apr 2026 01:55:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec83fb152f23fdcfc782e44dc3257b4fa3dfa349c36f4b978f9fb2dacfa4abc8`  
		Last Modified: Tue, 07 Apr 2026 01:55:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a450b75a5a3c8a731c23be45d47a61198984857ef08d782af3043cd3df8f4e`  
		Last Modified: Tue, 07 Apr 2026 03:26:25 GMT  
		Size: 55.1 MB (55105636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccae612de2d87a6a98a1bf08e5f65b4a8a3cefeea5f875fa4c690a0dc279f46`  
		Last Modified: Tue, 07 Apr 2026 03:26:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837595c48aefd1a7b0a446881b4121474c5f3de3b600d02b7d4ff3b6240c1bfc`  
		Last Modified: Tue, 07 Apr 2026 03:26:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:25716ed61e1cf22b2012fb46aa5b765573d721906012954b1b4b42b6eecdf748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6061721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ec6af766f075b2304c750a395ebe1bf496b970dd6315cb38af352caafaa3a4`

```dockerfile
```

-	Layers:
	-	`sha256:3fdc5f56a5cc77515654ddb4936ec0d2ceeed624389ebe0a95b789226705e3b2`  
		Last Modified: Tue, 07 Apr 2026 03:26:24 GMT  
		Size: 6.0 MB (6045377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f0df1b30588cbdef9cb2b99f19d1b3be36ccd08e1a9b0847b7293469b19f1b`  
		Last Modified: Tue, 07 Apr 2026 03:26:23 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:0d307746295e41b13878c5492607ff118a4cc7da15f24327b8265fdc22af27d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263639423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59c02106d2c80e33cdfd1248029cfcf49ca18f78983b789edffe3d4632f7673`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 04:30:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 04:30:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:30:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 04:30:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:30:08 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 04:30:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 04:30:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 04:30:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:30:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:30:29 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 14:38:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:38:39 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:43:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 14:43:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:43:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:43:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:43:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb69da8bc15c0a11682f0906f2e84b672591fc9ed3e7de40c3263c178cfd38`  
		Last Modified: Tue, 07 Apr 2026 04:31:03 GMT  
		Size: 24.1 MB (24093111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0751806b983367e1b69302b4a8844029c65878e0479bd95ab0736ddaa5743f05`  
		Last Modified: Tue, 07 Apr 2026 04:31:06 GMT  
		Size: 145.4 MB (145442153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee430c280fe9675b85d025ec19ae8d0b8b3a5671f60348b58a9f3908173b7c2`  
		Last Modified: Tue, 07 Apr 2026 04:31:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122adcba4fd6dccca3b9beb417390082947480ea7e3fade42b157e971125308a`  
		Last Modified: Tue, 07 Apr 2026 04:31:02 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc0e57e0ec5fbba4fe21c012f433a7e05a0276cfb94a7213581781e324f17f5`  
		Last Modified: Tue, 07 Apr 2026 14:44:03 GMT  
		Size: 59.8 MB (59787341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c45a2eab029bb19a3f1f8055f4d9124dd71faa7f7deb6c21e67c9f22cfc71d`  
		Last Modified: Tue, 07 Apr 2026 14:44:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a725af6502e9aac82ece82699a916837d74655257e42b80a6b0e1ec73b002ba`  
		Last Modified: Tue, 07 Apr 2026 14:44:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:d06a4b6b0ddcad5e2b4ee586e466bdbb138b98a33e6dedba1c4abc45fe896add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5974885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdaac0430d71215175b77547558b649e79f40f1cbbd2928f67b7422e9c8d7ac`

```dockerfile
```

-	Layers:
	-	`sha256:5e414be46cb711f72bc6ae1f16db8f1c34df538764793ccb1ebe3c9ec8175c99`  
		Last Modified: Tue, 07 Apr 2026 14:44:01 GMT  
		Size: 6.0 MB (5958607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23540e37db1f1f3085d517910b85b718b849812979e2ec3487c03588124ebf2b`  
		Last Modified: Tue, 07 Apr 2026 14:44:00 GMT  
		Size: 16.3 KB (16278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-noble` - linux; riscv64

```console
$ docker pull clojure@sha256:7ead42e9075bcf41407dea1662b7567fb247786f9a8913cce00af2b5d3a73a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259408012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7fa378a2f1ec3c47a283a2d07baabf55a5dc61ea253bbbb1b0ba9836a57d94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:35:32 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:35:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:35:33 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:36:09 GMT
ADD file:59e78909d1b1cd9a524f68d8ff44bb077ea09f4f39da5e046d635b48da9d33bf in / 
# Fri, 03 Apr 2026 15:36:13 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 02:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 02:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 02:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 09 Apr 2026 02:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 02:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 09 Apr 2026 02:12:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 09 Apr 2026 02:12:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 09 Apr 2026 02:12:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 09 Apr 2026 02:12:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 09 Apr 2026 02:12:14 GMT
CMD ["jshell"]
# Sat, 11 Apr 2026 21:11:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 11 Apr 2026 21:11:16 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 21:30:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sat, 11 Apr 2026 21:30:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 11 Apr 2026 21:30:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 21:30:23 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 21:30:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23ef52cbd4674ce4f8269086177a6a1fc3abbc052567212551b8169743067808`  
		Last Modified: Fri, 03 Apr 2026 15:56:59 GMT  
		Size: 31.0 MB (30963791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd6942c5ca1b5297223819bdcd4483eaaa83528d81c0895b5729ce9bff4d8f0`  
		Last Modified: Thu, 09 Apr 2026 02:16:00 GMT  
		Size: 22.3 MB (22267147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760a9aa81189b8f89a995cbec6573a2cca971c78829b7f01729489a6c434855f`  
		Last Modified: Thu, 09 Apr 2026 02:16:17 GMT  
		Size: 142.7 MB (142673727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8afb15f0bf5a42cc1bfd95b8fb518321f2bc664afbbf9359f2713493c85ce8d`  
		Last Modified: Thu, 09 Apr 2026 02:15:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febfc132a2c45d18ac2a01289326a36d48e9ce6eeee639136a994d0f6446aa9c`  
		Last Modified: Thu, 09 Apr 2026 02:15:53 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e75515bece2a237f68a13dd5a9f8a4de4e6f944be04190adbb9bb4c6bcfee7`  
		Last Modified: Sat, 11 Apr 2026 21:34:10 GMT  
		Size: 63.5 MB (63499856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d85fc16b6a9da256ef68df4c9e0b0b3c63326464ecee500386f4a3e7e7a6112`  
		Last Modified: Sat, 11 Apr 2026 21:34:00 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d197d435081f4588dec23da098b616a2e1242cda4587388073ddeb2eccfa20`  
		Last Modified: Sat, 11 Apr 2026 21:34:00 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:aef6bfde20d569ffa48ec2db97c4e942fdfff7c9f167e1d8d59445ec5b11555a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4dac94dd0167ba6d4d25bdb75db9cb8d8169d755c693613e05643da3d3f341`

```dockerfile
```

-	Layers:
	-	`sha256:1265aa568ca1c883316954db392a6a6546f42b60276de2521b52b2cb8fd223ec`  
		Last Modified: Sat, 11 Apr 2026 21:34:01 GMT  
		Size: 6.0 MB (6009541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eccb41cf2e52a014af3f9dc87c4dd726622a8bcf0be61a7b741e6e516fb6063`  
		Last Modified: Sat, 11 Apr 2026 21:34:00 GMT  
		Size: 16.3 KB (16278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-noble` - linux; s390x

```console
$ docker pull clojure@sha256:83be917c9895fe142688bf51d78fac2d2aa81ae665ab7b4513a596f32530ced6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244195212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34491b13cc8261d43bce7b490e4068bafa9d478f31dadcd0354749ab12ad3d20`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Tue, 07 Apr 2026 03:09:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:09:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:09:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:09:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 03:09:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:38 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:43:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:43:21 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:43:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 05:43:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:43:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:43:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:43:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f58d1092e2c2c340321a8297fc8bee6b44f6de56771a16f20395b432a9bd42f`  
		Last Modified: Tue, 07 Apr 2026 03:10:02 GMT  
		Size: 22.1 MB (22127181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cab1876529a2c46d4c5ff9373dca1be01d5b09a9481d774d4c1678f9939c810`  
		Last Modified: Tue, 07 Apr 2026 03:10:04 GMT  
		Size: 135.6 MB (135631395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26556adc0a7bc4a73104e7711f4587b4972c0d6615a86c57bd254a456c7d02ed`  
		Last Modified: Tue, 07 Apr 2026 03:10:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c2c4f36a6cc4f63b88685ec7c3bc548e5eccbbb502670e37c90b8b3c4336be`  
		Last Modified: Tue, 07 Apr 2026 03:10:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1a1d63f4bdba581b9060d7927bbcc879cb37c659dce8e3dab149329116c468`  
		Last Modified: Tue, 07 Apr 2026 05:44:00 GMT  
		Size: 56.5 MB (56521308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e130ae938d9f94cb3d74bce5206e8987efac1f524019b34063ae46591698ae01`  
		Last Modified: Tue, 07 Apr 2026 05:43:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbf9747a8f0aa7f5bade6fe88a07b33b4d09fd18bd8734b2d21e1519a401faa`  
		Last Modified: Tue, 07 Apr 2026 05:43:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:dd34be99173e4eba3c0119b119cc7050fd88c82596b3686c9a3b1ede14455e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42054b3c449ca95d1056e10eb4861c6542993fc4a011ba7059a3c9caf16ba851`

```dockerfile
```

-	Layers:
	-	`sha256:efd8e1b98bd814fb0302c62bb6746dfcb725d2cdfbdc214a1179353e715a4ab3`  
		Last Modified: Tue, 07 Apr 2026 05:43:59 GMT  
		Size: 5.9 MB (5853086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7a36f3b081f7fc9d03a57cd93526131d0352ed0893eaef1b7480a8001ffffc`  
		Last Modified: Tue, 07 Apr 2026 05:43:59 GMT  
		Size: 16.2 KB (16226 bytes)  
		MIME: application/vnd.in-toto+json
