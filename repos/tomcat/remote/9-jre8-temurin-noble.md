## `tomcat:9-jre8-temurin-noble`

```console
$ docker pull tomcat@sha256:10892583c27fb00cbf7e8041f36c6fb3efcd8bb4f672c88b131f15f5fc4b6987
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

### `tomcat:9-jre8-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:f9efa646368d3bf06ab9ee87e9ba3cb97759d31ac435c178f3e29b2dcf5973a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102544473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66d89274ddcbb50a4430cb8bab0c553a931368ce6b14be9b9210d3f095e7a47`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:56:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:56:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:56:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:56:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:56:44 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:56:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:56:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:56:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:40 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:40 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:40 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:41 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:47 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ff51bd88b17a4b71c3855e946e7d0a32ce8fd47acf57730e221abbf02a5500`  
		Last Modified: Sat, 08 Nov 2025 17:57:10 GMT  
		Size: 17.0 MB (16972115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d085363653f2a2c7b1fac6006bd16615f2db16ed021027b0ec645bfe99da07`  
		Last Modified: Sat, 08 Nov 2025 17:57:11 GMT  
		Size: 41.9 MB (41891236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccbd3e9ed5a3534b12f7269822387c33fd2c2c75e624afc9089be4bf02a9d66`  
		Last Modified: Sat, 08 Nov 2025 17:57:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c2f322c6eed60599c95fb313afb8bd8918a5aafc2cb907c59e86c5259a703`  
		Last Modified: Sat, 08 Nov 2025 17:57:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687f9f1482c38e0d7a3582a15c5ac723b56f6e1f4866ee47a904cc54ebd5e5a2`  
		Last Modified: Mon, 10 Nov 2025 19:13:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d89c8b34741ec7944ec47c80954c86a60fdd79a111dc45814801566c02f8f`  
		Last Modified: Mon, 10 Nov 2025 19:13:01 GMT  
		Size: 13.7 MB (13730597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa5921c2237247902b25ab5d9bb95e07929f983fda80f9c489cd14d21bedb7`  
		Last Modified: Mon, 10 Nov 2025 19:12:59 GMT  
		Size: 224.8 KB (224768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:fa698b94f3db38490d629613b3bc8dd23895b28ca6b629928d0aa790b890bd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3397642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a93b02c3a41437e84ad8cc649fc685704c4ca8ec78f4f5c817fe587fb1f936`

```dockerfile
```

-	Layers:
	-	`sha256:2603099a1538be5315c54f8d244a9c75205476cdb6bed9bd8e2ef87e76605f88`  
		Last Modified: Mon, 10 Nov 2025 21:48:16 GMT  
		Size: 3.4 MB (3374579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2977ee8b99bcfaa9689c68870f10454412f63b372fc72c9c7614f4cbbfa9f761`  
		Last Modified: Mon, 10 Nov 2025 21:48:17 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:3d6ce7634d8edd733e0f1fcd7ba1405073b4bec50f88d089c39a97d1fe1b641c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96396210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2b295de894d28f4cd1d7ed2e2ce59555234bcd1a64fe2e1d7dd46484cc28cd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:36:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:36:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:36:57 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:36:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:36:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:36:57 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:36:57 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:36:57 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:36:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:37:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:37:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:37:06 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:37:06 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:37:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e99228d18f80bd71885fe31ad1cccade678da80e35309de81248451ddf6b92`  
		Last Modified: Sat, 08 Nov 2025 17:53:47 GMT  
		Size: 39.4 MB (39374179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164ad8bef43a6c29cfbebdda16f8171632e8761252efe5b6294ba6b90eecbfce`  
		Last Modified: Sat, 08 Nov 2025 17:53:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68884063f83e88a7846491ea335d47335bb5610150e04132d971092466b6350a`  
		Last Modified: Sat, 08 Nov 2025 17:53:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7b0c3a70bbf7b475cfc1501c07160b649fe75ee0da32240f5db8fcce4b3576`  
		Last Modified: Mon, 10 Nov 2025 19:37:19 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faf124b9642af7fafe0b0c5669583cb9eebe89b7eb8b307223d3fd34f90511e`  
		Last Modified: Mon, 10 Nov 2025 19:37:28 GMT  
		Size: 13.7 MB (13664230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999b7c4d17e9716f6b960a5cdaa74e8fe19c2cf6ce6293487b7c09560e2e975`  
		Last Modified: Mon, 10 Nov 2025 19:37:19 GMT  
		Size: 197.0 KB (196963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:c6c54544c07a209e6cc20ccd5220c566c949bea12dc96238b728c8abea3b76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3403851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7ec10fbb533a2066859bada9283e8db1877a3134fe35387651ed26812b71fd`

```dockerfile
```

-	Layers:
	-	`sha256:459295a1733fc1366ba6c663977cb9202f5b0f13af37778b763cfa92a3380317`  
		Last Modified: Mon, 10 Nov 2025 21:48:21 GMT  
		Size: 3.4 MB (3380620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca42278fc5866ac11a2540d62714bfa63387f214d49325d3c91cd7657fd7c4e5`  
		Last Modified: Mon, 10 Nov 2025 21:48:22 GMT  
		Size: 23.2 KB (23231 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:886cbd7734aca16c3a8d104820a66bd0ecaaec2deecd08aa7094d6e1acda6e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100701584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268c99b547da8f27daee8b4253ce90b2f7329b58158a155dfa10bce03095944`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:55:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:55:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:55:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:55:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:12:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:12:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:12:11 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:12:12 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:12:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:12:12 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 19:12:12 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 19:12:12 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:12:12 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:12:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:12:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:12:21 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:12:21 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:12:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71ec760f0edecd945494f78573e581ac956b186ac2427ae2556a154015d6ddb`  
		Last Modified: Sat, 08 Nov 2025 17:55:55 GMT  
		Size: 40.9 MB (40884346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707ff7a3bc37e72f31e6be8a17f71c4ae76d37e953e78a3bbfd2ace40f6970bd`  
		Last Modified: Sat, 08 Nov 2025 17:55:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d17d2cf675ca4803bedad41d2b12efb7f511d661215860b0a0856e84d3059d3`  
		Last Modified: Sat, 08 Nov 2025 17:55:52 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8731d47e7cf3965a99e06f992e1c551b8dd6fe7172ae075e3f6e65b831335202`  
		Last Modified: Mon, 10 Nov 2025 19:12:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f656498d3db8102df611a2a1521014b04c1812da5dd486a411b6ac38fb0d2c0`  
		Last Modified: Mon, 10 Nov 2025 19:12:37 GMT  
		Size: 13.7 MB (13738157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687f2f3b74afcf268ab553fd2efe34ca4c11f046304f3a10d6963369097fb805`  
		Last Modified: Mon, 10 Nov 2025 19:12:34 GMT  
		Size: 225.4 KB (225429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:8d77210e455de7b0d6986b6c8246a0c3dfaea5c7bdbc151df0a81c1c39750815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3399084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd974c907275bd9ebb1484e7f33ecd251832b603369d8f85608e50d40836232`

```dockerfile
```

-	Layers:
	-	`sha256:c76a120ac0fe910bb43387e7b904a736aad62de83e38ed924d91f2c1fbd1afff`  
		Last Modified: Mon, 10 Nov 2025 21:48:28 GMT  
		Size: 3.4 MB (3375801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9055a3a098d1dd6378cc446a53146403eaec30b79101b5c4efcbd6595f787b0f`  
		Last Modified: Mon, 10 Nov 2025 21:48:28 GMT  
		Size: 23.3 KB (23283 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6cb421978e6976717cf203bf225d790e7abe6ba73535dee18f4ef13cad1df675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108413440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efec8f3581307a8fd72d221a3b47cbe30ce8e4f671331e27a2e442e04dc8819e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:59:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:59:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 23:14:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 23:14:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 23:14:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 23:14:20 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 23:14:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 23:14:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 23:14:20 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 23:14:20 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 23:14:20 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 23:14:20 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 23:14:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 23:14:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 23:14:30 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 23:14:30 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 23:14:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c3c84c9145d6e39b87361420c42775001b0a5d2bff0b29876f0b582e69bdbf`  
		Last Modified: Sat, 08 Nov 2025 17:54:48 GMT  
		Size: 18.8 MB (18814703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ac7106938414735c0bc6417599932a3e2543e7409ebe13cb3b62358287bbf7`  
		Last Modified: Sat, 08 Nov 2025 17:59:42 GMT  
		Size: 41.3 MB (41272782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5049b18c741ef343d4e70e9bb3202cec0db70373e5f962a8abc3781a655ddb10`  
		Last Modified: Sat, 08 Nov 2025 17:59:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97270f3a142f619a4953f403ce8eca73172ce02af5012f253e5f33db1187043e`  
		Last Modified: Sat, 08 Nov 2025 17:59:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caeba1b131105016b36ee9591abfce1dfbc5fd008d5a1363987452f3fe0c3ce`  
		Last Modified: Mon, 10 Nov 2025 23:15:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df234727e5bfcec4b6d84c4f15cb3cf2bb9080129aeb11daa2f2cb45e1124de0`  
		Last Modified: Mon, 10 Nov 2025 23:15:09 GMT  
		Size: 13.8 MB (13763214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e104d405c66e698014aca8c606be897c94313f5381d31ba3cd74b022781ece`  
		Last Modified: Mon, 10 Nov 2025 23:15:05 GMT  
		Size: 256.6 KB (256604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:6626ed459c04b5d0e932eec3c89f2475839d9edf6e41c00ff39d650593232e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3402527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dc92b8792462d8ddf2b3ef8665ac630021670c64d8f77e19a162ae8fd615c0`

```dockerfile
```

-	Layers:
	-	`sha256:8f62fce85808b24b24ce227e8a2863e0c7d20af15d3d721de491d4c3b2422dff`  
		Last Modified: Tue, 11 Nov 2025 00:36:20 GMT  
		Size: 3.4 MB (3379376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea498631b35598cb2bc3707beef7c976608c1e5c0cfc5167ead4d52a89f00d2`  
		Last Modified: Tue, 11 Nov 2025 00:36:20 GMT  
		Size: 23.2 KB (23151 bytes)  
		MIME: application/vnd.in-toto+json
