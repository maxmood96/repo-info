## `tomcat:jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:d35a6b3741eaae5bba164efe0103ff1ae34d1b77f75261c5425897cbfc75372a
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

### `tomcat:jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:425780d9d4d8bbb120f141b7b52f3d01fac6decd5f849e83b68d6898e73473dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113187843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a338103e51172a8314e170dfe9dbdbdc50e4b818bd4069cb3e0baee860be1746`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 21:13:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 21:13:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:13:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 21:13:24 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 21:13:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:13:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:13:24 GMT
ENV TOMCAT_MAJOR=11
# Mon, 08 Dec 2025 21:13:24 GMT
ENV TOMCAT_VERSION=11.0.15
# Mon, 08 Dec 2025 21:13:24 GMT
ENV TOMCAT_SHA512=876beac5138cf8277f30fe8f6b519fcdd0bfe3d8ca3d20f734cab0f83e9b2e83de9395ee71052c2604f29f700d9646eddaeec72da5807a2d7edea3936096c742
# Mon, 08 Dec 2025 21:13:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 21:13:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:13:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 21:13:32 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:13:32 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 21:13:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10875650961bf4063d5186970a8c79ef61cf11ca22d49b715b9d59712e0869b`  
		Last Modified: Tue, 13 Jan 2026 00:55:08 GMT  
		Size: 16.2 MB (16150480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be944c6b743dbf21ecbe2d28355dc9f0e5ceadd25ba4c33e09883ea3fb27acc`  
		Last Modified: Tue, 13 Jan 2026 00:55:16 GMT  
		Size: 53.0 MB (52978531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f0f6707dd14f4b50b2fcf046afafdd21c569b1c8c0d05eed070ceaa196fdf0`  
		Last Modified: Tue, 13 Jan 2026 00:55:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55135a7213f6021c2f7be62142583bd9d4eef722869235128decb808bad7d3cd`  
		Last Modified: Tue, 13 Jan 2026 00:55:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d403ed70cec23639868b169e78adb2ad0c4276fc7961a81364931170678e1`  
		Last Modified: Mon, 08 Dec 2025 21:13:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfd3920360caabec5b440e90af9e7bb583e361e9ec6694185021fe30f45f9d2`  
		Last Modified: Mon, 08 Dec 2025 21:13:55 GMT  
		Size: 14.3 MB (14289677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66621c2695e28725ad24d683d876c59fce7c03fbffa250d787f0c55dcf7121e`  
		Last Modified: Mon, 08 Dec 2025 21:13:47 GMT  
		Size: 229.7 KB (229713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:2ea5dd10193c2e970a7878df3b14021320c27aa924e3639fb8d779a2b813dfff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280bc449218250ff3d2944c0544d9a991ae272c3df2a89ba7f78676b80cdb1d6`

```dockerfile
```

-	Layers:
	-	`sha256:bfa5ddb6bc5bad395452885c49ee3e20618be500b012b11b92a9274a0e721492`  
		Last Modified: Mon, 08 Dec 2025 21:32:54 GMT  
		Size: 3.9 MB (3942753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75307baebb7da09120de5da3abd5949effb3cbf511c0c507ff9857152e0757da`  
		Last Modified: Mon, 08 Dec 2025 21:32:54 GMT  
		Size: 21.5 KB (21544 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b66802949cdb46a4c4c7f95d088e9338c6540e137b36a5d7c09da679cc086aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110121318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227519af1d2ca4d05d705330db3bba2349a5e4d18e100f416b78e9840cd0035e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 20:15:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 20:15:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:15:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 20:15:33 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 20:15:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 20:15:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 20:15:33 GMT
ENV TOMCAT_MAJOR=11
# Mon, 08 Dec 2025 20:15:33 GMT
ENV TOMCAT_VERSION=11.0.15
# Mon, 08 Dec 2025 20:15:33 GMT
ENV TOMCAT_SHA512=876beac5138cf8277f30fe8f6b519fcdd0bfe3d8ca3d20f734cab0f83e9b2e83de9395ee71052c2604f29f700d9646eddaeec72da5807a2d7edea3936096c742
# Mon, 08 Dec 2025 20:15:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 20:15:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:15:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 20:15:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 20:15:40 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 20:15:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44e93e2f17680350eef250800f885c5ec5b1dfc6fb7c43cf8e92ea04d5a6f0b`  
		Last Modified: Tue, 13 Jan 2026 01:13:11 GMT  
		Size: 16.1 MB (16066283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc40a6001ee01be38cea704e5d4e64e6b569c37c42227eabc9d308b26755e806`  
		Last Modified: Tue, 13 Jan 2026 01:13:13 GMT  
		Size: 52.1 MB (52148587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fed4c697cbdb704ffa20faeed81c4eb8b16824faa140cce1fd03b6eff14fb7`  
		Last Modified: Tue, 13 Jan 2026 01:13:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bce0f23b926276f17f46f51d48a66370bf819d5c3e83cff5d93b2d3345ebe6`  
		Last Modified: Mon, 08 Dec 2025 20:15:57 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec808600898f374afa1fc01399908e9ef15d1d4dae5a0bb08b5676627ed60c4`  
		Last Modified: Mon, 08 Dec 2025 20:15:59 GMT  
		Size: 14.3 MB (14291180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f142e22ffc4b315f98b66b5295b0907be7e724e7e719eadd9435495cc128f5f`  
		Last Modified: Mon, 08 Dec 2025 20:15:58 GMT  
		Size: 228.7 KB (228748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:bf76e801de7c513613bbc3d910ae468fe41ad3ee5a4bd82f57e96df25327913a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e82c3168d0e5751ae07b41f0b83652512e56732f5622b651c7ed9fdb001d699`

```dockerfile
```

-	Layers:
	-	`sha256:ebd7e3429b24f61b6d78054677ae89978f172866d93c6c8fcabb4346a4dbd4c8`  
		Last Modified: Mon, 08 Dec 2025 21:33:00 GMT  
		Size: 3.9 MB (3942434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2223627bd9632d9e03526aebe9f1918ceff2547f5b9d476b7b0be8c7a5acf5f`  
		Last Modified: Mon, 08 Dec 2025 21:33:01 GMT  
		Size: 21.7 KB (21704 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:872852fdc330710967cd6b9d6a345bfeda4765c5ac2612e517446c55b2de57a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119626008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09eb18e7654a5ffb85b7f666596b8edf3285ed8d86d61f3eb33a52b567585a17`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:28:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:28:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:28:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 21:59:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 21:59:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:59:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 21:59:01 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 21:59:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:59:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:59:01 GMT
ENV TOMCAT_MAJOR=11
# Mon, 08 Dec 2025 21:59:01 GMT
ENV TOMCAT_VERSION=11.0.15
# Mon, 08 Dec 2025 21:59:01 GMT
ENV TOMCAT_SHA512=876beac5138cf8277f30fe8f6b519fcdd0bfe3d8ca3d20f734cab0f83e9b2e83de9395ee71052c2604f29f700d9646eddaeec72da5807a2d7edea3936096c742
# Mon, 08 Dec 2025 21:59:02 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 21:59:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:59:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 21:59:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:59:13 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 21:59:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7981811f07ac9eb3c9a58776fcd918efc4e1b55f3918ffca403a7cdb419d26d`  
		Last Modified: Tue, 13 Jan 2026 03:00:11 GMT  
		Size: 53.0 MB (52985377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604ced66345def7cb398c82a62cef8238b9618bf05090c9e9b7cb42b06f342b`  
		Last Modified: Tue, 13 Jan 2026 03:00:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f48406d6a19b8080d4ef1c51d90387e0b1221722e879c7a9c35f676c263cb64`  
		Last Modified: Tue, 13 Jan 2026 03:00:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd754ecd032318ef5ca6e02d754ea4c284198719f3688eb2704dd4787ec39a0f`  
		Last Modified: Mon, 08 Dec 2025 21:59:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86240ed9b427543e76764a64a99f2999bbd4e5878a58734ae1277ccfd82c2cf4`  
		Last Modified: Mon, 08 Dec 2025 21:59:40 GMT  
		Size: 14.3 MB (14308187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5a75f6f0937c2299f7eff27ab403f6ef4997698dc9315cef2521469eb322b6`  
		Last Modified: Mon, 08 Dec 2025 21:59:39 GMT  
		Size: 259.2 KB (259224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0ce29b1f0e79d39e747265c12cea64a2d16ae7bc9b82e4cb4380159f9db55996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1536008bd8fa4e55bc7e6eceae8298cfcf51a47e91ac2f773d99be5a5a1db7`

```dockerfile
```

-	Layers:
	-	`sha256:6c9e71cc8e82a4b7e4cf526fd873d8723eff93210f432dabd2830db277d09439`  
		Last Modified: Tue, 09 Dec 2025 00:38:16 GMT  
		Size: 3.9 MB (3946847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c239580b0a2d7da3fa2e2f78f27a09f0ba4751394b16b8e8652aa5de975c648`  
		Last Modified: Tue, 09 Dec 2025 00:38:17 GMT  
		Size: 21.6 KB (21601 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:d3696df78132e14e54a8d15382c6f395d3ea5496f6eb82c205bb759ee5dae424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108201934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8f84eff0cc45ec20e3c28da2bab0cb3b3ae2dad05a6c1e3da652b4d2b52433`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:06:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:06:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:06:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:06:25 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:09:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:53:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Jan 2026 23:53:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:53:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 15 Jan 2026 23:53:45 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Jan 2026 23:53:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:53:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:53:45 GMT
ENV TOMCAT_MAJOR=11
# Thu, 15 Jan 2026 23:53:45 GMT
ENV TOMCAT_VERSION=11.0.15
# Thu, 15 Jan 2026 23:53:45 GMT
ENV TOMCAT_SHA512=876beac5138cf8277f30fe8f6b519fcdd0bfe3d8ca3d20f734cab0f83e9b2e83de9395ee71052c2604f29f700d9646eddaeec72da5807a2d7edea3936096c742
# Thu, 15 Jan 2026 23:53:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 15 Jan 2026 23:53:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:53:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 15 Jan 2026 23:53:49 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:53:49 GMT
ENTRYPOINT []
# Thu, 15 Jan 2026 23:53:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817c28fd1674e902e8c2258dd5597f668d610e64feba2532604bc61a8e4ba2fd`  
		Last Modified: Thu, 15 Jan 2026 22:07:14 GMT  
		Size: 16.1 MB (16146443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93b5ce375928373ab6b1091166a97d3f16205cd7f00b39f3b27c03968c27642`  
		Last Modified: Thu, 15 Jan 2026 22:10:34 GMT  
		Size: 49.5 MB (49521850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7864b99467bfa2de329397dce5563f929731779e2cb0ebc27d35175b3cbb55`  
		Last Modified: Thu, 15 Jan 2026 22:10:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf8ae01510bc04c2d4b113e5d1d1f1d6ff5462d99e73c27e10411cad69ac781`  
		Last Modified: Thu, 15 Jan 2026 22:10:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc08edb9763290c180ad2e036fbb7dee05efcbd01607775954acd2de134477f9`  
		Last Modified: Thu, 15 Jan 2026 23:54:07 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c5dc77046d382b63d6922540de3f70ba54347d29cd3a96f6aa994724bfec0e`  
		Last Modified: Thu, 15 Jan 2026 23:54:09 GMT  
		Size: 14.3 MB (14297103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebbe2e53486b37a25003447e4008434dac719ae3eb2e4e0358a54d5e028cc4`  
		Last Modified: Thu, 15 Jan 2026 23:54:07 GMT  
		Size: 230.8 KB (230759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:5fe7e85448f4418d27a3ff60cd419b344ec580b03a4500528f2167e234cfa656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad741439e89e34425cc6098a851459eb2bd11c7503a723188644c6ea3488e08`

```dockerfile
```

-	Layers:
	-	`sha256:be61c13c8aa84304d2aa46e3b5356afce67ff45a14efafda194914fc316d7307`  
		Last Modified: Fri, 16 Jan 2026 00:37:39 GMT  
		Size: 3.9 MB (3944356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c26882ec2b64b82608c37e8989d48a27afadcd629404335bcd7c6546ed82e4`  
		Last Modified: Fri, 16 Jan 2026 00:37:40 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json
