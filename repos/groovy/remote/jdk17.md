## `groovy:jdk17`

```console
$ docker pull groovy@sha256:8d391bd55f14176aa7a1e25930868ad96b4c2eacd3e92bbcdbc1d9a0d182a36a
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

### `groovy:jdk17` - linux; amd64

```console
$ docker pull groovy@sha256:950dea3d3f4a391e1b24219c3dce502b8632ad8cf1fead6dc06ac1684c8f9e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233388384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453f4e76d197e1dd3ea08ac1b4aabdea87e857ff027b31841fcd2d74a879c0d1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:37 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:14:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:14:43 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:13:22 GMT
CMD ["groovysh"]
# Tue, 02 Jun 2026 09:13:22 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 02 Jun 2026 09:13:22 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 02 Jun 2026 09:13:22 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 02 Jun 2026 09:13:22 GMT
WORKDIR /home/groovy
# Tue, 02 Jun 2026 09:13:26 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:13:26 GMT
ENV GROOVY_VERSION=5.0.6
# Tue, 02 Jun 2026 09:26:59 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 02 Jun 2026 09:26:59 GMT
USER 1000:1000
# Tue, 02 Jun 2026 09:26:59 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e81aa30db3c59f2e5328e275b501f7a3305c8cc88c00bf8d4ed72ebd8f8b4e`  
		Last Modified: Tue, 02 Jun 2026 08:14:59 GMT  
		Size: 23.0 MB (22967073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347855006e7d0a66be2de2afbcad9be5ad2b4e480ec03d05473a53091090f1e6`  
		Last Modified: Tue, 02 Jun 2026 08:15:01 GMT  
		Size: 145.9 MB (145913860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6433dc7124a3aa5e6168e8a3ea16d13ebc0ed887843b275c4dd772f0e1da955e`  
		Last Modified: Tue, 02 Jun 2026 08:14:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53a5c207c4191f4aa279920278a481310c882de2d85a4f23c907a06a4153f49`  
		Last Modified: Tue, 02 Jun 2026 08:14:36 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a58b68d11babb9c45c0801824cbe799ac677153c65af0c197be5540f63994b9`  
		Last Modified: Tue, 02 Jun 2026 09:27:09 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652758159d6865db1b2f6422aa0818c461ca93b3714a240c1833da046369dd52`  
		Last Modified: Tue, 02 Jun 2026 09:27:09 GMT  
		Size: 242.2 KB (242233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34cf634ffc2812841914da94a02b0be07e08967e80b9d165e73f91b454d036d`  
		Last Modified: Tue, 02 Jun 2026 09:27:10 GMT  
		Size: 34.5 MB (34528499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6af0576f530a7155aba9e9fdc522b90deed50ae7266eb79fa8a04282af524b`  
		Last Modified: Tue, 02 Jun 2026 09:27:09 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:efa54593b1ab9fa9158cfa80c7a31e1353dd0900d1688a769b1a602771b2786c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466992b1aa94deadec0cc01ed95b74aee9c40ad8286ea9f7583e4e2511a71eda`

```dockerfile
```

-	Layers:
	-	`sha256:145e9911f63f9f3eb24bc8f75860daa9c54c32cf71be1e3adf1c82e956178e84`  
		Last Modified: Tue, 02 Jun 2026 09:27:09 GMT  
		Size: 3.6 MB (3634714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08baa38bbdd88407bdc49250850cc242395323d426bb5af979df057542738098`  
		Last Modified: Tue, 02 Jun 2026 09:27:09 GMT  
		Size: 26.4 KB (26429 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk17` - linux; arm variant v7

```console
$ docker pull groovy@sha256:48d43c3e8741b2a8eb455b72996ac63f18d98ff4657705fea8afdac065701c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226199755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85347a1ab64f404803198eafb46d938e8c64c83279f0700f59619a123965acb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 20 May 2026 01:36:59 GMT
ARG RELEASE
# Wed, 20 May 2026 01:36:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:36:59 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:02 GMT
ADD file:6d117ff682b1d31146902ad551197b012e75561d62d92d029219fcbf5c493c35 in / 
# Wed, 20 May 2026 01:37:02 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:13:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:13:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:13:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:13:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:13:24 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:13:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:13:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:13:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:13:40 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:14:42 GMT
CMD ["groovysh"]
# Tue, 02 Jun 2026 09:14:42 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 02 Jun 2026 09:14:42 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 02 Jun 2026 09:14:42 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 02 Jun 2026 09:14:42 GMT
WORKDIR /home/groovy
# Tue, 02 Jun 2026 09:14:48 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:48 GMT
ENV GROOVY_VERSION=5.0.6
# Tue, 02 Jun 2026 09:20:51 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 02 Jun 2026 09:20:51 GMT
USER 1000:1000
# Tue, 02 Jun 2026 09:20:52 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:a2dede8d0e9ca179460cb274dab10c5c4b741cf1544b130df872809a4467e3e4`  
		Last Modified: Wed, 20 May 2026 02:15:37 GMT  
		Size: 26.9 MB (26859709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b409c5973c180288bd87216d0331b56c1abe47a076556cee28d237197fcd74`  
		Last Modified: Tue, 02 Jun 2026 08:13:56 GMT  
		Size: 21.4 MB (21391726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7b0d118fc4ed6b0d7459319eae073346681cd56e1c19e55aa8ea10d24438a`  
		Last Modified: Tue, 02 Jun 2026 08:13:59 GMT  
		Size: 143.2 MB (143187199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6561a0a2ee5de0d6336d013d1e14dcbbd20fea0e882d929e459be843846025fa`  
		Last Modified: Tue, 02 Jun 2026 08:13:55 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50c260d643eda9e3021ed3eda473afdeb5a1aa5f0fc8debc6a115780bba8294`  
		Last Modified: Tue, 02 Jun 2026 08:13:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b204985b00f4758f79b0f3e34f28b7b8989f99943fddcf8d746a380c807aaf5`  
		Last Modified: Tue, 02 Jun 2026 09:21:01 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1b5a8f6068de286d94b558df80cc4483cffd6893f0f14ac36ab82f66a77034`  
		Last Modified: Tue, 02 Jun 2026 09:21:01 GMT  
		Size: 228.7 KB (228715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf99c0866d737d31ac2bcf6b51f3280ab527ebb654a1b526c4c3c436ee12738`  
		Last Modified: Tue, 02 Jun 2026 09:21:02 GMT  
		Size: 34.5 MB (34528485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4324ab321e552ede1641a9dc9a0ef3f66213a5b12416bf93e98da7a2b49b8721`  
		Last Modified: Tue, 02 Jun 2026 09:21:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:0a8afaeaf9d6d9d3515fbf87b92b30b732e169d64fb542675fca5ad794b44779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3600809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5f3ecd588cff20f0b4f31e5f71a23b65f31145ba06344b0d476e5f37bb94ea`

```dockerfile
```

-	Layers:
	-	`sha256:920acc6d5fc7173673819c3698ed965646b50a2fd3fa20bdd2319ec594637f48`  
		Last Modified: Tue, 02 Jun 2026 09:21:01 GMT  
		Size: 3.6 MB (3574229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773a9f9fddec4a7edb02cce567e23adef851406b475eb95f284eebe752a67d7e`  
		Last Modified: Tue, 02 Jun 2026 09:21:01 GMT  
		Size: 26.6 KB (26580 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk17` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:63a74169c52cf70db61cdbe80a9c02ec291d6220b277482210276bbb451f2e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232565237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb114020f703b46770d2d9e3c35a85c66cbbd26893eff4f0573433041ed3748`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:45 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:15:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:15:52 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:14:07 GMT
CMD ["groovysh"]
# Tue, 02 Jun 2026 09:14:07 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 02 Jun 2026 09:14:07 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 02 Jun 2026 09:14:07 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 02 Jun 2026 09:14:07 GMT
WORKDIR /home/groovy
# Tue, 02 Jun 2026 09:14:12 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:12 GMT
ENV GROOVY_VERSION=5.0.6
# Tue, 02 Jun 2026 09:23:05 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 02 Jun 2026 09:23:05 GMT
USER 1000:1000
# Tue, 02 Jun 2026 09:23:06 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b561305034436042730e6b308d923ef359c4058869b7469bef9d89022c93e0`  
		Last Modified: Tue, 02 Jun 2026 08:16:10 GMT  
		Size: 24.2 MB (24172714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a5efc7e4ab768c8fac1479a43343bfb33d32a70fb406eef444830616ed9587`  
		Last Modified: Tue, 02 Jun 2026 08:16:13 GMT  
		Size: 144.7 MB (144741987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6405573be247c0ce1018a802381d08865983340dac502eb1267238da0206387`  
		Last Modified: Tue, 02 Jun 2026 08:16:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ad068d0e57373293c4b64b88af658e6140240ec6c7bdc40cce1744141a642e`  
		Last Modified: Tue, 02 Jun 2026 08:16:09 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f34844b7dc4c202aa819e1812592f2f5d89c28842ca6fa07c9b903bdf0e0aa3`  
		Last Modified: Tue, 02 Jun 2026 09:23:16 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ba36896d8272b7115a87d3facba7e11cdff574564a0d898e156062fd35a2f`  
		Last Modified: Tue, 02 Jun 2026 09:23:16 GMT  
		Size: 241.7 KB (241725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e817ccb9aef5e367ce57278599a4052c11215195a65e9c2dd80703b0735588`  
		Last Modified: Tue, 02 Jun 2026 09:23:17 GMT  
		Size: 34.5 MB (34528484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6828d55206031d2fd0aa2a7bd7309e338720b092376baf42ae898731216ae8b`  
		Last Modified: Tue, 02 Jun 2026 09:23:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:2553302dda83791a651bba1b7e4d4bcf72da8c745569c1f7a64794f7871405ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f7b116d7b0b5aa7586cfcf954727599a1b88c0bb28e5ea3ad0815bfbb0df85`

```dockerfile
```

-	Layers:
	-	`sha256:36c8aa0ec3d71f620ac5771c8d4f35af012e8b3c1bd27c861cfd3997badef730`  
		Last Modified: Tue, 02 Jun 2026 09:23:16 GMT  
		Size: 3.8 MB (3766283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71033c18fa9c2341b9eabe0b7a87f770cbc94a9052cd401940961de51574380a`  
		Last Modified: Tue, 02 Jun 2026 09:23:16 GMT  
		Size: 26.6 KB (26625 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk17` - linux; ppc64le

```console
$ docker pull groovy@sha256:b46d8d1e68b1d0b563551766276b7593942ec9cdd8aff1c71bcf0ff1b8ff561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238988691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47d260a5736238a584e955eaedb05fbfa0b914b8fdab5aae3fa5379e5937f3b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:12:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:12:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:12:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:12:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:12:24 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:12:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:12:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:12:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:12:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:12:38 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:19:05 GMT
CMD ["groovysh"]
# Tue, 02 Jun 2026 09:19:05 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 02 Jun 2026 09:19:05 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 02 Jun 2026 09:19:05 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 02 Jun 2026 09:19:05 GMT
WORKDIR /home/groovy
# Tue, 02 Jun 2026 09:19:12 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:19:12 GMT
ENV GROOVY_VERSION=5.0.6
# Tue, 02 Jun 2026 09:34:23 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 02 Jun 2026 09:34:23 GMT
USER 1000:1000
# Tue, 02 Jun 2026 09:34:25 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c1670fe2f067637ded122a0663c456ca6091e763c878866bd1996f0f3852f7`  
		Last Modified: Tue, 02 Jun 2026 08:13:11 GMT  
		Size: 24.1 MB (24096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad1820de185d9eeb8c58b43851b3cb20a00b420e7d9e52d6e747fb06ca28321`  
		Last Modified: Tue, 02 Jun 2026 08:13:15 GMT  
		Size: 145.8 MB (145774128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7e0b9b96dcd64d36e337bc7d6fbd959a1f3080617f8a5d83ff022f9e8486ea`  
		Last Modified: Tue, 02 Jun 2026 08:13:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5a9ca2122193d89f1297fca3fa676b274b702de22f2258b05bba1c35a0df74`  
		Last Modified: Tue, 02 Jun 2026 08:13:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27af26e27411acc92681460c9d70e79caf586c99316a9bd574e7699d3a45d8a6`  
		Last Modified: Tue, 02 Jun 2026 09:34:41 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbae6125523df1411ebf63072a824516a310a13f487e9b76f009c4da4de8f06`  
		Last Modified: Tue, 02 Jun 2026 09:34:41 GMT  
		Size: 272.0 KB (272019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a91fe64c8c20d51b89106d0cfc73be5537a49d37fb37a7053d6edfe6065f1b`  
		Last Modified: Tue, 02 Jun 2026 09:34:43 GMT  
		Size: 34.5 MB (34528486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ee681e5ec4114fb029ac11fad31f96e3ce79ea2f6432efd1fd21a376c27ed1`  
		Last Modified: Tue, 02 Jun 2026 09:34:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:abe6ee31ccff74f7fa2539155eb55bb25b543c98116d4941673a43159bb31246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5480d79ff66e92444cdfb4a77163645f5abaadb291e7a86c1d6832ef4ff0b99a`

```dockerfile
```

-	Layers:
	-	`sha256:6f1414df1d2483f26821c21d331e02e8826b986740709e9a08259e3c34c5be4b`  
		Last Modified: Tue, 02 Jun 2026 09:34:42 GMT  
		Size: 3.7 MB (3682510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1799020c9650da6bea7d184aa55b949ce63727aa49d7bcc008c8085b2de1e81`  
		Last Modified: Tue, 02 Jun 2026 09:34:41 GMT  
		Size: 26.5 KB (26503 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk17` - linux; riscv64

```console
$ docker pull groovy@sha256:017fbe2dca6976d5a58c094badc8179347503289855857a18be439519cf0ef9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228810729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de96679a68bce8fc2e489ccd9fc3b9e7548dd57a48657bac9f816f3de6e56de`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 16:46:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 16:46:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 16:46:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Apr 2026 16:46:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 16:46:37 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Sat, 09 May 2026 05:25:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 09 May 2026 05:25:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 09 May 2026 05:25:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 09 May 2026 05:25:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 09 May 2026 05:25:23 GMT
CMD ["jshell"]
# Mon, 11 May 2026 02:07:29 GMT
CMD ["groovysh"]
# Mon, 11 May 2026 02:07:29 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 11 May 2026 02:07:29 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Mon, 11 May 2026 02:07:29 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 11 May 2026 02:07:29 GMT
WORKDIR /home/groovy
# Thu, 14 May 2026 10:48:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 10:48:34 GMT
ENV GROOVY_VERSION=5.0.6
# Thu, 14 May 2026 10:51:26 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Thu, 14 May 2026 10:51:26 GMT
USER 1000:1000
# Thu, 14 May 2026 10:51:33 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb43b647117c9f43692f378d47bfa7800d85b1756ada8ad0318423a33c02a7d`  
		Last Modified: Thu, 16 Apr 2026 16:51:32 GMT  
		Size: 20.2 MB (20151745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b08e8e0b833c21962a26a712618fd4df5964be0adbb23ad435bfc5a3206671`  
		Last Modified: Sat, 09 May 2026 05:29:32 GMT  
		Size: 142.9 MB (142907308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6409b16b02342ec50f4b5ce13b162d0638b51ba73682e51405fe8a420a08b00f`  
		Last Modified: Sat, 09 May 2026 05:29:11 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa38d5b4d61eaa859c19ef65ae9ca6c239936d03f4c445e397a722933e3c8a8`  
		Last Modified: Sat, 09 May 2026 05:29:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6057e905b2af0ba5774a24a87c26ba258d04b7bcc924398c012692b4ae3198bb`  
		Last Modified: Mon, 11 May 2026 02:10:56 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7060474aacf75bdf2a0318e701661d667d0a83e333cf819813e4e2da36c2c24`  
		Last Modified: Thu, 14 May 2026 10:53:57 GMT  
		Size: 253.9 KB (253943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062118c43a179f828639faa73907535d53dada08021b4b1752ec68234daa2e24`  
		Last Modified: Thu, 14 May 2026 10:54:02 GMT  
		Size: 34.5 MB (34528484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a6825c0bb57ca609ae14e3060194b0a060a5e5e465385fe365c0f429f8a87b`  
		Last Modified: Thu, 14 May 2026 10:53:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:d2247323145b231c60fbb9daa7c76aff07337b7e5521bcad7d46a3b4192f2ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a588606767a6e53f81bc535b6c963ad49e4554782503d1ab06529afc2e945d5`

```dockerfile
```

-	Layers:
	-	`sha256:aed18916f62e0523554c914420dd504cee7d17fa6b4061209fae546474b9b622`  
		Last Modified: Thu, 14 May 2026 10:53:58 GMT  
		Size: 3.7 MB (3740048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d7231030699ae2716816794085dd68dab74757f6a5c973e1e1093f670770d5`  
		Last Modified: Thu, 14 May 2026 10:53:57 GMT  
		Size: 26.5 KB (26503 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk17` - linux; s390x

```console
$ docker pull groovy@sha256:8367072321d8af0ff7e15cede28a84a2845530e0324be68b1cae17ce8bffd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222747982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e5e731946539a57d4eea66b818060ed51995724ac984fca6f325ca30ef430b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 08:10:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:10:09 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:14:30 GMT
CMD ["groovysh"]
# Tue, 02 Jun 2026 09:14:30 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 02 Jun 2026 09:14:30 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 02 Jun 2026 09:14:30 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 02 Jun 2026 09:14:30 GMT
WORKDIR /home/groovy
# Tue, 02 Jun 2026 09:14:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:34 GMT
ENV GROOVY_VERSION=5.0.6
# Tue, 02 Jun 2026 09:24:22 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 02 Jun 2026 09:24:22 GMT
USER 1000:1000
# Tue, 02 Jun 2026 09:24:22 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ffdfbfb4f4944b96a11c166d27eb5354ff148467639a9d681ba97ff5b81204`  
		Last Modified: Tue, 02 Jun 2026 08:10:32 GMT  
		Size: 22.1 MB (22130668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb2537183efe7bad27200381a0a2f12443c73e053e853ed204dd8426ec757af`  
		Last Modified: Tue, 02 Jun 2026 08:10:34 GMT  
		Size: 135.9 MB (135919264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2cc63b1a16dc201bb49eb6f518074747c1995f0d408d5b80041c5f407fbcc5`  
		Last Modified: Tue, 02 Jun 2026 08:10:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c76ab5db2ad6b46eb77faec4b2222116830afd7e876c0054acb2e3c5329546`  
		Last Modified: Tue, 02 Jun 2026 08:10:31 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b350736bb55d582cea8543d3a2b2185069c50ee76c31e458ade3b3c6a8c3d0`  
		Last Modified: Tue, 02 Jun 2026 09:24:37 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa463913bea9edcecbac60b2e3587936d2f81c7354cf3ddfb09d0ce479c57f65`  
		Last Modified: Tue, 02 Jun 2026 09:24:37 GMT  
		Size: 252.8 KB (252811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0f71df36d3becb9dad4e03ea81a74002727008e00c3bc7eec6adc92b8a357b`  
		Last Modified: Tue, 02 Jun 2026 09:24:37 GMT  
		Size: 34.5 MB (34528485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7773dc469f86fb6c383d306d23f7c386128abe7af674f258c7528169c68d018`  
		Last Modified: Tue, 02 Jun 2026 09:24:37 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:2ac1f25d4538522c90d7235416ee6080e33563772c34c2307abf4fa5b575c841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2358e68b6e0c7ca90b719c3b1a9497ef8893ad55a0d999f69534c8359d680b80`

```dockerfile
```

-	Layers:
	-	`sha256:b08ca9f1274e67324a01596013fc668a8491d316bba5e3d1edc0bf99216c3d38`  
		Last Modified: Tue, 02 Jun 2026 09:24:37 GMT  
		Size: 3.6 MB (3580525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b0de9ad30493415de65a9e2cf677b0ba7e0d62c54b4bff2e810de5c32170ca0`  
		Last Modified: Tue, 02 Jun 2026 09:24:37 GMT  
		Size: 26.4 KB (26429 bytes)  
		MIME: application/vnd.in-toto+json
