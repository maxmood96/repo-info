## `groovy:jre8`

```console
$ docker pull groovy@sha256:001d97caf1f178c6d29bef838b6819f29ef14c41c2975331b2158c01ba7e2b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `groovy:jre8` - linux; amd64

```console
$ docker pull groovy@sha256:3aaec5d40c2fcf4e972534a17b7e02e8d4c320c43e0a88485678ca3e11f41636
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128156761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaea0f44300c08f6cd4a46c0f6ab370dc2c1b3a78cfc8a9c1fd49374114b9fe`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 19:27:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Apr 2020 19:28:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 19:28:13 GMT
ENV JAVA_VERSION=jdk8u252-b09
# Fri, 24 Apr 2020 19:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='30bba4425497f5b4aabcba7b45db69d582d278fb17357d64c22c9dc6b2d29ca1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u252b09.tar.gz';          ;;        armhf|armv7l)          ESUM='107699a88f611e0c2d57816be25821ef9b17db860b14402c4e9e5bf0b9cf16fd';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_arm_linux_hotspot_8u252b09.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='fbc559e8f75107f3c2ef92b33938dd48aee5728d471774d04fa3f68ed3b992fe';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u252b09.tar.gz';          ;;        s390x)          ESUM='23daa316ebcd965197e74dff011708a050516cd108a27a40e5b5cfa3c88beaba';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u252b09.tar.gz';          ;;        amd64|x86_64)          ESUM='a93be303ed62398dba9acb0376fb3caf8f488fcde80dc62d0a8e46256b3adfb1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_x64_linux_hotspot_8u252b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Apr 2020 19:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Apr 2020 01:08:44 GMT
CMD ["groovysh"]
# Sat, 25 Apr 2020 01:08:44 GMT
ENV GROOVY_HOME=/opt/groovy
# Sat, 25 Apr 2020 01:08:45 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Sat, 25 Apr 2020 01:08:45 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sat, 25 Apr 2020 01:08:45 GMT
WORKDIR /home/groovy
# Sat, 25 Apr 2020 01:08:51 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         fontconfig         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Fri, 22 May 2020 19:19:55 GMT
ENV GROOVY_VERSION=3.0.4
# Fri, 22 May 2020 19:20:00 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)";     for key in         "7FAA0F2206DE228F0DB01AD741321490758AAD6F"         "331224E1D7BE883D16E8A685825C06C827AF6B66"         "34441E504A937F43EB0DAEF96A65176A0FB1CD0B"         "9A810E3B766E089FFB27C70F11B595CEDC4AEBB5"         "81CABC23EECA0790E8989B361FF96E10F0E13706"     ; do         for server in             "ha.pool.sks-keyservers.net"             "hkp://p80.pool.sks-keyservers.net:80"             "pgp.mit.edu"         ; do             echo "  Trying ${server}";             if gpg --batch --no-tty --keyserver "${server}" --recv-keys "${key}"; then                 break;             fi;         done;     done;     if [ $(gpg --batch --no-tty --list-keys | grep --count "pub ") -ne 5 ]; then         echo "ERROR: Failed to fetch GPG keys" >&2;         exit 1;     fi         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Fri, 22 May 2020 19:20:00 GMT
USER groovy
# Fri, 22 May 2020 19:20:02 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3058952867bac0b1deeecce925b304f4e354c7b8781d75fbfc6d36373ead53af`  
		Last Modified: Fri, 24 Apr 2020 19:32:11 GMT  
		Size: 13.3 MB (13324407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7664375c20fabba4facfc8e8255ee81231c491ad7c11f5dbc17147b2aa87d9`  
		Last Modified: Fri, 24 Apr 2020 19:32:29 GMT  
		Size: 41.5 MB (41453811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e1e7fde90512d213c1513da5f27f99f2da43fc66a80c342193ceb0f416477`  
		Last Modified: Sat, 25 Apr 2020 01:10:38 GMT  
		Size: 4.5 KB (4517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e81d9bb58ecfa41f09aeb69d84ad73109cc461adc9e3253812e3e2371a837`  
		Last Modified: Sat, 25 Apr 2020 01:10:39 GMT  
		Size: 3.4 MB (3445054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643b1023dc253f79edfc27e72f7ce535f158c05521d02e8c49e560325c4b8f50`  
		Last Modified: Fri, 22 May 2020 19:21:24 GMT  
		Size: 43.2 MB (43202655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a27b33c036986781cfbcd5c043f1df1583d106ce9c5d1b2c10049ac031eac79`  
		Last Modified: Fri, 22 May 2020 19:21:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jre8` - linux; ppc64le

```console
$ docker pull groovy@sha256:974380fc24e6d43958049518393463f1e6a9afcc47581d0b2a1850f84d95cbc8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132357968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d206159ba6ae5ea21a6d5f88f294b02b205ed106e6ccf315878b8e4f78c403`
-	Default Command: `["groovysh"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:22:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Apr 2020 11:23:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:23:49 GMT
ENV JAVA_VERSION=jdk8u252-b09
# Fri, 24 Apr 2020 11:24:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='30bba4425497f5b4aabcba7b45db69d582d278fb17357d64c22c9dc6b2d29ca1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u252b09.tar.gz';          ;;        armhf|armv7l)          ESUM='107699a88f611e0c2d57816be25821ef9b17db860b14402c4e9e5bf0b9cf16fd';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_arm_linux_hotspot_8u252b09.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='fbc559e8f75107f3c2ef92b33938dd48aee5728d471774d04fa3f68ed3b992fe';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u252b09.tar.gz';          ;;        s390x)          ESUM='23daa316ebcd965197e74dff011708a050516cd108a27a40e5b5cfa3c88beaba';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u252b09.tar.gz';          ;;        amd64|x86_64)          ESUM='a93be303ed62398dba9acb0376fb3caf8f488fcde80dc62d0a8e46256b3adfb1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_x64_linux_hotspot_8u252b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Apr 2020 11:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 17:00:01 GMT
CMD ["groovysh"]
# Fri, 24 Apr 2020 17:00:04 GMT
ENV GROOVY_HOME=/opt/groovy
# Fri, 24 Apr 2020 17:00:12 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Fri, 24 Apr 2020 17:00:15 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Fri, 24 Apr 2020 17:00:20 GMT
WORKDIR /home/groovy
# Fri, 24 Apr 2020 17:00:50 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         fontconfig         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Fri, 22 May 2020 19:18:10 GMT
ENV GROOVY_VERSION=3.0.4
# Fri, 22 May 2020 19:18:40 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)";     for key in         "7FAA0F2206DE228F0DB01AD741321490758AAD6F"         "331224E1D7BE883D16E8A685825C06C827AF6B66"         "34441E504A937F43EB0DAEF96A65176A0FB1CD0B"         "9A810E3B766E089FFB27C70F11B595CEDC4AEBB5"         "81CABC23EECA0790E8989B361FF96E10F0E13706"     ; do         for server in             "ha.pool.sks-keyservers.net"             "hkp://p80.pool.sks-keyservers.net:80"             "pgp.mit.edu"         ; do             echo "  Trying ${server}";             if gpg --batch --no-tty --keyserver "${server}" --recv-keys "${key}"; then                 break;             fi;         done;     done;     if [ $(gpg --batch --no-tty --list-keys | grep --count "pub ") -ne 5 ]; then         echo "ERROR: Failed to fetch GPG keys" >&2;         exit 1;     fi         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Fri, 22 May 2020 19:18:43 GMT
USER groovy
# Fri, 22 May 2020 19:18:53 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841fc1003510ef9b0e7994850d1dd2608238f020eb8892ebb14f71b9b02c1170`  
		Last Modified: Fri, 24 Apr 2020 11:36:20 GMT  
		Size: 14.0 MB (13970642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28bc0ecd618cad1d9251e06ea3b9b7b7421d2e8216bb070210db774d516f116`  
		Last Modified: Fri, 24 Apr 2020 11:37:00 GMT  
		Size: 40.5 MB (40529137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9a20ef8a840c41428609a8f965ddb5aa068fb12d7405cbc06c4fded8dcb5c9`  
		Last Modified: Fri, 24 Apr 2020 17:10:11 GMT  
		Size: 4.5 KB (4545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb8e44ba74945fe1016260a57cdcdb2fbe4ae2713a4c0eb73c65e2b726f6bdb`  
		Last Modified: Fri, 24 Apr 2020 17:10:12 GMT  
		Size: 4.2 MB (4214300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f43a695635bc36cee41e13106a318b4bdc68ded472f6b2846098a7eaa7584bb`  
		Last Modified: Fri, 22 May 2020 19:23:29 GMT  
		Size: 43.2 MB (43202635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2431d29fdcd53b07e1ea6582133d5901bf1c0ad651331c6b977a1618303319`  
		Last Modified: Fri, 22 May 2020 19:23:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jre8` - linux; s390x

```console
$ docker pull groovy@sha256:f1647622bbf1163c12a221a7231a3331283d63e55d2bea9830c195281ef368e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124213855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a641bcf3ffca168a1f2d42a2d41bb32b6471816d4e15dd78c1e445c1e218e9a5`
-	Default Command: `["groovysh"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:36:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Apr 2020 07:37:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:37:08 GMT
ENV JAVA_VERSION=jdk8u252-b09
# Fri, 24 Apr 2020 07:37:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='30bba4425497f5b4aabcba7b45db69d582d278fb17357d64c22c9dc6b2d29ca1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u252b09.tar.gz';          ;;        armhf|armv7l)          ESUM='107699a88f611e0c2d57816be25821ef9b17db860b14402c4e9e5bf0b9cf16fd';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_arm_linux_hotspot_8u252b09.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='fbc559e8f75107f3c2ef92b33938dd48aee5728d471774d04fa3f68ed3b992fe';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u252b09.tar.gz';          ;;        s390x)          ESUM='23daa316ebcd965197e74dff011708a050516cd108a27a40e5b5cfa3c88beaba';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u252b09.tar.gz';          ;;        amd64|x86_64)          ESUM='a93be303ed62398dba9acb0376fb3caf8f488fcde80dc62d0a8e46256b3adfb1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_x64_linux_hotspot_8u252b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Apr 2020 07:37:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 11:02:48 GMT
CMD ["groovysh"]
# Fri, 24 Apr 2020 11:02:49 GMT
ENV GROOVY_HOME=/opt/groovy
# Fri, 24 Apr 2020 11:02:50 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Fri, 24 Apr 2020 11:02:50 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Fri, 24 Apr 2020 11:02:51 GMT
WORKDIR /home/groovy
# Fri, 24 Apr 2020 11:03:01 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         fontconfig         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Fri, 22 May 2020 19:42:11 GMT
ENV GROOVY_VERSION=3.0.4
# Fri, 22 May 2020 19:42:19 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)";     for key in         "7FAA0F2206DE228F0DB01AD741321490758AAD6F"         "331224E1D7BE883D16E8A685825C06C827AF6B66"         "34441E504A937F43EB0DAEF96A65176A0FB1CD0B"         "9A810E3B766E089FFB27C70F11B595CEDC4AEBB5"         "81CABC23EECA0790E8989B361FF96E10F0E13706"     ; do         for server in             "ha.pool.sks-keyservers.net"             "hkp://p80.pool.sks-keyservers.net:80"             "pgp.mit.edu"         ; do             echo "  Trying ${server}";             if gpg --batch --no-tty --keyserver "${server}" --recv-keys "${key}"; then                 break;             fi;         done;     done;     if [ $(gpg --batch --no-tty --list-keys | grep --count "pub ") -ne 5 ]; then         echo "ERROR: Failed to fetch GPG keys" >&2;         exit 1;     fi         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Fri, 22 May 2020 19:42:21 GMT
USER groovy
# Fri, 22 May 2020 19:42:27 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cda817e3f7c865b0840c4d8029ccd310418aaf7af7a0aeda3eaa4cb945fca4b`  
		Last Modified: Fri, 24 Apr 2020 07:41:58 GMT  
		Size: 13.0 MB (13043886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68bc8aae94714b6cfb57f57d0784273c9c3a28c8d8375b79a1cae5e5c6642a7`  
		Last Modified: Fri, 24 Apr 2020 07:42:17 GMT  
		Size: 39.2 MB (39161290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6068a6f3ac28b46ea3010bd53fe1ee7b821aac0635ffc310bc4ac45f75ee3c86`  
		Last Modified: Fri, 24 Apr 2020 11:04:57 GMT  
		Size: 4.5 KB (4548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d547d0ba40fc5194e2669107c04cbd87f83b2adbdd9915cad3a06097a98289`  
		Last Modified: Fri, 24 Apr 2020 11:04:57 GMT  
		Size: 3.4 MB (3398779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b131372a38ce23de9f5fbeeee7ded543ee2368ad4e0946285bc1523a4296a7`  
		Last Modified: Fri, 22 May 2020 19:44:08 GMT  
		Size: 43.2 MB (43202631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd02a93d331d6891dd0f7471135448f345d04a7f30b5aa5a590351c7322c3f97`  
		Last Modified: Fri, 22 May 2020 19:44:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
