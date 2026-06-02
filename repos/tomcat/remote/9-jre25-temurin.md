## `tomcat:9-jre25-temurin`

```console
$ docker pull tomcat@sha256:4becb4570daf0fc516a334c0dc7df8dbf09ecef903806a57d35b5708c5e10362
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:9-jre25-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:cb602b78b0437fda77d7e35047e67e62ec65825314be9b3cd4a19703bcc2cb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118265427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cda34c4b307790cf9a86242d7b3c5d24ec896c13669f09a027286938bf3428`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:55 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:15:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:17:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:17:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:17:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:17:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:17:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:26 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:17:26 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:17:26 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:17:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:17:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:17:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:17:32 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:17:32 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:17:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d0df2f6a2ab4ebe6312620361d10bc95934f9c0b214263709202f165ca7dd2`  
		Last Modified: Tue, 02 Jun 2026 08:15:22 GMT  
		Size: 11.5 MB (11481021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9506eaedce63a0941d41b9b3b7f027e715f7d4724bb184a69093d8bfc11fac`  
		Last Modified: Tue, 02 Jun 2026 08:15:23 GMT  
		Size: 63.0 MB (63042669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c6a52a9f2d0a2c17c05bbf39b1d11933cf0c821cc38a4d29de0b85597dd6c0`  
		Last Modified: Tue, 02 Jun 2026 08:15:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c678f915c60f31ba3661799ca1d20192b5b909872ec7d3f608df40a27a4ac682`  
		Last Modified: Tue, 02 Jun 2026 10:17:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da7a08dbdd1fd7a3cff70eb4ce86aef84790c43f82301bbe3ae8be647d0295a`  
		Last Modified: Tue, 02 Jun 2026 10:17:42 GMT  
		Size: 13.8 MB (13798745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9823da11ab3883d07aee4721faf326b6b507097ad66750bbaa4bfaf95793c77f`  
		Last Modified: Tue, 02 Jun 2026 10:17:41 GMT  
		Size: 207.7 KB (207671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:d8894ea38f04565003d4c9a82bc74d281c95025eed20d316500557dd8ad6b28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6795c78e9aef9abf0263f3415305dcbaf80ade365dfb6a8514bf8adaa7b2c1d`

```dockerfile
```

-	Layers:
	-	`sha256:e1baf58ae98feb3c4f48b6e79ce7d69a90be694a4f6c45493cab9e1e5c4c6941`  
		Last Modified: Tue, 02 Jun 2026 10:17:41 GMT  
		Size: 3.1 MB (3125659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e1cdafc111402d6ebd7ca517a9fff3ebbe9b4d5088b4b7687a50d4c87bfe83b`  
		Last Modified: Tue, 02 Jun 2026 10:17:41 GMT  
		Size: 23.1 KB (23082 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:ad31a17ef4ac1025dcf17379e5e743c270f1efbcd08975f874a40dabff3bc456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116315008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dacbe1d92d61380ad1a799fec2147a54f888858aea81c22bbae3719432c6dec`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:20 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:16:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:46 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:46 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:46 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:46 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:53 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:53 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b7f0fccaa95dd1f467cb56660e823611c5dceab12394080192b2d096b51837`  
		Last Modified: Tue, 02 Jun 2026 08:16:50 GMT  
		Size: 11.5 MB (11476696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedcf77a89a74305c7149e84edf17b9eead7a533f590a7794436a3ae0ee0e8c3`  
		Last Modified: Tue, 02 Jun 2026 08:16:51 GMT  
		Size: 61.9 MB (61943121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de26c161c75c21efc1e78e614f5b450580938483d69ea769b709551852428c24`  
		Last Modified: Tue, 02 Jun 2026 08:16:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c15b08984fce3840d6480b22893fa23e3cb98026424357578ed1d266b69d004`  
		Last Modified: Tue, 02 Jun 2026 10:13:59 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245050056f1568c3e2a37641b3993329b088b5e75cca9d2ba42066e19045d138`  
		Last Modified: Tue, 02 Jun 2026 10:14:02 GMT  
		Size: 13.8 MB (13808992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fa0b11b11a21554ec392ec98a0df5e820f859f26c93a52089b679d6b51be6d`  
		Last Modified: Tue, 02 Jun 2026 10:14:02 GMT  
		Size: 207.3 KB (207275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:08d2f93c50fbeb2e467e5d55ab6179492a3c32ebd48038ba4eeca67add267c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b8a514624368aa1d9df30ff54afe7b42c487bb2f2b634896de6e0f65834982`

```dockerfile
```

-	Layers:
	-	`sha256:4c5170d09c79d868bdaaeff25dd4d2ab3e65019becd3b890806de05c5d340149`  
		Last Modified: Tue, 02 Jun 2026 10:14:02 GMT  
		Size: 3.1 MB (3126169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1581cb62bc51dc2ceed8f58a79a8c12200ed5e45fbb12f4142911965c7869bc`  
		Last Modified: Tue, 02 Jun 2026 10:14:01 GMT  
		Size: 23.3 KB (23302 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:b55a9e83fed6fb74e3df4e7662283baccf7f850a466f34b65c104314732796f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122881430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07576a4dff311ee612c8193cfdd3193b7fe4af33c3c0dd0e43a9a1eef900070`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:33 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:15:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 11:09:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 11:09:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 11:09:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 11:09:58 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 11:09:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:09:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:09:58 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 11:09:58 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 11:09:58 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 11:12:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 11:12:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:12:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 11:12:16 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 11:12:16 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 11:12:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14555f1475b5161df9db41ed4a7e500e82373184731715cb4aa463c046a5eb8d`  
		Last Modified: Tue, 02 Jun 2026 08:15:28 GMT  
		Size: 12.0 MB (12047670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f4460cf7c7d2f0cdcc8e013a547be64a5626d1a813f4b843da16b4ab31dc26`  
		Last Modified: Tue, 02 Jun 2026 08:15:30 GMT  
		Size: 62.4 MB (62442841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e0bf549bb69914d40c79d648069e4c5e50b2e7b21e3c22e32064475d65a878`  
		Last Modified: Tue, 02 Jun 2026 08:15:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070ec7eeef643528f42e1007447cec7de7d43be795a39b34202ff34632c34fe7`  
		Last Modified: Tue, 02 Jun 2026 11:10:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843eb5df5b80a98313d4c30d6e45af50d87403f1b41ae571be7ca09900d5a340`  
		Last Modified: Tue, 02 Jun 2026 11:12:33 GMT  
		Size: 13.8 MB (13835611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d148cb4b621189c1cfa5f414faae64ed3b793bdad3a0bd9b7a4cc2c7dcfeb98`  
		Last Modified: Tue, 02 Jun 2026 11:12:32 GMT  
		Size: 238.7 KB (238691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:742d217ce5cab4be3370de4acc6c269dda136beda8581e055494e97da78435ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75409def321df8b002de19f8b9d2231daff7c83133773ee165def32981a76a16`

```dockerfile
```

-	Layers:
	-	`sha256:becad7752e210f68120f525ca34481570f9aebbba74b89255cdf9bde30921814`  
		Last Modified: Tue, 02 Jun 2026 11:12:33 GMT  
		Size: 3.1 MB (3128986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b7706e9388cc5d8c9287621f4ad3e673ce26c1c87d8422006c86dc877ad2de`  
		Last Modified: Tue, 02 Jun 2026 11:12:32 GMT  
		Size: 23.2 KB (23170 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:33a3c6b6124fb794c16c1f9203d9dc1b57ac5df6b2bca14173353d044dd0a2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118758132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0d69b5cf41d09276d19b58cda879c52327e83770332d099e989bf1d7862cda`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 17:16:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 17:16:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 17:16:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Apr 2026 17:16:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 17:16:29 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:49:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:49:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:49:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:49:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 13:33:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 15 May 2026 13:33:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 13:33:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 15 May 2026 13:33:34 GMT
WORKDIR /usr/local/tomcat
# Fri, 15 May 2026 13:33:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 15 May 2026 13:33:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 15 May 2026 13:33:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 15 May 2026 13:33:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Fri, 15 May 2026 13:33:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Sat, 16 May 2026 19:30:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 16 May 2026 19:30:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 May 2026 19:30:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 16 May 2026 19:30:56 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 16 May 2026 19:30:56 GMT
ENTRYPOINT []
# Sat, 16 May 2026 19:30:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb1da3a1b0530db8bac4f80d6d7cf1cab174ba1fdb49b966e841ec211df17d0`  
		Last Modified: Thu, 16 Apr 2026 17:21:23 GMT  
		Size: 11.6 MB (11570962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40941cf16e4717c40e5532cf516bb886886846120960f18c87affbe922325b4e`  
		Last Modified: Thu, 30 Apr 2026 23:52:33 GMT  
		Size: 61.7 MB (61693654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614352beef2c40d720b7a1387b3a660d056f4e7578072704da8135acd2507070`  
		Last Modified: Thu, 30 Apr 2026 23:52:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497fd2185f8a4d63fe8796afcf556172f2f100d2e96b2b6577747da1b9f137fc`  
		Last Modified: Fri, 15 May 2026 13:36:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1d1fdc09823d4639bae40aae8d4778017721395512b5933233ef33c40da776`  
		Last Modified: Sat, 16 May 2026 19:32:42 GMT  
		Size: 14.3 MB (14315531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e598654b537604addc1c85e2f6aef203ba08857f9cd314126d5696151a6240df`  
		Last Modified: Sat, 16 May 2026 19:32:39 GMT  
		Size: 210.1 KB (210140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:3961e5c80710d75faafd461db486e1bc645305900d40912cc98f8a693ffc7bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d218f1ef566cc5965fad0961e828f2f01d6c2461cb4932f4285717e1fc4772`

```dockerfile
```

-	Layers:
	-	`sha256:6dab2cbf500b5979c04ac75cc217b7b41fdbd291c62055bc2215709a49d7c84d`  
		Last Modified: Sat, 16 May 2026 19:32:40 GMT  
		Size: 3.1 MB (3117664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b7d95756fc0b72d5276471041aa869ff9f70adfaa3bf89c632ac7efa7e1f71`  
		Last Modified: Sat, 16 May 2026 19:32:39 GMT  
		Size: 23.2 KB (23170 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:1a32475fa755cf0d033dae47c75469631da06acebaab6e353b588a0a9cc51fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116228422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8bd7f6fb47a58e85d658b45abcee25b4344351ce7f3ac561dd109ed4c80f85`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:11:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:11:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:11:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:11:28 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:11:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:11:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:11:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:11:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:11:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:11:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:11:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:11:30 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:11:30 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:11:30 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:12:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:12:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:12:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:12:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:12:55 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:12:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6c1347d2071e585abbda6faebc016cf3adb9603862f369e8bf6e3e4a04cdc`  
		Last Modified: Tue, 02 Jun 2026 08:12:00 GMT  
		Size: 11.8 MB (11758188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5a75241f89dfa61867b04cf818ca7cc81e06f565d067527aca7eaf4c77d4f`  
		Last Modified: Tue, 02 Jun 2026 08:12:01 GMT  
		Size: 60.5 MB (60531627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad705c368036c8d2aaf4d7deff0c053a7a5d7389f543fa32b710c17040099f`  
		Last Modified: Tue, 02 Jun 2026 08:11:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d781fc2d4956767abe4d03391febd935841c6c100fd00627d8d554a132cbf2`  
		Last Modified: Tue, 02 Jun 2026 10:11:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4720b55cc88bbf5b51bf6cb9bf19049de1867d2b6f01ed90ff5a8de5e7fd4886`  
		Last Modified: Tue, 02 Jun 2026 10:13:09 GMT  
		Size: 13.8 MB (13808072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3f7b5cb2a0752f45d482e52b220bc264be3ea86862e8f19e312280159b3025`  
		Last Modified: Tue, 02 Jun 2026 10:13:09 GMT  
		Size: 215.2 KB (215183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:60a6cde102342ccec7fef70f9296696ff39b956ecf91d18f556c45f22cef05fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1477107b5380248e4204222482230195db708a3291aa5909178b1e35333bae1`

```dockerfile
```

-	Layers:
	-	`sha256:3b4e852f491f895bc24ca11d58e925e029eb80090af497a3c247353af5fc0af3`  
		Last Modified: Tue, 02 Jun 2026 10:13:09 GMT  
		Size: 3.1 MB (3127256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac49b058bbcf576b8bbb45f1561e585f63a81fbc8fb23daa435e888b2892d399`  
		Last Modified: Tue, 02 Jun 2026 10:13:08 GMT  
		Size: 23.1 KB (23082 bytes)  
		MIME: application/vnd.in-toto+json
