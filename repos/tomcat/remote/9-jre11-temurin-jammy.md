## `tomcat:9-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:a7e437843342ebe07c3f7567e5a7ffa3752340f6dd7d2eeb0e2a7bc1b14ed1cf
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

### `tomcat:9-jre11-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:bed5a9a39d79b487565f8e50a6c80bed623ca8eacd46dd3a73908d7dd574c18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106635826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2526b92a7a0468cb55c7b27c5e4b57d226ea05fd871bc25db0ceb278dcb2eef`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Mar 2025 15:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Mar 2025 15:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_VERSION=9.0.102
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_SHA512=cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a
# Thu, 06 Mar 2025 15:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Mar 2025 15:03:40 GMT
ENTRYPOINT []
# Thu, 06 Mar 2025 15:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda2dc7c824b3c1a5d543e2a293daf8618b3a09ea4cd3dc135d9938396e37b77`  
		Last Modified: Wed, 09 Apr 2025 01:15:35 GMT  
		Size: 16.1 MB (16146021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46aba5d91117812394232597ea51a699499a5a8e9855a9bf687828082d18589`  
		Last Modified: Wed, 09 Apr 2025 01:15:35 GMT  
		Size: 47.2 MB (47216257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a9a09343ce59e8f7e5b01076c3de7b02a7a803a075b6bc3593b06df2b075ca`  
		Last Modified: Wed, 09 Apr 2025 01:15:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95164171bbd2318a61f8f65dc0a9888990a88cc4de9926e718bb2f78e905bf4a`  
		Last Modified: Wed, 09 Apr 2025 01:15:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc39a18196445416ae486f80fab2fa3c503fec8443cf9762b96af4bff520be`  
		Last Modified: Wed, 09 Apr 2025 03:11:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf28675095d9707d2cd12d3e7b9d15297e03ff26fde2b6fc5e66148ef2d3a225`  
		Last Modified: Wed, 09 Apr 2025 03:11:28 GMT  
		Size: 13.5 MB (13508899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac45fca6aca39dc67ae956c97ebb3eb96b12dcce01606b46f563664f0125e6`  
		Last Modified: Wed, 09 Apr 2025 03:11:28 GMT  
		Size: 229.6 KB (229643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:11694d598d169bc3155f65a8bdc137e307c851f3f22fcf31af9bce5aa0d4bbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff254c60292070f68334c44a242d7b21ac71170a1ea31c8ed126ddb60b649bd`

```dockerfile
```

-	Layers:
	-	`sha256:fec357d5651451044db1c8859b87b94c9c6e9ecb516e372e03bfbfbd2f6e15ff`  
		Last Modified: Wed, 09 Apr 2025 03:11:28 GMT  
		Size: 3.8 MB (3778719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038e52c311eced5a9bfc9fa1dac1d0c2a204c789a8814b4c3d32f413354b9fce`  
		Last Modified: Wed, 09 Apr 2025 03:11:28 GMT  
		Size: 21.3 KB (21255 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:63d2fc6d8c75e0a3122ca0e9152f35eaa4b900663ec971197bafcdb9547d46eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101510239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2271bce3a18cb99a04471534f1d2d73421efc277f670f9616f2b8ec7aa4ccb80`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:b27bdc0157c0d964026ea411ed5874766d804b491dfc3d5ac10188c76746bbb0 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Mar 2025 15:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Mar 2025 15:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_VERSION=9.0.102
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_SHA512=cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a
# Thu, 06 Mar 2025 15:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Mar 2025 15:03:40 GMT
ENTRYPOINT []
# Thu, 06 Mar 2025 15:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f3e10eb95482b14d0f5a969fafb71afd541d5efd38890d551e27c957ed3ae84e`  
		Last Modified: Mon, 07 Apr 2025 08:26:39 GMT  
		Size: 26.6 MB (26640334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c38f06e215a1fbf49c830181d7341b1b395e52f4245dca30239c9be2d76548`  
		Last Modified: Wed, 09 Apr 2025 11:39:21 GMT  
		Size: 15.9 MB (15890794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e8bdb8d54c8d8f80ec9879e329409e9f87d3e8f7df576f30b6ed3a1e344049`  
		Last Modified: Wed, 09 Apr 2025 11:45:56 GMT  
		Size: 45.3 MB (45330356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142e1405be1a56b3be9393ecba80b51f563a6274efef7d6577b532f1f1eecec`  
		Last Modified: Wed, 09 Apr 2025 11:45:54 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e00ba060881a19519cfa56ad9789eab471ab95bbe406a85a67b21ebd748a5`  
		Last Modified: Wed, 09 Apr 2025 11:45:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7d36f4f2d74b8a226c736a4400bb0864f3a45d7a54b31695a59f74a8bdd10a`  
		Last Modified: Wed, 09 Apr 2025 13:49:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f60ac7725e3f6a3935be17a1c699fa095d7f2670dd85a868b381e1432d6653`  
		Last Modified: Wed, 09 Apr 2025 13:51:08 GMT  
		Size: 13.4 MB (13443759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b8c00585f38ecb1e2205c3425cde26a5e2e41f64de54ba9f368abca99d2693`  
		Last Modified: Wed, 09 Apr 2025 13:51:07 GMT  
		Size: 202.4 KB (202355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d60f044eca238e9ebef16ed24b88b6b1b0074a57ee59ddb81dc3f3b5e2ced4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c832def629ab68ecd567b2e93b01aa350f10a30169fce4982350cc05e106d5`

```dockerfile
```

-	Layers:
	-	`sha256:e5a78177e68462339faa459a3f9a042577418f5154e02b64c06b1cf737192d14`  
		Last Modified: Wed, 09 Apr 2025 13:51:07 GMT  
		Size: 3.8 MB (3782317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2749d3d23fcfbe1971f6ef0d7c2e38a5c707796c477460129228d533333a4d98`  
		Last Modified: Wed, 09 Apr 2025 13:51:07 GMT  
		Size: 21.4 KB (21372 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:5e48c017d6131031c3d95fae3b2ee11b7c26a0bf723ebfcaf9365e06113cac32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105319632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e73db6445efc62843e592334153c3326df5747ffe5c3590887b448430221c5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Mar 2025 15:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Mar 2025 15:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_VERSION=9.0.102
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_SHA512=cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a
# Thu, 06 Mar 2025 15:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Mar 2025 15:03:40 GMT
ENTRYPOINT []
# Thu, 06 Mar 2025 15:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a52ffb175ad1dcd8d364fe67acb246aab94c398d959d8d166ec5f141d4b8c3`  
		Last Modified: Tue, 04 Feb 2025 09:20:15 GMT  
		Size: 45.6 MB (45575892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad623ccfcd77de0cc124fb4db0bf8ddd65fab1fd731cc5749533bcc9d6d9806e`  
		Last Modified: Tue, 04 Feb 2025 09:20:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb340c54cb7dc17dcd4b8bee473c99474a4ffcb686470f5d4866eba12637ff4`  
		Last Modified: Tue, 04 Feb 2025 09:20:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b47e6822d90b0befe2f601d4e9dec8f4bb4e382a428f6a77a880c9051c2f998`  
		Last Modified: Thu, 06 Mar 2025 19:13:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd8ef531c8aed6939cc361e43e1e9b67cc8d0619a602a72c3fff0f0d138ba99`  
		Last Modified: Thu, 06 Mar 2025 19:13:02 GMT  
		Size: 13.5 MB (13515234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba34c28b8b72214e4da8eefeeef2c8832eb7ecaa06be19a77213406ee0364fb0`  
		Last Modified: Thu, 06 Mar 2025 19:13:02 GMT  
		Size: 2.8 MB (2815034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ddcbca3f53bfc5e690adba4a9249639ed8be097e264c3ddada88d540dc7b93da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a2a342b0439a7a2c0a27147a01839ed82fdbf812c09ede9adf4626d9ceb208`

```dockerfile
```

-	Layers:
	-	`sha256:736af456b6eb550c6aa941c0af121f3a569d8f32dc0f572202c03931d5cfaf46`  
		Last Modified: Thu, 06 Mar 2025 19:13:01 GMT  
		Size: 3.8 MB (3778331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d91acf5f8910a6bc3c443183fde270fd9b1edfabe2232dd66758e0c25f3a67b3`  
		Last Modified: Thu, 06 Mar 2025 19:13:01 GMT  
		Size: 21.4 KB (21405 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:0d4b1603137357e16cf1e6c6568fe2a4c9814f1bd3c9727cadd1e5b19a924785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108533175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7fbc3d5b6e42875b407e98010e2a10246165948111feaa6e4ad3b8b52a28a8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Mar 2025 15:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Mar 2025 15:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_VERSION=9.0.102
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_SHA512=cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a
# Thu, 06 Mar 2025 15:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Mar 2025 15:03:40 GMT
ENTRYPOINT []
# Thu, 06 Mar 2025 15:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c38ec2b4ee36ca93f19596eb065a396e648e65a58e52db4e0886be5ded596`  
		Last Modified: Wed, 09 Apr 2025 04:35:13 GMT  
		Size: 17.6 MB (17617815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dde7544f82231a07fd24e351855443dcb0ab1758ea9b3f59e8ec9a82227389d`  
		Last Modified: Wed, 09 Apr 2025 04:42:58 GMT  
		Size: 42.7 MB (42674671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a362bb6c6ac10235b5d5db493c570c6783604a7ab8d5aa351704b243a334c9a`  
		Last Modified: Wed, 09 Apr 2025 04:42:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cefb3a010c97f53a561fb0b94172bdafaff18cf5b8299258633b146faba02d`  
		Last Modified: Wed, 09 Apr 2025 04:42:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaa4987e5051bc205598aa7ca4f509af9da6c3f01b5d290416af870a0c4d207`  
		Last Modified: Wed, 09 Apr 2025 13:56:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2063c0a31a32985784e48c355400d547e00cc78665ee15904de4753422e7bad`  
		Last Modified: Wed, 09 Apr 2025 14:00:10 GMT  
		Size: 13.5 MB (13536292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f852c563a8594e68de751c714c77e1ce8465d5db4d96868b975072a661572b99`  
		Last Modified: Wed, 09 Apr 2025 14:00:09 GMT  
		Size: 259.1 KB (259057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:9a822ebdd80c782a2b0f854430d04b3b0b2d3514a41b7a39c14ac4b72e48a5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347d0b88c8373a34f622c2e219695c210af25308bbf07eb393c15eaa174940a3`

```dockerfile
```

-	Layers:
	-	`sha256:7af631fa78f92fd20d4693f954729b0f2a0cccf050b8cf47e2104350754f0aad`  
		Last Modified: Wed, 09 Apr 2025 14:00:09 GMT  
		Size: 3.8 MB (3782661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85dcb5d0f94ce06625a1a2c766d77342a7ed83f0a37ac91581600c775d2e9b6`  
		Last Modified: Wed, 09 Apr 2025 14:00:09 GMT  
		Size: 21.3 KB (21308 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:b594698c184a30e673209cb10fa88dea4a69b17ae6590ea63ee5064b18b92d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98721370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505f584e6dca3922fd64b2307def4b579ccf633a5756aa3f89d615a23e90006b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Mar 2025 15:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Mar 2025 15:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_VERSION=9.0.102
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_SHA512=cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a
# Thu, 06 Mar 2025 15:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Mar 2025 15:03:40 GMT
ENTRYPOINT []
# Thu, 06 Mar 2025 15:03:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ffac1a60b6cb80417a2deaa826c5568b388878415c01490d46c373b76b9af`  
		Last Modified: Wed, 09 Apr 2025 04:16:19 GMT  
		Size: 16.1 MB (16143553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec31af260e56272c908ed50fe6e4a88caa52a4bd9f9358ccabadad83b329696`  
		Last Modified: Wed, 09 Apr 2025 04:18:27 GMT  
		Size: 40.8 MB (40838341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6721f699b927a4bc3bf969a589ae327010bf43b3d22bf7e9e26fe1d5c3c68f`  
		Last Modified: Wed, 09 Apr 2025 04:18:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d25f763a3782a520defd330b560184cf180cc1bcfce6a65939d2b8c87fbcc0`  
		Last Modified: Wed, 09 Apr 2025 04:18:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b29c37033498a15c870d438d268f3c00f5187daa882604eae835b6237494b2a`  
		Last Modified: Wed, 09 Apr 2025 07:35:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f396792f13bf3bec49b0d0fd68e458d7cf41c0feb1caf409a8cf79193f8d634e`  
		Last Modified: Wed, 09 Apr 2025 07:39:47 GMT  
		Size: 13.5 MB (13505821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05c3fced16fc90ce0f09c0285c0139a17f8e1cb83737d2e00eb315363acfaf7`  
		Last Modified: Wed, 09 Apr 2025 07:39:47 GMT  
		Size: 230.9 KB (230896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b0d9254dad9c52d7223f944f54a14bdb4e975e8969596d465c1f397bd676e768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a519d9cd7bcbbd6e0cd9bf52549cfdddc3827190408702e0260678b33aeba114`

```dockerfile
```

-	Layers:
	-	`sha256:20fc93ddb5940f7d3b6dfb88db9f51f53884111483fa09c1a117625d48613ede`  
		Last Modified: Wed, 09 Apr 2025 07:39:47 GMT  
		Size: 3.8 MB (3780316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bfe0867704ed17f30cf28c623d4016c1ffcb085a10af962cc4889322b818c5`  
		Last Modified: Wed, 09 Apr 2025 07:39:46 GMT  
		Size: 21.3 KB (21256 bytes)  
		MIME: application/vnd.in-toto+json
