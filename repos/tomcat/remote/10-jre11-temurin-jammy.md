## `tomcat:10-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:1616dc861e195938ea3166b9f58461ebbe6c8eb4e7c2d3b0da365894e982d30f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:10-jre11-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:8a5e84ff08e1ce34fe5abe2bbeed581e7c74523bd5b5ddefa96b9111b659e4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107247047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc0d5cbf35dd97ec1d85daf03e0eed4281a10c4d831a3139a880f025f018f5a`
-	Default Command: `["catalina.sh","run"]`

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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 Aug 2025 16:46:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 16:46:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_MAJOR=10
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_VERSION=10.1.44
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Thu, 07 Aug 2025 16:46:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 07 Aug 2025 16:46:24 GMT
ENTRYPOINT []
# Thu, 07 Aug 2025 16:46:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93562cc6f9bc192c13f2b83501a048f58b2eae6db305fc14c3eb783ccf271c`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 16.2 MB (16150617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3e1ddc9434423fb5ee9cc9563841d70dd98f93b48c6db377c94edaf971db9`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 47.2 MB (47234732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29deefaacc1b08c2cd6dd4da058658cbc1cccd46ffb4365bf9265265c5a0f7e`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee05d3a8171244d8a0a91dcc24cc8f88a022f84a6332f1c53cbd3277f23c216`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a335f9d3912dc9a77390de9ff3210341f628a6f3420da09aaee1af063e6b9ef9`  
		Last Modified: Tue, 02 Sep 2025 01:13:12 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2518022f1d5f806969164979647d73bd6e72be8731e8594d4f9a7d8c584586b0`  
		Last Modified: Tue, 02 Sep 2025 01:13:13 GMT  
		Size: 14.1 MB (14092463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924346b103fbade679828379201cecfb0644f818683d8d8d8f61d24c3301fd93`  
		Last Modified: Tue, 02 Sep 2025 01:13:12 GMT  
		Size: 229.7 KB (229663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:086eaf75ccb10a0677516b7d8737bbf32361f8966c5707926414b52e198b1257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2825321ebf8ce6b8baba551f672091fe7288c9bfc55fdfd45f0a2093adeb644`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b8bfbe986d6bbfc1b2c072e2c59d59ea141a98050ce83eb01250d31e641df`  
		Last Modified: Tue, 02 Sep 2025 02:29:46 GMT  
		Size: 4.0 MB (3954561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a1c6b6accfb6f0416c33a33b4d473f463bc4071f18799d336cfc40e19963bd`  
		Last Modified: Tue, 02 Sep 2025 02:29:47 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:5060e3ae19a9e97943047afb6946ae38820aeb39674e5ec1cda1694cf483a05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102150865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95927246b5cae6ee94fa67fbfa06491d89b4d3cc4093e82ca1e37c8364b986d`
-	Default Command: `["catalina.sh","run"]`

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
ADD file:1b718ac25471aa07aabcef27ec2e737bdbf36fd950c8d6e6103ad3dfeacd8e98 in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 Aug 2025 16:46:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 16:46:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_MAJOR=10
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_VERSION=10.1.44
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Thu, 07 Aug 2025 16:46:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 07 Aug 2025 16:46:24 GMT
ENTRYPOINT []
# Thu, 07 Aug 2025 16:46:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9e6391cf5a380a152971ee67d9bbbdd494023e7e2a2da9c7b92dd6d51593fee6`  
		Last Modified: Mon, 01 Sep 2025 23:13:56 GMT  
		Size: 26.6 MB (26642908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf151b513ce2784601808e6c9ca1a399d393f9a94a6bc7e7157b64d4f3a05`  
		Last Modified: Tue, 02 Sep 2025 00:14:16 GMT  
		Size: 15.9 MB (15889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8e5701d852e0716009d4aae79d0fad37b4138084d53861d04a87ec2113085c`  
		Last Modified: Tue, 02 Sep 2025 00:18:41 GMT  
		Size: 45.3 MB (45345096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a742ba9cb531ccb00639c202873245f83447556d6c428a4cdb801e37eea6e495`  
		Last Modified: Tue, 02 Sep 2025 00:18:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5823ef7fe150f2558f813d739acb26b72f652892f39126cfcb601434808147c4`  
		Last Modified: Tue, 02 Sep 2025 00:18:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0335cc67fd0f9a5906f0d5e09ddf9902f3920a058fca58efb56dbb0c409d03`  
		Last Modified: Tue, 02 Sep 2025 02:24:47 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c905b9a8fc2e25afc390565e8f53c0ae2d765fa117b3bf849f3678aa53147c5`  
		Last Modified: Tue, 02 Sep 2025 02:24:49 GMT  
		Size: 14.1 MB (14068071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ae5b71aa237ebc2b560a43a03fdd3dc9fbca89f6b0870951a975dfa756033`  
		Last Modified: Tue, 02 Sep 2025 02:24:47 GMT  
		Size: 202.4 KB (202404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:e8f63b758d4d706193880c87f909619ef1b35f9ea65b2fa535d993452c1baef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c35f61689b49b07a892362691575a8c631ea9f4ea3cb0f57ac203c1b14aaac`

```dockerfile
```

-	Layers:
	-	`sha256:90cbac6f6fa9359d5ead5232311f5ed62faa9784d9eb5ff2dff031534f867f85`  
		Last Modified: Tue, 02 Sep 2025 05:28:47 GMT  
		Size: 4.0 MB (3958159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225f93fdde04a1f89d69075c30134d948f3fdeb5d9d366183b4e0b422c9b7532`  
		Last Modified: Tue, 02 Sep 2025 05:28:48 GMT  
		Size: 21.4 KB (21380 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b09ba7828f2ad3b1b65b423f1bfa21cf53562550bbf6b58098f4213e924420a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103338414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5ce20aa03f72f6e610f03c43c3030c74fb4390d04c30ef906c2715c928498f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 Aug 2025 16:46:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 16:46:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_MAJOR=10
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_VERSION=10.1.44
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Thu, 07 Aug 2025 16:46:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 07 Aug 2025 16:46:24 GMT
ENTRYPOINT []
# Thu, 07 Aug 2025 16:46:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5618e0cf5548b3c1b1acb808dbd651baa9f894576ea435f1e2b6296d89cbe799`  
		Last Modified: Tue, 12 Aug 2025 18:34:44 GMT  
		Size: 45.6 MB (45589768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972144b0f2fc58b59dda462b9cae8d50f5c34458e1dfa2597c7ca9e073f3e8e7`  
		Last Modified: Tue, 12 Aug 2025 18:34:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0975f919b7d374f69245ee4b84267050962976d2a3661bb6f5895ec2ed1c829`  
		Last Modified: Tue, 12 Aug 2025 18:34:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806a3ee1171b07fac33f97d5babed712f4ee4ace0a931bb59aed09d9a7739b3b`  
		Last Modified: Wed, 13 Aug 2025 14:35:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e4b42e56aa0e937326b07746d294d9dc988955b38ba3a26ee53de1effc391f`  
		Last Modified: Wed, 13 Aug 2025 14:38:14 GMT  
		Size: 14.1 MB (14094318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8502a4fa3ae1be3e1e3da9e48b115ffbb1a6f3db7a76dd972102c48f741c1eae`  
		Last Modified: Wed, 13 Aug 2025 14:38:10 GMT  
		Size: 228.7 KB (228697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:dded0196ceefd67bed8a94bc4e95227cb23d430833a6358861955cce4f7479ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ebeebbb17b196e6de022e278d7654dfb95dd64738d104066e0199cbd9e1f56`

```dockerfile
```

-	Layers:
	-	`sha256:fdd324c5bdb3be89e9679b00b1fc484a08cb679449c7ccc61797e46836214d86`  
		Last Modified: Wed, 13 Aug 2025 14:28:45 GMT  
		Size: 4.0 MB (3954832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795cd0fefbb669781c35449044199bd825b76a93fa549b196adf463f98231433`  
		Last Modified: Wed, 13 Aug 2025 14:28:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:7c1ac4ac0f6145eeb2df9f2e31f5df6d22b2acf86dd3038a706f3221a178ef53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109115557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a8181c79c85b341b155263e0f73727dbea5ec128b5aac6dcc39f0a4263f48d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 Aug 2025 16:46:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 16:46:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_MAJOR=10
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_VERSION=10.1.44
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Thu, 07 Aug 2025 16:46:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 07 Aug 2025 16:46:24 GMT
ENTRYPOINT []
# Thu, 07 Aug 2025 16:46:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c50520b2833414582dcec4e87265a64dd9e5acd7b3ec03378e25ec51523b3`  
		Last Modified: Tue, 12 Aug 2025 17:29:14 GMT  
		Size: 17.6 MB (17624214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba75586e1e4ccb98eb66f3e98000cf939ab56f62899fa73f36b0f9c7343497c`  
		Last Modified: Tue, 12 Aug 2025 17:35:52 GMT  
		Size: 42.7 MB (42680241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac35d762c696d18c1f15cc618b54febe016c73c300078d0838da8c7af39358b`  
		Last Modified: Tue, 12 Aug 2025 17:35:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebda0cbce2de647fe44e6e811728dfcbc09b08472a4051484a7056b6dfb1f002`  
		Last Modified: Tue, 12 Aug 2025 17:35:35 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997c562ab6f836a43f49a3262a2f2482a6b428d254a5752c0732d44def095d33`  
		Last Modified: Wed, 13 Aug 2025 17:57:47 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564602b196399925d28bf4b6637eb36f33cccc2bb96d17afb05b030329e5ddaa`  
		Last Modified: Wed, 13 Aug 2025 17:57:49 GMT  
		Size: 14.1 MB (14106257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef2406496223af4a078d04d151c139c5093a3d22b1bb94be009c5282a4b40b1`  
		Last Modified: Wed, 13 Aug 2025 17:57:48 GMT  
		Size: 259.1 KB (259057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:cdcae484349a6e117d688c8e45039bd91cee39e4cdecdb59edc342d9e6c177aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8efaaa58946409af56e6ccdf585076fdd380600a683539f34d69a5738c76a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7ff14e453bf73a12d918f3196d6ba272ec5ab84f716ddcceb1ca3e1b9f21b65a`  
		Last Modified: Wed, 13 Aug 2025 20:28:52 GMT  
		Size: 4.0 MB (3958639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a899a9097b85b5e152ed937b1b46beb9b9066f9cc6868335d424cf51d3e1eac7`  
		Last Modified: Wed, 13 Aug 2025 20:28:53 GMT  
		Size: 21.3 KB (21315 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:38567e015992342740c233faf19834660f69c689b539e3380b09f5fd85dd24e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99332169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6b8691efdf113f4e84b31a04b4666d59d0eefd71ab8dd6abbf8f42855c5fee`
-	Default Command: `["catalina.sh","run"]`

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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 Aug 2025 16:46:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 16:46:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_MAJOR=10
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_VERSION=10.1.44
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Thu, 07 Aug 2025 16:46:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 07 Aug 2025 16:46:24 GMT
ENTRYPOINT []
# Thu, 07 Aug 2025 16:46:24 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:78acb84e0769475573c767611b2619952764a43ea01b849b0adc861bf00d6fd9`  
		Last Modified: Tue, 02 Sep 2025 03:50:39 GMT  
		Size: 40.8 MB (40849257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9769be7f306bc0301f34df90bf578db888940f2fdb6a69843acdd0dd97d0d6ae`  
		Last Modified: Mon, 01 Sep 2025 23:39:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3735fda8fefac6f716872ca1fa16b1c918b281460101ef13faaf2c5e241c66`  
		Last Modified: Mon, 01 Sep 2025 23:39:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f8b8ab0ef063fa5611111a8a6975cf3893abcc37b2ba8b4b5d9699d83e490`  
		Last Modified: Tue, 02 Sep 2025 02:49:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6980c714f97ec0bde44a4219c0e4990dc3c200e68793b3042b134cc78b5af57`  
		Last Modified: Tue, 02 Sep 2025 02:49:19 GMT  
		Size: 14.1 MB (14095839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cec8e1917f329066a3b28c65c47ccece5dcea2c043dccacdd51370125027f6d`  
		Last Modified: Tue, 02 Sep 2025 02:49:18 GMT  
		Size: 230.8 KB (230811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:e286d6017b63fc3b13d51999d64c126a12a55913557db8b12f2a06e3400be8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a5920741d1a5d6cb57cebd3f0d2af406e94c5b87d22faba57f3401112e0852`

```dockerfile
```

-	Layers:
	-	`sha256:fd353d80b474236e0775a7290e867f64aed83fa319e9389dc00b829382c87da8`  
		Last Modified: Tue, 02 Sep 2025 05:28:57 GMT  
		Size: 4.0 MB (3956158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a14981ff0dada5c79dd4281b4b4c0432c34792547457c863827fc81f30766ba`  
		Last Modified: Tue, 02 Sep 2025 05:28:58 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json
