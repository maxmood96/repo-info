## `maven:3-eclipse-temurin-23`

```console
$ docker pull maven@sha256:8da30b27ca9470e8fe969cd22dcbf5ef7501b32aad00684b97149f1dedcddbc7
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

### `maven:3-eclipse-temurin-23` - linux; amd64

```console
$ docker pull maven@sha256:dffa49f1574279755948590f8fc197a5a4326c4ba115211485c4f3a0993f3715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249719511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe3d3abd5ff354b194f2179509e19fa8a56def61095d09618ae62bb954b614`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Sep 2024 17:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='80d7bab9f9614bdf934c6bc441031bd1fead3aea85f16770123bd8a6bcdc52b6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a2820effaf631fdc5c7905a0a34c77ed8edebc3593039d9153d402429d53f3`  
		Last Modified: Tue, 03 Dec 2024 02:30:37 GMT  
		Size: 21.3 MB (21323240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b0c0e52bfe7eba92934b064c73089ef2e4d794769fcce7f88e61caec6c62fd`  
		Last Modified: Tue, 03 Dec 2024 02:30:39 GMT  
		Size: 165.3 MB (165299719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ce5ab8b33cce8425bbbfbf1455dd2343c59e03956b03db6cc01653770b0937`  
		Last Modified: Tue, 03 Dec 2024 02:30:37 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd901c231bd1da988b48a469afab5d8821c84eb1151f5f71dacd0f346f6019c`  
		Last Modified: Tue, 03 Dec 2024 04:32:17 GMT  
		Size: 24.2 MB (24170792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5ea697591eb2b164f217615660c740a4b4fa3f69ee87e290b8504d14991afa`  
		Last Modified: Tue, 03 Dec 2024 04:32:12 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492a339a2993b8e0299ef0069479bbd86ae2fb6b0430b8d7beb071d83642f14b`  
		Last Modified: Tue, 03 Dec 2024 04:32:12 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d241c204f4ec5b763870de577e9e5a8fb487d699a2b6d597152519bd19e1e06`  
		Last Modified: Tue, 03 Dec 2024 04:32:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23` - unknown; unknown

```console
$ docker pull maven@sha256:b70c944001664c0077b5567a3ebecaf4515550b0a01df485e51c913f2ae36bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4882827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae04387a692d69dfedc1df7f273ffa5c4338ec2b84865827cc8362863c51c44`

```dockerfile
```

-	Layers:
	-	`sha256:227afa54b3ebd7cd06a539b1834fd5ce2bdc390419ffc18f505c6f0979cacc46`  
		Last Modified: Tue, 03 Dec 2024 04:32:12 GMT  
		Size: 4.9 MB (4863221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2cfe276cb3fb4163596a41dc85296e2060c263dade1ed9d633c24f411b7149`  
		Last Modified: Tue, 03 Dec 2024 04:32:12 GMT  
		Size: 19.6 KB (19606 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2754c99563bdb65b5162b4e19cc2a0da1734bbb82ff9ec4e21265624e71cb597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248108632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec795ef2559c34826725be570b91c7ae2c7ab1cb69063bcb0b85e5e5b1f21254`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Sep 2024 17:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='80d7bab9f9614bdf934c6bc441031bd1fead3aea85f16770123bd8a6bcdc52b6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adfab973869e2ba64bf31c6fdfc25b68f8cc3c7837be9e03adaf9f950e8bd5d`  
		Last Modified: Sat, 16 Nov 2024 03:13:22 GMT  
		Size: 22.5 MB (22501597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c93636bf1b0bbe8c0f3d897798190b3035e547832b2c62a41cbb0b801da3edc`  
		Last Modified: Sat, 16 Nov 2024 03:13:25 GMT  
		Size: 163.3 MB (163279535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b1125124ef5bead8611908586624ec3983706461e160c03beba8680c6a4f51`  
		Last Modified: Sat, 16 Nov 2024 03:13:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ba165ad7f14e063295a84492c12e045ce8be5340061b34d198129096680cd2`  
		Last Modified: Sat, 16 Nov 2024 07:32:03 GMT  
		Size: 24.3 MB (24261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b47cbe32c6fe38b71fb983d3834d10d5ac84c61c2c13fcbe2eb9ef366717f0d`  
		Last Modified: Sat, 16 Nov 2024 07:32:03 GMT  
		Size: 9.2 MB (9170429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8752acf611b3338a7bec862f88a9675cb8229789be76113eb0962e83e9b08789`  
		Last Modified: Sat, 16 Nov 2024 07:32:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bdbea914de864fb199de308bfed8cda63921ed29c798a713d11783c2b048e0`  
		Last Modified: Sat, 16 Nov 2024 07:32:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23` - unknown; unknown

```console
$ docker pull maven@sha256:43cef3ee3805d7e0ca87cb7ea6d271a6ac5d0f9e8f4bbd4ba8e5812e34941b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5020046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e09942c9216ecad7bdc9ab824b544be689d74db1e861d680c3ed99b178bb981`

```dockerfile
```

-	Layers:
	-	`sha256:2ddb527debdc334beb5092bf35b7a790dd3e6c111f616417a7b336393be9c7bc`  
		Last Modified: Sat, 16 Nov 2024 07:32:03 GMT  
		Size: 5.0 MB (5000307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff80c329ac3f69cf4e3e5f90a39c9f9b8b5f4045c503421f811444d6bd2a729`  
		Last Modified: Sat, 16 Nov 2024 07:32:02 GMT  
		Size: 19.7 KB (19739 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23` - linux; ppc64le

```console
$ docker pull maven@sha256:4415718098d88c650bcbf30f5a61e9a29b36029fde48fc69ea39dcaf63786476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259579810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255bde293184662c7d9dbcaf5ce56e038b10048aadedc1fa8b479c8a404c618`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Sep 2024 17:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='80d7bab9f9614bdf934c6bc441031bd1fead3aea85f16770123bd8a6bcdc52b6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bedcf406293d80ace361b74277b7ea5aa7fc43cbda43d9df745b082826fa0`  
		Last Modified: Sat, 16 Nov 2024 03:07:05 GMT  
		Size: 22.1 MB (22080707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048b2070bab5fba0fd1b318279c9391d20616cd0cc78308d1cafe0f04ba1c569`  
		Last Modified: Sat, 16 Nov 2024 03:07:09 GMT  
		Size: 165.2 MB (165188411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4064f9ace7ba881c569b8c1b390801333f1304d5c1fd08caa29c30f97d1733fc`  
		Last Modified: Sat, 16 Nov 2024 03:07:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8baafa5f28ecb17a15407d3735f3402da2850a6fe8b4f55e19aea765405c24`  
		Last Modified: Sat, 16 Nov 2024 05:13:23 GMT  
		Size: 28.7 MB (28748084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef49c60a21ceae3bfda2434740fae7ecf016db71d5f8a456d0bacc5bd2745a9`  
		Last Modified: Sat, 16 Nov 2024 05:13:22 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1708cdd69588d18f59c4aa2a797edadea370a5811fd6c280a97eb0a3d463b288`  
		Last Modified: Sat, 16 Nov 2024 05:13:21 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf25b4003cd45d70eb96537aa3993a06e06c300ad6d667014417c290a049f70f`  
		Last Modified: Sat, 16 Nov 2024 05:13:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23` - unknown; unknown

```console
$ docker pull maven@sha256:4c58690ba37179bc809455708b8d16c26bb3c93e5796bbf7d88cf51204d6e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963b940977b912d4081ab9ddd26730c4b32bdf48d1e4ebc2710fbafa9c9f3513`

```dockerfile
```

-	Layers:
	-	`sha256:045dbfbc3cd584c59059fe9621f895cbfff8005b6a9b224efbff84f19f817304`  
		Last Modified: Sat, 16 Nov 2024 05:13:22 GMT  
		Size: 4.9 MB (4913402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e361c1e6755bea2e1f733e9138eb20348018fc4f20aa972e0447820df6a35d97`  
		Last Modified: Sat, 16 Nov 2024 05:13:21 GMT  
		Size: 19.7 KB (19656 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23` - linux; riscv64

```console
$ docker pull maven@sha256:be668710ec909b91d1b66e4852f4be45f97ecbfc3a518f229f472c405c74f64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252191860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285af73354db84fb510e6dbd39b19bc3f0fed1ec7d5f1d5e3eff0205f28a39ec`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:c7a07ab82f7f269608b3c78a3d2b0cd74630ea7220aee252fb2a61f78978b08f in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Sep 2024 17:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='80d7bab9f9614bdf934c6bc441031bd1fead3aea85f16770123bd8a6bcdc52b6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ee732b5fddd0a964c04b11ad9b9ec9f70f7df9e1e96825973cdf803cf1fba8e5`  
		Last Modified: Wed, 16 Oct 2024 12:48:30 GMT  
		Size: 31.0 MB (30980747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea41e4cf6a86e91ea2a9d321a5cbc05a3d3879fab7440ec47f14d2835194db86`  
		Last Modified: Sat, 16 Nov 2024 05:10:57 GMT  
		Size: 18.4 MB (18380352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6d16d0478564036d5af30eb952ee45f2c6f557682ed174d2171e5715c09855`  
		Last Modified: Sat, 16 Nov 2024 05:11:13 GMT  
		Size: 160.9 MB (160909467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df825c4b631e114f3f9eebeed3f9303315668d1e0567b531c38c1739adb302e`  
		Last Modified: Sat, 16 Nov 2024 05:10:51 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451eb5d35abd2621fdb5c98e759ddf499d2cecd07162cd134b98c73e4fbdde20`  
		Last Modified: Sat, 16 Nov 2024 10:24:13 GMT  
		Size: 32.7 MB (32747497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d998ade34461c8691e9b21cb2df748a58b9037a89644bced6da96f257c3e55`  
		Last Modified: Sat, 16 Nov 2024 10:24:10 GMT  
		Size: 9.2 MB (9170444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd7dfabbde50eb74eb3450dbe943142b1794f311fe338ff545bd55c910acddb`  
		Last Modified: Sat, 16 Nov 2024 10:24:09 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5902ca85655c341c18f708e274c8ede7ea6a337ad5216b16df332917f3e12963`  
		Last Modified: Sat, 16 Nov 2024 10:24:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23` - unknown; unknown

```console
$ docker pull maven@sha256:0a25643b5d630c13cdc9d50b9d3891efafa27ad145e8610fa9864c724d5c013a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7368c519e107aaff560cc15dc661d4f7c97d8ccf825bf594968013ef85d10a44`

```dockerfile
```

-	Layers:
	-	`sha256:b5bd07999a1f6716f833122ac138472e613ea2fff4406c3b59e9c2bfaa851d3e`  
		Last Modified: Sat, 16 Nov 2024 10:24:09 GMT  
		Size: 5.0 MB (4966858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dec2930042ad1a0da0799e6bc297f312096806fbed10ac68b6d57997577725`  
		Last Modified: Sat, 16 Nov 2024 10:24:09 GMT  
		Size: 19.7 KB (19655 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23` - linux; s390x

```console
$ docker pull maven@sha256:3a4e2cb770b1c43cf3aa5feb0d5f40dcf74dd694996f43da55e060bda1f5d770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239554850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dc7b1a09fcf27634e1f37dc60c5d2243402a54a60a577e3a03f070e1f6f8da`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:1c592b6de2557bde912d6291330e1604327193966f24da30f3ecf513f06fd372 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Sep 2024 17:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='80d7bab9f9614bdf934c6bc441031bd1fead3aea85f16770123bd8a6bcdc52b6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4d3763c838a1509ac75e9b37aa0fba11067b054033fda0d642f7e32e542b7994`  
		Last Modified: Wed, 16 Oct 2024 12:48:36 GMT  
		Size: 30.0 MB (30021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4eaefc8feda7065ec869cd29d09eac19993d9b8883e7de1e0b8f204af12d43`  
		Last Modified: Sat, 16 Nov 2024 03:03:26 GMT  
		Size: 20.4 MB (20442498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee62dbb36d02a448f04a66e96289cbf1e31377064039ca82806fac69d866684`  
		Last Modified: Sat, 16 Nov 2024 03:03:28 GMT  
		Size: 154.4 MB (154416890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdf5f01ea54c07c7dc5e834785d7c630d38b940d678831b3e7f5df68f5c4810`  
		Last Modified: Sat, 16 Nov 2024 03:03:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f355d95b15fcbba1a1a7221988a7a7df80505afa6c80c783cd6f5a6c8cfba91`  
		Last Modified: Sat, 16 Nov 2024 05:03:30 GMT  
		Size: 25.5 MB (25500396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f183ddb7ce30590ccc4e9134d3c6c8483bf20bfab80c76a6761ebce6d4905b3`  
		Last Modified: Sat, 16 Nov 2024 05:03:30 GMT  
		Size: 9.2 MB (9170428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef2046623c9e276499f50b440207fbe2391725998bbb132bcfe2a7a27dfce71`  
		Last Modified: Sat, 16 Nov 2024 05:03:30 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c89d8779e2c5694a2c7f7785261bd79795fa66b928defad7a0dc0030540265`  
		Last Modified: Sat, 16 Nov 2024 05:03:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23` - unknown; unknown

```console
$ docker pull maven@sha256:c249e456b7e705ba7cb86d44defd44159c1a447db7cf4e48a3b3b1688b50eb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4827908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9928ac6215a00fd54b0dc1dbdbd029e6943211c556d91a86b2a6be3da8c1cfb0`

```dockerfile
```

-	Layers:
	-	`sha256:3f565524dfcd58b4a7a74c46e7dba510a9d12d5e30265ca59b42db3bad6aad4d`  
		Last Modified: Sat, 16 Nov 2024 05:03:30 GMT  
		Size: 4.8 MB (4808304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16aaf91bbf6187ae1a10089cc9c1b34388d755c5c906b1bd96af14a7c6090480`  
		Last Modified: Sat, 16 Nov 2024 05:03:30 GMT  
		Size: 19.6 KB (19604 bytes)  
		MIME: application/vnd.in-toto+json
