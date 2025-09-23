## `clojure:temurin-11-tools-deps-1.12.2.1571-jammy`

```console
$ docker pull clojure@sha256:c5e07b3c373a52e7f0671cdfa778ddb19029399101b914a276b9bd5a4c1dbc52
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

### `clojure:temurin-11-tools-deps-1.12.2.1571-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:a8f7162f737251b692566ffe66dbe2d9ff23e32e3a4fea6bcea6f6e8abc45285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242264529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfa2219f7996296acf718afe4753ce2d5935871b4036f8615d48e97c45b0dab`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626e0066814941272596c597780bba5c1c5946777688734462b04050bbfc86aa`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 16.2 MB (16150578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5af6814b849fd03f35bb04c172c54aed74a2f1b2c0874ee0d0a741afb248ab`  
		Last Modified: Tue, 02 Sep 2025 00:11:15 GMT  
		Size: 145.7 MB (145669093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481ed921877fec7fe7c67ad46baaa417fd72c7d23bdc6947ad207f016f9a0c76`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04773f58314fb5a8e58a12dcc9f230f3bd11368c661df5d942a2db056acb31c`  
		Last Modified: Mon, 01 Sep 2025 23:08:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1194cbb834ef62d9d0e039e19dc9aeb1d808be9d5bedd42723518235b82b2d84`  
		Last Modified: Mon, 22 Sep 2025 23:45:15 GMT  
		Size: 50.9 MB (50904834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16869778939f2d66ad424b9bd630469fd085c680063cea66d45a856f9048695d`  
		Last Modified: Mon, 22 Sep 2025 23:44:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1571-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:5a454234867eeed9ac7da7f368e353a7016f6bb4f9e8063a1a5be4cfd0498979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5384342b05de91211193d467c656fea7501dcc895083e7d693e0802c1b5d2c`

```dockerfile
```

-	Layers:
	-	`sha256:b7c2f984c196f3e0863492928084edac56ddd438c90d0db8bdd6632cfa9e920f`  
		Last Modified: Tue, 23 Sep 2025 00:35:41 GMT  
		Size: 6.3 MB (6320836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f105b110eed8737f92247c5e9ace6fa0939d8d49ac0db9da8fd06be694b3682a`  
		Last Modified: Tue, 23 Sep 2025 00:35:42 GMT  
		Size: 13.6 KB (13550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1571-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3be0bab6ef12aedb7be3b20b39f91b6baeb2d8a5cb7d5969cce734995966d5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236746220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f392d221cef61b612489764cc57f481e35319072d187d073ba20ffef8ff0f942`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4511ef1f8818f22c1b93fbb3e77ebb0b1001005ab33f8e9dd3aff34d0ab1d8ba`  
		Last Modified: Tue, 02 Sep 2025 00:59:41 GMT  
		Size: 16.1 MB (16063768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06afd4aeacbca9fc0d0f55d452755af69341efff7d0a1cb0b315d92fc14c6cb`  
		Last Modified: Tue, 02 Sep 2025 03:26:06 GMT  
		Size: 142.5 MB (142464245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e738ee9ba298d6fcb0c568a51b7ecf2e3ae666bdcedbcb6817aebea4ce2e45a`  
		Last Modified: Tue, 02 Sep 2025 01:44:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c99aa56b831d30f1a407141e0dfa453d664c4c93324d22b36463fe02003c3`  
		Last Modified: Tue, 02 Sep 2025 01:44:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6d5753e48f1b68735f87db555da8643be41ffc589d503ea59fd08bb5937793`  
		Last Modified: Mon, 22 Sep 2025 22:18:12 GMT  
		Size: 50.9 MB (50853650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33963a4f9e705b374459c639a86c32f46129eb88aa0130675412d3d5641a4cba`  
		Last Modified: Mon, 22 Sep 2025 22:17:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1571-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:03752bb3eaa8b074f7a9cfc142944cdd78e9efe80d0b8458847a23df478fed5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f67f7b364d2c79101fd3f40610f9767016913218d8f8ff0f8ea6bbc1787de27`

```dockerfile
```

-	Layers:
	-	`sha256:1e2d7e4cdcc1d1c7efa45500c3f255bd6040e516918dfdc5e0ec013b20e19a7d`  
		Last Modified: Tue, 23 Sep 2025 00:35:49 GMT  
		Size: 6.3 MB (6327220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6be4941e5fff5f4bf23eefe1c13d75eb6804423f2bbea78bed59d25ff41b25b`  
		Last Modified: Tue, 23 Sep 2025 00:35:50 GMT  
		Size: 13.6 KB (13640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1571-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:b68386066b6474137d373d7969fbb8c02aacd5e2f919d60e94cbb88882be5e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239773881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f417f24a77b93d1a3496bd810adefc57972d623de8b15a7ce3f22b970004c67`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb8a6a11d6a8aa6cb1265b04b48ac3ea54c5e642546199e4ec643364cc84fb`  
		Last Modified: Tue, 02 Sep 2025 00:15:21 GMT  
		Size: 17.6 MB (17624314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875ad18bcf69d0dbbd676132276146b2ba758ce550d4e14bd46b6c372bbc1ab9`  
		Last Modified: Tue, 02 Sep 2025 06:10:41 GMT  
		Size: 132.9 MB (132862983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a06d51daae232b5675e8196c551098aac5e132c5933d3e1638e96fe16d0490`  
		Last Modified: Tue, 02 Sep 2025 00:19:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283447e9860e6ae3158a8ac804dece435236a3ce1b26eafe3798f57b9441f68a`  
		Last Modified: Tue, 02 Sep 2025 00:19:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffa6acff19122ff77312b96c9bada0610cf13ec9182a67c57fe128c52521b61`  
		Last Modified: Mon, 22 Sep 2025 22:51:09 GMT  
		Size: 54.8 MB (54840271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c2960dde76b4b720bfda077f872686797599e709c5548617fd5d37dc2fcca1`  
		Last Modified: Mon, 22 Sep 2025 22:51:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1571-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:78f3d23c1c996971ecd6a218510ccef0258169eef1517f3761837d5b36e66824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6339031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e3adf1c9b140e78ddd359e416ad0c2bb48292ab1ef43138bcf47a6b895f500`

```dockerfile
```

-	Layers:
	-	`sha256:ec836e16efc9843d712e1d7b8c6cb1de75ee95d8eb8adb30be9971714938f55a`  
		Last Modified: Tue, 23 Sep 2025 00:35:55 GMT  
		Size: 6.3 MB (6325444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2df091849f4b2f4ecace5b7ce82b6d22f678330c28db5b7c215aaad4bf6b001`  
		Last Modified: Tue, 23 Sep 2025 00:35:55 GMT  
		Size: 13.6 KB (13587 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1571-jammy` - linux; s390x

```console
$ docker pull clojure@sha256:bb1f998a740d5896a6ecdd9df37c99976ba62b87f76c0634db2f731020ad43fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220702943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a15877ecd4bb001f91afc233bd0151b87d614c9382c0215f25e5f9623ef34f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9a055cccbd579a3774f2095602ffe4afd51473766e809ce2a67b5cfb09608`  
		Last Modified: Mon, 01 Sep 2025 23:11:44 GMT  
		Size: 16.1 MB (16149951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed6a5707be8fa02908801c16ce329216fe3caf3c4e0857c8b0fa6906ce2a7af`  
		Last Modified: Mon, 01 Sep 2025 23:11:54 GMT  
		Size: 125.6 MB (125635785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc0b2e58e4773ddbf85f262b6892a8a44e260ecc60407d16cad8262b7cdb563`  
		Last Modified: Mon, 01 Sep 2025 23:11:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559ea82e93f86715103b708a7fcad7ff84b7ad6298854f0b63cf242cf55fe8a4`  
		Last Modified: Mon, 01 Sep 2025 23:11:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a475874c85ea0e9884b1fc685991652c1961880cc71f8da87f267606c7c17f18`  
		Last Modified: Mon, 22 Sep 2025 23:01:01 GMT  
		Size: 50.9 MB (50910452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270cd4226608cec9d492af36d7a74a0a7e22a6fa507ffdcf41536c8b50ee8268`  
		Last Modified: Mon, 22 Sep 2025 23:01:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1571-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:81799481d502db49862cf19af84bcdca6bedc1de05aa7522ad2c575e265da453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df838c2fa7b44dfe6bedb887975b4d18bf0cc4e9fb2f56c5e88bf799146dd74`

```dockerfile
```

-	Layers:
	-	`sha256:cf1d2b998a53d3c62da4418f43feb3b71a23404288d4c9dcb2becf2571afad41`  
		Last Modified: Tue, 23 Sep 2025 00:36:01 GMT  
		Size: 6.3 MB (6316763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6f282a11ea04c9714f23d9daa51668600158e35f2b6a3b5e638d687a2051ab`  
		Last Modified: Tue, 23 Sep 2025 00:36:01 GMT  
		Size: 13.6 KB (13550 bytes)  
		MIME: application/vnd.in-toto+json
