## `eclipse-temurin:25-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:1f12ca3f1527ae593d1f326fc1c8cfa5dee38517549f43c86349a109615c5cfd
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

### `eclipse-temurin:25-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:be23e89e4f260a37eb4aa5b7194d40f96bb7d562562d3267b8d6b1d5af73af17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103631553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4925b2342e757f6b913012b4336996cca6bc4ddb3424d5c587b52106bd4f6c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:22:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:22:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:22:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:22:14 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 13 Nov 2025 23:22:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:22:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:22:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:22:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a47168568d5683cca8c7a011f86c4fafb0bd1ff72e40389ee97864ea28dfea7`  
		Last Modified: Thu, 13 Nov 2025 23:22:55 GMT  
		Size: 11.4 MB (11404607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108c6de37075a02115e9fed7fdba1503554ebffce8ed5b5673dc8b1dc61c1370`  
		Last Modified: Thu, 13 Nov 2025 23:22:59 GMT  
		Size: 62.7 MB (62687834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531d7f05a11d08d4c746d418cf7db9a6dcad593b18b39d0c761d8abcdc15dd19`  
		Last Modified: Thu, 13 Nov 2025 23:22:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:362475f911a2e7fde7884cde58a4b0499ee81518d33f3fe85acd8fa99b236af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3669313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d7ac6a9557608c3db596326715768c802384bd250407f953af2624e58e1502`

```dockerfile
```

-	Layers:
	-	`sha256:7f09cdab61dd9341e288aa46fce658c0faa0c74d3dd0c4e6f52ce12e14def4a8`  
		Last Modified: Fri, 14 Nov 2025 01:19:30 GMT  
		Size: 3.6 MB (3647076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b5cb79b4a55b8794da05c21219fc20926f45967549603ac01db09d19cadf96`  
		Last Modified: Fri, 14 Nov 2025 01:19:31 GMT  
		Size: 22.2 KB (22237 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7ece379d4668d0aa3d6d66d70d71ef9b3921db98dc9356fbc098b11f1805152d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100382655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbc0ede15f7ac79f49f539f32d96cce6308916019c0ba10f5f3489d3c540239`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:44 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 13 Nov 2025 23:22:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:22:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:22:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:22:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3692c318c5ecec02ba317bcb8b3e126da19c794eb692de5ced9dbbb30c6cd2`  
		Last Modified: Thu, 13 Nov 2025 23:22:24 GMT  
		Size: 11.4 MB (11357757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4e0baa24dea9a0f631acf7e12f1e33aaabdfdf2f9b530a1ee87b8e91dfbe4c`  
		Last Modified: Thu, 13 Nov 2025 23:22:31 GMT  
		Size: 61.6 MB (61638706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435f2e942c2099b67bb826915c859b97f9b227a2209b4fa3e4ad1c47daf2fbe3`  
		Last Modified: Thu, 13 Nov 2025 23:22:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f433332dc9bf2eea07725a9ce81d4715e97b8f586c301fcf7622913c05cc9645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3669061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f65884aac35a47069fc57bd1670eac8bb0a040befa45450dcec86d859f25bf`

```dockerfile
```

-	Layers:
	-	`sha256:621fa59b71ea21537964818dfd06bff1d2f570c6278626e179f21aee9d35ea46`  
		Last Modified: Fri, 14 Nov 2025 01:19:35 GMT  
		Size: 3.6 MB (3646714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c813579b70538bc11c6b001414fc6ec60f99761c8409e51363cd360c522df3`  
		Last Modified: Fri, 14 Nov 2025 01:19:36 GMT  
		Size: 22.3 KB (22347 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b1767c8f6e00295472b16a205107a020adbe6df1cf8097103b8bb0f4948bb73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108466060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad48ad177211e65194237dd9ca22d44abbd099d8de8ae4a25834580f7985162f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:34:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:34:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:34:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:03 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 13 Nov 2025 23:34:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b381eb4f070f5b979b6037af06998dda31a4fc0947bfe506eebe30ec96852b3`  
		Last Modified: Thu, 13 Nov 2025 23:35:08 GMT  
		Size: 11.9 MB (11893834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9406d6921d367ca7762208e468cdb7239f998aeb5c662d0bcba0f822fcb8968f`  
		Last Modified: Thu, 13 Nov 2025 23:35:13 GMT  
		Size: 62.1 MB (62123190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573f0f7ae13a0186447196ef1be1ed836d98af4eb5e814e32ac341c153b18aaa`  
		Last Modified: Thu, 13 Nov 2025 23:35:07 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2b5a211c08f00ca2cd50899f03f502436ffab3783ae83eb09d1a79f6b5a7d008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b70b91d090a1f6a59136fbaad17aee2a03531b9cbfec14fc4f95d68e1f0d2d`

```dockerfile
```

-	Layers:
	-	`sha256:2909bba17f624fadc3d390209d35af9543275e22a69796fd4b7aeaa2fd8b5fb4`  
		Last Modified: Fri, 14 Nov 2025 01:19:40 GMT  
		Size: 3.7 MB (3650401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e653ef113e02c5f41019266d2611cde1b6207b145b1613521d5093d8c2ded2b`  
		Last Modified: Fri, 14 Nov 2025 01:19:41 GMT  
		Size: 22.3 KB (22273 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-jammy` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:aef8318a9f2af98eccec85f2c370e4e20fa0f95c88f73120870d0f5c208c5f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99813167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87abf3938deaa1ad2935fea7ad6a7c2feb9fc271ea21d5d6cfa83b25932a44dc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:12:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:12:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:12:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:12:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:12:29 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 13 Nov 2025 23:12:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:12:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:12:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:12:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21f1986c8a9a9c9a6ab836f8a108273fc1342c24d8a6e1c802a33d63f1eaa36`  
		Last Modified: Thu, 13 Nov 2025 23:13:08 GMT  
		Size: 11.5 MB (11497370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a32b95e819bd19793f4f2eec5f61cc60524b1cd22fb7259cab9c441d3f4d76`  
		Last Modified: Thu, 13 Nov 2025 23:13:12 GMT  
		Size: 60.3 MB (60310197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb78c2802ebfd84ea2a01ff1c27c1759a20e174b87839d9afb9d2c0ed76a7c4`  
		Last Modified: Thu, 13 Nov 2025 23:13:07 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:37bdb50396ecec5d8f38eee9d376d9ed6f3436d09a9f0ea079395cb926664f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbd87cb3f323097a2cb379d4f6890da430814cb51df5765859d8e1fd85732d0`

```dockerfile
```

-	Layers:
	-	`sha256:107ce737fef2a1f3a3c2c1789209c39443b30de96168cbc87209118d247b4611`  
		Last Modified: Fri, 14 Nov 2025 01:19:45 GMT  
		Size: 3.6 MB (3648062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b65942570601d50e9479abb98c1fa537e96152ad5248adb08bc8060056a2488`  
		Last Modified: Fri, 14 Nov 2025 01:19:46 GMT  
		Size: 22.2 KB (22237 bytes)  
		MIME: application/vnd.in-toto+json
