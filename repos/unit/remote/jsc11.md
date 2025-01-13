## `unit:jsc11`

```console
$ docker pull unit@sha256:059474e8d4680408ad240c46b21ffff0091254c38499e74075b3437e324dff9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:jsc11` - linux; amd64

```console
$ docker pull unit@sha256:66ddbf3010b1081d7400650923b649700c087df1b1d33d48945ab698183a751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220358320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b56e83af0a7214d10f49386ed9101612fe416df49fbb5b81be3c12149d047cf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.title=Unit (jsc11)
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.version=1.34.0
# Thu, 19 Dec 2024 18:23:57 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y          ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config libclang-dev cmake     && export RUST_VERSION=1.83.0     && export RUSTUP_HOME=/usr/src/unit/rustup     && export CARGO_HOME=/usr/src/unit/cargo     && export PATH=/usr/src/unit/cargo/bin:$PATH     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in          amd64) rustArch="x86_64-unknown-linux-gnu"; rustupSha256="6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d" ;;          arm64) rustArch="aarch64-unknown-linux-gnu"; rustupSha256="1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2" ;;          *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;        esac     && url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init"     && curl -L -O "$url"     && echo "${rustupSha256} *rustup-init" | sha256sum -c -     && chmod +x rustup-init     && ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch}     && rm rustup-init     && rustup --version     && cargo --version     && rustc --version     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.34.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs                 --otel"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure java --jars=/usr/share/unit-jsc-common/     && make -j $NCPU java-shared-install java-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure java --jars=/usr/share/unit-jsc-common/     && make -j $NCPU java-shared-install java-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && rm -rf /root/.m2     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
STOPSIGNAL SIGTERM
# Thu, 19 Dec 2024 18:23:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 19 Dec 2024 18:23:57 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:23:57 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1967582fbbe48da0f44ae5f24d4ecdbfcb32e005c0235041b1ddb4382bebd088`  
		Last Modified: Thu, 24 Oct 2024 00:57:00 GMT  
		Size: 16.1 MB (16142475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcdd5be0eb71025a105ec18ff66181d19cc62fddbd5f7b8d19fb9ea2be0630b`  
		Last Modified: Thu, 24 Oct 2024 00:57:02 GMT  
		Size: 145.6 MB (145608978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c1b19c29aea542e16531282f52055656af827ab49ce0ccba2d468e2324ff33`  
		Last Modified: Thu, 24 Oct 2024 00:57:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cacf2d88ab4fffd9cd634473d5ceddad404c00911e743d7fc3e43ed07560b04`  
		Last Modified: Thu, 24 Oct 2024 00:57:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfba05f5a04bdb0e00b120b7a64ecb06d7fd1446c6258aa80853b0f7cd18db2`  
		Last Modified: Sat, 11 Jan 2025 01:33:15 GMT  
		Size: 29.1 MB (29066026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa5a543e115f74ec4141971cb484f3cd60e8cdf7939705163d0132af9219c21`  
		Last Modified: Sat, 11 Jan 2025 01:33:14 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e5a5b84ded7e71f7c1c50da2005cd99bf93d8bd659aab1e9bcfa5c30344e28`  
		Last Modified: Sat, 11 Jan 2025 01:33:14 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:jsc11` - unknown; unknown

```console
$ docker pull unit@sha256:e372d9950b9cf1fd1faaf15312b20f43df0d0832a3668592346166495ba5e67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (26994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7cd864fe2e7124273d75f52da59f41c43863ddcff13e1df995f493b693ee9b`

```dockerfile
```

-	Layers:
	-	`sha256:54627ee708b1adf7c1f848681161224cef0e8272aafdf11971bda459a285067b`  
		Last Modified: Sat, 11 Jan 2025 01:33:14 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:jsc11` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:20b3dbb4eb6dffc59fa7e674629efd9bb7132eacfde73f89c289329dc53183a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214308492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3491e8ec6257ba748c4dbd1f42d1cc6dad0e88fa4fce1ee19a9507f817c085`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.title=Unit (jsc11)
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 10 Jan 2025 21:01:46 GMT
LABEL org.opencontainers.image.version=1.34.1
# Fri, 10 Jan 2025 21:01:46 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y          ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config libclang-dev cmake     && export RUST_VERSION=1.83.0     && export RUSTUP_HOME=/usr/src/unit/rustup     && export CARGO_HOME=/usr/src/unit/cargo     && export PATH=/usr/src/unit/cargo/bin:$PATH     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in          amd64) rustArch="x86_64-unknown-linux-gnu"; rustupSha256="6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d" ;;          arm64) rustArch="aarch64-unknown-linux-gnu"; rustupSha256="1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2" ;;          *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;        esac     && url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init"     && curl -L -O "$url"     && echo "${rustupSha256} *rustup-init" | sha256sum -c -     && chmod +x rustup-init     && ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch}     && rm rustup-init     && rustup --version     && cargo --version     && rustc --version     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.34.1-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs                 --otel"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure java --jars=/usr/share/unit-jsc-common/     && make -j $NCPU java-shared-install java-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure java --jars=/usr/share/unit-jsc-common/     && make -j $NCPU java-shared-install java-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && rm -rf /root/.m2     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Fri, 10 Jan 2025 21:01:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Jan 2025 21:01:46 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Fri, 10 Jan 2025 21:01:46 GMT
STOPSIGNAL SIGTERM
# Fri, 10 Jan 2025 21:01:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Jan 2025 21:01:46 GMT
EXPOSE map[80/tcp:{}]
# Fri, 10 Jan 2025 21:01:46 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729a387a18221fc41372d1fed9f3cde9512052f8bc68125d01d3c71ef2b5cd08`  
		Last Modified: Thu, 24 Oct 2024 01:03:52 GMT  
		Size: 142.4 MB (142386670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ca6248b7bdf803452c2e8c8ad830432f6693f9c08e3f74a3ef8bf48906e648`  
		Last Modified: Thu, 24 Oct 2024 01:03:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bec2e0ea1baef3f64532625145074b35338d2a1adeaaa7914d0828b1338cb90`  
		Last Modified: Thu, 24 Oct 2024 01:03:48 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374140f5ba27178d76fd741e744dad92bfac5514bf78bb088d455fd460f239be`  
		Last Modified: Mon, 13 Jan 2025 19:44:49 GMT  
		Size: 28.5 MB (28496208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d23380aafab71e40a7c0c0497ac1c4775fcb9ba11bf80083d174a5cc3d42716`  
		Last Modified: Mon, 13 Jan 2025 19:44:48 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b33cb4136cddca61e6b538af8e6b9923e5d48980efc97f3b4ef825c51ec53`  
		Last Modified: Mon, 13 Jan 2025 19:44:48 GMT  
		Size: 1.5 KB (1456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:jsc11` - unknown; unknown

```console
$ docker pull unit@sha256:6d7c554e5997e954d1b2aaf65809b561b62a49625a864c7050aec2380dddf054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67d66a5531507bde51f8864107deee99c512f13250035a23037dd30412073e9`

```dockerfile
```

-	Layers:
	-	`sha256:54769d36351a10186b0d9f12f016731642c73ad1d008b50e26391ce1265697c9`  
		Last Modified: Mon, 13 Jan 2025 19:44:48 GMT  
		Size: 27.1 KB (27085 bytes)  
		MIME: application/vnd.in-toto+json
