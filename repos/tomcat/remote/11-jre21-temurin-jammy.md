## `tomcat:11-jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:1a933d66dfd86baa7fe749584b6fffe3ab53bfe361c388b8c2516fd6661e82ed
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

### `tomcat:11-jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:701027c58b4daab23764b6e14085ddfa5ceeb0219fa59e549e5321d73ac94ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112990740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd17d9eaa40c8418706019ebcf12b60d3a39591e484e767dc8bd9facd22dd070`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04853e34f5a8151c7f20c6027a9364b9233dfe2686ed91def6576890be0c65df`  
		Last Modified: Mon, 01 Sep 2025 23:08:56 GMT  
		Size: 16.2 MB (16150632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f900126b195dacbe382dbd48644d787bc3a578ff2cd19633d92fb038833b3b2d`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 53.0 MB (52968663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f1d4c8a8a52dbb4ae50ee5c9f56237520178681692e173483441961e599a1a`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae447ab70ba7e9cf828167fce33f0b94177b7e1f6fa7966cf1071a8e017c91a`  
		Last Modified: Tue, 02 Sep 2025 01:13:05 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58edf0dee830b666dbe7c5e9a17092a2a15e0a98d011c5cfabbbd9ac9064ac8`  
		Last Modified: Tue, 02 Sep 2025 02:35:34 GMT  
		Size: 14.1 MB (14102152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f7ff83990a53850478368eec63555f96b160f24ffcb970cff0482e96e3b30`  
		Last Modified: Tue, 02 Sep 2025 02:35:32 GMT  
		Size: 229.7 KB (229716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:214f70a21b4ed499be37a670ef37cc3253e2ed163113c90aef24aff4141bd956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cb1b77a97103786aa713e38688f16d6350113f889150a1c5ed73bc58fb7547`

```dockerfile
```

-	Layers:
	-	`sha256:62bc4ae494b4f45505fa49e052327508fbe1e9ee1bd0c5fc3ccf3451779a2619`  
		Last Modified: Tue, 02 Sep 2025 02:33:33 GMT  
		Size: 3.9 MB (3944265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0dbe9e4a82ba2cf9551ab5bb19eeb9c9b0e245f5ba733611723e658147dd215`  
		Last Modified: Tue, 02 Sep 2025 02:33:34 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:c71c05601cd339c61ab2b983e327b138c39692d4c55d0e632b0b9209e38365e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109905720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbc5283264bc30b024cc45e79b498ed8a684d8ce1427775f53a77f0fa125e0d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e52f3080aac2f7abe2d858a9dfe47d820850f11dcba9da3ee78a5072085399`  
		Last Modified: Tue, 12 Aug 2025 18:39:07 GMT  
		Size: 52.1 MB (52148319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222689666f0565f2906e70d8a5eb586c7ba09eaef163ff5625994374a9b3bfdd`  
		Last Modified: Tue, 12 Aug 2025 18:38:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca372eebceee03ecddb4b24f67489039af1d4266be937af8e10492ed348c23df`  
		Last Modified: Tue, 12 Aug 2025 18:38:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d4b5d0f9effbe3e43315a4395351daf71a5c35b3388759eef3f58535ef8bd7`  
		Last Modified: Wed, 13 Aug 2025 13:38:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d993fab6c10d33a0214ec7e9e2bf56bae60f879e55182dc9d71c5de4429903f`  
		Last Modified: Wed, 13 Aug 2025 13:38:37 GMT  
		Size: 14.1 MB (14103067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d72990e634d3ab433cfbc7f4af843042ea8456fab7ad55069d905f5abf0dbda`  
		Last Modified: Wed, 13 Aug 2025 13:38:36 GMT  
		Size: 228.7 KB (228704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:25696f721d1cae69f7f6c4c0e0061bf90e7b907cf8d92cc6564dd3011f0b4c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8a8734d696a415afa808350e76f8b862d366804484990168ed2bc8d63ea938`

```dockerfile
```

-	Layers:
	-	`sha256:40a3bf2fb4fb9912efa568417d9b4ef8cfaf9fec9fb9cc7235b517dff86b0e27`  
		Last Modified: Wed, 13 Aug 2025 14:31:01 GMT  
		Size: 3.9 MB (3943930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:606740b04f553c44770dc85cb08e7579c2d0b00c5f248fff211887a1f483439d`  
		Last Modified: Wed, 13 Aug 2025 14:31:02 GMT  
		Size: 21.7 KB (21745 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:8108a7ce061f9ccf347b7fcfee71d73f6cf2a6df52766f2ab20da14060f5dbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119442357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6139cd34b42d003c93b1351580ca1c50befb4bbe5df961871ac2aef5631321a0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c50520b2833414582dcec4e87265a64dd9e5acd7b3ec03378e25ec51523b3`  
		Last Modified: Tue, 12 Aug 2025 17:29:14 GMT  
		Size: 17.6 MB (17624214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7738418538360b7943cf9fc24eee0efe088e3ef70769abfc05029db56f7ab9d`  
		Last Modified: Tue, 12 Aug 2025 17:45:14 GMT  
		Size: 53.0 MB (52994807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5af7752bad3a1d288041748b2c90ebae78a334877d2db92d801b5532bdd8f0`  
		Last Modified: Tue, 12 Aug 2025 17:45:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8fa348d065811a47e8f914763d82d9e1dfee83d05e40da649253c7277b1e4f`  
		Last Modified: Tue, 12 Aug 2025 17:45:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85cf9291fd24ed51fdb8175a936358c3e598411401abcd76aa964d94237c3c1`  
		Last Modified: Wed, 13 Aug 2025 17:51:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb28d57f1a5de06508a8c6eb8066135c941fa01484d9a84fd5deee809b7cf512`  
		Last Modified: Wed, 13 Aug 2025 17:51:49 GMT  
		Size: 14.1 MB (14118518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a67707d8e575acd5ef8811b966ba2e72eed3ced7830614fba1a1f8d036591d`  
		Last Modified: Wed, 13 Aug 2025 17:51:48 GMT  
		Size: 259.0 KB (259031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:052ade1f2e54f2ee168d56aa097c394e9d033aeb4dcd7630477b4a6734d2f396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f6516821c27040e0c6a1a2327975841e4dfb28455897dbca2c7b13ef891d84`

```dockerfile
```

-	Layers:
	-	`sha256:e1872def0c14fbc330ec4d36751e3987c6afb0c93aeb227e9d03c01c58a7ebe7`  
		Last Modified: Wed, 13 Aug 2025 20:31:16 GMT  
		Size: 3.9 MB (3948343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:911a5932c3a2c2439c06bba1116e556b0f25a0fd42847607e1098fd12dbf26c8`  
		Last Modified: Wed, 13 Aug 2025 20:31:17 GMT  
		Size: 21.6 KB (21642 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:da197c518bf419e77d160ebaf167e9b6c6a447f50906c494f4d2dcbae41252d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108001492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d130702cf880c7733b0c49a1afee72a6ea51a451415c72ceea7f67c69bbeca6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ad5d5d8733c993217ed51c06da1f717784940dfd73d260506fcf34539cf5c7`  
		Last Modified: Tue, 12 Aug 2025 17:26:58 GMT  
		Size: 16.2 MB (16150057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8705b5087aad2bc8a294c736b4c1d275231407c0c45612b11d77c4a38594cdd6`  
		Last Modified: Tue, 12 Aug 2025 17:35:51 GMT  
		Size: 49.5 MB (49507067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b565da2d23bacd0a7032eb614ca1d1e53dcd9332c65f48d30e52742e136cc7ab`  
		Last Modified: Tue, 12 Aug 2025 17:35:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6d2f1289ec892b8b7e9350de6e41a4eb488f4bca041f1cd43a47dcee1c139f`  
		Last Modified: Tue, 12 Aug 2025 17:35:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c886e2bb14813722e354c269145fd9ee3fae7d0c4d86090a01f5d6fd6e0353`  
		Last Modified: Tue, 12 Aug 2025 21:30:57 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2520f4d1e20289fd2b0e36f55b7321021dea3654444a81e518be8e7eceffd451`  
		Last Modified: Tue, 12 Aug 2025 21:31:02 GMT  
		Size: 14.1 MB (14107604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724d798862c6f3691b8dbdd59703a01d80cd84ea459cc04e38dc228f0e830047`  
		Last Modified: Tue, 12 Aug 2025 21:30:58 GMT  
		Size: 230.9 KB (230901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ed856daa4f60b807f473d4ebe06062b44438cd4e51095abe9e75028da46c47ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02aa99c0449a14fa4b29a32e016ec358fef3636588c10046d1a7a3874d0cf27`

```dockerfile
```

-	Layers:
	-	`sha256:9c9bfdf597f985c49c4656da26d889eb9ac33e1587c2b86398653a48b8cbeef5`  
		Last Modified: Tue, 12 Aug 2025 23:31:12 GMT  
		Size: 3.9 MB (3945840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3f0cf65f4d9b6f2ffaf678affc780366ca95e98d502e64e9b08039ef11df6b7`  
		Last Modified: Tue, 12 Aug 2025 23:31:13 GMT  
		Size: 21.6 KB (21585 bytes)  
		MIME: application/vnd.in-toto+json
