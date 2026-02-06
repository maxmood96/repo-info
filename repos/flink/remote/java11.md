## `flink:java11`

```console
$ docker pull flink@sha256:21d8ca8a83bd777ea12ab42a707065a50b49291492387f75a41dd068b3bd6354
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `flink:java11` - linux; amd64

```console
$ docker pull flink@sha256:57bed216a4aa9a5cc0309009cb8e0b18dab70235c38ae8d5ad3dc10f1b909649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (673963092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20db395a7c183c6340444102473bea4e97aaa0ba3e15f6f5ba64bbc99ca137e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:13:53 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:16:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:16:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:16:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:16:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:40:22 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:40:22 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz.asc GPG_KEY=7BC9FA3EBE7E3DC7CD0EA0454C09617EAF241D76 CHECK_GPG=true
# Thu, 05 Feb 2026 22:40:22 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 05 Feb 2026 22:40:22 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:40:22 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Thu, 05 Feb 2026 22:40:22 GMT
WORKDIR /opt/flink
# Thu, 05 Feb 2026 22:40:34 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in hkps://keys.openpgp.org $(shuf -e                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Thu, 05 Feb 2026 22:40:34 GMT
USER flink
# Thu, 05 Feb 2026 22:40:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 05 Feb 2026 22:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:40:34 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Thu, 05 Feb 2026 22:40:34 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccdf4191aa259e84c498d6407f4f2b9cc91e84f53667da421ceaa3755af5e2f`  
		Last Modified: Thu, 05 Feb 2026 22:14:13 GMT  
		Size: 25.5 MB (25474378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2004c64bff9e4c55c5873b54e6db7b466d42c3171ecc5a20c480c4af4bf725a`  
		Last Modified: Thu, 05 Feb 2026 22:16:58 GMT  
		Size: 47.3 MB (47304878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67434e24faeb93c16b85564dccf41c5b48a06cf97861adeba9e4ff4757a500f3`  
		Last Modified: Thu, 05 Feb 2026 22:16:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea201b6782256a4b5bec163be6b6d3375829e792b9771fcb0ec86e2c725fca93`  
		Last Modified: Thu, 05 Feb 2026 22:16:57 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f889bd9163e129c1d53ba61367467e0704e29cc2d10a86341140700eefab793`  
		Last Modified: Thu, 05 Feb 2026 22:41:06 GMT  
		Size: 1.3 MB (1323506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cbe1bceedb4591e0b01d1daa7ed2c9c1006de72b2fa8934ed511134c06f4e9`  
		Last Modified: Thu, 05 Feb 2026 22:41:06 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa40d59d42dc4ff55dd88e1b54f3cb76b178fcb70a54639434cee2d6040f2c5`  
		Last Modified: Thu, 05 Feb 2026 22:41:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d8d4e6d587db36acbe75b9a9e9b811e75b7b7b4043f0bfc44e438f19fc2598`  
		Last Modified: Thu, 05 Feb 2026 22:41:17 GMT  
		Size: 570.1 MB (570128367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a445b5f9cf1111f7acffeb1a46d668c43f3839dc6f57d3f58aabf52c3f14239`  
		Last Modified: Thu, 05 Feb 2026 22:41:07 GMT  
		Size: 2.2 KB (2237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

```console
$ docker pull flink@sha256:507fd4cd90c04740ec1c67219dc2beb781633edd7880c0568324c859386331bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2945ca18b22a04a49cac958bc1fa3bc09fd7d870a2d78ab91df72be1e8e1d8e8`

```dockerfile
```

-	Layers:
	-	`sha256:0b296bc0adfde3a9913ca7fd64745b982881e7bb2cf0f1a49be8c7f569158fc1`  
		Last Modified: Thu, 05 Feb 2026 22:41:06 GMT  
		Size: 3.4 MB (3406500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939bfdc1f0f94d3460e4004c3e06b8bf65ba273f8fb8a0f670433f70442883d4`  
		Last Modified: Thu, 05 Feb 2026 22:41:06 GMT  
		Size: 23.8 KB (23769 bytes)  
		MIME: application/vnd.in-toto+json

### `flink:java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:e88782ab53e6fc8b4f21fe3353722e09b4091a26fbb7b01c38457fe64d34f716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.9 MB (670880493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bcbf96482b3e05d4bdba3c996968120be469e41bd5a47c1d1fedc68d16bf28`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:13:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:13:24 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:15:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:40:20 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:40:20 GMT
ENV FLINK_TGZ_URL=https://dlcdn.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz FLINK_ASC_URL=https://downloads.apache.org/flink/flink-2.2.0/flink-2.2.0-bin-scala_2.12.tgz.asc GPG_KEY=7BC9FA3EBE7E3DC7CD0EA0454C09617EAF241D76 CHECK_GPG=true
# Thu, 05 Feb 2026 22:40:20 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 05 Feb 2026 22:40:20 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:40:20 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink # buildkit
# Thu, 05 Feb 2026 22:40:20 GMT
WORKDIR /opt/flink
# Thu, 05 Feb 2026 22:40:33 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in hkps://keys.openpgp.org $(shuf -e                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     CONF_FILE="${FLINK_HOME}/conf/config.yaml";   /bin/bash "$FLINK_HOME/bin/config-parser-utils.sh" "${FLINK_HOME}/conf" "${FLINK_HOME}/bin" "${FLINK_HOME}/lib"     "-repKV" "rest.address,localhost,0.0.0.0"     "-repKV" "rest.bind-address,localhost,0.0.0.0"     "-repKV" "jobmanager.bind-host,localhost,0.0.0.0"     "-repKV" "taskmanager.bind-host,localhost,0.0.0.0"     "-rmKV" "taskmanager.host=localhost"; # buildkit
# Thu, 05 Feb 2026 22:40:33 GMT
USER flink
# Thu, 05 Feb 2026 22:40:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 05 Feb 2026 22:40:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:40:33 GMT
EXPOSE map[6123/tcp:{} 8081/tcp:{}]
# Thu, 05 Feb 2026 22:40:33 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0493720b8d8524b2c676f6eb5c5ec1f85ea66e648b37bc97a9c40ec8d9b8e688`  
		Last Modified: Thu, 05 Feb 2026 22:13:41 GMT  
		Size: 25.1 MB (25069393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c69c70453b49f0acf17e7a15758b95879b7f9e779da24099b312e30445a05c0`  
		Last Modified: Thu, 05 Feb 2026 22:15:35 GMT  
		Size: 45.6 MB (45624804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c838be702f964f393af36f4d99f814ddc74c99e8fe6d174c014fe9fe6dbdf6aa`  
		Last Modified: Thu, 05 Feb 2026 22:15:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293a3e4eb15a57c973ccd9529eccf31c2a5fcc05e94c31e646f4c0734ab04bca`  
		Last Modified: Thu, 05 Feb 2026 22:15:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cec4a834adccfa88dea211c999dcd154aa80c169d0e2b0a2ec2f17f548c019`  
		Last Modified: Thu, 05 Feb 2026 22:41:07 GMT  
		Size: 1.2 MB (1188136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5400672efb17f9ec2ec01c16ffd904ae8098a5ff1093b26399fef30a20b8890a`  
		Last Modified: Thu, 05 Feb 2026 22:41:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea35ce505c7c3d4b27fb4d9444a1d9771563b5e6042bc9d154b364554b7782ee`  
		Last Modified: Thu, 05 Feb 2026 22:41:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f5dcb651ee6fe4c82661adb3c4e45ea7f1b8cbad4c9612fb2381aacef8bac5`  
		Last Modified: Thu, 05 Feb 2026 22:41:20 GMT  
		Size: 570.1 MB (570128382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1d7b36cba39a613b361ecda9ec49412aa300a2e87baed36d171508cd1ad2a5`  
		Last Modified: Thu, 05 Feb 2026 22:41:01 GMT  
		Size: 2.2 KB (2238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `flink:java11` - unknown; unknown

```console
$ docker pull flink@sha256:d8a8f87d14324d7db43cc98e04b9c5064f9884a98f46502b705f3712df1bde33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9185b2d95d1ca79c7aaa8f50ed822c158bddeccc990fe40d3e291bb14aeacf35`

```dockerfile
```

-	Layers:
	-	`sha256:3253bd51f2afea32f059fa8a14e13b32d16e4dfccf8818341f8d44d69c9fc6f7`  
		Last Modified: Thu, 05 Feb 2026 22:41:07 GMT  
		Size: 3.4 MB (3407618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40cffd65006f70219fefb2febb15beface9be81a3465d2962b1611a8ba44e82b`  
		Last Modified: Thu, 05 Feb 2026 22:41:06 GMT  
		Size: 23.9 KB (23927 bytes)  
		MIME: application/vnd.in-toto+json
