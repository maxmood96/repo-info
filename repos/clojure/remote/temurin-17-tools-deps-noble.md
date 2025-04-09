## `clojure:temurin-17-tools-deps-noble`

```console
$ docker pull clojure@sha256:26fb8a2667be2917c4e23793cb5387807efc55c224980eb5ea6e1702677ac1e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-noble` - linux; amd64

```console
$ docker pull clojure@sha256:e5075c8af1bd35fa941e04426d1512bd107cd7d920ed4fd82110b66b678c385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252216721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07476f47e5dbf835a9b6dc74614b119350abac221b12e3e4720013b0599a323e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89e30e15697dc232f3654f9e157d3b28ca771ecac2c0967492c7f89f64b2f4b`  
		Last Modified: Wed, 09 Apr 2025 01:15:53 GMT  
		Size: 23.0 MB (22952728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75915a4c1fbb50377dd6825b9e1cf0b7f02d18043c67736b7b010bc6c2266c6e`  
		Last Modified: Wed, 09 Apr 2025 01:15:56 GMT  
		Size: 144.6 MB (144576259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5282e02cf084d971bf51a730f375efbdae60bb5467dc2a47bd58e3ab58aeec4b`  
		Last Modified: Wed, 09 Apr 2025 01:15:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04ceb2e7f7d5fd3b358054d518735e3c16709b068a6afcd8340a03a88f3ea6`  
		Last Modified: Wed, 09 Apr 2025 01:15:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b85d713802fbcc3cef35335bc5fe98f4c38a19030b1dbebed583e3d47969d4c`  
		Last Modified: Wed, 09 Apr 2025 02:18:59 GMT  
		Size: 55.0 MB (54966593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3695cb36fb677239ee6a2600e5290dd983d928dc393c480dc7e0b0c5f9a25e2`  
		Last Modified: Wed, 09 Apr 2025 02:18:58 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773123b85a636ba82f0e7ad8007d29686c4e20dfee0f93d74024c88a8ffd1ca3`  
		Last Modified: Wed, 09 Apr 2025 02:18:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:d34a83e4f41cb46aeb960bf2e18c7bbf6b1b9e2136364982721688c8de0fbdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5680725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa99a1d51de08e035fa5059f5dccd3e2a3966050003a98efe726c875ea8148be`

```dockerfile
```

-	Layers:
	-	`sha256:1d2b72536efa7c92393a40ac599a8b72a570147f0f09e70c3cda90f1d32586b3`  
		Last Modified: Wed, 09 Apr 2025 02:18:58 GMT  
		Size: 5.7 MB (5665138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d30d3de2b69d787b1dbb4b779c5e2182ce711b6cd94d9f80f3dea692c41d38`  
		Last Modified: Wed, 09 Apr 2025 02:18:58 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:621222826e3e04307bec76ba4b43f20ba90462132dc1b4cfc320307bc649eb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251398623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6fc346cf73f1c5255a6cbdab083ea23b4f46eaf7da5a8b0da7df94fc814867`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bb4e2189afd83aaf4ebaa5d182e82cf4839444cb97cb855a17178b08a9012`  
		Last Modified: Wed, 09 Apr 2025 07:05:34 GMT  
		Size: 24.2 MB (24163226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eae8ebab9bae9078a2efc6360aaf360df25465e4387af24def8cada2271b60`  
		Last Modified: Wed, 09 Apr 2025 07:05:36 GMT  
		Size: 143.5 MB (143461784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a89cb7c086c6517d945cb3cd3868f5956cd73c322e7f2b6e9fa291d63579d66`  
		Last Modified: Wed, 09 Apr 2025 07:05:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c6f03a28df78a73729402169461858f5e39d3928067ad67dc945c97ad8d24`  
		Last Modified: Wed, 09 Apr 2025 07:05:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cfb2b8f15e5b718d972f24179eb68bce25388fd5e1b506cb0115ef78f69063`  
		Last Modified: Wed, 09 Apr 2025 17:37:50 GMT  
		Size: 54.9 MB (54923172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d543227516d836cda99baa43e1108d70d5eee8f10411723b57ce67034aff0fd8`  
		Last Modified: Wed, 09 Apr 2025 17:37:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fa31c7c1ef6da617049831853e762890059b31fd3f00196c8cefe78c79de8d`  
		Last Modified: Wed, 09 Apr 2025 17:37:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:0ff4d5893cb1da7c85168e3591673282202f75c8a44d6513dd8e9860af863f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381dbc667e5d32e1205698a5f6ec5edb67534c05d21aff489a5970920c3e94d3`

```dockerfile
```

-	Layers:
	-	`sha256:4aa79d70214049df7126a84b8993665aaaa8e2dcbd7eac8410af6d109d42a5a5`  
		Last Modified: Wed, 09 Apr 2025 17:37:48 GMT  
		Size: 5.8 MB (5802751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe163602265fa314622c9e7e43d2d89ce322a17a0a3b32a6a21524aa450a27f`  
		Last Modified: Wed, 09 Apr 2025 17:37:47 GMT  
		Size: 15.7 KB (15679 bytes)  
		MIME: application/vnd.in-toto+json
