## `tomcat:10-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:6d4e5cf70fb213ba1716c101f01981e7ee776b9296ccadae485965f3fb7b4d51
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
$ docker pull tomcat@sha256:64f06767654b3dc6fa32da3b3fce3be552032446705297b72d97c348b5cc1e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106692869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4509af60124f099c82942c3309dcea909de92c20c8a03e94b2b702a4c0da88`
-	Default Command: `["catalina.sh","run"]`

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
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9f253e30bf10597ab51cfeae198ac65b228e577750e871c097150cc79a060d`  
		Last Modified: Thu, 24 Oct 2024 00:56:53 GMT  
		Size: 16.1 MB (16142360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8233e39bf60fa5622425c07f933fcf0d9b21271c01769cecb8142d19a6d3c`  
		Last Modified: Thu, 24 Oct 2024 00:56:53 GMT  
		Size: 47.2 MB (47216714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59d22db63f3eb3d77e5b705449730b93d844bcfa1ce1f13df22d49f13d15606`  
		Last Modified: Thu, 24 Oct 2024 00:56:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80a9c727cee83bf408beb00d113d06d03954eb063419370a72b7844400e2d79`  
		Last Modified: Thu, 24 Oct 2024 00:56:53 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a15ff5195016f8d10ec92f5676fa6f8bf6c3d46a527538d0b34bd25e2dba60`  
		Last Modified: Thu, 24 Oct 2024 02:54:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad72650e06657ce2e11c2726acefe9551c59262e1964aa1fd73131ff0f0399`  
		Last Modified: Thu, 24 Oct 2024 02:54:14 GMT  
		Size: 13.6 MB (13566322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a328b3a10561d4027f1032de4bf38e3ef79e1dc0bd1b40fbda8e735a5ffe42`  
		Last Modified: Thu, 24 Oct 2024 02:54:14 GMT  
		Size: 229.1 KB (229144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7e2ece7a673b915206983e23fa88fd0c7a1ccd321db1554ed0078a1f6cee0cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b55ea8f20e6f5a3e4c003103450ac35b2f7220fcaad8a9985eae2c263fa193`

```dockerfile
```

-	Layers:
	-	`sha256:ad6f7a4463e2e7c7329ade7d9b0b8f9656c13c5b3543425c330b6679a6015baa`  
		Last Modified: Thu, 24 Oct 2024 02:54:14 GMT  
		Size: 3.8 MB (3785671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06dd56e142440ed85b578643a615ebee4a8f5ec98d108a2746a195bdc151c47`  
		Last Modified: Thu, 24 Oct 2024 02:54:14 GMT  
		Size: 21.8 KB (21778 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:99568324d78fc2991275a3244e9ea4997ee08614c07d309a8642370c2c39b293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101611722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4310c997ad1fead5b7c42098a8c7dcf645c7f066333798027359d6d3fcedbd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed86084ba4ec44c57061b2db095ef9690641a41020a61ffaf80be611a6be6241`  
		Last Modified: Thu, 24 Oct 2024 00:59:31 GMT  
		Size: 15.9 MB (15891671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bfd8d4469ca05e8d1cc250f43590a657c78eb92464f4124149cbc4cb84cece`  
		Last Modified: Thu, 24 Oct 2024 01:08:03 GMT  
		Size: 45.3 MB (45332427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5965f7813011785b126509aefedb841cfdde9e1a684a5f44fb2392df1a4f849c`  
		Last Modified: Thu, 24 Oct 2024 01:08:02 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa32df3ceec8af6367522db81498aef990a43c02534b21a68c22f0eb7cbac0d`  
		Last Modified: Thu, 24 Oct 2024 01:08:02 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723b5a322a6b249ffd5f2f9d069f194f23cbb5accb8596d9b746f519efc8fa1d`  
		Last Modified: Thu, 24 Oct 2024 02:58:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db79ff8f1d1aca2a72c60a877b2e53a98fe18635a93a4941195c474a7cf63c1`  
		Last Modified: Thu, 24 Oct 2024 02:58:02 GMT  
		Size: 13.5 MB (13543605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e606241199180228d7a9e401644932efc9b3db73ad5ad1c5286d53738dd3d807`  
		Last Modified: Thu, 24 Oct 2024 02:58:02 GMT  
		Size: 202.1 KB (202083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:400f3202ecc69f90b09a4ee855ad8d0f7ceef26ada26ddda63be81b8a59c477f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b23ccfab2fc0a0934046068c21b10eec8d36471a07da784799b440c3f7907f`

```dockerfile
```

-	Layers:
	-	`sha256:d312eeb5da3bea0bf87714deda6782a0e51239a50114e03570089781159354e5`  
		Last Modified: Thu, 24 Oct 2024 02:58:02 GMT  
		Size: 3.8 MB (3789270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08da80f2ea08d2963a5812fa034c0af14dc5e0ca99baeebaddb986723f7de9f`  
		Last Modified: Thu, 24 Oct 2024 02:58:01 GMT  
		Size: 21.9 KB (21894 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:5b12db32db56da6908f51a005e583fb56545fe148300a9275865f87e9ba8ee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102796754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c4f7a5e48d937bae11969beaea877c05a3f5f2c845567d1f8159432b409038`
-	Default Command: `["catalina.sh","run"]`

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
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:2df4b49837842cfab8a95fec666778763869dffc44881af662c920632ae031b5`  
		Last Modified: Thu, 24 Oct 2024 01:06:21 GMT  
		Size: 45.6 MB (45576593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ec09f4527c9ff858afbd6c055995c0e8a4d9d97ea97cf12b1b94149cf94c9d`  
		Last Modified: Thu, 24 Oct 2024 01:06:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d5bbc6a56336b0b3fcb22659e14fab1d3b2fdc016b66655dcb9b28a075bb68`  
		Last Modified: Thu, 24 Oct 2024 01:06:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1e31da5d5daad486b814a30e886080a32c031586faf7252a80bcdeb22fcd4a`  
		Last Modified: Thu, 24 Oct 2024 12:37:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15690c8b2841b67c761ef6e3b8117f62ed9abe56c2b981d268b60df6c725ebe3`  
		Last Modified: Thu, 24 Oct 2024 12:37:32 GMT  
		Size: 13.6 MB (13568694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a220fd4ba70347b57834cca791081ccfc741a886712ed4a856dd295639a49a`  
		Last Modified: Thu, 24 Oct 2024 12:37:32 GMT  
		Size: 228.4 KB (228370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4fd30d714ca312a1e0b15b269c71054ca32d64807da27ea545ef2490b88ab0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12eedc5f75c2f0111109cc1e7c2a51425c4a7cf0f3cfdb2a8db9062f9d95d29`

```dockerfile
```

-	Layers:
	-	`sha256:9c59ae7db9771462d8353fe5fe2ab3f9dd792dfd2ee839675b896031c90b167a`  
		Last Modified: Thu, 24 Oct 2024 12:37:32 GMT  
		Size: 3.8 MB (3785957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9788cb11b0e633b32e017fb72587a0f97282c36f82c83ff5365bad5804a5589`  
		Last Modified: Thu, 24 Oct 2024 12:37:31 GMT  
		Size: 21.9 KB (21926 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:5ef3937cdbd02029aabd469bd0c8b9bae21e459bc121840b3a3ee2620f8aea75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108617926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e68032d1888e36a09714773eb92130a556bae9679e10fc08ab99c2975c688f7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b325b4835c7b63af6942a8011aff4e2d93be2d7ccdd1217727fb765f060cc81`  
		Last Modified: Thu, 24 Oct 2024 10:36:30 GMT  
		Size: 42.7 MB (42675208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950f42f43a2afcfe1dcab0b6b3bb6f691eaba252fc112f758bf801fcb8bfb078`  
		Last Modified: Thu, 24 Oct 2024 10:36:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a9b0fda34cadcc76588c178b936b186f77dd2a589dd21f772fd4bf2d3414e1`  
		Last Modified: Thu, 24 Oct 2024 10:36:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0369aa63e63c10ffadf1ab031850af374ac5507ba87c52b317ff2e6c9a26419b`  
		Last Modified: Thu, 24 Oct 2024 13:04:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8945c83bbd7bef1075a8b60d9b802b74bbb848aa8b1b953256e8b60a05713fd`  
		Last Modified: Thu, 24 Oct 2024 13:04:16 GMT  
		Size: 13.6 MB (13584058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b38449c4ecfa554d8f927627dc278dddf03856308fdb63ec93544a62ca5a3b`  
		Last Modified: Thu, 24 Oct 2024 13:04:16 GMT  
		Size: 258.9 KB (258870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:906ff215416b4d00281e39898f921d3b0992d6db4d51e4b46b82ea25466bc475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2312ab25a29e7bb85e22d55f540226299338345835a10bfd44b1d79bb67cddc7`

```dockerfile
```

-	Layers:
	-	`sha256:8911a8a701ab582f07ecafa10c58622dca11681143a227512a3a3c1d6168bc28`  
		Last Modified: Thu, 24 Oct 2024 13:04:16 GMT  
		Size: 3.8 MB (3789611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf737c46231afd779bac91671db6178219f508e359fb9396a5f0795dc14ffed8`  
		Last Modified: Thu, 24 Oct 2024 13:04:15 GMT  
		Size: 21.8 KB (21830 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:330a720b5e91067db85cd3d47b80713081275fb6fcdf419fe65fee9fd0fd8e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98788948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa006d278776257b4ae194b6cd2a2a342297147157ef62b60b31a4c465acc63`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9994cad72290d99d0275f342ad14206d889a15e886b2243fd599e3d74aeac9f8`  
		Last Modified: Thu, 24 Oct 2024 17:04:51 GMT  
		Size: 16.1 MB (16141938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5e0f6193e73bbe6dba381f5b604d78c687fb568a3426004724906455c5b2b8`  
		Last Modified: Thu, 24 Oct 2024 17:12:25 GMT  
		Size: 40.8 MB (40840105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608df4b783f11f89006ecb3fe175ffb71fddf64ebad8ab1caf4d45a77259beee`  
		Last Modified: Thu, 24 Oct 2024 17:12:19 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4efa76e38434b60e6982fdefcf54fcea4a600ab20ccb3cd2597d69602f0ca72`  
		Last Modified: Thu, 24 Oct 2024 17:12:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc82571d253c3a3d18b2a2bbfe191d3c9089727c9201533472f17f1c4e080dc2`  
		Last Modified: Thu, 24 Oct 2024 21:18:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8395abdef23649f8179944759b786f3fcbfe45fe7d8d966c4137994c6977485`  
		Last Modified: Thu, 24 Oct 2024 21:18:42 GMT  
		Size: 13.6 MB (13571661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4927286b5b99c74b95f6057d6baa500d52a8f38e15d6551d82f22293a68d60`  
		Last Modified: Thu, 24 Oct 2024 21:18:41 GMT  
		Size: 231.1 KB (231125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:444d66c876fff1d6cfffca1904e3490d2ef09487f873ff1df2bacbec29ac85ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9570958b3ec326edad79cc101da170f11745b56929bc5101fd86a573753be5d0`

```dockerfile
```

-	Layers:
	-	`sha256:e23ade7f0d330b53f64f0134a54744077d9250cb64f9bdf8cf14c48722520242`  
		Last Modified: Thu, 24 Oct 2024 21:18:41 GMT  
		Size: 3.8 MB (3787271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63d123b15c52003f5bfc1eff3d3e8e1cd14132ebdf2dc3fa21cc7916e3a8f6f`  
		Last Modified: Thu, 24 Oct 2024 21:18:41 GMT  
		Size: 21.8 KB (21778 bytes)  
		MIME: application/vnd.in-toto+json
