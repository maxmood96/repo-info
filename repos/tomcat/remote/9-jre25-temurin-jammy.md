## `tomcat:9-jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:9394f3c1a25627a0815edee47a4e82eca7a0461fe6c991c3120951eb5737dfae
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

### `tomcat:9-jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:16db770e3daec85b993ae9d922f4ffdc362c540fcce49623e7bd5117c72dfa1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117679270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7eed7ea097ece2babe23e8986bd0e8c7dda5bc0260d8fef78f114fe62046fb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:20:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:20:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:20:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:20:25 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Feb 2026 20:20:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:56:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:56:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:56:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:56:40 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:56:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:40 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 21:56:40 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 21:56:40 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 21:56:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:56:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:56:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:56:52 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:56:52 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:56:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2b1d2cb9d1bd60c450c5e1e8243f74415d535d2fff36f9f23d7401a659e467`  
		Last Modified: Tue, 17 Feb 2026 20:20:55 GMT  
		Size: 11.4 MB (11405193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12eb83475165cae8ee6184056846e81f2ec3dde0f39df55ae5d432c79c2029a8`  
		Last Modified: Tue, 17 Feb 2026 20:20:57 GMT  
		Size: 62.7 MB (62708383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cd82c70ffdc9d69e605e00c0a6b6160559af751f1779fa09f90e69693a389`  
		Last Modified: Tue, 17 Feb 2026 20:20:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585a9940c4cc6337480a18e681136c0f5363d77e3c15a06a0bc31b4b6d4aec94`  
		Last Modified: Tue, 17 Feb 2026 21:57:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fd4a4224f215325b0f6a2ed06d1e96fbe09a80258b74db4567391afaa5ab1`  
		Last Modified: Tue, 17 Feb 2026 21:57:03 GMT  
		Size: 13.8 MB (13812310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30da51650f898b558399268581f48b3907463e0ddb71916219a87e42b6aad431`  
		Last Modified: Tue, 17 Feb 2026 21:57:03 GMT  
		Size: 213.5 KB (213501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:23b2fba61e8711f0d44d4ab8e3ea6d5a402596ad3d8c45c5ef8ec45bfab11af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1e101bc098cd6a106263940dbb2fc697aebad4712e823da2bbffe6e03d9852`

```dockerfile
```

-	Layers:
	-	`sha256:85cf149cddbe5ffcadc439152a772674848bc445c9e407052d400a8de41859d6`  
		Last Modified: Tue, 17 Feb 2026 21:57:03 GMT  
		Size: 3.7 MB (3704997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b15038b5df46c38ee99fd919a80833140233983ed095a248116aab902a76b7`  
		Last Modified: Tue, 17 Feb 2026 21:57:03 GMT  
		Size: 21.2 KB (21205 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:070206caab918a8bfaf458896e0e260da3295cd6dbdd9c64ebe56e0437b65e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114465618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244c075b2ba9da1eb98f7ede85449ef313cfbeb1316a39f4c11e06ef7ca41944`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:25:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:25:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:25:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:25:03 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 01:25:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:25:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:25:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:25:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 03:28:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Mar 2026 03:28:37 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:28:37 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Mar 2026 03:28:37 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Mar 2026 03:28:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:28:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:28:37 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Mar 2026 03:28:37 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Mar 2026 03:28:37 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Mar 2026 03:30:01 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Mar 2026 03:30:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:30:11 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Mar 2026 03:30:11 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Mar 2026 03:30:11 GMT
ENTRYPOINT []
# Tue, 17 Mar 2026 03:30:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f624e573b3a7b5405d838f185ec5fbcc027f717d6de99fcb3ea59bc7ab2bd42`  
		Last Modified: Tue, 17 Mar 2026 01:25:39 GMT  
		Size: 11.4 MB (11353553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876f51126dd3ec8d3d88ab6fe11d76b099b10c5a1476ac75cdb14f4cdf7896a2`  
		Last Modified: Tue, 17 Mar 2026 01:25:41 GMT  
		Size: 61.7 MB (61669317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb29dbbcf7f4798144a0b93b2acff13e19344328cf8718c53e6766aea4867f01`  
		Last Modified: Tue, 17 Mar 2026 01:25:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7941a7f640b27a4e40733b71db50f943a3c81393632b72f9b91372b06bd48d27`  
		Last Modified: Tue, 17 Mar 2026 03:28:57 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e5f4ebf67bad857a1a982f6e8767cffde33a22216b038ebf5b1e02b8e1596e`  
		Last Modified: Tue, 17 Mar 2026 03:30:21 GMT  
		Size: 13.8 MB (13821264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe88cc95900915e9affc4481d7f91b1f31a9a80e045fbb045b62ce5742652f70`  
		Last Modified: Tue, 17 Mar 2026 03:30:20 GMT  
		Size: 229.9 KB (229944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:160ce8d029499e08284c3298deb479409fe5c3689522bdcdf61654e5e86e4c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e465947e77c5e32c41ba4de8cfa8b242af62839f447f38cd3eb0ca593f53a734`

```dockerfile
```

-	Layers:
	-	`sha256:e2d159cfc201b97646d9868c5f4cab264aa061073f067d723b46cbf473184896`  
		Last Modified: Tue, 17 Mar 2026 03:30:20 GMT  
		Size: 3.7 MB (3706335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ce1cc788471b318d149f524464b39398496e72575766cf0d6c1a742257e47`  
		Last Modified: Tue, 17 Mar 2026 03:30:20 GMT  
		Size: 21.4 KB (21353 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:318861b7be76a3ec9e8bb3a4cf8d89c923a0015b550b11101deba39c9c700887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122553153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35078eeb0e92777a3e156ad5f9ce555496ac4298516d5b231b48c01fde3197ed`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:24:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:24:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:24:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:24:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:24:23 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Feb 2026 20:24:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:25:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:25:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:25:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 01:03:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 18 Feb 2026 01:03:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 01:03:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 18 Feb 2026 01:03:08 GMT
WORKDIR /usr/local/tomcat
# Wed, 18 Feb 2026 01:03:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:03:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:03:08 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 Feb 2026 01:03:08 GMT
ENV TOMCAT_VERSION=9.0.115
# Wed, 18 Feb 2026 01:03:08 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Wed, 18 Feb 2026 01:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 18 Feb 2026 01:11:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 01:11:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 18 Feb 2026 01:11:23 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 18 Feb 2026 01:11:23 GMT
ENTRYPOINT []
# Wed, 18 Feb 2026 01:11:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a0aedfccdbd86c94bae8993c6e074c129bb683f0b75a689c96144922440e95`  
		Last Modified: Tue, 17 Feb 2026 20:25:32 GMT  
		Size: 11.9 MB (11892992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8faddb2a69e46a27935af8023025b34114327f4808f026d10d1f99c70b4e308`  
		Last Modified: Tue, 17 Feb 2026 20:25:34 GMT  
		Size: 62.1 MB (62127069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deda06a1ba628b8720504ee0255b2498fe029d010a7431ae0ec67bcaccd10fb9`  
		Last Modified: Tue, 17 Feb 2026 20:25:32 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22c1cf06789d551197d8b76746280a6aa52aca8e063bd5aa0e52a71a21080a6`  
		Last Modified: Wed, 18 Feb 2026 01:03:41 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4c61151b5d30632ef9c2c469328b02586c2991b7db033449ae57ebcd5eaa02`  
		Last Modified: Wed, 18 Feb 2026 01:11:54 GMT  
		Size: 13.8 MB (13841445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105fa582f6821f60bf3b0805ae968bf5f3ff02720e133559f9599a3a3f9efef0`  
		Last Modified: Wed, 18 Feb 2026 01:11:54 GMT  
		Size: 243.0 KB (243029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:396e0ea728e9e14cec779150a84fbfe5fedbd71688a699c2156ed7d6007bceb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27adda1c795217266a74fde34382156371280420dd88e6f096e05fe939e68e80`

```dockerfile
```

-	Layers:
	-	`sha256:0a7577fcd874c5c44e7a142dd0ac42ba10c1ff2b448893262ab0b7b6ed8a1956`  
		Last Modified: Wed, 18 Feb 2026 01:11:54 GMT  
		Size: 3.7 MB (3708337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b35efccae8dc03ee628803b5d81933e9d44576ea54a1be71b617f33412a533f`  
		Last Modified: Wed, 18 Feb 2026 01:11:53 GMT  
		Size: 21.3 KB (21256 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:15dc21b439a81684d51bd338557bd121aca1d79b2c73a22f3b7cdd87c9f3e96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113851621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08271e592c177d5bd027579cf31e14dd0068799ebdc31f05ec4f9207641524b5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:33 GMT
ADD file:682bbddd1f3d784d0c4ab5eef9460f0b47a94f3c62f629b59163a7f6543a159f in / 
# Tue, 10 Feb 2026 17:41:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:15:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:15:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:15:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:15:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:15:39 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Feb 2026 20:16:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:16:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:16:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:16:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 22:41:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 22:41:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:41:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 22:41:48 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 22:41:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:41:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:41:48 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 22:41:48 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 22:41:48 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 22:47:10 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 22:47:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:47:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 22:47:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 22:47:17 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 22:47:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e2905dbd81d6a42c24ec5f7ce51f2d8f24a616b4fe2e90d0be791922a8d3b5f`  
		Last Modified: Tue, 10 Feb 2026 18:14:06 GMT  
		Size: 28.0 MB (28004382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9171afe0ea8e4f8900abcc421754e3dd85ec6a08d3673bc5769349efb2e05ad`  
		Last Modified: Tue, 17 Feb 2026 20:16:43 GMT  
		Size: 11.5 MB (11497888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d983ea9b6daf9a46bf6f798d037a31d4526dd821942635d42141409d10e43e`  
		Last Modified: Tue, 17 Feb 2026 20:16:44 GMT  
		Size: 60.3 MB (60322122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92fc68ca54c4d8e5f4365d53a9a49c3568c7ea7c19bf794d35d9714ce6c2d31`  
		Last Modified: Tue, 17 Feb 2026 20:16:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6cf682546b3209bb2edae05b475a871de61f63fee6de9e8a0c61de7c20d69b`  
		Last Modified: Tue, 17 Feb 2026 22:42:41 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3a32580a8d5778a243d0c825c52ae5f8958943b15b3892b985f8532d1c60df`  
		Last Modified: Tue, 17 Feb 2026 22:47:40 GMT  
		Size: 13.8 MB (13809921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a3e9c1d64fa372d12fe8d1277f5d9053bd9a0692c499f16b8aec980452d5c2`  
		Last Modified: Tue, 17 Feb 2026 22:47:39 GMT  
		Size: 214.8 KB (214792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:a00080b15f6a0ffea45d0bbfb9f65c360250ab74e38b4f2a4552ed645b4429ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b5fe288dd19290d95d0b699144477588137bd4197dce22abfb396cc8113541`

```dockerfile
```

-	Layers:
	-	`sha256:f64399ce128ce3a6f9c5aea0350d933b4c5e8f7af13befa316afef81a16d0522`  
		Last Modified: Tue, 17 Feb 2026 22:47:39 GMT  
		Size: 3.7 MB (3705982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c3f876ac753240db50aed87a43f06400ab5d17ed99dd2ada4c1772fd172c78`  
		Last Modified: Tue, 17 Feb 2026 22:47:39 GMT  
		Size: 21.2 KB (21205 bytes)  
		MIME: application/vnd.in-toto+json
