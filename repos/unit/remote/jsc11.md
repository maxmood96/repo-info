## `unit:jsc11`

```console
$ docker pull unit@sha256:6207dcc4390b2800086eaf08f8dcbb4419fd2b70e1db1304f73fd8b3af808fb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:jsc11` - linux; amd64

```console
$ docker pull unit@sha256:82c3c446d7a96c33efaf337d9c7d8e42b9c548b9c3aeb0ae65ff57d3d6f32a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202680506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd811ee57db3d28019ba123d195e744cda95d84ec87acacd987f3d1be6a9a5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 27 Feb 2024 15:15:42 GMT
ARG RELEASE
# Tue, 27 Feb 2024 15:15:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 15:15:42 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["/bin/bash"]
# Tue, 27 Feb 2024 15:15:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 15:15:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 27 Feb 2024 15:15:42 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Tue, 27 Feb 2024 15:15:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["jshell"]
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.title=Unit (jsc11)
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.version=1.32.0
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure java --jars=/usr/share/unit-jsc-common/     && make -j $NCPU java-shared-install java-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure java --jars=/usr/share/unit-jsc-common/     && make -j $NCPU java-shared-install java-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && rm -rf /root/.m2     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
STOPSIGNAL SIGTERM
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 15:15:42 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f7a72ac2f841ebf3f4f9be405c1cce2173ce0ca79c0e0176d93b4a66d33b0e`  
		Last Modified: Wed, 06 Mar 2024 06:08:50 GMT  
		Size: 145.3 MB (145288641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5824857684b596ada67060f30f1f216dffbe7639156df1d163f2cc54e06754`  
		Last Modified: Wed, 06 Mar 2024 06:08:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc26d2df5bff2703f0e2f5f9f6458bd9a9e97b8e380aa55ff957ccae9762a9b`  
		Last Modified: Wed, 06 Mar 2024 06:08:39 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e238c9fd72ba8762d26f1a99084cf16b58b836c6e85f600e1035685fd429df87`  
		Last Modified: Wed, 06 Mar 2024 06:50:18 GMT  
		Size: 14.0 MB (14032335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53844cb1c7144fc7a5968ed26a5cf2ec74edcc3a2cb526d41774087cdb72ea49`  
		Last Modified: Wed, 06 Mar 2024 06:50:19 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57825af01e0557147f7e31c2ea185467d25f05581fb025059220b89f0a59c6`  
		Last Modified: Wed, 06 Mar 2024 06:50:19 GMT  
		Size: 1.5 KB (1456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:jsc11` - unknown; unknown

```console
$ docker pull unit@sha256:ac68b25cf1947b3113d142fb476170d77f8261f88d1842d39634223fd6444e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acc671d5778670089a0f81b96a5c678a343514a82e457c23af9215afcb9a1fe`

```dockerfile
```

-	Layers:
	-	`sha256:916274b7df4a7f4e94416a5a1476b86217f02b2deb9abc71d37582f5a245840c`  
		Last Modified: Wed, 06 Mar 2024 06:50:18 GMT  
		Size: 3.5 MB (3466029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c2ac6483b6a7aa706adbc380fd4d19978e2ee1956300ea7c8a21518d0505e0`  
		Last Modified: Wed, 06 Mar 2024 06:50:18 GMT  
		Size: 24.3 KB (24292 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:jsc11` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:6ab33d89d40d678378e340ce1d07c9b1bb43a600f3ee64ebea3eb1ff86e2ada5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 MB (197246834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888c5e19fb46a60b1995925a9835962c4b17ab216a5c379d1b2f90f837e2e747`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 27 Feb 2024 15:15:42 GMT
ARG RELEASE
# Tue, 27 Feb 2024 15:15:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 15:15:42 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["/bin/bash"]
# Tue, 27 Feb 2024 15:15:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 15:15:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 27 Feb 2024 15:15:42 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Tue, 27 Feb 2024 15:15:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["jshell"]
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.title=Unit (jsc11)
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.version=1.32.0
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure java --jars=/usr/share/unit-jsc-common/     && make -j $NCPU java-shared-install java-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure java --jars=/usr/share/unit-jsc-common/     && make -j $NCPU java-shared-install java-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && rm -rf /root/.m2     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
STOPSIGNAL SIGTERM
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 15:15:42 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bfd5bfe547de42293e06789ac2988bbe5fbbd4f4ac78a8070a941dff3183d`  
		Last Modified: Wed, 06 Mar 2024 04:07:01 GMT  
		Size: 142.0 MB (142017009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076d634f0a452e0cdb92737701295ddcc42e46814fac11519c857e46924923f4`  
		Last Modified: Wed, 06 Mar 2024 04:06:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d1793396c8cb16391935eca337d49c27aaed9f5f2c006984ecb4617d13e60`  
		Last Modified: Wed, 06 Mar 2024 04:06:52 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c6d5a216d56a42e165dbef1ca31d77c200d3c9a99e9ce21a7c586ad8022f9`  
		Last Modified: Wed, 06 Mar 2024 19:05:46 GMT  
		Size: 14.0 MB (13979191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87bf943314e88441a9468fa3b21571790102ac37e9dbdb4371f2735f9896cdd`  
		Last Modified: Wed, 06 Mar 2024 19:05:46 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7063bf0bd204a71fd76a44d8ee4c069933c0bb3a3c84d8fc15a60d38ed71c3`  
		Last Modified: Wed, 06 Mar 2024 19:05:46 GMT  
		Size: 1.5 KB (1458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:jsc11` - unknown; unknown

```console
$ docker pull unit@sha256:f9ab6e38d42a73b60c67a99d72254f7745bc3b9691eadc311af7a7efec3a5334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3489755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1885109f0d78e458c5a2d460df9a14b20e8bba24f79063456b391380e7509ac3`

```dockerfile
```

-	Layers:
	-	`sha256:ac078c83dddf937fd5fe11c14b1a407fe19defd7ea0911ff85389987a7dd7dc2`  
		Last Modified: Wed, 06 Mar 2024 19:05:46 GMT  
		Size: 3.5 MB (3466273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b73540f736b67cf4b58722bed1bab734365ef5961bc4de99ebf1ea079c313c9`  
		Last Modified: Wed, 06 Mar 2024 19:05:46 GMT  
		Size: 23.5 KB (23482 bytes)  
		MIME: application/vnd.in-toto+json
