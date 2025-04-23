## `tomcat:10-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:35bec5d12930e0f1741754b1f6571053b9f36c792a836ea28a058da23b9921df
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
$ docker pull tomcat@sha256:b6aab2a6bf2d44f95aeecf7be4e23415cac0406cfebc04c68b70791dc3952ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106974701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd97a3247d5590d763e1c5e6bd99465248334ff8f3971909c35467ee71aa08f1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_VERSION=10.1.40
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_SHA512=2bde772acf2e6f300f0f8341eb4de7da5d59af6a95f607bcdb92e4c22e0a253d437ea9a423d7d3e334af1c608f33489f32d32d346fbef5b0abef1dee666895ea
# Tue, 08 Apr 2025 20:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT []
# Tue, 08 Apr 2025 20:03:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ed2c14dc35cadb9be8eae30092c08047c7a92c991ce46bb2879cc5062104c`  
		Last Modified: Wed, 23 Apr 2025 16:31:40 GMT  
		Size: 16.1 MB (16146104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcf21dcaba64ce66616cddd8855c6af8fc87f7abd5bd9a9de4853c136bdaf13`  
		Last Modified: Wed, 23 Apr 2025 16:31:41 GMT  
		Size: 47.2 MB (47222865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b66c1391fc104d1410daf6eb1c7583ffee89fceaff141b39ac7d02e047f6c1`  
		Last Modified: Wed, 23 Apr 2025 16:31:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dd5bc592c5c010b3c072636a18ecbc8cb265afa811151d9dd11d28c1ce6d23`  
		Last Modified: Wed, 23 Apr 2025 16:31:40 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7634dfa7e250885aaecae2c8766d22f63b6cc5d76ea75314fdcbae6130e80e`  
		Last Modified: Wed, 23 Apr 2025 18:11:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee7cf9fb8a2080e630c576c4b6705b78b611b78c00cd429b027a26eea18b9aa`  
		Last Modified: Wed, 23 Apr 2025 18:11:13 GMT  
		Size: 13.8 MB (13841081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f9c302fb7eeefc6a6eb86f69152486b6e55184e9bfc885c17a2df8a6b0ff19`  
		Last Modified: Wed, 23 Apr 2025 18:11:13 GMT  
		Size: 229.6 KB (229644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:a5b72981b8be718e1e5337daa16ef7ca36581a13738d08bfec73a3506442c30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb22806b37173d2bb47b7b2f0f7c36f78fc8096da12fa054fd0b0ab657f58e8`

```dockerfile
```

-	Layers:
	-	`sha256:122b56954ed559dacc0eaca94e17111ef86cc641a1a587f3a58a4fd9213efe71`  
		Last Modified: Wed, 23 Apr 2025 18:11:13 GMT  
		Size: 3.8 MB (3782598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bf6e2bc0b5d6b153c32edd420cc9a3e347281344815bdc42d2593b863e3ac6`  
		Last Modified: Wed, 23 Apr 2025 18:11:13 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:c5fb6bdf32d331b511a458b7487db53d1135ad1dd62b94501d3b1b468ba93345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101889037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e86bff57267193ba72c2af254e2458262410c029916b93e7a07b7e27eb3428`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:22 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:25 GMT
ADD file:b27bdc0157c0d964026ea411ed5874766d804b491dfc3d5ac10188c76746bbb0 in / 
# Mon, 07 Apr 2025 07:27:25 GMT
CMD ["/bin/bash"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_VERSION=10.1.40
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_SHA512=2bde772acf2e6f300f0f8341eb4de7da5d59af6a95f607bcdb92e4c22e0a253d437ea9a423d7d3e334af1c608f33489f32d32d346fbef5b0abef1dee666895ea
# Tue, 08 Apr 2025 20:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT []
# Tue, 08 Apr 2025 20:03:21 GMT
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
	-	`sha256:c4c1b05c4993de47c4bb917f120c7e7bc0e5572a9dfe923f21047104130cd4c9`  
		Last Modified: Wed, 23 Apr 2025 17:05:42 GMT  
		Size: 45.3 MB (45336505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09917f5ddd9a0b808fada61ef5a6c4a583066f7602d8f58d69ab4ee84e4676fe`  
		Last Modified: Wed, 23 Apr 2025 17:05:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82baf3fc8d3fb0b1d7ed28b863d43edf6576dc3950517c262bc414bc34719efc`  
		Last Modified: Wed, 23 Apr 2025 17:05:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8661d2e9c30241a4f18c621f18b2af2a55562afe726c29055cace107decf438`  
		Last Modified: Wed, 23 Apr 2025 18:20:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b2ab6d6c86c40ca282765f7bcdbe7788f205e5a29ce7e343bdeba080fb8fab`  
		Last Modified: Wed, 23 Apr 2025 18:20:54 GMT  
		Size: 13.8 MB (13816442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a630de234669d537f26619ab809bf0dbb77787a160567016ca4b24c22c3c67df`  
		Last Modified: Wed, 23 Apr 2025 18:20:53 GMT  
		Size: 202.3 KB (202318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ab57c288af7d0b50a575a2ed93f7dda27249bcd04c2193e4ccfeadd70665e979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16164eb5ef18607be01968b23b8d11de3d253bb2aa7bf72ff738ab3b9980556`

```dockerfile
```

-	Layers:
	-	`sha256:99c0c702b2eadbcf10c1cb58ac42d14f527167c0f8d88e48170fdff680edaed6`  
		Last Modified: Wed, 23 Apr 2025 18:20:53 GMT  
		Size: 3.8 MB (3786196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d123fd086013e2f2e5a44a8543d9b62f8c900a881bf6bef31ebd8528558b79`  
		Last Modified: Wed, 23 Apr 2025 18:20:53 GMT  
		Size: 21.4 KB (21380 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:c45df1564654518a274a1586435438c1b7b04e0ae347b2790dea7572b33768bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103065124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d2e1538476c022f121994f28f8603fa8c6638e4f90cce3a34d1afeaab6345c`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
# Tue, 08 Apr 2025 20:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_VERSION=10.1.40
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_SHA512=2bde772acf2e6f300f0f8341eb4de7da5d59af6a95f607bcdb92e4c22e0a253d437ea9a423d7d3e334af1c608f33489f32d32d346fbef5b0abef1dee666895ea
# Tue, 08 Apr 2025 20:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT []
# Tue, 08 Apr 2025 20:03:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d988c284109adb0ee08f6d6a95a152f6e364456e1a4853bb6c3ebc58c40f099`  
		Last Modified: Wed, 09 Apr 2025 06:58:01 GMT  
		Size: 16.1 MB (16059566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67dbe119a2ce8ff639dead6b3afbf505a5c72548dd53a51e7efc6632f22ba7c`  
		Last Modified: Wed, 09 Apr 2025 07:02:35 GMT  
		Size: 45.6 MB (45576991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba7fd16eb5988b8efe5dbeff5717cf6472feff3d8a5f32cdf9fb7e5b8a92cca`  
		Last Modified: Wed, 09 Apr 2025 07:02:33 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528004d4c4b47ba57e8d0a152cf84780e2f8bec7f46a69a62d7253d09a6f51c1`  
		Last Modified: Wed, 09 Apr 2025 07:02:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b132adfb05f1483e149ac41e8066bd7a929469a0205b745fe3bd5faf76b1ab40`  
		Last Modified: Wed, 09 Apr 2025 20:00:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f4c87ad715440a9b22baf3418fbe5a64645815a1eaeb48af4c0fac2e14ef69`  
		Last Modified: Wed, 09 Apr 2025 20:00:27 GMT  
		Size: 13.8 MB (13843022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf63193bc710613cec4fcb096353d3c68a89e0baf6d5fbbbb083944a3ece21`  
		Last Modified: Wed, 09 Apr 2025 20:00:26 GMT  
		Size: 228.7 KB (228671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c95d140fbab5fa2f60f0d06e5614dc4e45b13eabc9d3c4d432752c5418f88020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e525bb8c33ab24b442827dbf3328ceaf39a380e506149c7b68c4d1e42dd3db5c`

```dockerfile
```

-	Layers:
	-	`sha256:c9571f28b547a14a7b8cf5fd4e9e9ef6d0ddb46c421655801ff26afaaf7eed9a`  
		Last Modified: Wed, 09 Apr 2025 20:00:26 GMT  
		Size: 3.8 MB (3782885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2280e9a7d09b2107d8deceef3611f322a6859f107da1ebf53615726adabde1`  
		Last Modified: Wed, 09 Apr 2025 20:00:26 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:207b1e3c0064bc5ca05f1070dbceaa2036bd4a1b2c78b299cb5f5c66e16e8aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108855424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3f7ef6b526ce8f5e033019175b693cef1897de8fdd9cb39ed2c3cfb79293e0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
CMD ["/bin/bash"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_VERSION=10.1.40
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_SHA512=2bde772acf2e6f300f0f8341eb4de7da5d59af6a95f607bcdb92e4c22e0a253d437ea9a423d7d3e334af1c608f33489f32d32d346fbef5b0abef1dee666895ea
# Tue, 08 Apr 2025 20:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT []
# Tue, 08 Apr 2025 20:03:21 GMT
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
	-	`sha256:581d6d84bde8236ba32237ecc60e430c0b7ebd4ac11c2d7d8c9386b940f10598`  
		Last Modified: Wed, 23 Apr 2025 16:38:24 GMT  
		Size: 42.7 MB (42678572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1566d95b5e544c0fc8a7935a1e5e2c6d7b8be3c54af4df52df1f5cefd45083`  
		Last Modified: Wed, 23 Apr 2025 16:38:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a827606718b09ed44b68022af619abfc078046f21313ce6b6827f2aa90b65a`  
		Last Modified: Wed, 23 Apr 2025 16:38:22 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc206469a403916b8ae0f139f5760a6c91f9b011098555e03d2367e77017ed3`  
		Last Modified: Wed, 23 Apr 2025 19:03:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376831ce372bd0590bc9a14ebc2c9fbba7d4c9aee2e16a62aed602fb6a9c267c`  
		Last Modified: Wed, 23 Apr 2025 19:03:03 GMT  
		Size: 13.9 MB (13854609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceef51035982246072cf004635a4fbce7c562b2738b0c7fbedacf6b934d2d120`  
		Last Modified: Wed, 23 Apr 2025 19:03:03 GMT  
		Size: 259.1 KB (259089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:1cd39d35c3080dfb71fcfc2344bfb4d412997b12742cca14d900e7355924dfcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5635fa0be4744e6c4d56a4a11b33a13c044857acd29abb800dbf343cb1a861be`

```dockerfile
```

-	Layers:
	-	`sha256:030c3e635b7e6fb4cd156b3afbb0daf71edc751e944a1babe664b4a67dcb424e`  
		Last Modified: Wed, 23 Apr 2025 19:03:03 GMT  
		Size: 3.8 MB (3786540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbab64e72c21cf308469ba267b768724c71b0a8d0842f4fc1db6c93bcc43026`  
		Last Modified: Wed, 23 Apr 2025 19:03:02 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:04fcad3c0ececf182d723858cc4f4be55adfd9038698c8b81e0760d36a0f95a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99061840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8ab98ef70e7b9b03838cd090ee8c2f39c9039c08b75b4208aaec24b69689ab`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:00 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:00 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:02 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Mon, 07 Apr 2025 07:25:02 GMT
CMD ["/bin/bash"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_VERSION=10.1.40
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_SHA512=2bde772acf2e6f300f0f8341eb4de7da5d59af6a95f607bcdb92e4c22e0a253d437ea9a423d7d3e334af1c608f33489f32d32d346fbef5b0abef1dee666895ea
# Tue, 08 Apr 2025 20:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT []
# Tue, 08 Apr 2025 20:03:21 GMT
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
	-	`sha256:07f36c456d4031df31256ad76640c57eed524c021d034d68b0ae289681ba71bf`  
		Last Modified: Wed, 23 Apr 2025 16:35:18 GMT  
		Size: 40.8 MB (40839664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d6f9ea55a662419d9d51e0185b2a237945c8c345810b39eee2659f0f61506e`  
		Last Modified: Wed, 23 Apr 2025 16:35:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed11ab89390f96ee5b7291b78fae56a9223fe71a6f7af5230c00a2001efdf7b`  
		Last Modified: Wed, 23 Apr 2025 16:35:17 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3aa5fa7b8187139f9ef8f823985afd84cdca2d4ccb8ba2f0340059c001f16af`  
		Last Modified: Wed, 23 Apr 2025 18:15:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48148409fa9bf81079d61a8f48a965cb81476a928e0d9eeac2f18b4cadfe2e4a`  
		Last Modified: Wed, 23 Apr 2025 18:15:31 GMT  
		Size: 13.8 MB (13844964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67024484f7f63f0cac021047bcb16d4c1de95694d9e7a5efd4b0b636bbd15ce1`  
		Last Modified: Wed, 23 Apr 2025 18:15:30 GMT  
		Size: 230.9 KB (230897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d24222fb2f4f6c0b98b498c430eccaf451ea9704fdd72da09dbd482d024391e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3805459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42425ab89cc5b23b908cf5e687e304d11cec551f9bc6dfd9ee3edadb905ec1a8`

```dockerfile
```

-	Layers:
	-	`sha256:a8dc2617000fe0df190177040ab1c1a1d86a30c7775c075fa2339f7641bdb77f`  
		Last Modified: Wed, 23 Apr 2025 18:15:30 GMT  
		Size: 3.8 MB (3784195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71339334d5d07e70a54176f989dea07fca7928406835c54c4a490d9637559740`  
		Last Modified: Wed, 23 Apr 2025 18:15:30 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json
