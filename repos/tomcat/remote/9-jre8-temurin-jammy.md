## `tomcat:9-jre8-temurin-jammy`

```console
$ docker pull tomcat@sha256:4c77f563295de0dd44a15be8a1177daacada7aeaec1c3988cc0be2f65768af7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `tomcat:9-jre8-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:93051737890060c4f566df60f2b1de88c3ea0eb37ffe903f2c26666d6ba3b240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101580245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6bbe45e275c6238883ed3ff1e9995b937ca930f9a9d342e4c44f26d3c7f5f3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:24 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:41 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:41 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:41 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:41 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:41 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:49 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:49 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582c190d866c35ef95118a566ad1c39b17ab52aaa5c019bba7697baa0acd8f7f`  
		Last Modified: Sat, 08 Nov 2025 17:57:44 GMT  
		Size: 16.2 MB (16150241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db2df554a6a583352255445a9268c5b83d9d6ad18aaf019a4cd63192f95ea`  
		Last Modified: Sat, 08 Nov 2025 17:57:44 GMT  
		Size: 41.9 MB (41891100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334b47b61da0dfd015e349ed46861f7c99bec14b47e14f370ffd958c9a684599`  
		Last Modified: Sat, 08 Nov 2025 17:57:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dfe383872d9b141dae8fe682acbf0aaacf61285994676d25a97ff3bc5924bc`  
		Last Modified: Sat, 08 Nov 2025 17:57:42 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac64fafabd7c0864ce37622525dc10f8fde147b8c6953b00c013ec46178a2d`  
		Last Modified: Mon, 10 Nov 2025 19:13:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c627aaaed7d7adcb927744b6feee4db4c46ad3b97d8f940df218be315112df`  
		Last Modified: Mon, 10 Nov 2025 19:13:03 GMT  
		Size: 13.8 MB (13769904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47f8f5942b617cdcd0bc56c46e8e71640be75c8fa0a0aec073201d7987c53d2`  
		Last Modified: Mon, 10 Nov 2025 19:13:01 GMT  
		Size: 229.6 KB (229572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:35f14796948f2e8fa6a02a13482a63181ee04a4d045d2bcad0f21df6b48c3def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052153c7811ad14f2eef52ea3d8c35354ea1a7ea15a0617b81f433f5af67f61d`

```dockerfile
```

-	Layers:
	-	`sha256:119fd1f74b45cefca99f35fd71afebe6e900e15de40e94800fda9a27eca317c6`  
		Last Modified: Mon, 10 Nov 2025 21:48:31 GMT  
		Size: 4.0 MB (3967370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eed149e627274957c1b305acd051187357bc6333db795ea42300f5b12660c92`  
		Last Modified: Mon, 10 Nov 2025 21:48:32 GMT  
		Size: 21.2 KB (21195 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:3fb524a487de529f9eda7c27e17e539b3711f928b9176b2d64127d8bc361b963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95820787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b290d4363dec5bdd844dcf49a57a4b53aab3b629bc068315f6882885107293c1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:33 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:36 GMT
ADD file:7939f961de8cf091ed251aa1d8e432c16ec7506130ed39a1db4028efdad8fbfe in / 
# Wed, 01 Oct 2025 07:06:36 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:25 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:05 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:05 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:05 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:05 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:14 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:33392950d914bf1e16e980fc0bbcec6367a2d2b8ecbd726dc5fc65b4c96ce79f`  
		Last Modified: Wed, 01 Oct 2025 18:17:15 GMT  
		Size: 26.6 MB (26643435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1345e0b53413e99f889c26d5ec17e483aedeef73cf90f7586033224325438fc`  
		Last Modified: Sat, 08 Nov 2025 17:53:05 GMT  
		Size: 15.9 MB (15889483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97549f87a7539ad69ee686bb599991dec093b53cc8dd9ab050b1ef0c409149d`  
		Last Modified: Sat, 08 Nov 2025 17:53:32 GMT  
		Size: 39.4 MB (39380216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0428ce8cf5ce2ed6e61a3e68ce6a18cc982444a0ab438b4105c36080e3e4c5a0`  
		Last Modified: Sat, 08 Nov 2025 17:53:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927fa4e27888d0569ead26f6d071262010768f6abefc735f4685967d6fb18c66`  
		Last Modified: Sat, 08 Nov 2025 17:53:30 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632e48e4beb71679aba18f7c6c0ddb5b86d149c1eb010662c1824e31b38811da`  
		Last Modified: Mon, 10 Nov 2025 19:12:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca8c207a8052535762cf2eac9693904c45848ebaab2b843015511ab4097dc6`  
		Last Modified: Mon, 10 Nov 2025 19:12:33 GMT  
		Size: 13.7 MB (13702388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad06718a348a98983acd472ca6caa41b85b40c29f76892e5ce014ced96a0820`  
		Last Modified: Mon, 10 Nov 2025 19:12:31 GMT  
		Size: 202.7 KB (202652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:04e2036f53da20dface187d7e00f4e2a0e96176d58c2f22d07a6bebec81b3384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2e16d56e532989b5658fdaee8dd05762cbc5fc62828bc3be8b3f968695bc61`

```dockerfile
```

-	Layers:
	-	`sha256:17b28995705cc401de2377b7c56528208257559064c8a94c54657c4e2695c489`  
		Last Modified: Mon, 10 Nov 2025 21:48:36 GMT  
		Size: 4.0 MB (3973386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3f0caed0a2bd93de41c097d4e5f131c1023ea5e30b7e10718f47d5cfd1c870d`  
		Last Modified: Mon, 10 Nov 2025 21:48:37 GMT  
		Size: 21.3 KB (21315 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:6b95cf7342d464a180d80d614419490b0f457d45cfb7fc49f3c484bfb38f121b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98341928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1debe39be22627521850ee16be37d94cff3841e39b0e03bcecd9aa4797d89144`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:32 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:55:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:55:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:55:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:55:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:13 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:13 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:13 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:13 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:13 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:20 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:20 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d472da75e5a9ca19105e900ee792e3c05455eae9fac582f6b9d20eeb9320c2`  
		Last Modified: Sat, 08 Nov 2025 17:53:01 GMT  
		Size: 16.1 MB (16066125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdc98f8f0e78b8955066e5a1b64ee3a8aa71eb332ef84567f3e18b5ed8938a1`  
		Last Modified: Sat, 08 Nov 2025 17:55:36 GMT  
		Size: 40.9 MB (40884232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e42a39f2ae3e062f5aec9b24ebcb479ac94dd35dbd1fd09a4294a69cc615d4`  
		Last Modified: Sat, 08 Nov 2025 17:55:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f143c7145989f2cd0860c5498d83739f5e8f459bc03006ca14dd180d359a09`  
		Last Modified: Sat, 08 Nov 2025 17:55:33 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43da8b103947f00ed0e3994824d5f8131cd1828a18255443faa7ad9c132abe35`  
		Last Modified: Mon, 10 Nov 2025 19:12:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ef5f2adcb746e4614f37960c7a0ecf658a17073623d956865dbc62301950c1`  
		Last Modified: Mon, 10 Nov 2025 19:12:36 GMT  
		Size: 13.8 MB (13777139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498ce121eeedd764cdef528cc7b647174cdf730753df6a3a159c5b2424436755`  
		Last Modified: Mon, 10 Nov 2025 19:12:34 GMT  
		Size: 228.7 KB (228713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:275e7206b2e4a027791d415a249b82eaf56bde3173983491b0e13fae77905183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4a9981e652fa05bf21856f3f640185da4cc3c6e4dc4857a8bbf8cc9350a4ef`

```dockerfile
```

-	Layers:
	-	`sha256:7659e9073c2a82393a16a42e663331072661bc079edf4739833852ce37d3b825`  
		Last Modified: Mon, 10 Nov 2025 21:48:42 GMT  
		Size: 4.0 MB (3967729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6012a2b5aa6667870d5dd166d400fdbf64e20fab02c44579e4fff4c2906c365`  
		Last Modified: Mon, 10 Nov 2025 21:48:43 GMT  
		Size: 21.3 KB (21343 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:196ee06e60fbdda4e1e1fea80314e79a2275e8e25103961db0d401b1c21c6041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107402140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7831c655894cecb2e680c81255aa3e691fc4f55bbf07fe943f8cd6471c42d287`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:17:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:17:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:17:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:17:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:17:59 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:58:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 23:15:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 23:15:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 23:15:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 23:15:06 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 23:15:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 23:15:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 23:15:06 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 23:15:06 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 23:15:06 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 23:15:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 23:15:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 23:15:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 23:15:15 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 23:15:15 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 23:15:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f254a691cf2e11e88dd1675267d067d174b5f0efb8778e29e1be56983c48a`  
		Last Modified: Sat, 08 Nov 2025 17:58:52 GMT  
		Size: 41.3 MB (41272653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8364d37d5daa28ed044e8dea657a8dd24d52315ab1288ef5a2476d63eb1785`  
		Last Modified: Sat, 08 Nov 2025 17:58:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d6a78e796c33586ede570d6f58d074f0fca4450d83a3cbc8b9af4fc68ab494`  
		Last Modified: Sat, 08 Nov 2025 17:58:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338dcf9050180261c6879494272589619eba957e6482eb3999077ef80b1ffde9`  
		Last Modified: Mon, 10 Nov 2025 23:15:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40311da66102323dbd79789c4a8a66d70537832df16f132b0f64907e7eb6c901`  
		Last Modified: Mon, 10 Nov 2025 23:15:45 GMT  
		Size: 13.8 MB (13797389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9be41bba04b1054dcf69da06fc9e4fb847c163abad367d1d1a88daebf42e36`  
		Last Modified: Mon, 10 Nov 2025 23:15:41 GMT  
		Size: 259.0 KB (259021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:358ff1c030f75f3b4f52df85bf8ded3950db7608ede705b9eee3530c96369ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ff756b96e6381c89e96e66cd5936c39e343d9c60e85cff8d4f08a943a4ed9c`

```dockerfile
```

-	Layers:
	-	`sha256:5d3bec586ec94817033986d4dcdda17f80a213dfe5e9d02aadc740e3c5552621`  
		Last Modified: Tue, 11 Nov 2025 00:36:30 GMT  
		Size: 4.0 MB (3972148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c25d870ab76ed49fa2690cf71a4e2c5c6650a793c5efa1773f96f5570f098c`  
		Last Modified: Tue, 11 Nov 2025 00:36:31 GMT  
		Size: 21.2 KB (21247 bytes)  
		MIME: application/vnd.in-toto+json
