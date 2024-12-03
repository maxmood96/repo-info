## `tomcat:10-jre21-temurin`

```console
$ docker pull tomcat@sha256:8bd355ee461e5fb9a8991fc7d1f7a9b30e6f4568d863338ea391973f8eaa5f6b
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

### `tomcat:10-jre21-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:53064524f636b1d08cf37797a53b93ebbd708df29a3880e45ee54a4db91b4845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113406164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09bee4dd0d420c9b92cde26c7563c1e2174fdee7d0b8918b9dad5177b89a37c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 Nov 2024 15:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Nov 2024 15:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_MAJOR=10
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_VERSION=10.1.33
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_SHA512=f58c9d8029b1ec18d017019dcd68eb679b323f5c4f5d3f33f1a9bf3a4616db718ee3b44f8acc421ffaed67f4c2ca4647be0c7fa04a80274afd18a083711c5ece
# Mon, 11 Nov 2024 15:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 Nov 2024 15:03:18 GMT
ENTRYPOINT []
# Mon, 11 Nov 2024 15:03:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2aca828e4248fce10f3d3612c8801ec98c9a90f3ac01dbcb1adecb3ac3193b`  
		Last Modified: Tue, 03 Dec 2024 02:30:20 GMT  
		Size: 17.0 MB (16966373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264d6c2361d9ef278241352b7ce7ca256b09cd106435cbc74c86fe974ba46c4`  
		Last Modified: Tue, 03 Dec 2024 02:30:20 GMT  
		Size: 52.9 MB (52870621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be197bb0b2190e79c72c4caea1b75e2a9c83e6f34899e6361efc0e4aff53d1b`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e726bec53c7d78d1aac86986290ae677eaf0efbb016458d43adc75b7a2e19b34`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744cb103e61e1916978581b179d02f5c3843886ba1ff08207c1aff21768ae39c`  
		Last Modified: Tue, 03 Dec 2024 04:31:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9342f6ea87a8b72434dc2920caea305923f6c2330de8605a2da6a8fd88c2860d`  
		Last Modified: Tue, 03 Dec 2024 04:31:50 GMT  
		Size: 13.6 MB (13591142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d76b35577398cd4521de5d834118c825f74c5a3c987b26fcbedb26d2c0add68`  
		Last Modified: Tue, 03 Dec 2024 04:31:50 GMT  
		Size: 223.4 KB (223414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:6368605d2ea4b46eec91d7068a9b9605d87e6346fa61c097c164ab983d632bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2f08c55ecd89be52b7f6b071f3733b0e138aaa5d349bcc7911ea2430a476eb`

```dockerfile
```

-	Layers:
	-	`sha256:32e13ea62793762ada8df20842e9c345af0eb073a634369ba95bf125de2b5d09`  
		Last Modified: Tue, 03 Dec 2024 04:31:50 GMT  
		Size: 3.2 MB (3185757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8793b9a75236d678041c4d76d4e7a34deb37a2999c0559d225141d6b6707ee61`  
		Last Modified: Tue, 03 Dec 2024 04:31:50 GMT  
		Size: 23.7 KB (23666 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:22a08609ab6bc1a4b2094a59eb4df6878e9a11fc05f6e6645056e6fd2248c026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111728431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e0a98218fbcd4074e52b5188ca522d8bd1f8bf9031b46736ef1bfac2def674`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 Nov 2024 15:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Nov 2024 15:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_MAJOR=10
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_VERSION=10.1.33
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_SHA512=f58c9d8029b1ec18d017019dcd68eb679b323f5c4f5d3f33f1a9bf3a4616db718ee3b44f8acc421ffaed67f4c2ca4647be0c7fa04a80274afd18a083711c5ece
# Mon, 11 Nov 2024 15:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 Nov 2024 15:03:18 GMT
ENTRYPOINT []
# Mon, 11 Nov 2024 15:03:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bc18bc29eb715bf1a5f404a45956786287384c81d8f10b7a98a9c7b8ff8c11`  
		Last Modified: Sat, 16 Nov 2024 03:07:33 GMT  
		Size: 17.0 MB (16980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40d280792cd30f40f405b2f432a3d45eb8b4e479a2da9b6239f3a3c497ea1af`  
		Last Modified: Sat, 16 Nov 2024 03:12:24 GMT  
		Size: 52.0 MB (52035430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0a27b4a62a63fea04f67099308fc96f1d2d707d918bfdca790a9c2e08bf479`  
		Last Modified: Sat, 16 Nov 2024 03:12:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb002bc09ae04aeded351f27cc24b0bb84d6035a2fe37ea7c9667cf917bf5781`  
		Last Modified: Sat, 16 Nov 2024 03:12:23 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df722e3954e728ec9589e2c516fdb908b3538c9ef7ad1d932129585d9a74df19`  
		Last Modified: Sat, 16 Nov 2024 06:10:08 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4696b50356fbcb24d383ecd85b28b1f13610e61e0644dfcc92c69b33ccad238`  
		Last Modified: Sat, 16 Nov 2024 06:10:51 GMT  
		Size: 13.6 MB (13593336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531eb7665a20af3d3df3c5bae8e56fd0c47befb356939d67176bf2e071df6a30`  
		Last Modified: Sat, 16 Nov 2024 06:10:50 GMT  
		Size: 223.6 KB (223620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:5199387e9e4d29d310454c38b291ff62dd033e22d67a201c78a9116033e04613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c34e8352aa53a69b5381bf8055c20d5a4d75e438689577ad003290a4ef7039`

```dockerfile
```

-	Layers:
	-	`sha256:0dad7b7ba2bc8be5c2908e0841066f36d1d88335386174c879b8eb68580652df`  
		Last Modified: Sat, 16 Nov 2024 06:10:50 GMT  
		Size: 3.2 MB (3186268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f18baa695c6f0366d6a59f3e97e60f1bf9ca65351b2a876f99a4fbea1f5876c`  
		Last Modified: Sat, 16 Nov 2024 06:10:50 GMT  
		Size: 23.9 KB (23886 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:d932c578af64d087cc89869f5157dcb15f6a0cf8051aa795980fc81c4eeefb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120015619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0946b2a1cb7ba347bce936639a370a4f26783eed8da30257316d02b0317b7418`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 Nov 2024 15:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Nov 2024 15:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_MAJOR=10
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_VERSION=10.1.33
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_SHA512=f58c9d8029b1ec18d017019dcd68eb679b323f5c4f5d3f33f1a9bf3a4616db718ee3b44f8acc421ffaed67f4c2ca4647be0c7fa04a80274afd18a083711c5ece
# Mon, 11 Nov 2024 15:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 Nov 2024 15:03:18 GMT
ENTRYPOINT []
# Mon, 11 Nov 2024 15:03:18 GMT
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
	-	`sha256:3e9d469975d531705369f0c991a9b8b8cb2b7bebb890ce19a4f016e84ca9b678`  
		Last Modified: Tue, 03 Dec 2024 04:52:26 GMT  
		Size: 52.9 MB (52917730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a37c17b4b9a8ca81350bdb26518415f6a12e4477afb517449540d6e361de6d`  
		Last Modified: Tue, 03 Dec 2024 04:52:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad37454f8693b742b67266e79edb6f7194b92df2cd00c6b484f18f63f27ebaf`  
		Last Modified: Tue, 03 Dec 2024 04:52:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac96353f95ae1d22aa41c8d5813dcaca772a501e2aaa58a4665dbc038f912ac`  
		Last Modified: Tue, 03 Dec 2024 16:38:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e77b1eb8cf536912c3738387e1f5d27f9e430d39e30189a5db37aed7f77b7d`  
		Last Modified: Tue, 03 Dec 2024 16:39:10 GMT  
		Size: 13.6 MB (13605253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5b94b9a068625052df72e903d5f0e0ba9d86d5c68043023626d670873a1cc1`  
		Last Modified: Tue, 03 Dec 2024 16:39:10 GMT  
		Size: 255.3 KB (255265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:4c767c09455cb93f32c2fbdd2291d8ea3decca5edb611cb78f5b3918d5709c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3213472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61db4e38a18a565f1028da6b9eb2eff440d4798f756cd1f1b8dcb9b2b8fbd5dc`

```dockerfile
```

-	Layers:
	-	`sha256:6611ab9c2c513acdd17521cc1e3bb69409b3de31adb47bb3c672d1c340bb3f7e`  
		Last Modified: Tue, 03 Dec 2024 16:39:10 GMT  
		Size: 3.2 MB (3189718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a8fda94da9274d72b641ac8040776d983a38ed5fac6940a9a7b15cddee6118`  
		Last Modified: Tue, 03 Dec 2024 16:39:09 GMT  
		Size: 23.8 KB (23754 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:e63b4dd1c15c40aadb2639ef0229b5e6ab82f0c755934cf89acc1a393cb083de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113479928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b44ad4fc7c6059c44606e759dd1881ea0ced14d2cc09bab23bef8a0428a2029`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 Nov 2024 15:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Nov 2024 15:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_MAJOR=10
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_VERSION=10.1.33
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_SHA512=f58c9d8029b1ec18d017019dcd68eb679b323f5c4f5d3f33f1a9bf3a4616db718ee3b44f8acc421ffaed67f4c2ca4647be0c7fa04a80274afd18a083711c5ece
# Mon, 11 Nov 2024 15:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 Nov 2024 15:03:18 GMT
ENTRYPOINT []
# Mon, 11 Nov 2024 15:03:18 GMT
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
	-	`sha256:8e892a79f39130d99271ac6de69a4da8bd98965dfef4a220a36c77c79554a715`  
		Last Modified: Tue, 03 Dec 2024 07:09:43 GMT  
		Size: 50.6 MB (50631759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f6057097232eb00fd538a2925a7f1751866b4522ca32549ced37665d6afa05`  
		Last Modified: Tue, 03 Dec 2024 07:09:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77391e25426093f861e8e6be8b2bc18c1b4155323bac2540015a330a4cfcda06`  
		Last Modified: Tue, 03 Dec 2024 07:09:35 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb96a0985308039252110fcef61351ffbe2d9791a0a401ce4a9422cd721e9608`  
		Last Modified: Tue, 03 Dec 2024 11:43:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3d42ce2c6a8c0744831d671678b21113643e869f579682d30bc6fffdff001`  
		Last Modified: Tue, 03 Dec 2024 11:50:50 GMT  
		Size: 13.8 MB (13776693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b03b8a013713901950d9bce25fd7f0e76f4bc26f51b0608fd4d9759d95e844`  
		Last Modified: Tue, 03 Dec 2024 11:50:48 GMT  
		Size: 226.1 KB (226090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:727056c0523a4d499de7ec611fff0972c85c93466212b11086cdb920951bafd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3201790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf438346ab3418d4d961f0dcb302b8b9d8bfeaed20750ded3c877af294b8ef21`

```dockerfile
```

-	Layers:
	-	`sha256:c4ba690d9a04802a1924e249c45451cf270a819ec1c872022be9eb5be6ec0a6d`  
		Last Modified: Tue, 03 Dec 2024 11:50:48 GMT  
		Size: 3.2 MB (3178036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da1718029bff88ac5526230fedc7f57f4c9d437784d472f386f0ec626e6f626`  
		Last Modified: Tue, 03 Dec 2024 11:50:48 GMT  
		Size: 23.8 KB (23754 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:c0c9391d739a0a18078674b4de62f7a9ff06c6bc485b7347f666ac38377d0d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110935267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff753e42504a13789c6c9f76203d6c22fa948d10373a695bdf02ef02f5dd8e01`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 Nov 2024 15:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Nov 2024 15:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 Nov 2024 15:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_MAJOR=10
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_VERSION=10.1.33
# Mon, 11 Nov 2024 15:03:18 GMT
ENV TOMCAT_SHA512=f58c9d8029b1ec18d017019dcd68eb679b323f5c4f5d3f33f1a9bf3a4616db718ee3b44f8acc421ffaed67f4c2ca4647be0c7fa04a80274afd18a083711c5ece
# Mon, 11 Nov 2024 15:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 Nov 2024 15:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 Nov 2024 15:03:18 GMT
ENTRYPOINT []
# Mon, 11 Nov 2024 15:03:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797233a5c5384584920c35814bc8b38ea24dccbedde0a0e68b3fb1a30877a17`  
		Last Modified: Tue, 03 Dec 2024 04:16:13 GMT  
		Size: 17.6 MB (17613148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5e866b62bafcf23f50c4f6929da5d0f17777a700540327589829f3748e334d`  
		Last Modified: Tue, 03 Dec 2024 07:32:48 GMT  
		Size: 49.5 MB (49467155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d167057d00a6b0d737c1eeaad9d9d16dc02ed3538095e6ab62e4bbb384495e`  
		Last Modified: Tue, 03 Dec 2024 07:32:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0036f9f5e1271778ace95a138fdd1716c6e2a6e09e07214b48e052c8442ad5`  
		Last Modified: Tue, 03 Dec 2024 07:32:47 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9777dd1718f6837d70c09e95c544f164bf46695ed5e34b7e06d068e3169705`  
		Last Modified: Tue, 03 Dec 2024 11:06:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7d9797d6056d5e9da6b7b6066cce81f905b1cee7840a7fe0a8ce7a2df47994`  
		Last Modified: Tue, 03 Dec 2024 11:08:08 GMT  
		Size: 13.6 MB (13599978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c34815f44b6366dc2cc34c42a5596fbe2082a64256677e343e10dfc15591e9`  
		Last Modified: Tue, 03 Dec 2024 11:08:05 GMT  
		Size: 231.5 KB (231515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:5d6c86ef5cff4932f4d43b01fa8682fc93c74a6d8b33b68c5ab2a08115140324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f35b82fd048d70e9bf31428dbf485a496e3655e8f656b0131839399cb30e2`

```dockerfile
```

-	Layers:
	-	`sha256:8ad3bec307b1c0916861de116b0b26799e35e54d2a3511ba0c3d16ba00b3c3b4`  
		Last Modified: Tue, 03 Dec 2024 11:08:04 GMT  
		Size: 3.2 MB (3187960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:137bf0ccbd545cd94d48f192a2d0baae776b260601221ce49a21848bcaa7acb2`  
		Last Modified: Tue, 03 Dec 2024 11:08:04 GMT  
		Size: 23.7 KB (23666 bytes)  
		MIME: application/vnd.in-toto+json
