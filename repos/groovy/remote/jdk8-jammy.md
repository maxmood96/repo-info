## `groovy:jdk8-jammy`

```console
$ docker pull groovy@sha256:eae6746eb549c12b6b99cc304aef26c3125bf867ddcaec5cb68c165aad825679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `groovy:jdk8-jammy` - linux; amd64

```console
$ docker pull groovy@sha256:ca8c96110d0e0f7c9658543bd5e23374a1f6b7d4248d33a6fefce761e9a1ae41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180375389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699a1d2879e89c106d5698a90b65a9915a5bc8666942c3f3400ded4ca5059170`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 01:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 01:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 01:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 01:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 01:58:34 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 02 Dec 2023 01:58:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='9e574cff0b8dba29930e38eeec4cb4350a77a56a27d03fa316fa6b2383eeef9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 02 Dec 2023 01:58:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Sat, 02 Dec 2023 01:58:40 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 01:58:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 07:04:05 GMT
CMD ["groovysh"]
# Sat, 02 Dec 2023 07:04:05 GMT
ENV GROOVY_HOME=/opt/groovy
# Sat, 02 Dec 2023 07:04:06 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Sat, 02 Dec 2023 07:04:06 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sat, 02 Dec 2023 07:04:06 GMT
WORKDIR /home/groovy
# Sat, 02 Dec 2023 07:04:46 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:04:46 GMT
ENV GROOVY_VERSION=4.0.15
# Sat, 02 Dec 2023 07:04:56 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Sat, 02 Dec 2023 07:04:56 GMT
USER 1000:1000
# Sat, 02 Dec 2023 07:04:57 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a0dd4e5224ba77a5588baadfd0a49dbe1c202ba2c6eaab5e29c7a2904e8718`  
		Last Modified: Sat, 02 Dec 2023 02:03:43 GMT  
		Size: 12.9 MB (12902809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03441d1d9cced70c526fd4b59bf8378ecc812353ce58371d91abcb630b3b0401`  
		Last Modified: Sat, 02 Dec 2023 02:03:49 GMT  
		Size: 103.6 MB (103597812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db162541c53c683418ae5238665c2f116963601165bb62f3256c3fe77355c7bd`  
		Last Modified: Sat, 02 Dec 2023 02:03:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7b8015b57912cf43c00c1d0691d32b04b757e40b1b33374ce19c6e3b5f4f50`  
		Last Modified: Sat, 02 Dec 2023 02:03:41 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef36e44ded85cec7c5f2fffa4e25f329a502ca0c2eea58c9153c664b24611349`  
		Last Modified: Sat, 02 Dec 2023 07:06:44 GMT  
		Size: 4.4 KB (4388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3f0c0fee7ae0aecc4ab338a34431d59aecf7ca6a137a3f9c6c7fa29da66d0c`  
		Last Modified: Sat, 02 Dec 2023 07:06:45 GMT  
		Size: 3.7 MB (3738782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407d43848441eabfc02eb28afd764a9ee7f912a32c2288211be1887e29b7ec47`  
		Last Modified: Sat, 02 Dec 2023 07:06:46 GMT  
		Size: 29.7 MB (29684211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131bd42c0e5bb6c2c30029f0d4250b1495a776678b170ce31599bd2395c3d64c`  
		Last Modified: Sat, 02 Dec 2023 07:06:44 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk8-jammy` - linux; arm variant v7

```console
$ docker pull groovy@sha256:29a6f808027a138c84c391d9cbfd7834723fd0226063f28c16fe7fa53fde8278
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172818450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61857fdc3beca82a4efa9977f1b667aa3d50abd61a49a790ab1a7ab276fd1b5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 01 Dec 2023 07:58:40 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:58:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:58:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:58:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:58:44 GMT
ADD file:852469f16f85d8eff83511eb82d6d4409a4608b882c1634281a43c1c481f70c0 in / 
# Fri, 01 Dec 2023 07:58:44 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:52:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 06:52:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 06:52:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 06:53:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:16 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 02 Dec 2023 06:53:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='9e574cff0b8dba29930e38eeec4cb4350a77a56a27d03fa316fa6b2383eeef9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 02 Dec 2023 06:53:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Sat, 02 Dec 2023 06:53:27 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 06:53:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 07:39:04 GMT
CMD ["groovysh"]
# Sat, 02 Dec 2023 07:39:04 GMT
ENV GROOVY_HOME=/opt/groovy
# Sat, 02 Dec 2023 07:39:05 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Sat, 02 Dec 2023 07:39:05 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sat, 02 Dec 2023 07:39:05 GMT
WORKDIR /home/groovy
# Sat, 02 Dec 2023 07:39:23 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:39:23 GMT
ENV GROOVY_VERSION=4.0.15
# Sat, 02 Dec 2023 07:39:33 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Sat, 02 Dec 2023 07:39:33 GMT
USER 1000:1000
# Sat, 02 Dec 2023 07:39:34 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:24265e8b291700ac2b80b990af5be5827ef3d9ba54e498a6e36563c879970e0f`  
		Last Modified: Wed, 29 Nov 2023 22:33:38 GMT  
		Size: 27.5 MB (27523678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca56cd7c50818a0ddad15a810796d44bf99dd0578c20198db6da1751082578f`  
		Last Modified: Sat, 02 Dec 2023 06:56:43 GMT  
		Size: 12.5 MB (12492095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbcc59d02fcf8b162e520045215d64d3d67670c95063acd163c538296ddb089`  
		Last Modified: Sat, 02 Dec 2023 06:56:50 GMT  
		Size: 99.2 MB (99234952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818f69b81acd851c7c51262889eefcae84ec9226046c9a96516236feed9d03da`  
		Last Modified: Sat, 02 Dec 2023 06:56:40 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bf57bf76f082cf1fa0a047d56c9736992d7ac258f12b4767dff65b544cee72`  
		Last Modified: Sat, 02 Dec 2023 06:56:40 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45e4d795cf84ef25f75e0a88d2729d6b9c94c17739805bc7b75080617096348`  
		Last Modified: Sat, 02 Dec 2023 07:40:31 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8191d0599f2b3d0df5ee1be2c791816685caf489ae31823fb45d9d8d496729d`  
		Last Modified: Sat, 02 Dec 2023 07:40:32 GMT  
		Size: 3.9 MB (3878077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee7a9f6645546b3d1ba9a3e4044f2436b028c03f6fe2aa482dffbd3f65e8ef6`  
		Last Modified: Sat, 02 Dec 2023 07:40:33 GMT  
		Size: 29.7 MB (29684205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29406970c943bc06366ecdd6eed24398d1a813229f77c32af50d2d683b02326d`  
		Last Modified: Sat, 02 Dec 2023 07:40:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk8-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:266c4ff8f46a714846305cd8beee1246d0a7703d81bfa523ebd83b979b3b6eaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.3 MB (177339873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a042aad3874b603e5dee9fa014225c14b0b552045bd58cd32cb385bcf158fe22`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:46:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 02:46:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 02:46:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:41:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2023 01:37:12 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 02 Nov 2023 01:37:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='9e574cff0b8dba29930e38eeec4cb4350a77a56a27d03fa316fa6b2383eeef9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Nov 2023 01:37:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 02 Nov 2023 01:37:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 02 Nov 2023 01:37:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 Nov 2023 03:11:02 GMT
CMD ["groovysh"]
# Thu, 02 Nov 2023 03:11:02 GMT
ENV GROOVY_HOME=/opt/groovy
# Thu, 02 Nov 2023 03:11:03 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Thu, 02 Nov 2023 03:11:03 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Thu, 02 Nov 2023 03:11:03 GMT
WORKDIR /home/groovy
# Thu, 02 Nov 2023 03:11:09 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Thu, 02 Nov 2023 03:11:09 GMT
ENV GROOVY_VERSION=4.0.15
# Thu, 02 Nov 2023 03:11:37 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Thu, 02 Nov 2023 03:11:37 GMT
USER 1000:1000
# Thu, 02 Nov 2023 03:11:38 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4035bfa3ea28e4a939fa769d2862227b94b4b5b961f65ac5df2ea3df7a0c51e4`  
		Last Modified: Mon, 30 Oct 2023 23:48:25 GMT  
		Size: 12.8 MB (12843579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed95f81ccc58908188be8e5864a55b5acb462d4d1c8975e7fcace7f8df56fd50`  
		Last Modified: Thu, 02 Nov 2023 01:40:05 GMT  
		Size: 102.7 MB (102705552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5c3bb9f1dcf7a493d56a2be859d6b5fa3b4457c72df420834c4a2afddc5e0`  
		Last Modified: Thu, 02 Nov 2023 01:39:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0663f8654b9bb70808dd2c3a07fbf4cf2648ee096a941d7c92aa742784dbf84b`  
		Last Modified: Thu, 02 Nov 2023 01:39:56 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b7c5a0815f91c0936872a6f9434f30ac4f7dbfd75346a96af9701061070b92`  
		Last Modified: Thu, 02 Nov 2023 03:12:36 GMT  
		Size: 4.4 KB (4391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdd10633e729df22885cd97d629ba2801961e3e788b22d5d6bbcffc15490077`  
		Last Modified: Thu, 02 Nov 2023 03:12:37 GMT  
		Size: 3.7 MB (3709132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ce890093dddabdcf1e380a4275abd74cf4c0fbdcb9ca2a58353c6f8698f31`  
		Last Modified: Thu, 02 Nov 2023 03:12:38 GMT  
		Size: 29.7 MB (29684215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b43ee8e307fb167361331ce7f50b05a6b01a857ffea685c5a38f9bf4f7249c6`  
		Last Modified: Thu, 02 Nov 2023 03:12:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk8-jammy` - linux; ppc64le

```console
$ docker pull groovy@sha256:567e8189ae9ebd9c2b61d3264cb8015b1065bf0b142b244a695fd54ff3e4c454
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184658187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046bfb91d825f3d39b0bb0051f50d353b78693992f70e0f2458b8efe691672ca`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:00:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:00:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:19:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2023 01:19:03 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 02 Nov 2023 01:19:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='9e574cff0b8dba29930e38eeec4cb4350a77a56a27d03fa316fa6b2383eeef9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Nov 2023 01:19:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 02 Nov 2023 01:19:17 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 02 Nov 2023 01:19:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 Nov 2023 02:08:45 GMT
CMD ["groovysh"]
# Thu, 02 Nov 2023 02:08:45 GMT
ENV GROOVY_HOME=/opt/groovy
# Thu, 02 Nov 2023 02:08:46 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Thu, 02 Nov 2023 02:08:47 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Thu, 02 Nov 2023 02:08:47 GMT
WORKDIR /home/groovy
# Thu, 02 Nov 2023 02:09:13 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Thu, 02 Nov 2023 02:09:14 GMT
ENV GROOVY_VERSION=4.0.15
# Thu, 02 Nov 2023 02:09:25 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Thu, 02 Nov 2023 02:09:26 GMT
USER 1000:1000
# Thu, 02 Nov 2023 02:09:29 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c5d264e1020afdce89cd369c927646ea9f3d19c1a2f659b6d4e83c21618a2b`  
		Last Modified: Mon, 30 Oct 2023 23:29:59 GMT  
		Size: 13.8 MB (13768056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27c13fdf3f0ec3085f4b5e96920a5d509367c7f8a83b83d9a3e67ae07cff3a9`  
		Last Modified: Thu, 02 Nov 2023 01:23:05 GMT  
		Size: 101.1 MB (101068868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af99300d8928d011282b2c3a58bca017723a342e2d9849f5f4fc8df3eea69b70`  
		Last Modified: Thu, 02 Nov 2023 01:22:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a28860291c3f1aceb945520b28ed8fc55528b569e5c64bca772e3cfb8a834e`  
		Last Modified: Thu, 02 Nov 2023 01:22:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32c0b5d9196eeba4ca6b023f3b5b6cb7234ac34a0c22a82236173d06a75aa2b`  
		Last Modified: Thu, 02 Nov 2023 02:09:54 GMT  
		Size: 4.4 KB (4388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d546cab6060fa21a64a94925bbb0bcb8941324311ad40d6920a447534af894`  
		Last Modified: Thu, 02 Nov 2023 02:09:54 GMT  
		Size: 4.4 MB (4448801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245eb2d17780a5033f923f7ff06d001846cbf6b0313171e2ac7e7d292e5c9d39`  
		Last Modified: Thu, 02 Nov 2023 02:09:56 GMT  
		Size: 29.7 MB (29684214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0aec8a4137b9fe4153711cc66789656a1173840779fd16cb3e274326243e8b`  
		Last Modified: Thu, 02 Nov 2023 02:09:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
