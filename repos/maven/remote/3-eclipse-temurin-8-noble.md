## `maven:3-eclipse-temurin-8-noble`

```console
$ docker pull maven@sha256:8135a3d9d2247f75973a23c984baf0b0b758eed1a85491d78fd4340a9cb35f76
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

### `maven:3-eclipse-temurin-8-noble` - linux; amd64

```console
$ docker pull maven@sha256:a4671e541e6f394e822804a7acbeecba58ebd7c9b2abbfad3fd71f9df0d1b71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133215860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ce943ec2cf00f0df3b614ad567762745f952ff370a6e372885f4f63d599634`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae45f3df58196dc0514340a9385c9ad9e00220ccd2d5a411befb5015109f0c76`  
		Last Modified: Tue, 12 Aug 2025 17:24:45 GMT  
		Size: 17.0 MB (16971743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071b6148706fbdc721b07f3620c373180ed7aa1fa197c962f08bd45cfe1a1111`  
		Last Modified: Tue, 12 Aug 2025 17:24:56 GMT  
		Size: 54.7 MB (54739649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6b5e22bfa993cda9c93e29e9d7883430f828493590dc13572a3d0c758f661c`  
		Last Modified: Tue, 12 Aug 2025 17:24:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e086d6b9f5e5d3a0e6f9b4d8a38827467a25169b41b89bb7e9028619113ac5`  
		Last Modified: Tue, 12 Aug 2025 17:24:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26b97ec7d7eca099393d1e89d69954ebb2138fe405ecdfefe0c405b3007a87`  
		Last Modified: Tue, 12 Aug 2025 18:10:12 GMT  
		Size: 22.5 MB (22535196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f5a270dd29ba7f1ce40954746b57106b6bc194937eb04a8ebf57f469bce932`  
		Last Modified: Tue, 12 Aug 2025 18:10:02 GMT  
		Size: 9.2 MB (9242587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d92d802b7729e4490b924b10760521260ade510308c24f07e684d54a949d72`  
		Last Modified: Tue, 12 Aug 2025 18:09:59 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5561513cbfe0fbb164bdf09aacc640ff5ca6c54d7530eff6b575796c5469a38d`  
		Last Modified: Tue, 12 Aug 2025 18:10:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-noble` - unknown; unknown

```console
$ docker pull maven@sha256:61ab67ef2a8dabad68e68fa28fb41d12bb06e04a5864cc174de762e109cde1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5034696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585dc63f37b1346180086f6c32de4c46569043a50877ebc7a02f54ccdc47866d`

```dockerfile
```

-	Layers:
	-	`sha256:708de7d5ba662363680d5bf8066e036aba86427e02ce58e35c3a5d083ff0175d`  
		Last Modified: Tue, 12 Aug 2025 20:30:07 GMT  
		Size: 5.0 MB (5013988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4de97ae004ea9064f407f4d867e4749847e37ece09a68ab681eeb558c35245`  
		Last Modified: Tue, 12 Aug 2025 20:30:08 GMT  
		Size: 20.7 KB (20708 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8-noble` - linux; arm variant v7

```console
$ docker pull maven@sha256:2c59b0da0917e870ab501914e383d1587dbed0dc9cbaa672d25741ddc4bac6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129796521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636c11f90932dbadb42d6c847209206d81632d29122983421ebd9ba04b6b2a98`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 06:54:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:54:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:54:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:54:14 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:54:17 GMT
ADD file:3d0bcbe19ab589b9febc888a3f1e7d731d2ffc32ab216f5a65461d73e6542ece in / 
# Wed, 30 Jul 2025 06:54:18 GMT
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5775aaee0b6caf578e138eda76ce3385180e0796b81e02b9edf4909084017d62`  
		Last Modified: Wed, 30 Jul 2025 10:35:13 GMT  
		Size: 26.9 MB (26851072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45125b04509c0c0ff9d377acdb196a3379f30661dfa80092b16c7dc194b409a`  
		Last Modified: Tue, 12 Aug 2025 17:26:52 GMT  
		Size: 16.3 MB (16305691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077e715c9761e592132bc78ae0a4d8900a0f41b7d01de948a9fe3bcbf5ca2ad`  
		Last Modified: Tue, 12 Aug 2025 17:26:59 GMT  
		Size: 50.1 MB (50123524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9324e5e1f8f541b1eabde0592e9bf4a974732de992860a7e8ee0933e562328`  
		Last Modified: Tue, 12 Aug 2025 17:26:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393bc56c1c379a96abbc888bf0b3ef3446bf121cf490e31bee480061feea9cad`  
		Last Modified: Tue, 12 Aug 2025 17:26:46 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be35d00689b676a94e16580cf69a72dee98967367f637b84e9a29b74ec9d75d`  
		Last Modified: Tue, 12 Aug 2025 19:23:36 GMT  
		Size: 27.3 MB (27270198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7ad8230bf3090d74f754dede2fc54d86382509227a01b85e2578b2283be04e`  
		Last Modified: Tue, 12 Aug 2025 19:23:36 GMT  
		Size: 9.2 MB (9242565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0084e8e017adeec8fcfe9638d4fde289f0472f66cc6846883075f8c0ff4220d4`  
		Last Modified: Tue, 12 Aug 2025 19:23:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319b2be493beca7cefd12f1b80563906fc612dac84adfe4c9da7b5314478e771`  
		Last Modified: Tue, 12 Aug 2025 19:23:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-noble` - unknown; unknown

```console
$ docker pull maven@sha256:5358da025ec4f39bc3097484f3f933f0193d5e65661a3878fc8198929819d2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac41b8a8da446b25bc57ef1b89227c13fdd67faf6f4037b34413e51f062f989`

```dockerfile
```

-	Layers:
	-	`sha256:597af1d91d8bf427a98e021b0eeb11a11e1a1c429d0a22cae0a623c693f49610`  
		Last Modified: Tue, 12 Aug 2025 20:30:14 GMT  
		Size: 5.0 MB (5016734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a64234013d7de8856fe53a90fce8550e900be11cc9c2c990331017d87ae698f`  
		Last Modified: Tue, 12 Aug 2025 20:30:15 GMT  
		Size: 20.8 KB (20835 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f74f2818dc9722286fb60ab6ee70b78825db5caf96de7f5576e68814411046ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131537623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a15c5eb96d194f3edbdb86778d04e8a16c7d3daef779b89b8985e957cedd85b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3eefddfbcab06ca4f10ce56a232d4ec2d822b72ac91b8958abc9acd3c4223c`  
		Last Modified: Tue, 12 Aug 2025 18:31:54 GMT  
		Size: 17.0 MB (16988833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bc97fb1cc689758ba003a9153e88dbce8328d0db914d0ed1fe69c78280b7d0`  
		Last Modified: Tue, 12 Aug 2025 18:32:00 GMT  
		Size: 53.8 MB (53839386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d784d682c780e3571037fdeefb5c9a39f7526f93b08fca46118f4b8808f987`  
		Last Modified: Tue, 12 Aug 2025 18:31:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c002051e274106277ee7aafebf09d8da27cb403ceb5fd31d9a290b189205603e`  
		Last Modified: Tue, 12 Aug 2025 18:31:54 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249f3ed2ef17072f46c9df12bb637c1c8a4e58fd29bd73af47dc7a2cbe102bd6`  
		Last Modified: Wed, 13 Aug 2025 19:58:44 GMT  
		Size: 22.6 MB (22602969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e619c3c1f5140c1d9504d1b1fdaf8ccf08f1b6f7dff182aeca2d0e8724948a`  
		Last Modified: Wed, 13 Aug 2025 19:58:43 GMT  
		Size: 9.2 MB (9242586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b137e5f7a89554223bce67a2e24f3669ec20711a827616d1c29dd8612eb939db`  
		Last Modified: Wed, 13 Aug 2025 19:58:43 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a5d5f0a2dec94cff4b85f1dfa4d7d9d79a943b39cb02c1b8ec40bd0a816a15`  
		Last Modified: Wed, 13 Aug 2025 19:58:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-noble` - unknown; unknown

```console
$ docker pull maven@sha256:23f389dbc8c61c301df0b3fa76113a51544e1e0560e5dec3748c738fd4985196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5042109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ad72e7599d7f4bb885a2ca6942158a85c60d9bc341f24a624058ea1434923d`

```dockerfile
```

-	Layers:
	-	`sha256:37609d4fcde3e7e810a91c2c4964f8e1ade8adc6bb1e4c133372ceab9252b317`  
		Last Modified: Wed, 13 Aug 2025 20:29:18 GMT  
		Size: 5.0 MB (5021233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411154fbc8cf0ce03149dd8351eb51c7072fcfbf2f4bbffc1e5e1c83518ab8d1`  
		Last Modified: Wed, 13 Aug 2025 20:29:20 GMT  
		Size: 20.9 KB (20876 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:3a9e50f0703aa3fa6c658d6f17399135e987a75cea53caa039406937fdd20232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141141610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ef856fc550ca13a52f64b92f8e51714e1c626a42625a0e65db8541d53ca22c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096eab1deeb8fde16ff57db7eaa184cd4e8ab0d206018acdb9ab5ac1843566c9`  
		Last Modified: Tue, 12 Aug 2025 17:31:12 GMT  
		Size: 18.8 MB (18814780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9b1087fddcdc35739a584a107723a0f4b26861095336fc9ff97e21cd030124`  
		Last Modified: Tue, 12 Aug 2025 17:31:28 GMT  
		Size: 52.2 MB (52167329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5eb8055282fb833cc942f85611da1cfacf2a50043d0bb47c3c9957108809e`  
		Last Modified: Tue, 12 Aug 2025 17:31:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4317d0cad8d9dd17e412e96f167682b1af18de5936b2fe7d3bf0736c3745d7c9`  
		Last Modified: Tue, 12 Aug 2025 17:30:59 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dee868011134b6106856dd276cae40511ee1a0fc796a07725fb581c4c29c706`  
		Last Modified: Thu, 14 Aug 2025 02:06:50 GMT  
		Size: 26.6 MB (26583787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a684181440b78545f07f960b13a3d5a2c731b98b9db5bbec0986a119fae2285`  
		Last Modified: Thu, 14 Aug 2025 02:06:50 GMT  
		Size: 9.2 MB (9242590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b742f3654569e45fde6cf40396f9e8242327f8b1ea1e6751f83e2d57f8dab72b`  
		Last Modified: Thu, 14 Aug 2025 02:06:50 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece2ee49610fd681d6d1cf76bfbec1155f81acc8480d4ee818dd8a18e6db0e8e`  
		Last Modified: Thu, 14 Aug 2025 02:06:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-noble` - unknown; unknown

```console
$ docker pull maven@sha256:eca0d15115ef09f82e21333f18b47a34c0e7c445d6400ac7b86ce53ff6404e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5040307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747153d19625727b760681ab5f3fdd89e173d2bde4dd63f6566fb311dfa59131`

```dockerfile
```

-	Layers:
	-	`sha256:b0aa02affd870859a38d814a9b63fc152d003897421cc50eb7814262be6bcd58`  
		Last Modified: Thu, 14 Aug 2025 02:28:48 GMT  
		Size: 5.0 MB (5019531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f3f2c02fbd0dfa72c66a80bc69928356a6290a499eeadbea9ebab0784310820`  
		Last Modified: Thu, 14 Aug 2025 02:28:49 GMT  
		Size: 20.8 KB (20776 bytes)  
		MIME: application/vnd.in-toto+json
