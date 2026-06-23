## `tomcat:11-jre17-temurin`

```console
$ docker pull tomcat@sha256:178ee85ced6a424171ba07f1e91ce533ec04505836c72755ad135d83fed04b83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:11-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:f7c4065bb0b38c4608253b2c2b0b1c3186364a7335f5e10c08122df7f5b17389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111688485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d94db55dade3bc7630259b021fd35e0b5d7caeb362fe26d579c00ffc0dd9f4`
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
# Tue, 02 Jun 2026 08:14:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:01 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:14:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 23:10:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 22 Jun 2026 23:10:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:10:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 22 Jun 2026 23:10:59 GMT
WORKDIR /usr/local/tomcat
# Mon, 22 Jun 2026 23:10:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:10:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:10:59 GMT
ENV TOMCAT_MAJOR=11
# Mon, 22 Jun 2026 23:10:59 GMT
ENV TOMCAT_VERSION=11.0.23
# Mon, 22 Jun 2026 23:10:59 GMT
ENV TOMCAT_SHA512=f5acb7a1e5ad60dea682ffe16cf075596f0e7b62e460828eb176639714d125ab08c763753fb709e3626ce6f42712c281b4ccf54930354aa07325550d6e6cbdac
# Mon, 22 Jun 2026 23:10:59 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 22 Jun 2026 23:11:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:11:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 22 Jun 2026 23:11:03 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 23:11:03 GMT
ENTRYPOINT []
# Mon, 22 Jun 2026 23:11:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0479b3e13d15e71a0f435758770a5bcee00c798f2a9ab9fdfbbb8245d9e6b0`  
		Last Modified: Tue, 02 Jun 2026 08:14:15 GMT  
		Size: 17.0 MB (16984214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc9f142be00090c33540f13b089c514cdd8ec280cb4409348efcc123e79fa46`  
		Last Modified: Tue, 02 Jun 2026 08:14:38 GMT  
		Size: 47.6 MB (47565010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9c065cf78e497d2a96f613eec79173692952621df022335a7b25fecd9b7b2b`  
		Last Modified: Tue, 02 Jun 2026 08:14:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53a5c207c4191f4aa279920278a481310c882de2d85a4f23c907a06a4153f49`  
		Last Modified: Tue, 02 Jun 2026 08:14:36 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87821daa5d3fe4176c07481fb15114cf44cf47e947ca0847dae9a46b5c0c0b57`  
		Last Modified: Mon, 22 Jun 2026 23:11:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a8a553f4fc8fc804ee9d3e90310e920da2c0c4c5bd2ce8928a2ff820a9a519`  
		Last Modified: Mon, 22 Jun 2026 23:11:12 GMT  
		Size: 14.4 MB (14373432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d832b8d55f0070b3d6fd3494e5b9f2695200e0cdbb1fc74356016e797bf51c1`  
		Last Modified: Mon, 22 Jun 2026 23:11:12 GMT  
		Size: 3.0 MB (3030381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:bfa52b16783a0da2b83fcaee341c5603a156bb69f3f8387ff2ef22e9f2dd1e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9468ba3724bd4cdeb57bcd7a0ea1f973cd37438a781dac017e867d7029a5ae9`

```dockerfile
```

-	Layers:
	-	`sha256:e966e31095a67c5d78c889e5490616f941ef965290ba33300d44f2d6a66007dc`  
		Last Modified: Mon, 22 Jun 2026 23:11:12 GMT  
		Size: 3.4 MB (3350041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad02a3a48af64eac7cc59ae03b67d0d0511ba6d5486bb6d356cd0ad91972b005`  
		Last Modified: Mon, 22 Jun 2026 23:11:11 GMT  
		Size: 24.0 KB (24046 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:c0018cc2cdbb65d7db4add60d112425947885c69780003981b38566fd3750f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104996719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0f0a4803a984f360e00dce73bc0a0b7184525947c6534afe71fccaa17e64eb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:36:59 GMT
ARG RELEASE
# Wed, 20 May 2026 01:36:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:36:59 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:02 GMT
ADD file:6d117ff682b1d31146902ad551197b012e75561d62d92d029219fcbf5c493c35 in / 
# Wed, 20 May 2026 01:37:02 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:25 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:14:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 23:09:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 22 Jun 2026 23:09:47 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:09:47 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 22 Jun 2026 23:09:47 GMT
WORKDIR /usr/local/tomcat
# Mon, 22 Jun 2026 23:09:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:09:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:09:47 GMT
ENV TOMCAT_MAJOR=11
# Mon, 22 Jun 2026 23:09:47 GMT
ENV TOMCAT_VERSION=11.0.23
# Mon, 22 Jun 2026 23:09:47 GMT
ENV TOMCAT_SHA512=f5acb7a1e5ad60dea682ffe16cf075596f0e7b62e460828eb176639714d125ab08c763753fb709e3626ce6f42712c281b4ccf54930354aa07325550d6e6cbdac
# Mon, 22 Jun 2026 23:09:47 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 22 Jun 2026 23:09:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:09:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 22 Jun 2026 23:09:53 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 23:09:53 GMT
ENTRYPOINT []
# Mon, 22 Jun 2026 23:09:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a2dede8d0e9ca179460cb274dab10c5c4b741cf1544b130df872809a4467e3e4`  
		Last Modified: Wed, 20 May 2026 02:15:37 GMT  
		Size: 26.9 MB (26859709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2507b22e56bdabd19d56cd5e548741849d5aa95fae887fc799ecc06b085851e`  
		Last Modified: Tue, 02 Jun 2026 08:14:43 GMT  
		Size: 16.3 MB (16310658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bc0126a0c28b3eeffcf008d0fc9e46ba612f1e8819c9278ef7140ace8f52e9`  
		Last Modified: Tue, 02 Jun 2026 08:14:44 GMT  
		Size: 45.1 MB (45131953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108605b0223c05ef5f99061f3501d1d14d37e9e1e5a806c59eae7a9409e7b128`  
		Last Modified: Tue, 02 Jun 2026 08:14:42 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a7361a0c6825285be9a7617de6d10a67129ba9838861ac1ce88e1d1e6eae6`  
		Last Modified: Tue, 02 Jun 2026 08:14:42 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afac96f06d10d5ef5bafb98dfd7e2b62746281e13ac4d690ce24a487f055d796`  
		Last Modified: Mon, 22 Jun 2026 23:10:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7f632b7d52f42093214752b23360aafffda97c0abf79e43a302a38319510`  
		Last Modified: Mon, 22 Jun 2026 23:10:02 GMT  
		Size: 14.3 MB (14346679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e14538e7743095595fad3c3fa1c3da1d5a9f02ba8b4f2cba42a5fbab2af1569`  
		Last Modified: Mon, 22 Jun 2026 23:10:02 GMT  
		Size: 2.3 MB (2345076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:ca873594882e528901dbaf52d584ff0c4b7e7a76280416effd60feddd90e8305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b6b2c2cc432d19f50e63600a0e1e43f710a900a870a428527789640fd4288a`

```dockerfile
```

-	Layers:
	-	`sha256:97997f927aa287ac3ead1aba7e70b2766fb7ab7f22aefbd6fdb9034a575747c2`  
		Last Modified: Mon, 22 Jun 2026 23:10:02 GMT  
		Size: 3.4 MB (3352445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fa77e0bba3cdef9323f661deb58c05c2814f5927434a2031046ec8548683b0`  
		Last Modified: Mon, 22 Jun 2026 23:10:02 GMT  
		Size: 24.2 KB (24238 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:6fa883acaf6e6bc47ca68903ec78159257edef6ede75664fa56e868901f4bc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110130838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcebf6ed0790b9f96118b5a5248de29a54789b0a1f268d7b9301daeb08f5ca3`
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
# Tue, 02 Jun 2026 08:15:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:49 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 23:11:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 22 Jun 2026 23:11:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:11:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 22 Jun 2026 23:11:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 22 Jun 2026 23:11:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:11:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:11:32 GMT
ENV TOMCAT_MAJOR=11
# Mon, 22 Jun 2026 23:11:32 GMT
ENV TOMCAT_VERSION=11.0.23
# Mon, 22 Jun 2026 23:11:32 GMT
ENV TOMCAT_SHA512=f5acb7a1e5ad60dea682ffe16cf075596f0e7b62e460828eb176639714d125ab08c763753fb709e3626ce6f42712c281b4ccf54930354aa07325550d6e6cbdac
# Mon, 22 Jun 2026 23:11:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 22 Jun 2026 23:11:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:11:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 22 Jun 2026 23:11:37 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 23:11:37 GMT
ENTRYPOINT []
# Mon, 22 Jun 2026 23:11:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bae551a8d85f3d624b546e7c0ac283c40790de251411223ebe48b2436b9a289`  
		Last Modified: Tue, 02 Jun 2026 08:16:05 GMT  
		Size: 17.0 MB (16997563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4fdf0a5ae0738ba447b4545101a25040b3e43979c381fe706aad49f9c51f5`  
		Last Modified: Tue, 02 Jun 2026 08:16:06 GMT  
		Size: 47.1 MB (47050255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674b3dc2174426f844391a3f1b8bfe71cc1847db2221468e30aa16b3e5cb051`  
		Last Modified: Tue, 02 Jun 2026 08:16:04 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f8076be277e77be7e5cbd09350922dab3ff99e87085f0d27144d6897900208`  
		Last Modified: Tue, 02 Jun 2026 08:16:04 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3717674f2c3a9e637b593b07f843ce8fe9203784b392eb72fa2afe173f9eea0`  
		Last Modified: Mon, 22 Jun 2026 23:11:45 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46862e60bb5e0b2de858a2889501734da4d082fb7c71285f71d671bc097c08b3`  
		Last Modified: Mon, 22 Jun 2026 23:11:46 GMT  
		Size: 14.4 MB (14374013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981e9fedfde42696e2693d683ac50b56407b7763adcd95c0a7a2eefb63cfdc9`  
		Last Modified: Mon, 22 Jun 2026 23:11:46 GMT  
		Size: 2.8 MB (2829957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:2fcfaab0f3c81d0ce353a51dec0febec0e9c247f7ce4d61c863e4d92322849ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb0a0fb00b72f9d564026f9b881806ab61cd23d76e45420be82547baf494137`

```dockerfile
```

-	Layers:
	-	`sha256:df146bef05f9f0b9a18147b4f0d2ddfbf9f991d29e644174c14ad3a530c7cbf7`  
		Last Modified: Mon, 22 Jun 2026 23:11:46 GMT  
		Size: 3.4 MB (3350609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5adcb6ce3ba95ec5b17c55fa569b71a18f90ff54a62f51c7464b0a3c42827872`  
		Last Modified: Mon, 22 Jun 2026 23:11:45 GMT  
		Size: 24.3 KB (24302 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6c1c98623699dc62a03bba879ed250c0a331e714b825fb8d55d7ab83cfa23ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118325862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a31e338d0ee9aa828b5392d19ebaed8599ec9a4d5698e7797f0ff29d199249f`
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
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:11:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:12:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:12:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 23:11:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 22 Jun 2026 23:11:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:11:55 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 22 Jun 2026 23:11:55 GMT
WORKDIR /usr/local/tomcat
# Mon, 22 Jun 2026 23:11:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:11:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:11:55 GMT
ENV TOMCAT_MAJOR=11
# Mon, 22 Jun 2026 23:11:55 GMT
ENV TOMCAT_VERSION=11.0.23
# Mon, 22 Jun 2026 23:11:55 GMT
ENV TOMCAT_SHA512=f5acb7a1e5ad60dea682ffe16cf075596f0e7b62e460828eb176639714d125ab08c763753fb709e3626ce6f42712c281b4ccf54930354aa07325550d6e6cbdac
# Mon, 22 Jun 2026 23:11:56 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 22 Jun 2026 23:12:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:12:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 22 Jun 2026 23:12:04 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 23:12:04 GMT
ENTRYPOINT []
# Mon, 22 Jun 2026 23:12:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446e49e9f89060bc304b8fef0ec225a1bbe8d83d16bc21674a8944851007289e`  
		Last Modified: Tue, 02 Jun 2026 08:12:24 GMT  
		Size: 47.5 MB (47487489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa39e29e88ec706ec5b3a92acfe0c8a99f2d7134c0c4bc8930a64ed9f6857e6e`  
		Last Modified: Tue, 02 Jun 2026 08:12:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd17ed68671bb0de7314a744f666ff78b1bb7a5b7edd42295c46e2064c0d7f19`  
		Last Modified: Tue, 02 Jun 2026 08:12:22 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45c374b995e14cb95d0c48134d044f663b15bb662e385da74b3664f7e99920`  
		Last Modified: Mon, 22 Jun 2026 23:12:32 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b534de80a50b84aa30848a025f4a97bb6c67462e72554af83cf55ec71d3a1d1`  
		Last Modified: Mon, 22 Jun 2026 23:12:33 GMT  
		Size: 14.4 MB (14388270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3aa70ea25c7d88361bc85e9444ec1273e97f4c5f4fc4e507a51c6840eb0639`  
		Last Modified: Mon, 22 Jun 2026 23:12:33 GMT  
		Size: 3.3 MB (3319936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:445a57a1a7bb8a3722908f9f080f4e0a199edf91f9ffd7d9cd0861b6113352e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3378318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64549983c4858c94417634b70e2129ddbcc5ea7709f31a8c7eb8bc5603d08c7`

```dockerfile
```

-	Layers:
	-	`sha256:f5b38e90ea35e988883ae868ae3dcf95400574b1c59585e620fe0b8558f53b7d`  
		Last Modified: Mon, 22 Jun 2026 23:12:33 GMT  
		Size: 3.4 MB (3354166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57e7ddc410cccee7f1925e9fa17673ef5339043674b7112f84623053e7f2c9e`  
		Last Modified: Mon, 22 Jun 2026 23:12:32 GMT  
		Size: 24.2 KB (24152 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:e8ebc664694b44c8a96caab19c7165136e63cdba1f502bcd18676cc95417fd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109704405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5bc47d1320fa71a3a18e2197ff98ae77829e9e9edf098ddcd3c4ec4158b35db`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 02:06:08 GMT
ARG RELEASE
# Wed, 20 May 2026 02:06:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 02:06:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 02:06:59 GMT
ADD file:f1fd7ee282731834f2f36b17e9b538e569ade4ce8b89924b635551ff3a45c706 in / 
# Wed, 20 May 2026 02:07:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 18:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 18:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 18:15:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 18:15:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 18:15:05 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 18:15:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 18:15:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 18:15:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 18:15:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 03 Jun 2026 05:15:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Jun 2026 05:15:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 05:15:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 03 Jun 2026 05:15:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Jun 2026 05:15:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Jun 2026 05:15:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Jun 2026 05:15:19 GMT
ENV TOMCAT_MAJOR=11
# Wed, 03 Jun 2026 05:15:19 GMT
ENV TOMCAT_VERSION=11.0.22
# Wed, 03 Jun 2026 05:15:19 GMT
ENV TOMCAT_SHA512=4ee77f604009daeab50d015835f221707f64a03756c6e5ac8736a6947cd60f6796315ceb255428765017038d79d466988582eb8b986dc48d3649bbc35bdd8bd7
# Wed, 03 Jun 2026 05:15:22 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 03 Jun 2026 05:16:02 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jun 2026 05:16:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 03 Jun 2026 05:16:09 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 03 Jun 2026 05:16:09 GMT
ENTRYPOINT []
# Wed, 03 Jun 2026 05:16:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:924f9a731915e06f77b3487378ddf9426f8422fa1d96461bef1d0e0a35c36743`  
		Last Modified: Wed, 20 May 2026 02:15:52 GMT  
		Size: 31.0 MB (30965919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbef1fc78839b65664f9a375b2f139fa8fc2f1b2bda645197a6f3921d196f9e`  
		Last Modified: Tue, 02 Jun 2026 18:17:50 GMT  
		Size: 17.9 MB (17875390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83ba377912c52a7a160ecf46474447901b9cfecd1fc3c95eb183b2149330beb`  
		Last Modified: Tue, 02 Jun 2026 18:17:54 GMT  
		Size: 46.1 MB (46111458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d6788112422f9e23f66863655afa9c22f95370010c72ed33bb78bc2318ac85`  
		Last Modified: Tue, 02 Jun 2026 18:17:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1149875bdfa25b1c2dc804b1f56a04d4be2650aa2c67d5f16d71dfdbc143d7e6`  
		Last Modified: Tue, 02 Jun 2026 18:17:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fb93c0f87c39fb8d6cac6290bae72fa50b70703e60b73c5c73641882efb18c`  
		Last Modified: Wed, 03 Jun 2026 05:17:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba728b427e6d7770b0d1abc6a32b4d750f1546b0e2e1de45064cad9c187e1a9`  
		Last Modified: Wed, 03 Jun 2026 05:17:48 GMT  
		Size: 14.5 MB (14521098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73480a8a05e586c038f35c92f2a90cc6810e398ba5c498abb9cab75c611899a8`  
		Last Modified: Wed, 03 Jun 2026 05:17:46 GMT  
		Size: 227.9 KB (227896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:44be2a897c19c2c74e8518fb738607f9aaee01e5895a53b788f97564b95fac05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3366314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fed1efb18887a1b3107199d7820eaf65f244650b27dabce8eb4ed3c04b0134`

```dockerfile
```

-	Layers:
	-	`sha256:532fcd573593eaadc1ef8c468e265019d5e659db66702efba89e8bde9e88aaf5`  
		Last Modified: Wed, 03 Jun 2026 05:17:47 GMT  
		Size: 3.3 MB (3342164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3520105ce139abadff240de1b936629509a710ed4012232d5cad6fb9382c816`  
		Last Modified: Wed, 03 Jun 2026 05:17:46 GMT  
		Size: 24.1 KB (24150 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:6eb096e1b7e137a337104cd0bc9e0dd8dc2163d046be7cfec98a303cade70e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109168268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26d94bff3ca28d174a1056287ea5ef694dd7d20aa238447b7eeaf8c4204dae7`
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
# Tue, 02 Jun 2026 08:10:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:41 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:10:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:10:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 23:10:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 22 Jun 2026 23:10:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:10:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 22 Jun 2026 23:10:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 22 Jun 2026 23:10:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:10:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:10:18 GMT
ENV TOMCAT_MAJOR=11
# Mon, 22 Jun 2026 23:10:18 GMT
ENV TOMCAT_VERSION=11.0.23
# Mon, 22 Jun 2026 23:10:18 GMT
ENV TOMCAT_SHA512=f5acb7a1e5ad60dea682ffe16cf075596f0e7b62e460828eb176639714d125ab08c763753fb709e3626ce6f42712c281b4ccf54930354aa07325550d6e6cbdac
# Mon, 22 Jun 2026 23:10:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 22 Jun 2026 23:10:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:10:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 22 Jun 2026 23:10:23 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 23:10:23 GMT
ENTRYPOINT []
# Mon, 22 Jun 2026 23:10:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129e96aa53f0450efaf479f3f13f6458a079dca114760c8791cb4a29a73fd13b`  
		Last Modified: Tue, 02 Jun 2026 08:11:00 GMT  
		Size: 17.6 MB (17579904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b82b664b1b85f55219f3cf8974a8a1f9c1015353bad9143c5aec78b1875b3aa`  
		Last Modified: Tue, 02 Jun 2026 08:11:01 GMT  
		Size: 44.5 MB (44541838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e95923db86451c78e2026462e68e91cceeefe7808ce322364e31a2b8f39299c`  
		Last Modified: Tue, 02 Jun 2026 08:11:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8bd676b281f70cbd703ce4914dfd595bb2a4dada9b3abfa20158327d4c936d`  
		Last Modified: Tue, 02 Jun 2026 08:11:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5006f694e398dc90940180cc967f5b45723a328cd902f4b618a17aec6e1b6a2a`  
		Last Modified: Mon, 22 Jun 2026 23:10:36 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158dd4f8b306787904c6fc217c64b517ec15782ae582b9bdd2b82e3445534c83`  
		Last Modified: Mon, 22 Jun 2026 23:10:36 GMT  
		Size: 14.4 MB (14382161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8505d64d4373464aaa6759b3b3a7a4bc6db14b9196491ca0f5bc3f81529b1907`  
		Last Modified: Mon, 22 Jun 2026 23:10:36 GMT  
		Size: 2.7 MB (2748886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:1aae48e59f915c0774d33911ae606b8bc761383614b53bb60971efb6066bb99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef827122fb804dd711de6ceba77dc40380f0c930aba8c6c9be5cbe0a65dfb808`

```dockerfile
```

-	Layers:
	-	`sha256:d1408c4501a6be556d758dbbbfa33c90a225baddf04d8e106453606547419fcb`  
		Last Modified: Mon, 22 Jun 2026 23:10:36 GMT  
		Size: 3.4 MB (3352240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9551728c173e1382ea0cb35e40262c7f486158b663257e26d081cd5c9ebbfbe7`  
		Last Modified: Mon, 22 Jun 2026 23:10:36 GMT  
		Size: 24.0 KB (24046 bytes)  
		MIME: application/vnd.in-toto+json
