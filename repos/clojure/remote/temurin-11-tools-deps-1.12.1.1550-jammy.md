## `clojure:temurin-11-tools-deps-1.12.1.1550-jammy`

```console
$ docker pull clojure@sha256:2d98ad405c9262406b8c9f8140074819601f9f17d2fbd5725b379569cf01529c
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:881b45e7f7593cfee82bf878d123deeff940c0023818c25309dddf97e4c37742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242084936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b1c219757c752406c6ba72916fbc598ef3976d9e670382ce42d7a93da1e26f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9aa610249b82d4f2c18091b8f803c25132d08e9bcc72165577662bf7f6142b`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 16.1 MB (16146340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7583e02af379ef87d3195e081244c40bb4a0155dd5b8ff4954bb736937a81e`  
		Last Modified: Wed, 02 Jul 2025 04:11:32 GMT  
		Size: 145.6 MB (145645058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30914a62c803f975c25fea5961a34ce06c9fa64d2b50ad6d5eb3cf0655f376a2`  
		Last Modified: Wed, 02 Jul 2025 03:10:35 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cee5bd7bdee887cd57628a32e0eacb4f6940713657f92370be865c1d342dd98`  
		Last Modified: Wed, 02 Jul 2025 03:10:35 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bab5a5c6d4f9ed315173870eb865ea5d1fb711047aca0ae7312b72f4666f67`  
		Last Modified: Wed, 02 Jul 2025 04:16:28 GMT  
		Size: 50.8 MB (50754767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b677a072a13ca764c389a893b6c47980d3518f1d651a487217661d302d4e8a20`  
		Last Modified: Wed, 02 Jul 2025 04:16:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:33b0048dbe060ccb0eff9bf218e86dcfce171539607884e9891fb354284db6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b91f261d2eb7175e2fd7d87b685b3b685b715dfaee2e00c04f6c6b7c6e0137`

```dockerfile
```

-	Layers:
	-	`sha256:403e2414921c419f272d721a6421451b0139feb6b9038905c227403822e71ca5`  
		Last Modified: Wed, 02 Jul 2025 06:35:26 GMT  
		Size: 6.3 MB (6320791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752932b0a794e9db635edc64bc2da367c628606f22feca8c05b8491ca421dc5e`  
		Last Modified: Wed, 02 Jul 2025 06:35:27 GMT  
		Size: 13.6 KB (13550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f76ee633a8324b48cf3dfd2eb0e591f28788bc0e3e53affc32500f19e6a7635c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236550546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac7217b5fb2b7ac734427e3cd97627dd45031d2eec61ce721b554ead7cbfe75`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf37c5f5e10b3110a133ed367190f7cdd79aad284aef8d5335a2aee0c5fcfc`  
		Last Modified: Wed, 02 Jul 2025 05:06:30 GMT  
		Size: 16.1 MB (16059884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b536c3c54abf9994304faac2a0f04de0b34b009d6ec406dcd35bf9cec367b2c`  
		Last Modified: Wed, 02 Jul 2025 08:41:13 GMT  
		Size: 142.4 MB (142431526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe266740e3ee7ac675d064b94c2f5c1bcdc2da7142765cb1e9d8f3a84dc01c5`  
		Last Modified: Wed, 02 Jul 2025 05:08:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d54a6f92555bdab32328d6ae79e31aec23a72e929cc7f1fee146856207c678`  
		Last Modified: Wed, 02 Jul 2025 05:08:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c914ddea54b34b460ba48b855073d158b485a5bdf4224be4f2277ef9ddbbc974`  
		Last Modified: Wed, 02 Jul 2025 12:26:24 GMT  
		Size: 50.7 MB (50696775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db69402545ab9c42a66409513257e690aa86bf9e60dcb350dce7b532622771`  
		Last Modified: Wed, 02 Jul 2025 12:26:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:595635155974fd5d6b8336bd3b69ee29a80424f28da1d23fd22c5ac27bb7ed4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969462ae33e762d1df3100b953a83bde4359672d3ffea2945cb5f92a0c5cbfdd`

```dockerfile
```

-	Layers:
	-	`sha256:f2e9514201ecd51901e368fff05620f42554f2662f30f99fbf6b1501b0f96e45`  
		Last Modified: Wed, 02 Jul 2025 15:35:27 GMT  
		Size: 6.3 MB (6327175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd11b978aa1324b25eece4f23930c035d00e25df1feca4566a9650eb38ce025`  
		Last Modified: Wed, 02 Jul 2025 15:35:28 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:ccde63bd8e5f6f4cad53c146ffe8d9a7aec33ee10cad25ae729c9f71530acb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239583118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cc773b21675067df11ac377a3c83d9bbc6b83f2d8d0c25462619b374128650`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595b1fb797135dd0e29ee3176dc6a26da5fdd960326b5800ab21ad59036a273`  
		Last Modified: Wed, 02 Jul 2025 03:15:14 GMT  
		Size: 17.6 MB (17618409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0f7c9e10f540279ab28d93148959e64a61ffcc8b849b3df6df144c8253db0`  
		Last Modified: Wed, 02 Jul 2025 08:27:21 GMT  
		Size: 132.8 MB (132827983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374f9411181327cf83b002bf3ab666aa91751f0fc0facbc8d0bec892d67d64d5`  
		Last Modified: Wed, 02 Jul 2025 03:18:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1f8c833d86f2366b5725232120ce3a32f784f40cbe457d0488b9ddd185e0ee`  
		Last Modified: Wed, 02 Jul 2025 03:18:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f727fcab3ecccf500eb040b1661be489dcda5032857d01ac0cc18b9cbf3a41`  
		Last Modified: Wed, 02 Jul 2025 10:21:01 GMT  
		Size: 54.7 MB (54691015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c416e04f7817611332fec2eb149d7aa736966b1c080e1cdfb09d72385396779a`  
		Last Modified: Wed, 02 Jul 2025 10:20:58 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:91fe3de0684ecb93317c53472de74665ce79a1245610aa9b6d3fe6ae19b4f0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6338987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82636a568be2be44a3151a229dad12598bad578c30fceaa8e2fa49de4d66f3fd`

```dockerfile
```

-	Layers:
	-	`sha256:bdda787030218a342b10df963036efbe99e9ef855505a30ac39a69b35982386e`  
		Last Modified: Wed, 02 Jul 2025 12:35:19 GMT  
		Size: 6.3 MB (6325399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79303341beb2665f1a3f009086312360edab25c42150f5ae7b11cfac7871299e`  
		Last Modified: Wed, 02 Jul 2025 12:35:19 GMT  
		Size: 13.6 KB (13588 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-jammy` - linux; s390x

```console
$ docker pull clojure@sha256:62d0705686cf24c59b9c23d4f0b362191785e05aad1997fb84be07d72ff1c2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220508911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5515124b2919ef14ef817d6696c367c0abcf76a27034ef740c6645fc8409007f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7407b9fdf832fa4e3a41a2319aa3e0d04f31104a25092c677a83bf06472d7`  
		Last Modified: Wed, 02 Jul 2025 04:15:41 GMT  
		Size: 16.1 MB (16144420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcd8d0c9039f11caebe887bfc579b2c90492e09296b22ed26c42b28568cdb76`  
		Last Modified: Wed, 02 Jul 2025 04:15:49 GMT  
		Size: 125.6 MB (125596938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d6557a4bc8cc087c4d7694c437c775c5890ed16cb96e61cf558aeed68b83ed`  
		Last Modified: Wed, 02 Jul 2025 04:15:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0ee2894b179efb98ba05db5cd367934043b2d1490a08db34035a594ab1208d`  
		Last Modified: Wed, 02 Jul 2025 04:15:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b0621361592c0f40c7a8f1d266ed34eb897f5d862620bfdbf82b06708fd2cf`  
		Last Modified: Wed, 02 Jul 2025 06:31:15 GMT  
		Size: 50.8 MB (50762292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22be72be42057db835501d44064144d621facc2e1b2712220a3fe974cfdb439`  
		Last Modified: Wed, 02 Jul 2025 06:31:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:930c64eafd48be9d2f8eef8d5360812dc6d81ca00e8029fddb92da23715e4ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1214161ae67902b144849333084a33ca990ae8102590d436710c2b188fa518b`

```dockerfile
```

-	Layers:
	-	`sha256:7ad8497f84dcbd8b7479adae2902d3b6caee247eda1c6d3771545c9e1d385830`  
		Last Modified: Wed, 02 Jul 2025 09:35:22 GMT  
		Size: 6.3 MB (6316718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b8568e03cad17b14780a0be7742e837ec3a80b0d7d9b53d17e57e6cb58abe4`  
		Last Modified: Wed, 02 Jul 2025 09:35:23 GMT  
		Size: 13.6 KB (13550 bytes)  
		MIME: application/vnd.in-toto+json
