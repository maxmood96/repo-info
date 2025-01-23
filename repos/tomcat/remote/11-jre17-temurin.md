## `tomcat:11-jre17-temurin`

```console
$ docker pull tomcat@sha256:4820e7cf873710dbee50ff0be2a9aaa3093399ad0684f3c68471fce585cbbeb0
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
$ docker pull tomcat@sha256:e93ad1c50b55a119571c7c777579553fd68919723945bec53fb1b1a332ccc4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107515474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f6c016eeb9dcf9f27db7468a0e0c709164d1d03f71c0fce1c0455320ef0f60`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_VERSION=11.0.2
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_SHA512=635d0b704d47a97050e3de995d372ef361ddb7589efbc53003afd6ac692d8db4a4125ae5dcc01af9e7371e8e598c98982e2a25617179b6ba0a04406299cca544
# Mon, 13 Jan 2025 19:02:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT []
# Mon, 13 Jan 2025 19:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2cb0ec536fae9a1d80cad8b56b3c05119e2b57a0d04af676008312af681aea`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 17.0 MB (16966698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587b49ab5385c6f5be0e6991c10019ab858a1af9825c21ccdda057797d644f80`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 46.9 MB (46941810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca0dfb15aaaf344fb918a4b317840752b2893048212ad3919135d3f8a3f5a04`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a2aa0ee1f1005a034027e32ac2cf1fb52534ead7ab4409e049bf1126c86c96`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5ca9a2822c655c14ba8d9d9558a2adf897e236f06a598e56ac750354d30517`  
		Last Modified: Wed, 22 Jan 2025 20:31:41 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe3fbf9e9f6d347f60623d3d946d7f43433c69a214208a7f6ae9d21cf20cb5b`  
		Last Modified: Wed, 22 Jan 2025 20:31:41 GMT  
		Size: 13.6 MB (13628970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e94557c29d88b50ea4e2f958f00717fae2f862b15a1e1da5cddbd8ff40de8d0`  
		Last Modified: Wed, 22 Jan 2025 20:31:41 GMT  
		Size: 223.4 KB (223383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:3f4c837940a943222f571bd9e3a559cf51fef502d4bea86ef567f5cb96eacbc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3204626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e122017aee12b816125edb4d05e32e6722690305b2f24bce5b0913ecb1cf7b6`

```dockerfile
```

-	Layers:
	-	`sha256:ba85102a3170691e255bc86c661dfe2f74bd6e7b45228823ef85414e3720dcc4`  
		Last Modified: Wed, 22 Jan 2025 20:31:41 GMT  
		Size: 3.2 MB (3180548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c00f3a76b53ce3135dcb6b96ec0d01b6a1a559e4d7e244fff613eef0ec894a8`  
		Last Modified: Wed, 22 Jan 2025 20:31:41 GMT  
		Size: 24.1 KB (24078 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:67a7af7abdfea0fde23d97b78452204953a557bf9d6d175fb46d60754b0df6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103818645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f7ffc70051c55b871d531fd5caf2f18652dfc6e075644c8a50e0deb4d8f54d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_VERSION=11.0.2
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_SHA512=635d0b704d47a97050e3de995d372ef361ddb7589efbc53003afd6ac692d8db4a4125ae5dcc01af9e7371e8e598c98982e2a25617179b6ba0a04406299cca544
# Mon, 13 Jan 2025 19:02:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT []
# Mon, 13 Jan 2025 19:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bb03609fc493db283c91c9deb06c7b0f9447e9ec0047902ed4ffb8195fbdb`  
		Last Modified: Thu, 23 Jan 2025 01:40:03 GMT  
		Size: 44.6 MB (44615957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d9f8e55c756b9f044ccbd12dbad8925b980c880b226b170ec44496e315a14c`  
		Last Modified: Thu, 23 Jan 2025 01:39:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b23228402ecb69ebe4ea10ce74e4495add57d90900845f4bd6904cee18c7955`  
		Last Modified: Thu, 23 Jan 2025 01:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79aee268624e4d538f47946aa36d9acec6b7378bfce2c3c6c0d8daf4bf76b78d`  
		Last Modified: Thu, 23 Jan 2025 05:42:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d482dfabb447ca6727a31e969cdba6fec983b3548c4b928d213d6fe43311e6`  
		Last Modified: Thu, 23 Jan 2025 05:42:45 GMT  
		Size: 13.6 MB (13603745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145825f5b4cab7ef79f79cc706a0b37ce07b5515b59453210f59211e86c52d53`  
		Last Modified: Thu, 23 Jan 2025 05:42:45 GMT  
		Size: 2.4 MB (2426752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:dad8b816fc60781f1d36598c1c6c0226affa54dd01348b636797a1dbf83c825c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3207220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa92dd25d5dfe41e631e628e62d97cbd6ecdf624fac3847860894620f1d97aab`

```dockerfile
```

-	Layers:
	-	`sha256:d6f12b4cb490ff078d06183ec780b87344222515b5363f7fdc469bd6a7381ac6`  
		Last Modified: Thu, 23 Jan 2025 05:42:45 GMT  
		Size: 3.2 MB (3182952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685659d5b6d617b3bb8709bc1b4980d255f5328eb51dbafdbec831adb812b40f`  
		Last Modified: Thu, 23 Jan 2025 05:42:44 GMT  
		Size: 24.3 KB (24268 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:93349f12c91e32a3c73766baccc47cca53763f08cfcf2dda9f849494ca3daf25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107661694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1346475bcbb61ffb09deefedfb95d433750265c1ee31483c2ea52b065a4458`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_VERSION=11.0.2
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_SHA512=635d0b704d47a97050e3de995d372ef361ddb7589efbc53003afd6ac692d8db4a4125ae5dcc01af9e7371e8e598c98982e2a25617179b6ba0a04406299cca544
# Mon, 13 Jan 2025 19:02:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT []
# Mon, 13 Jan 2025 19:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdecf092a77e3bcc60bf2a2f0d9bb37477afb75ca7c9781f98a76d3722450717`  
		Last Modified: Wed, 22 Jan 2025 21:06:49 GMT  
		Size: 46.4 MB (46430926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46396c1812fff3f42c7bce2cfc29c910045b7fd281e96d27491bddc27a25f4a5`  
		Last Modified: Wed, 22 Jan 2025 21:06:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1d9c149d4e66dbbc5d2f77d496f834696346b93887893c1a1b4cd3dbc46ff9`  
		Last Modified: Wed, 22 Jan 2025 21:06:48 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97be03f8c1ceae9246d08d9cad75d685289df723a3277870c2dfec2f67ff8b`  
		Last Modified: Thu, 23 Jan 2025 03:46:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db095b20975126d1608074ae4193366c76eaadf049fc39d66f648ed31924664d`  
		Last Modified: Thu, 23 Jan 2025 03:46:37 GMT  
		Size: 13.6 MB (13630959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba034a5c918cd50b325b3d9e32b63b47790ea4b85e92c3d923b1ad79c3b3be9b`  
		Last Modified: Thu, 23 Jan 2025 03:46:37 GMT  
		Size: 1.7 MB (1721637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:03f4cad6157157278d27298a46982a6f769217cf0e293aec564e4d2be7db5107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3205452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d35a9b8e5b948585eb58393bfcbdff4bbad8d3f0caded81204c0b6910f4114`

```dockerfile
```

-	Layers:
	-	`sha256:342f8ea0f7547f7e7089f6ca87765722540582f68426e02705babc4018c1a746`  
		Last Modified: Thu, 23 Jan 2025 03:46:37 GMT  
		Size: 3.2 MB (3181116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a37ae82ddfa736f2a10d8faac7d90040ec5b87f73c6a0c96ccee96f698d56cb`  
		Last Modified: Thu, 23 Jan 2025 03:46:36 GMT  
		Size: 24.3 KB (24336 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:98d7be880521917ce5494aa2bb9fe6ce474606eb275abe405813b604b2c3599f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115625125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd36ac3b1728c158d75bb5c4ea37118942adb080f00f71a27b88b6077f72556`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_VERSION=11.0.2
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_SHA512=635d0b704d47a97050e3de995d372ef361ddb7589efbc53003afd6ac692d8db4a4125ae5dcc01af9e7371e8e598c98982e2a25617179b6ba0a04406299cca544
# Mon, 13 Jan 2025 19:02:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT []
# Mon, 13 Jan 2025 19:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08691d29d174440113fb3d94aec487ff706b850acfce25b3870b67886fdc90`  
		Last Modified: Tue, 03 Dec 2024 04:44:50 GMT  
		Size: 18.8 MB (18845906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8f9d6853a83ad5a37bd7c8a7161826d5afcd91b7453b145146a6797888de88`  
		Last Modified: Wed, 22 Jan 2025 18:49:38 GMT  
		Size: 46.8 MB (46762225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e2e2a2c9e65908e8ef164b1d8f2fdda444ba6fef016ae67bafbc6228acef5`  
		Last Modified: Wed, 22 Jan 2025 18:49:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09d73a72757bfd0c0dbd5f2be53b2f7ea8c6cdcb72abba5f2fb4fbcb0be1fec`  
		Last Modified: Wed, 22 Jan 2025 18:49:37 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ad6a8a334be2971d6fc5e818e6de199015b80a0890ec9dcd0672823fc1800a`  
		Last Modified: Wed, 22 Jan 2025 22:12:45 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe94f217eeae7aa34cb68734bc2161151cb115ce04e39cff054c0fc33b4930e`  
		Last Modified: Wed, 22 Jan 2025 22:12:46 GMT  
		Size: 13.6 MB (13645666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5fbdbe66c638104d8ebd28c8483c24dc60f0a14ffca8a72f90735d4c597a7c`  
		Last Modified: Wed, 22 Jan 2025 22:12:46 GMT  
		Size: 2.0 MB (1979862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:d3884bb4a3750ec860922477fe6910060dbb78c9512c499e0e9ca889ea96ace7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3208715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df31ba7f298202a4316e21ee2d5f6103441ff0c7d959e01359aca1ffb6a6461c`

```dockerfile
```

-	Layers:
	-	`sha256:6447979a86b0f52e39b1c8aedcc05da45c1ac8e3740bb3079ad32a7f0edbc773`  
		Last Modified: Wed, 22 Jan 2025 22:12:45 GMT  
		Size: 3.2 MB (3184529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3f188316cc9716b292b7367b14c188d13167d11e732d0a2878e15d80b00e1f`  
		Last Modified: Wed, 22 Jan 2025 22:12:44 GMT  
		Size: 24.2 KB (24186 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:f0f8336f77d29744c90026956dfcca4d9610e184c63c448b16d2d164e556fe60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106775512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50ba77ab0518e0139985bd313674475c8cc2dab7b759d252a80e9d4a4058a90`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 19 Nov 2024 16:33:48 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:33:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:34:25 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Tue, 19 Nov 2024 16:34:27 GMT
CMD ["/bin/bash"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_VERSION=11.0.2
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_SHA512=635d0b704d47a97050e3de995d372ef361ddb7589efbc53003afd6ac692d8db4a4125ae5dcc01af9e7371e8e598c98982e2a25617179b6ba0a04406299cca544
# Mon, 13 Jan 2025 19:02:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT []
# Mon, 13 Jan 2025 19:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f71802e45f04a2768174040c20bde61c8c2abaf2a16ed53d5c7442cf9dc97ae`  
		Last Modified: Tue, 03 Dec 2024 06:59:56 GMT  
		Size: 17.9 MB (17861902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6672ffb8744c6b61674432ef8878351da333e1cc92db9628630a951802262617`  
		Last Modified: Wed, 22 Jan 2025 18:36:52 GMT  
		Size: 43.9 MB (43887882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96dede376f399bb603ad27d7519a8060f0425818841e4c3c909b4ed83ba490`  
		Last Modified: Wed, 22 Jan 2025 18:36:45 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb482a30c0beb4c789b3f7435e936c7bdcae3b65093918c814d0804b6cae114`  
		Last Modified: Wed, 22 Jan 2025 18:36:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a203538122d409342b1ced026036171b302594ef5d508e2844b27af0c8f3612`  
		Last Modified: Wed, 22 Jan 2025 20:37:25 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2f80cefb04d95f011fb68256e340bd2396e8afe1f35d270a4f3e73ebf36adc`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 13.8 MB (13816078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfac8cc7866628de403bc9048428fbcb573b53ceb34e5addd3edfb96beae320f`  
		Last Modified: Wed, 22 Jan 2025 20:37:26 GMT  
		Size: 226.2 KB (226164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:8a502296d6ac0f563b9cb74b1a20a9db6ef0c70db2fb4ba15cf9c5e1f8c537df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3197007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33d260f1444c5ec21ca6f9c422710d4c69a223ec8c0348d4e9187b48bf745c0`

```dockerfile
```

-	Layers:
	-	`sha256:d90fa773e25842ec56d0bd32f7b94a159704c47a25ddead1056e735c72634407`  
		Last Modified: Wed, 22 Jan 2025 20:37:25 GMT  
		Size: 3.2 MB (3172823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc253792a0d907556f3892eabdabf61157e82cb89cc1ab018ce1fd642e921aff`  
		Last Modified: Wed, 22 Jan 2025 20:37:25 GMT  
		Size: 24.2 KB (24184 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:88399170aa76ed9cad5401142dc08cf57928497c0dd8cd9bde0be6d78f4811e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106877385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddfd71608bb400fbe674d6185fe8d098bc9155646bb0205fde712281e4a6770`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:14 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:16 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Tue, 19 Nov 2024 16:18:16 GMT
CMD ["/bin/bash"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_VERSION=11.0.2
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_SHA512=635d0b704d47a97050e3de995d372ef361ddb7589efbc53003afd6ac692d8db4a4125ae5dcc01af9e7371e8e598c98982e2a25617179b6ba0a04406299cca544
# Mon, 13 Jan 2025 19:02:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT []
# Mon, 13 Jan 2025 19:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13455a8ef0bbd24a83e365c2d75ff490c2b96ae8d038965b9151dd68fc2f3011`  
		Last Modified: Wed, 22 Jan 2025 21:45:34 GMT  
		Size: 17.6 MB (17614209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c099e3bf1f033a8c74b8e360a0a89ff2a11702f02653d0a67bc1f2fd8f8ec4b9`  
		Last Modified: Wed, 22 Jan 2025 22:00:35 GMT  
		Size: 43.9 MB (43943267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65d2507343af9ee6571dc4a972f2f016cc048c88f57fb049b4c073b5e00644`  
		Last Modified: Wed, 22 Jan 2025 22:00:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3613bf83e6a2825a8ad18388dabb683e2397ddc901e27f1729a14bcfd4984a`  
		Last Modified: Wed, 22 Jan 2025 22:00:33 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85377739c02645f82f154a1d27f03f895ec85211458a4958c1f7dd0bee1c71b`  
		Last Modified: Thu, 23 Jan 2025 05:14:51 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46732a2d7bb236fa93f88fd833dd036c7b30fb1a5ca90e6e042da5cc80f12c14`  
		Last Modified: Thu, 23 Jan 2025 05:14:51 GMT  
		Size: 13.6 MB (13639406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af0edac508d67442722f38a0ad39520a1d6aac761522f8c372f16ff1a70abce`  
		Last Modified: Thu, 23 Jan 2025 05:14:51 GMT  
		Size: 1.7 MB (1657032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:8735e6c50c72a5942e98c55bcea3183ce47597c7be9f851ac0dd490d6d4280d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4d400777041e7b42bb475cd2b71507ccbb4f97d7a2673ae23a54b081ab891e`

```dockerfile
```

-	Layers:
	-	`sha256:cfad0db9f3d87ff493f80f350be27e3f01eef5a966a904f20a3c069028f54358`  
		Last Modified: Thu, 23 Jan 2025 05:14:50 GMT  
		Size: 3.2 MB (3182747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ed5cb6132f388bb87c85b743eb4de098f76fb19d9d4f08c83f4370f0b215bd`  
		Last Modified: Thu, 23 Jan 2025 05:14:50 GMT  
		Size: 24.1 KB (24080 bytes)  
		MIME: application/vnd.in-toto+json
