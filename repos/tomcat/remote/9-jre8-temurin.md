## `tomcat:9-jre8-temurin`

```console
$ docker pull tomcat@sha256:18e5e51b3198b455602b6bac0ddb96418b28add1958bf2ea7c9b6a4d098e868f
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

### `tomcat:9-jre8-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:39cccc87e6717bf89a31602eedd500a8ad97e5b1cd4da8e3b0eb11a3e54b5d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102198653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe77980053d64712271246905c6ed608b0d24f1066bd720d0a18edc369ad069`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='49894dbe2f915dfad026cf7b4013118c0284e88359172499b1b25a4dac195ff1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055955e7c0bdd7731627a47c2b909505265e777f414b360f5817b2a9828684d6`  
		Last Modified: Thu, 24 Oct 2024 00:56:43 GMT  
		Size: 17.0 MB (16965892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff738d64e8041254685f7b12a1bd8fa586c0a4a1bb2f23fb992de8f9101c3c0`  
		Last Modified: Thu, 24 Oct 2024 00:56:43 GMT  
		Size: 41.9 MB (41884367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e23d769e80e3b494a1fd21ecb0f2e4159ce06694f704993de45eb425cb6997d`  
		Last Modified: Thu, 24 Oct 2024 00:56:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0320f3b646858da7ccb9c70b9dc34a039361c3a4269ee4ba80c591ade98f66fd`  
		Last Modified: Thu, 24 Oct 2024 00:56:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee55d0bb1c8869afe9b9d97e530cbcaff3b222149eda66faf123396737a7d53`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de996115e3e03eb7fd31554d418023436020a405e52584f10202b05b1d2d75`  
		Last Modified: Thu, 24 Oct 2024 02:54:26 GMT  
		Size: 13.4 MB (13372401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8128aa83986f887b06cd5894f230f0269077a87b1da8a4906b56ab5602801a5`  
		Last Modified: Thu, 24 Oct 2024 02:54:24 GMT  
		Size: 223.0 KB (223020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:2fcd79e7c2788d6588c9e8b07b252dd82af865757c5bbec440dd1e3841cbfe9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3234123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913459e0b07be3bd36b25a43e755ae782e4552956426fb156beabc6cf2a05d20`

```dockerfile
```

-	Layers:
	-	`sha256:070328ea13bf5828bc013038757068abd2248691044a669b493e35fe0af277a1`  
		Last Modified: Thu, 24 Oct 2024 02:54:24 GMT  
		Size: 3.2 MB (3210381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a039f119a98db251891d6acd6e2bba06e8efa6a37fe8b80f28d5b58a67a82ca`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 23.7 KB (23742 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:d72b0a4780b18221a27aa57699e744995aa7a70b0e419d4d7e65a1c0cec0ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96958421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfe06e908d5fbf4ca2ebf73f4bc4e596f4329ac8dae273a90730859a59e12ad`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='49894dbe2f915dfad026cf7b4013118c0284e88359172499b1b25a4dac195ff1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7366f29019b13f35e0d9413f97a4a0a5f8ba93fda8a3b0ffa435190fa01db3`  
		Last Modified: Thu, 24 Oct 2024 01:01:24 GMT  
		Size: 16.3 MB (16299151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2314476783c900e6706df1d64043cbaf11a89a3783049fe02c01944f23f1b12`  
		Last Modified: Thu, 24 Oct 2024 01:03:35 GMT  
		Size: 40.3 MB (40283263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a53c9b6087e700c7f9ed4f761954af8c23a17c06b2a35704415fa3e9f81e381`  
		Last Modified: Thu, 24 Oct 2024 01:03:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983a40113e83d1f6a0ee2b73ccfba08bbd96b45fa3352281762bccb5688278de`  
		Last Modified: Thu, 24 Oct 2024 01:03:33 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9577c168745c1323a6777ae3c0a7b33e8a4288ac3977a43db98865bbbf9a9bb1`  
		Last Modified: Thu, 24 Oct 2024 03:02:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7c54ffdc9bebe778cd74725dea6511aafdf30e248872241c9859b81bef787d`  
		Last Modified: Thu, 24 Oct 2024 03:02:18 GMT  
		Size: 13.3 MB (13312289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9d5e8e1cc51d8e55027dc82f8bf8c2d1fc95085c9ee041d5e76adfad9fcce7`  
		Last Modified: Thu, 24 Oct 2024 03:02:18 GMT  
		Size: 195.1 KB (195059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:0e5fbf55d8d1ccc8b5f203e2c2c83a4e8bc22c45e1ae0f4204bd1db4193fe0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb243bcd71e6c3aa41fc5d546b92ba6073f4a9b9b9262206161e1d7effb2657`

```dockerfile
```

-	Layers:
	-	`sha256:2bfb73c18fa1cc31507b4b16f5691b6ddf238353ea81f068e53239b0b68cbbd1`  
		Last Modified: Thu, 24 Oct 2024 03:02:18 GMT  
		Size: 3.2 MB (3216146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc049127079f3c512c9e54ae5f3f7c53eadf55ed0cddc25ac4702868a7c8b8f6`  
		Last Modified: Thu, 24 Oct 2024 03:02:17 GMT  
		Size: 23.9 KB (23905 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:fa23832358a48cd6e99d14bdbafe461520d208724b9cfe811eae0f1a0d640964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100344733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5a16c33643fa65a503ace260b5a1afe802f6f7890e45c8a69d6ac60fe7ae90`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='49894dbe2f915dfad026cf7b4013118c0284e88359172499b1b25a4dac195ff1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e2f7d4d887134d9aff4c6177e18f66336c5f3549bb3d16b0c27622e2b8b22c`  
		Last Modified: Thu, 24 Oct 2024 00:59:40 GMT  
		Size: 17.0 MB (16980397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f6307bf6600b4484d0bf66e8fe74a070d72cb21c8cc1a9d4b73c556c704116`  
		Last Modified: Thu, 24 Oct 2024 01:01:53 GMT  
		Size: 40.9 MB (40866852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d607b562041180b54cd10cb9644918d692e7a9a03475bd2684165dd2550d49b`  
		Last Modified: Thu, 24 Oct 2024 01:01:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc75a160106c7930339684e7bc788142bed3354d61e2de28815950205a48b6e6`  
		Last Modified: Thu, 24 Oct 2024 01:01:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfa20a12362f8a66298a11f98b508596f353099d14f26aea5c14e252e4a2215`  
		Last Modified: Thu, 24 Oct 2024 12:43:48 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323032f224eb935cac678f5f054a91d50ca66749d7ead75c128be2a40a06db5c`  
		Last Modified: Thu, 24 Oct 2024 12:43:49 GMT  
		Size: 13.4 MB (13385547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a51398445ce26549e48448b20f166052d281f200ca930f9a67e287f8cb5561`  
		Last Modified: Thu, 24 Oct 2024 12:43:49 GMT  
		Size: 223.5 KB (223482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:d954261a2f2c13b06bdad02ee54b7dd74691e7d0e945dc5fb7c8c28bfa657469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3235565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a98b3505692ea7cd5a150c7b4894dcbe4ea6a24a5f95a9c8d1a96b2c4e37a8`

```dockerfile
```

-	Layers:
	-	`sha256:1651bb96a919628cc31b7096c094dd65c8b1163161beeeeb3c4ba4fa469c27b7`  
		Last Modified: Thu, 24 Oct 2024 12:43:48 GMT  
		Size: 3.2 MB (3211603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08d65ba3f6aa3c5cc3c0679f4da155fdb4b878a0ad25d842d2a39b96e5ddb29d`  
		Last Modified: Thu, 24 Oct 2024 12:43:48 GMT  
		Size: 24.0 KB (23962 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:0d477d1323a7c8b8b462b6ef0e36ac9f84d751593ce847c1ae88bd8968588dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108174522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fb3c651b89c9f6b0d0100694999a10256c6456fda5f5853a67b8c007249426`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bb8c8cc575b69e68e12a213674ec2e3848baff4f1955d2973d98e67666ab94d7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='786522da4c761104dd8274c81edc90126a25acaafbbbc5da886b3fb51f33cba2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='49894dbe2f915dfad026cf7b4013118c0284e88359172499b1b25a4dac195ff1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='c573f33f9e5ba49a4838847d0d34efc9c1dc57a9ba71b926599530bbcda87f65';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934d62dfcbb2f92a5773b4afae3cf1e237d9d7480589662f71265729d2c39143`  
		Last Modified: Thu, 24 Oct 2024 01:00:29 GMT  
		Size: 18.9 MB (18858677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965ebbd71f6896ebe543d5180dc80f1b9c3571ec1572c43c9cdb7568650f2900`  
		Last Modified: Thu, 24 Oct 2024 01:04:05 GMT  
		Size: 41.3 MB (41258799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98424c692abe522f96bd5315b82ce19a01be2d22fbf9eeeaa97152a47415780b`  
		Last Modified: Thu, 24 Oct 2024 01:04:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803bbcbca249316d17602abfd0f88d0f1fa6b2be5463d4920677098a24841dfa`  
		Last Modified: Thu, 24 Oct 2024 01:04:04 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b83d9c722ee7cab82c5ddb867ae6c4a4ba7694d46a9c489548597a01b54466`  
		Last Modified: Thu, 24 Oct 2024 10:01:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ac2fa0ed15a8dd2389b52ef28262546896b271ff5032c82c342063c543c4ec`  
		Last Modified: Thu, 24 Oct 2024 10:02:00 GMT  
		Size: 13.4 MB (13410673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b550a2911ed3f03e6051d8a72b4c1cb21e8b6f87426ecad5e5a1b9dc177b7`  
		Last Modified: Thu, 24 Oct 2024 10:01:59 GMT  
		Size: 254.8 KB (254792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:74dfda43dd1d7fae43f920d068691e86e094dd4b5dac1b1368805bb5eca1e128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3238863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0c865dee9409d14196404cc2b78fe7083f8c49c7bfd20b88a7b7667b688499`

```dockerfile
```

-	Layers:
	-	`sha256:0b9cc1edda507dd8df958990979a6fbeb86908a4723a112924ba7f983a2f453a`  
		Last Modified: Thu, 24 Oct 2024 10:01:59 GMT  
		Size: 3.2 MB (3215033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5881e533159048329057bdcc333efad1b29cd7fc1306670a37f0b20d96498921`  
		Last Modified: Thu, 24 Oct 2024 10:01:59 GMT  
		Size: 23.8 KB (23830 bytes)  
		MIME: application/vnd.in-toto+json
