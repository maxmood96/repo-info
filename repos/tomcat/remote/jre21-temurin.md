## `tomcat:jre21-temurin`

```console
$ docker pull tomcat@sha256:1e8efa41829fb053e5935a3f48d7a3d683e6dbe257b11ce94cb057d4564a19f1
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

### `tomcat:jre21-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:341635ea3c5c12c972c822a0a734baef5bde461721961c609456d4d9d0c869ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113983175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6236b9f2661e281766972e6fc508b43a1a13dd06879e75c09eced246e702253`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b5aed643a2746ecfc921e7ee171f3fcda18376f6f8f6b7b86c19198b882f`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 17.0 MB (16971637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929e753abe01a9e7d3af83d05bdc847c5e9a63254f3229de0c0f8e2487a6a389`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 53.0 MB (52968896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a804483712f6cd22000b35e52c918077cb0e199f58858259d849136dd9b5`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b5750119b594b66e8ce6f0ad0e88067e7f320f7c36db50e1ff045c5d06f39a`  
		Last Modified: Tue, 02 Sep 2025 01:13:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc97f3e1b64cda7d71878540c6cf3485ddd1f9dbcae87f7811fbfed714c15ce1`  
		Last Modified: Tue, 02 Sep 2025 01:13:06 GMT  
		Size: 14.1 MB (14092238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f73d5c406db76e1c992015d072707771399beaf2e36c7cd4179ce82dbe11654`  
		Last Modified: Tue, 02 Sep 2025 01:13:04 GMT  
		Size: 224.7 KB (224698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:aa601ab7f98398ecd295849b114f0f57ed9756d07bfa02c76f2a442f91cbbcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33a289ddb0355da1c9d4fc7edf8d69386875fbacc0d371edd820f103c0cb4c1`

```dockerfile
```

-	Layers:
	-	`sha256:6af4244102fb60605d96f5c30eb5dc0f707ad22deb16c9b15885e5f2d60f4fa3`  
		Last Modified: Tue, 02 Sep 2025 02:32:57 GMT  
		Size: 3.4 MB (3352098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348d67c686bc68f537110f70abc52db6b35c64e534d9779a1df2188ad3c4ec93`  
		Last Modified: Tue, 02 Sep 2025 02:32:58 GMT  
		Size: 24.1 KB (24080 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:af9b10cff5e8740bd215d7777ade23f08c6a12c18b90d0c97673298cf869012f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112321131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0850d6d46fd2a6d2629fe3a0097004b7c4cf15c22938a97fc77702f1eb757f93`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82cb5b65623a0098d812fc3093e05fc877923cbe33814d2fdf26bfedfdc87fd`  
		Last Modified: Tue, 02 Sep 2025 01:00:01 GMT  
		Size: 17.0 MB (16988801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72895f8f6f6835766f4384b901cd9c849917e812386a716749233cc434286843`  
		Last Modified: Tue, 02 Sep 2025 01:07:12 GMT  
		Size: 52.1 MB (52148466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45da3a415496054b89e56e8796d3666d99d3a2023fd8d8f06b08fdba77c007a0`  
		Last Modified: Tue, 02 Sep 2025 01:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7646f1148db19c8d26d28f2132c9793bee48765609d023530dff185a5a6a36`  
		Last Modified: Tue, 02 Sep 2025 01:07:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0cea438020fce42ff4149bf9876824d674dc04264b5bc85f2ce081df667f21`  
		Last Modified: Tue, 02 Sep 2025 09:39:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8abc75af798d1e387aa4879a1057fc04bdbca9495795c4ccd7d55785603db4f`  
		Last Modified: Tue, 02 Sep 2025 09:39:56 GMT  
		Size: 14.1 MB (14095924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdae4be7f492ccbd0945ca5e269e302484e0ffb27d0727848ce742e1100e4ecf`  
		Last Modified: Tue, 02 Sep 2025 09:39:54 GMT  
		Size: 225.1 KB (225055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:ca5f304b6e445cdee5a1dba780d6991117b52226684b43d1162dd13ca020d1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6938cad18c17bb40e45f6a545aa2b0a9fe95f0ba12177188480e207b4eed629e`

```dockerfile
```

-	Layers:
	-	`sha256:481ad4a09bd8b02eceba31943f6063d578dd7a7446aed10230a52b820a9139a6`  
		Last Modified: Tue, 02 Sep 2025 11:31:22 GMT  
		Size: 3.4 MB (3352666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:003002ac2e31fd67d441268455304e5082ff7f33fc67834d556780b205e14411`  
		Last Modified: Tue, 02 Sep 2025 11:31:23 GMT  
		Size: 24.3 KB (24337 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6c731bb1402e5afd9bda4c3ad230a75478e63997daf7ec92a607e99928fa7fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120505129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae95f28f21f08589c38c5a39c0099ae655959de27cc85fa766976fa8c0d8247`
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
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85ac53e3ada2c73fae4a44e2b5328577d67806f9e18dabe8b55b2a62e771c8c`  
		Last Modified: Tue, 02 Sep 2025 00:16:49 GMT  
		Size: 18.8 MB (18814806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6942e90d4ed370039b17a91d00ca0af722fcffc8ebc405eff557e7091d3e6c1f`  
		Last Modified: Tue, 02 Sep 2025 03:33:37 GMT  
		Size: 53.0 MB (52994837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96b60e0b4bcad732c676ac05aae800cdfe43dd83c8483a5db2bdd2a9149e699`  
		Last Modified: Tue, 02 Sep 2025 01:19:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5b85f98496904cfb52272b542067760fd177744aec281aace00d00d9ce61a9`  
		Last Modified: Tue, 02 Sep 2025 01:19:11 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dc345b3d7fd5e36a266d2689e70ef0045587eadc0a590bca59648f7c009772`  
		Last Modified: Tue, 02 Sep 2025 09:53:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1fcfce8b47db5c5ab30cbb581edd220aefe5dc49f3765663ee9e052f8ed397`  
		Last Modified: Tue, 02 Sep 2025 09:53:43 GMT  
		Size: 14.1 MB (14106666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e52684e63ce1e678059040cb6ef17ca4f4afca2a061fc09e7ca1a298a327304`  
		Last Modified: Tue, 02 Sep 2025 09:53:44 GMT  
		Size: 256.6 KB (256644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:c6b0ab0b658f8f07070db6835714bcfa8f9da83d39b66b2bb92456f7dbfb4ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3380410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10869814527737bf97fd932f92e170b32da2fa0a88163c3c81e01c6a2de6e1c6`

```dockerfile
```

-	Layers:
	-	`sha256:2b95670202df3cd5a4ca442e43160cf73c3c57f58404cf9c49ce1547b9bd0679`  
		Last Modified: Tue, 02 Sep 2025 11:31:27 GMT  
		Size: 3.4 MB (3356223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17f1a04a76d2b2c59d1b7dfd60297d01f05435c01cd941440effb1e11add647`  
		Last Modified: Tue, 02 Sep 2025 11:31:28 GMT  
		Size: 24.2 KB (24187 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:dc4cddbec05fe068ff2dcb35874fb5026f449897094cfbfc283ba8d090d16443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114044990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4151d2ab06803b79fe8a3eb47cd03008b2a0e2099ca7cf0abb6567de9ae9caa0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 07:17:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:17:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:17:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:17:52 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:18:34 GMT
ADD file:07f3c32dd2b7f6af0f399701257442794654b72aa96759b98cb033a715461739 in / 
# Wed, 30 Jul 2025 07:18:38 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:b12e9b07091787c99b29dd2be63680c86c47e8be60a46566329007fb82cee41d`  
		Last Modified: Tue, 12 Aug 2025 17:05:53 GMT  
		Size: 31.0 MB (30951577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48af681b8ec6db282cced99124adaf7d258d933ef637b46da596f62b231927`  
		Last Modified: Tue, 12 Aug 2025 17:44:15 GMT  
		Size: 17.9 MB (17863907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbfe3ed9efed71dae22a46950ae2fd53b19b93e95762cb725d312d5374e785`  
		Last Modified: Tue, 12 Aug 2025 18:53:08 GMT  
		Size: 50.7 MB (50720811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a050e62896ae3f6627690501b0c497dff6e81e84dfbbe6fdb2eafa0173eb496`  
		Last Modified: Tue, 12 Aug 2025 18:34:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8360ba1c7447d291decf5adc5a48e97ae9b94614514edce23011d4f0df3c1`  
		Last Modified: Tue, 12 Aug 2025 18:35:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec103a472300ee2e921267481270690fb47f0c52d97475b1df9a87c980084801`  
		Last Modified: Wed, 13 Aug 2025 07:25:32 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b57994c0a2ec4006b21ed6385b7e46b3ee25fb22fc537bb6eb044c8fede9ff`  
		Last Modified: Wed, 13 Aug 2025 07:25:36 GMT  
		Size: 14.3 MB (14277966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43cbab61e58b89db917650b366fc953ea8b3f3084bc1e1043dbcb6a630e6c69`  
		Last Modified: Wed, 13 Aug 2025 07:25:33 GMT  
		Size: 228.1 KB (228085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:0f1ad817d4db9799116a6fbb4db56ad4f2c27e891ef9e7b7354559f98c767144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3368411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a5a92682d3d1bde97b7fd6e81aee646cf6117628d76c9a7f96600279d782bb`

```dockerfile
```

-	Layers:
	-	`sha256:811546fcfdca9751c1a16e19134c62eb6a102f9801eaa1bcaa638826749c1346`  
		Last Modified: Wed, 13 Aug 2025 08:30:17 GMT  
		Size: 3.3 MB (3344225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1f16364eacd1e1d8254645b2165d3292dc37215370563398db102b405dda45b`  
		Last Modified: Wed, 13 Aug 2025 08:30:18 GMT  
		Size: 24.2 KB (24186 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:a5f798aac1b92754b59716f6e9a0cb1f7afb292bd497d826b16ccdf3046923bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111357064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2bff18955dd0f7c8cbfcbaa25abdb9548b264074b016c0fc71d6fa7a4b35f9`
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
ADD file:9c3c50a7bf89c14623163f11927acdf7c8624c7519f83f2d95bf5a99ea4d21f9 in / 
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:80a64b6a7d961af355cc1a24ce954958de51e8bc2fb336684c1fbec689663c29`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 29.9 MB (29933009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d5f58fa09318554c52b155dcb73854bc79a0741b430e811ef3fa8a7793d23a`  
		Last Modified: Mon, 01 Sep 2025 23:13:45 GMT  
		Size: 17.6 MB (17580585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a63ecad82b8ee716b3b213599fa482279cbc3b8d696bbb149b6f5910d427bc9`  
		Last Modified: Mon, 01 Sep 2025 23:21:51 GMT  
		Size: 49.5 MB (49507311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee7e1a25504fee081580851375cc9c721296fa876ab017df07fa1eeec579cb3`  
		Last Modified: Mon, 01 Sep 2025 23:21:38 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b932a026df30a583d26bcfdaf74bfa4349681cde0e7bb2de116eb618524eef`  
		Last Modified: Mon, 01 Sep 2025 23:21:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f217685b3993cbb2f7e9b3ff4a029f0c8e575df407f99fbe6ef616e40e1b20c2`  
		Last Modified: Tue, 02 Sep 2025 02:44:03 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc87c07cbcaf355bf6aa11f2b2dfaf99c44844f48a91b44a78ac5fdaeffe66`  
		Last Modified: Tue, 02 Sep 2025 02:44:04 GMT  
		Size: 14.1 MB (14100846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81df90a254d8347753880d03f6fc318e75221c092c53dba1556a50dfe9c34e30`  
		Last Modified: Tue, 02 Sep 2025 02:44:04 GMT  
		Size: 232.7 KB (232670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:f19002154a63ea2914f8aeea28b3005c95466d1744c8830a3984fbfd000a6c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3378378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b680daeac7aec68085d10963117a2f578f6fe004789d2b0cbd52f582ff4d0f`

```dockerfile
```

-	Layers:
	-	`sha256:3eb5b7608bfc75f9aa4745397453b19d516a48be0fbcc7289b6c7eca3916f248`  
		Last Modified: Tue, 02 Sep 2025 05:31:15 GMT  
		Size: 3.4 MB (3354297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d138de0ad65f1d89c45a16d5d1ba88ad149c6e075275672c114d33a21532bb06`  
		Last Modified: Tue, 02 Sep 2025 05:31:16 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json
