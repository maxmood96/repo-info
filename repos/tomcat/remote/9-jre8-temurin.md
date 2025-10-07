## `tomcat:9-jre8-temurin`

```console
$ docker pull tomcat@sha256:5a3957eb28c6c44421b53ffd42d6fd8d5256081110ba9029c714d584176d091a
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

### `tomcat:9-jre8-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:3f92dd75e0378bad0dbe59a81da57281831af43cb71baf540dc995c91013487f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104929039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c01d082ad5ca469e3927b5035dc671f9cea2c98ca20f31407793ab3a34ee07a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Oct 2025 20:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Oct 2025 20:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 20:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Oct 2025 20:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_VERSION=9.0.110
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_SHA512=5783b88b4bb2fc1dbd10be072deccec0ec96c35b8de09d65b96a8f846e84f4655ddfa43a22e58ace6bf02a653d80629039c733c4b1ff628fa9501048318537f0
# Mon, 06 Oct 2025 20:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Oct 2025 20:03:39 GMT
ENTRYPOINT []
# Mon, 06 Oct 2025 20:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1afecb2aecaac596c3bfe3842e5cdd25fdae298944f8f8f8ce941d10053b14`  
		Last Modified: Thu, 02 Oct 2025 05:02:01 GMT  
		Size: 19.4 MB (19377076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a4eb59f6abfedb4c2e15503e686d83f35646e9702f3ee7abd174c61af5c1d9`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 41.9 MB (41878450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ad0b1647051450112bea139d87be8c7d084c6fa22d0e60e393b94d1c5c475f`  
		Last Modified: Thu, 02 Oct 2025 05:01:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cda57fb713e6613f03d85e519f1c5e599bbb66105a6f537639503fe0019d0f7`  
		Last Modified: Thu, 02 Oct 2025 05:01:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489d883528839414cdd9183c96393205f2f08f0a3b9f414d4909330e5ab02514`  
		Last Modified: Tue, 07 Oct 2025 00:11:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c899789192fb4aa03378cb1ed0fa0e9fe93a07e74ad02ca2bb035a77fa6d235`  
		Last Modified: Tue, 07 Oct 2025 00:11:21 GMT  
		Size: 13.7 MB (13723172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ce911a1d4d015c1720074cec364db9ff5fd2cbbdfbc2c3334ffc9488855ac`  
		Last Modified: Tue, 07 Oct 2025 00:11:20 GMT  
		Size: 224.7 KB (224719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:102e069ee5db9a7932a077988cbe29dfd8d5350c1c827073d5d5f90484f7c06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3397685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4227211c2aa0079dbb25720217dc28535d39320c89a7795939649d00b62bf1c`

```dockerfile
```

-	Layers:
	-	`sha256:d5ad35c360c1dca0e6b4a958c0d730facaaeb52b1dc8461e3b79db76988c6658`  
		Last Modified: Tue, 07 Oct 2025 02:37:21 GMT  
		Size: 3.4 MB (3374579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68123388f3fe2d677aa4c56d176824d83b428b78e16fabe46b647a5b7f929ff2`  
		Last Modified: Tue, 07 Oct 2025 02:37:22 GMT  
		Size: 23.1 KB (23106 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:cbf77b77f18f0c2f76dac41b9260f6a3e213e848783e4218b90d53127186d910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98152954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b274a0d487aa391bb9c80346d242fca93efd98deb23ee522642ad9989c17b93f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Oct 2025 20:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Oct 2025 20:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 20:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Oct 2025 20:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_VERSION=9.0.110
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_SHA512=5783b88b4bb2fc1dbd10be072deccec0ec96c35b8de09d65b96a8f846e84f4655ddfa43a22e58ace6bf02a653d80629039c733c4b1ff628fa9501048318537f0
# Mon, 06 Oct 2025 20:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Oct 2025 20:03:39 GMT
ENTRYPOINT []
# Mon, 06 Oct 2025 20:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e201ca0f5700c4dfb42a2e20c8f7064832cb4964add3dd9466f2ef7ab9cec49`  
		Last Modified: Thu, 02 Oct 2025 01:12:16 GMT  
		Size: 18.1 MB (18086953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09af1ec167544f0c70d5eb5815c417846ba5ca198ffa645ca5d4828784d94da`  
		Last Modified: Thu, 02 Oct 2025 01:12:17 GMT  
		Size: 39.4 MB (39356456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77688559c2befa1abe1ec4b8fae870263b98e1de852d935ec1b4b29fbc59e4ef`  
		Last Modified: Thu, 02 Oct 2025 01:12:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83bc4dd9c54d2ffadd2ff1db237009dcfea98c65a8ec903afefbdaf3d18aec0`  
		Last Modified: Thu, 02 Oct 2025 01:12:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398db291f6a2afd672e50e28d72f6b937ef29ca85cad87b3ed2813e38e874b66`  
		Last Modified: Tue, 07 Oct 2025 00:12:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048ee3c11e83398dcef66e76c3a8f79388639f0daeeca30a9979b3dba4d6e197`  
		Last Modified: Tue, 07 Oct 2025 00:12:02 GMT  
		Size: 13.7 MB (13659149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6df122e119e82d097162b11bc4229fb73c33bb22e6f8799e73539b732cc5511`  
		Last Modified: Tue, 07 Oct 2025 00:12:01 GMT  
		Size: 196.6 KB (196636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:f2e1ebf0fbbe37a1f06e16deaafc7c02939da08711011d70a0cd769260f09f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3403894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4df485263519e4a4d76e568de8ff69bdbc320e9df3592cc8290e97399f1a8f`

```dockerfile
```

-	Layers:
	-	`sha256:e6d9b3e34b7946615e21a3d5e12c5924af25284c126a0df5000474bd6d077baf`  
		Last Modified: Tue, 07 Oct 2025 02:37:26 GMT  
		Size: 3.4 MB (3380620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba95ca2e8bffbb42ef81070a2aa44d9fba7bb86b585e82536eb47ad11ec28989`  
		Last Modified: Tue, 07 Oct 2025 02:37:27 GMT  
		Size: 23.3 KB (23274 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:94f5c01aac89746b6141625d55a88d9c9b0ddd8158bbfdaaf77914f818d1e61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102910071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4704de45b9bbc6a9bb3bd313e443aee4b231505289dc70c53a08899ad798ff`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Oct 2025 20:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Oct 2025 20:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 20:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Oct 2025 20:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_VERSION=9.0.110
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_SHA512=5783b88b4bb2fc1dbd10be072deccec0ec96c35b8de09d65b96a8f846e84f4655ddfa43a22e58ace6bf02a653d80629039c733c4b1ff628fa9501048318537f0
# Mon, 06 Oct 2025 20:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Oct 2025 20:03:39 GMT
ENTRYPOINT []
# Mon, 06 Oct 2025 20:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713d9f39663d7803c802171de8a663ea6fdff2423b056951976cb86e10f4216`  
		Last Modified: Thu, 02 Oct 2025 01:17:06 GMT  
		Size: 19.2 MB (19206399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b3ab79b8c7bf00d47fadbb7f1e0942a7696c3b95236a2f7c74f71e75bd292c`  
		Last Modified: Thu, 02 Oct 2025 01:17:22 GMT  
		Size: 40.9 MB (40880052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12940e96e665f92ef75cca9e1dae2fc33f62da9f85df9d10b4196c8665409dd9`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb1c47183434b3da35f5c777564d1fab2c1f35c5fa4736802568cd072dddd`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588b19e018266f738a0d406d15cb5b9afd4eb7e9165e414e8cfcae45a8aad24d`  
		Last Modified: Tue, 07 Oct 2025 00:17:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfad84a471fa0c8a86c65aa6bc71c823e9e233992d5919e0c5fb9ddc7ae3495`  
		Last Modified: Tue, 07 Oct 2025 00:18:02 GMT  
		Size: 13.7 MB (13734131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a2afb088be89c161abcf92e513875fed77b5dc40403614fdcc97c43192073d`  
		Last Modified: Tue, 07 Oct 2025 00:18:12 GMT  
		Size: 225.3 KB (225301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:365f64ec75efda5a02b592c224ffe35252c686a0379139a78ff5fbe8a73fd2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3399126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f39d2207df3499e9c24a46384d027b4658ecc7a52e0f98b133ce4f83ef8d6b`

```dockerfile
```

-	Layers:
	-	`sha256:cbf0776f9213412aa564959047613efcfcfe0a83e1043013bcc8393d314ce20c`  
		Last Modified: Tue, 07 Oct 2025 02:37:32 GMT  
		Size: 3.4 MB (3375801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1223b5ed9546a237a424cfc6e7e682c672058c354ce6971e758b03522bd04f2b`  
		Last Modified: Tue, 07 Oct 2025 02:37:33 GMT  
		Size: 23.3 KB (23325 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:660aedd2a29138ea9d82432e47c14acde53f6c9051d6862807ac32bd0ecc5ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111018646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d390bad86fc6f8900a4dfbbc76846d104f77b06f2a1b4f84ab28e3533d6ed0cd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Oct 2025 20:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Oct 2025 20:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 20:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Oct 2025 20:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_VERSION=9.0.110
# Mon, 06 Oct 2025 20:03:39 GMT
ENV TOMCAT_SHA512=5783b88b4bb2fc1dbd10be072deccec0ec96c35b8de09d65b96a8f846e84f4655ddfa43a22e58ace6bf02a653d80629039c733c4b1ff628fa9501048318537f0
# Mon, 06 Oct 2025 20:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Oct 2025 20:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Oct 2025 20:03:39 GMT
ENTRYPOINT []
# Mon, 06 Oct 2025 20:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9acb17607aec02fd5fd93f2fde25243ef3044bcb4e30ef1e561b8b40c746b40`  
		Last Modified: Thu, 02 Oct 2025 01:21:01 GMT  
		Size: 21.4 MB (21437493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb07680a2895ddd35ef7cf0dc63655ad52bbfd44aa3e86ede596ebd28d84d5c6`  
		Last Modified: Thu, 02 Oct 2025 01:23:06 GMT  
		Size: 41.3 MB (41259392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003bc824a30982315869d12de137b7aab8fe435295655c7075bafe437e640246`  
		Last Modified: Thu, 02 Oct 2025 01:23:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38931524a6a18a70b1c78a3ac959fa784d35c65bfebab038e3ff8556c27723df`  
		Last Modified: Thu, 02 Oct 2025 01:23:00 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba8ecb10f3435e4b001cb17fb78cd5d96f1a189bd6883a0461af9052af4e7a2`  
		Last Modified: Thu, 02 Oct 2025 14:39:12 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e56fa0b8c808ebbc606baa3c26a0814b814000d58ce053748c1b6a60d627d`  
		Last Modified: Tue, 07 Oct 2025 00:19:01 GMT  
		Size: 13.8 MB (13758753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e2a4b7dce4d041d751370024b9025be0ff722fc742253b41e4c60e85c4bc6c`  
		Last Modified: Tue, 07 Oct 2025 00:19:00 GMT  
		Size: 256.9 KB (256850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:55f4e4d8d5b2c5aae87917d5271ca76b79527de223ac95970bb6c88e1bf2d273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3402570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00083bfbf604bc6e380f384081548870c1c4f7682f0610dba1f87f5f171f197`

```dockerfile
```

-	Layers:
	-	`sha256:b53780cea82db868e477b17d9629c308850b0c4287b0888446714606bc91728b`  
		Last Modified: Tue, 07 Oct 2025 02:37:37 GMT  
		Size: 3.4 MB (3379376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dbaf3488fc1c830e4c02980e5a79982ccccada549a61a4f3957b0d2f4d29cb`  
		Last Modified: Tue, 07 Oct 2025 02:37:37 GMT  
		Size: 23.2 KB (23194 bytes)  
		MIME: application/vnd.in-toto+json
