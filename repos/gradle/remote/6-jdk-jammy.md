## `gradle:6-jdk-jammy`

```console
$ docker pull gradle@sha256:4e0e579108d5b15dcaa2ce93dfea28b543bb988c8b41dbce2c454a5724621e45
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

### `gradle:6-jdk-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:1082ca440ece1718711a7b1bb1f22da26ca9095b8595ef25f0f9b61ad6ffc3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350246214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf218c28a08cf1a8d77fd84564fd2839421d7256b36fc4e9b0be852e8d5aec41`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf599904bab57f4fa8e3dc79abf53d23b0718b8b293d6c57c6611af6410e31`  
		Last Modified: Tue, 03 Jun 2025 13:32:25 GMT  
		Size: 16.1 MB (16146415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4121a4b308c3813e7ca16e4c30ff012542061d07386b3bdff7e38b95739a7d2`  
		Last Modified: Tue, 03 Jun 2025 13:32:35 GMT  
		Size: 145.6 MB (145645098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9093c9726fb77042e1abc93563b713ea02e481454345311f69b32a06757c0f`  
		Last Modified: Tue, 03 Jun 2025 13:32:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b977c46889de2487c980399cba0fa6c04d3bd8fde596eb59cccf75b06684ea8`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5953ad737cfa150b6f7ae6246a8e7c44cd8a8fe99b213c14d6f1f86cb7207ef2`  
		Last Modified: Tue, 03 Jun 2025 13:34:24 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa446bf242882ab91eb91abdd0c117027cb9dd8f61437c43eb0ffecb9150c0f`  
		Last Modified: Tue, 03 Jun 2025 13:36:09 GMT  
		Size: 50.8 MB (50786996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba325e2bc53a22d2ec509f688e77d64a5fb40fa0170304a6f0d03cf66ef41fd`  
		Last Modified: Tue, 03 Jun 2025 13:36:19 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c8364bed461466850aa92572d30fc93b6f803cb5bed779ef1abe9a49bc38c5`  
		Last Modified: Tue, 03 Jun 2025 13:36:07 GMT  
		Size: 431.3 KB (431257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:56e19eaadfefbfeb5bd4dabbe96148c2a87f75b5d3a44d70eb24c0b0d68e9474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f637a8916dfd53e655b27d71da8bca94b7d13e8744e6bf53ef231137e167e3`

```dockerfile
```

-	Layers:
	-	`sha256:0328f24ef670d777e47736caf5a2d6ebeb9b43beb9ae49af59bd260a28f44a67`  
		Last Modified: Tue, 03 Jun 2025 05:12:21 GMT  
		Size: 7.4 MB (7398798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ea73e3567e9ddd0257fe7dec377fae9f9c11e50e1bd3e4e464aca10aa30f5e7`  
		Last Modified: Tue, 03 Jun 2025 05:12:21 GMT  
		Size: 27.5 KB (27475 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:739fe88f51e5cfec5fa72a7143c47c4428ab2428dbfcca8056fbd8e8c7c4c528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341650029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee0d44f2e2602eeb1e4da889c278a8c6aa6fc4c85301826eb61a99479bce676`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
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
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:f35c50ead1843adba7d4d13281d31bc17c201a55b8bd1a3961e1bcfd131b762d`  
		Last Modified: Tue, 03 Jun 2025 13:42:56 GMT  
		Size: 26.6 MB (26640475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c869906112a22f8bcfcd7276bcc7d904f46535968a6e8d65eb57940c3ac442`  
		Last Modified: Tue, 03 Jun 2025 14:52:52 GMT  
		Size: 15.9 MB (15890981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd2fe76188645287fd6e1174029efc9c40dfa2c67628018341d06e5c5ebd716`  
		Last Modified: Wed, 04 Jun 2025 00:27:03 GMT  
		Size: 138.1 MB (138116363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4da1bfd69fb0d5ea5abdad53817609a183d9e8d7a6b570049c1e3adbf4e0b2`  
		Last Modified: Wed, 04 Jun 2025 00:26:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fcc7b6dfa812f0337384c7092c6c950c7f4e0df08cbea6aa5976012374def2`  
		Last Modified: Wed, 04 Jun 2025 00:26:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaebbcff913d1de8a33471249b793bbe7096ebfb8107afd3520243a4ac4b6e80`  
		Last Modified: Wed, 04 Jun 2025 00:26:48 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d74e9f162fefe4f0df15329f3044fb7a7355819a9276c642638915cc589797`  
		Last Modified: Wed, 04 Jun 2025 00:26:50 GMT  
		Size: 53.3 MB (53267505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157787a88ba1829a10be370d5d2f782f051a71b13c438919b70d5566fc02a34`  
		Last Modified: Tue, 03 Jun 2025 05:25:02 GMT  
		Size: 107.7 MB (107696666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562254e8152aea5b539eb6e3549ae46fcc359314845f31c4fde28db75aa952dd`  
		Last Modified: Tue, 03 Jun 2025 05:24:59 GMT  
		Size: 31.3 KB (31266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:ba13ec909d9622cef28fdf1e2ed339c36c4ddd445d0329b224f02d0770dd8a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef516c1a2eda20edd22900720219c25c3071d245205e81c312e3e3b5bea2550`

```dockerfile
```

-	Layers:
	-	`sha256:74664efbcc4f68c19d6ef4562a994776a3e4030881dd4b0d7398a1667ecfd354`  
		Last Modified: Tue, 03 Jun 2025 05:24:59 GMT  
		Size: 7.4 MB (7399000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:317b147f110abdceb35388fac376b2f29822bbb557c1f64a78e279d8441d180a`  
		Last Modified: Tue, 03 Jun 2025 05:24:59 GMT  
		Size: 27.7 KB (27700 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:622ed29a05b9f4c23dd3acb7adf6dba822a660560fecf97cf4d4567308d1688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.3 MB (344304270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b00c04fcdb665776951dfce9c519bf9e0995d7f41cf66c1f99342e1e643a7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cfe0c2e8be99f8d950a6958a0c910d4d550d66bf0da03d2cb05a26a4ba8061`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 16.1 MB (16059839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74e1f5c1ff37940e3726069bdd4d40b048bb80baabd78aa29c40db9282dec05`  
		Last Modified: Tue, 03 Jun 2025 13:31:39 GMT  
		Size: 142.4 MB (142431747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4a3d45342daab6cf4007a85ec3d8eaba6db2b38c3e121556061f93397b6181`  
		Last Modified: Tue, 03 Jun 2025 13:31:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2886475a6cecf4824dd4ce8354f317e69bacaa06cf236e1cd6fa721d93a2609`  
		Last Modified: Tue, 03 Jun 2025 13:31:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ab86e1e8ddc046803d3388d62086de380117a1601c1d31ad3d8b4766a3d20b`  
		Last Modified: Tue, 03 Jun 2025 14:23:01 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927f0aaf8f8b21e4120a845aeaa836342724b6b573e3455d2296e81ad108eaa`  
		Last Modified: Tue, 03 Jun 2025 14:23:08 GMT  
		Size: 50.3 MB (50328634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1487df0d7b93bf3490e369ca119dc04737b5a3ba8cc6b64f58ac9bc8860a1ebd`  
		Last Modified: Tue, 03 Jun 2025 14:51:35 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136b36821a147143b7bc2bfd826ecda4faecc657aea750ddcecab44eeebf3518`  
		Last Modified: Tue, 03 Jun 2025 14:51:26 GMT  
		Size: 425.0 KB (425016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:120aa52cf429743ae455b1adf65d3b90596dab342656e7562166caae59b67e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83712ae5ae24ec55f6106b040c00246f19d3005b2b1ac6c8400162905f4a609f`

```dockerfile
```

-	Layers:
	-	`sha256:6670702c46440c35fc85dc60abc74e1330905c06c608365d1157ec7241fd08a5`  
		Last Modified: Tue, 03 Jun 2025 07:18:38 GMT  
		Size: 7.4 MB (7405409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139e6c892031dd89753bfb8eede0a7c43d02a735bdb98c17c7ec6bd3328c6a20`  
		Last Modified: Tue, 03 Jun 2025 07:18:37 GMT  
		Size: 27.8 KB (27792 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:bf1efd664d60310e34e10db096c5e9780aa18dd0b3c57f629dc6b5fe9e2cef06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347375438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdc11f505c5960c173771bb8b8275e125584d65ab42a1fad0a0ea314ec1f3e1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
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
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de0e8a8949ec849c4e2d822052efc995cbfd8901f78e2be800be3fd9735154`  
		Last Modified: Tue, 03 Jun 2025 14:13:03 GMT  
		Size: 17.6 MB (17618370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5183ae9aceac171fbde0c7a115b3f753774893a6e5c86468639201adaf47aacb`  
		Last Modified: Tue, 03 Jun 2025 15:34:59 GMT  
		Size: 132.8 MB (132826387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9007a9495127ba84eec6debee4877c9728e8bf333643220772bebd9083b8e7`  
		Last Modified: Tue, 03 Jun 2025 15:34:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef9455743cd744f44a0dab6b49c18379ef911bc540cfe9b642fd351c14cf3b6`  
		Last Modified: Tue, 03 Jun 2025 15:34:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e29947679379f41d2e1b5f7bb9dbc60610a5b615fc184018836ebe6b53a909`  
		Last Modified: Tue, 03 Jun 2025 06:45:49 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfffe93eaad36d964572341b6dd573f5db0932d01ee77e1f413d465403a5588`  
		Last Modified: Tue, 03 Jun 2025 06:45:51 GMT  
		Size: 54.8 MB (54751892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdc9c61220c7d9062eff45bc165eec183455fc64552735fc8db888d7a596989`  
		Last Modified: Tue, 03 Jun 2025 06:57:30 GMT  
		Size: 107.7 MB (107696666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94505667c0ff394ba33f7de358c5f80ea888c8e3ce0eed5fe54cd30ff72d7a9f`  
		Last Modified: Tue, 03 Jun 2025 06:57:27 GMT  
		Size: 35.0 KB (34980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:fe368703328ca0b3e91524dc8a8e488f48b19fd943d4c4fa8a35e6856a3b8c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011a2f5b8bc3d3283189ef625b36d3df364e5c51c2d4c4a3576cd6a5bb399324`

```dockerfile
```

-	Layers:
	-	`sha256:e31d9a023c8f71d115c4efa4d4f2a46506babd148e8f5e0bea4c7b4451f64d35`  
		Last Modified: Tue, 03 Jun 2025 06:57:27 GMT  
		Size: 7.4 MB (7403727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:037f146d71e2262b93a821f0af5891dfd99a6c993302af25d22c41b83caf6dc5`  
		Last Modified: Tue, 03 Jun 2025 06:57:26 GMT  
		Size: 27.6 KB (27608 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:5559ef96e8f6740a1bc112e23f2fa8a6243709753453c5f23354735d16e848e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (327977085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0a59fc2f4c1ed028fad8ec4d7f0d46ecc02cbf79a1d82ae048c010c2fae8a1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
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
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b083bb928961c2c7996d495007331b50b7da602cad00b66781c07e7118c9394`  
		Last Modified: Tue, 03 Jun 2025 14:13:00 GMT  
		Size: 16.1 MB (16144355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72cea04f04c6035c059efe028edc77d7ab9d109f867cb75e0e0bc8aabac3478`  
		Last Modified: Tue, 03 Jun 2025 15:10:25 GMT  
		Size: 125.6 MB (125596854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceb8355a9c8a79c9659d02a6cc11dce3e7dea12d9107fb2f81bda8186a938d5`  
		Last Modified: Tue, 03 Jun 2025 15:10:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3988886004ba87a90e66a39507e68fd12b184ccbcf23e4311781c62df5ce52d`  
		Last Modified: Tue, 03 Jun 2025 15:10:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7365b4a7122e5655ba585e9f34fde52c50c140a0defbfb062383d581f4778ddf`  
		Last Modified: Tue, 03 Jun 2025 05:24:54 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d246445a704f3aa95f6992ad8e61eaeb47934676b31bc03a2713b2924b38340c`  
		Last Modified: Tue, 03 Jun 2025 05:24:56 GMT  
		Size: 50.5 MB (50496882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3782c38e54c5925845d63c07183ef944bc40093570d7d14b3e4474b51fa0f5b`  
		Last Modified: Tue, 03 Jun 2025 05:30:47 GMT  
		Size: 107.7 MB (107696632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94d9e4fabf1f183d699c9b74e9f13cc8eba891acf2a594dd77456899f3e5c13`  
		Last Modified: Tue, 03 Jun 2025 05:30:44 GMT  
		Size: 35.0 KB (34975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:3adc49dc1d660508704047d4b0d4b028eca49ede8f7e07ebb892ec8622641009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3372090f5cb8e8af65f9164be7a6d80569bff1539a750cda24a71c4c8e3597bd`

```dockerfile
```

-	Layers:
	-	`sha256:8b9707d0c32a3b346e7080e57233097154a8ef3047b19e332a46127c38c8179f`  
		Last Modified: Tue, 03 Jun 2025 05:30:45 GMT  
		Size: 7.4 MB (7394678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ce47769febc1fdc021ab1f3c854506bb2bfe4c86a7afa9eb8e1eb96d07e3c9a`  
		Last Modified: Tue, 03 Jun 2025 05:30:44 GMT  
		Size: 27.5 KB (27474 bytes)  
		MIME: application/vnd.in-toto+json
