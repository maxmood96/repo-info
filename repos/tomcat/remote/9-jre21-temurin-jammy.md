## `tomcat:9-jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:1402424419a2d7219c8fd84abc894ddc2f18544dbfc203a72b6aed0e09072a35
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

### `tomcat:9-jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:6d2105e246211a89f388d384aab045fbb5a05d73b714029eb69b3ec2c973bb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112669549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe434c3231adbe73c3d07b2641ef4aae3cc20c099ba6f70a09abfd934d9616c`
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
# Sat, 08 Nov 2025 17:59:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:57 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:00:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:34 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:34 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:34 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:34 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:40 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2efaf4f7327a471e1b969eaddc7e44e5ccae0df783fcaa48bf94864d07a0d`  
		Last Modified: Sat, 08 Nov 2025 18:00:21 GMT  
		Size: 16.2 MB (16150304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c0a6ab39aeac3774dd534c27427e0d533f07a637624ab254c6849bda796f16`  
		Last Modified: Sat, 08 Nov 2025 18:00:28 GMT  
		Size: 53.0 MB (52978483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f2a033ca8df84c1a3081f8ef917342b430ebdc1587bedf05eb381e45383ac`  
		Last Modified: Sat, 08 Nov 2025 18:00:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3096c0eb2bbc9ac33b0cdb8552433f874659010096eb476cdd53f1aae60a3`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d584b51c8da34d40b97bb029099fc24cf197e6a5e355b132986dcf82d5d9ddca`  
		Last Modified: Mon, 10 Nov 2025 19:12:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f2979502c9fa8dc18c7f6d956b3c68a1d4bf7e43ffa675d35c166b6c62d5a2`  
		Last Modified: Mon, 10 Nov 2025 19:12:57 GMT  
		Size: 13.8 MB (13771618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da436420fc5b34ff72f6401a1ac15d0bbf2a384f043b3e41e440e5b0275b2bb`  
		Last Modified: Mon, 10 Nov 2025 19:12:52 GMT  
		Size: 229.7 KB (229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:70a94d457e27dd08ff142b174ae4d7daff9756471d34734eff25fad4b5e4c1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194e66a3a2ef2c83029621fa9e51aa11f0dd09eee2f1232f423302c7104995af`

```dockerfile
```

-	Layers:
	-	`sha256:bcc46f26860f008390a27370123e14401048204c7ede33ce192db008fcca57c5`  
		Last Modified: Mon, 10 Nov 2025 21:47:34 GMT  
		Size: 3.9 MB (3939763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:983df2a7796f7d83f9262de9644a474319c822984ce41c8824dcba499b542918`  
		Last Modified: Mon, 10 Nov 2025 21:47:35 GMT  
		Size: 21.2 KB (21213 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:5f12dd0513aefa2a347e810fc82ba34346473046b286a9f230476836d5eab294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109607635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19331b9af841926094f293d1b5a581b11bb3ac0fac653a9025d2566c305f13eb`
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
# Sat, 08 Nov 2025 17:59:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:13 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:08 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:09 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:09 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:09 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:09 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:15 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:15 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028993be8a76c7119b0d8ee582ec1146a4a9da89a2876287461de42112766642`  
		Last Modified: Sat, 08 Nov 2025 17:59:53 GMT  
		Size: 16.1 MB (16066196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf12991e52872631db4f5866423e61c9aa264b18e7b99735b58d5e9b7424ea`  
		Last Modified: Sat, 08 Nov 2025 17:59:52 GMT  
		Size: 52.1 MB (52148599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e39452ec2196b4a744bd1ec7029e928fad324f4e0aa146be26945045f2e628`  
		Last Modified: Sat, 08 Nov 2025 17:59:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c83d3140bc0663488b5277b96f30f09c76765775b653007c9573825d31d1e`  
		Last Modified: Sat, 08 Nov 2025 17:59:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d48d98dbe63d150194b4d030a4fe1f23780056b8d98dd7f54a754dc1359812c`  
		Last Modified: Mon, 10 Nov 2025 19:12:30 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adf759afbbb727cb54590a4f41d2193f6cfd2733dd1acda8e5a6a973d6361a2`  
		Last Modified: Mon, 10 Nov 2025 19:12:31 GMT  
		Size: 13.8 MB (13778360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71b446d096b36d184382547e44fdbbcbf529ed3dc3a630099c5b3396360dfe2`  
		Last Modified: Mon, 10 Nov 2025 19:12:30 GMT  
		Size: 228.7 KB (228732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:41e60e8c826abf2d658e8c0ef5d73fb3f327dfad61177100076854ff69443244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda4eb219cc1b0b037b3896cbdd6dc08e77020526bee57a4a21b9299704b0964`

```dockerfile
```

-	Layers:
	-	`sha256:ec8bf3ae76217c7f144e53ce5b80ea5edaa852458660a4d9cf2efe369f6ab559`  
		Last Modified: Mon, 10 Nov 2025 21:47:40 GMT  
		Size: 3.9 MB (3939432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4778dbe13fdaf89098d353d70c173b101c670c89dbe51103089673a0224cba1b`  
		Last Modified: Mon, 10 Nov 2025 21:47:41 GMT  
		Size: 21.4 KB (21361 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6632325f507af8aa82239feebf143fc660499344bd3640a2e55a937af49be763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119116673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62486a81e3aba4935b5cdbf8c89e2e106be693571a6dafe1fe3125bbee6d747d`
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
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:24:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:24:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:24:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:24:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 22:17:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 22:17:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 22:17:56 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 22:17:56 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 22:17:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:17:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:17:56 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 22:17:56 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 22:17:56 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 21:21:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 21:21:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 21:21:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 21:21:52 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 21:21:52 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 21:21:52 GMT
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
	-	`sha256:5d2b78bf7aab04a664cba36d3a00b803683e45f2509dcaaaf6711c89e62ffda7`  
		Last Modified: Sat, 08 Nov 2025 18:25:32 GMT  
		Size: 53.0 MB (52985421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fd3523dfdca913e474ed23a2413af62b065c5e1ff96d42a473f876344f5a89`  
		Last Modified: Sat, 08 Nov 2025 18:25:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ea43d7efcd5fae4c426465a27fab42a8acf9b890aecc7b1b83fbdab38a12f`  
		Last Modified: Sat, 08 Nov 2025 18:25:28 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662fdb4c90c3cd9fe15e800f0686e1396c808a63ddeb04e761a7be739874774b`  
		Last Modified: Sat, 08 Nov 2025 22:18:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f531cb1fb7bbabef9093c68ecddecd74dca3da66dd5ff52480d675febde4e5`  
		Last Modified: Mon, 10 Nov 2025 21:22:16 GMT  
		Size: 13.8 MB (13799074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50c3b41c523ac39e1ade32a649addf2738d9cf46aec4ec14fefcf9518dd2fb7`  
		Last Modified: Mon, 10 Nov 2025 21:22:15 GMT  
		Size: 259.1 KB (259071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:06edad7fff8e8963b4d5d9a04c3cd27112d1451d4557e737437024266a1da74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28dfaa19244e372cbe87c8b79c6e7db94f21e83a9eb6262f85957fa10b190b6`

```dockerfile
```

-	Layers:
	-	`sha256:fc3dce5c2f9d4f2223488131850af7dbc9e922546c006622ce2a4277c673073d`  
		Last Modified: Tue, 11 Nov 2025 00:35:53 GMT  
		Size: 3.9 MB (3943851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1c5ff23b4f2bd416fb31a1f82c64e982551a6d335948f6c020d5efdf8d2934`  
		Last Modified: Tue, 11 Nov 2025 00:35:54 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:a54d947369c51a24035c76bcfe0c5257779e30754f90d4fd5c7966919cadf8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107675246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006197f7d48028248f59c2dfae3ff3a008a270ef9391dee01335d42afc00aa11`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:11:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:11:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:11:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:11:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 20:20:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 20:20:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:20:08 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 20:20:08 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 20:20:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 20:20:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 20:20:08 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 20:20:08 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 20:20:08 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 23:29:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 23:29:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 23:29:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 23:29:30 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 23:29:30 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 23:29:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a2a6650350741188bf24b297683b9031848cb94d72982191b1b30d174aad27`  
		Last Modified: Sat, 08 Nov 2025 18:12:17 GMT  
		Size: 49.5 MB (49521841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc96255305ecee9eeb584c51faa2a7c2cd7fe3906e10ffb2e1dc5203255bf65`  
		Last Modified: Sat, 08 Nov 2025 18:11:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4946814d629f38c2f3523ff15b7b2e63c20e31bd10dbd0b1f4f0c332b3c29bf`  
		Last Modified: Sat, 08 Nov 2025 18:11:58 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2221c80d1141d63289eff94cc07b2d04230489e79e7ecd1546e6965432c024`  
		Last Modified: Sat, 08 Nov 2025 20:20:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b87138db557ae750f7dfdbd0e44a82a00cf5bd4d35ca8e30203f03c7362c595`  
		Last Modified: Mon, 10 Nov 2025 23:29:51 GMT  
		Size: 13.8 MB (13766907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917acf150939c4a5ffcc164adfd325c26bf1db1357bbe071efc0a0b0f6f74ff3`  
		Last Modified: Mon, 10 Nov 2025 23:29:51 GMT  
		Size: 230.8 KB (230828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c2a371b19e9f7cd617035b1069d59218aecf7400d8e56a62066cd1266bcb7655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665811f2dcf86c76187532a37ed57b85ae3f6d8fab404d421b75608bcdb28107`

```dockerfile
```

-	Layers:
	-	`sha256:5fbc8807b5a28df23cf40d5e50e5ffe26fed3a74a59eb4507d0a215a29d0f338`  
		Last Modified: Tue, 11 Nov 2025 00:35:58 GMT  
		Size: 3.9 MB (3941354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80feed308562f45980df6646050a87f90158c47026904d24f717dba743f6928`  
		Last Modified: Tue, 11 Nov 2025 00:35:59 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json
