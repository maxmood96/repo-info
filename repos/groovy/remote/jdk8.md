## `groovy:jdk8`

```console
$ docker pull groovy@sha256:28c6dd5d8abfbc550182dc19162bb3c9f4875ac898b34e478fcb1a5b87f3cdb2
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

### `groovy:jdk8` - linux; amd64

```console
$ docker pull groovy@sha256:6215073167a70a6be069478afacc8eb9ed45d4e72c93e72c3a388cfc5289539d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179478652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107822dfdbc57a61ac9a6e348423225018ad4312059cc11e6563b7ed95f014fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Sep 2024 16:23:25 GMT
CMD ["groovysh"]
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 30 Sep 2024 16:23:25 GMT
WORKDIR /home/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_VERSION=4.0.23
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
USER 1000:1000
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802ed325d1cf41a45d1cbde5d2ec184079488d15b4dd6d4303533c1d55c4bf64`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 12.9 MB (12887765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db51cdecc7f625b03acc104e3f438ffb05258c707463d38cada5a905d74a442`  
		Last Modified: Sat, 19 Oct 2024 02:06:45 GMT  
		Size: 103.6 MB (103615887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e0e01eb7c7d1eef6e9ccb8142cf2f94fca511dccb531329129ba9508d81948`  
		Last Modified: Sat, 19 Oct 2024 02:06:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515d4ca2e911f1daca31c714b3a7546ad605de705020368a63468b6bd6371a40`  
		Last Modified: Sat, 19 Oct 2024 02:06:41 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ccbb97e8f692ebab38e995ef868642e069b39bf27eec485ec0ae099dce1209`  
		Last Modified: Sat, 19 Oct 2024 02:56:07 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36596b497f41cc5e82a45250542d9184599a9980094f4793b031752d1b9b9a8c`  
		Last Modified: Sat, 19 Oct 2024 02:56:07 GMT  
		Size: 3.5 MB (3500105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293873b20f91d0f22ce2f7e5da4d69e8da17c0c00c23861620e9254d0d4b0c5`  
		Last Modified: Sat, 19 Oct 2024 02:56:07 GMT  
		Size: 29.9 MB (29932446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a209e0710d4b53d5a3d4e4c50f72111415f48ce68e087ae50d966c36e96ea7`  
		Last Modified: Sat, 19 Oct 2024 02:56:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8` - unknown; unknown

```console
$ docker pull groovy@sha256:9883e6c2989e1d916f56c51b174d4f2119380c8e8cea98311d982545fd522fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3991c739ddd772f01acd03eff4aa6672081281ac83385252d42e035f39e60bb9`

```dockerfile
```

-	Layers:
	-	`sha256:de6f605fd281ea620ffb6d4796f5c67e26ef0ee3d83ae9d5f3aae277868bf184`  
		Last Modified: Sat, 19 Oct 2024 02:56:07 GMT  
		Size: 4.0 MB (4010338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8582655eec200b9dfd821909b24691fc4068df6214f21fd56a894d20304808c1`  
		Last Modified: Sat, 19 Oct 2024 02:56:07 GMT  
		Size: 24.9 KB (24927 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8` - linux; arm variant v7

```console
$ docker pull groovy@sha256:b0f71f57f850f3cdc6e8f28867916e5af55e5ac3f70f177bd219e17065e0606e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171705212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43dce7165b058ebfad499c91fe4c352c5ad56978cb2d552cb698427b6ab5c9d8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Sep 2024 16:23:25 GMT
CMD ["groovysh"]
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 30 Sep 2024 16:23:25 GMT
WORKDIR /home/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_VERSION=4.0.23
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
USER 1000:1000
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5b4d887278ade3f64ec61b88e5492ae03ef2a1f91c77eeccba0caf20b33e9`  
		Last Modified: Sat, 19 Oct 2024 06:50:50 GMT  
		Size: 12.5 MB (12476416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227a122c35346d59b10c83e6c845371fdd91948b47f4ec127b237feef5fc2a5`  
		Last Modified: Sat, 19 Oct 2024 06:50:52 GMT  
		Size: 99.0 MB (99011086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdebf83fe544741236346a5034d4ea7d170279b91c7eff07ca7f381057f0dcb`  
		Last Modified: Sat, 19 Oct 2024 06:50:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d877e1e07453f9279ab9bba5b2f50afc44cd1c4ab0bcfefb2c3814665f92e376`  
		Last Modified: Sat, 19 Oct 2024 06:50:49 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f209019b5cfe922acdca46b092a1a53eabcba8bec131846b3d14c7948d0cf5a2`  
		Last Modified: Sat, 19 Oct 2024 09:00:51 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5e91d8b2f83cd7d26a801698d55119ca2c6173b57248fa5c67088b90cf37c`  
		Last Modified: Sat, 19 Oct 2024 09:00:52 GMT  
		Size: 3.6 MB (3639240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc69cb958e2bd1b42643336b8876bb885ee75b8d79af934c77dd22e59463d03`  
		Last Modified: Sat, 19 Oct 2024 09:00:53 GMT  
		Size: 29.9 MB (29932427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0e59ac5ffb919bf9f283f890f2411efd1f3e41524565ad06479dffa59f811e`  
		Last Modified: Sat, 19 Oct 2024 09:00:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8` - unknown; unknown

```console
$ docker pull groovy@sha256:4925ae43cb142f27ad38fd6776c84da6025aa03c0c0ba93a2a67ee30c2c0026e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1734afc7576de8e9cab4babfd6968790dbffcbb811033f160f1b070934d3be`

```dockerfile
```

-	Layers:
	-	`sha256:197cc45c0c27727c2b9f7f4e51fe7bf5e0e54f06cbd8de6a5e52cbff268e9b51`  
		Last Modified: Sat, 19 Oct 2024 09:00:52 GMT  
		Size: 4.0 MB (4014072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c09147cd442885d481b3d1cf97bacaef720fe0519ab74b7f1894e0f4cb1741b`  
		Last Modified: Sat, 19 Oct 2024 09:00:51 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:d8665275757833305bfd529cda1a18b959875e76cf8d9607141e0bc997ca0b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176327862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39fda247b8f48387257533ae564d31386c631f076be089ee948d9d9d28a8e72`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Sep 2024 16:23:25 GMT
CMD ["groovysh"]
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 30 Sep 2024 16:23:25 GMT
WORKDIR /home/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_VERSION=4.0.23
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
USER 1000:1000
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dece6d062dc0723f97a73605fb14fdb50c21ad91f9182d5756336b6456a39f`  
		Last Modified: Sat, 19 Oct 2024 05:27:13 GMT  
		Size: 12.8 MB (12828465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28276c4628272fa60453cf1f2a05de4ab0b1a070777df2b86c4d55d436bbf21`  
		Last Modified: Sat, 19 Oct 2024 05:27:15 GMT  
		Size: 102.7 MB (102733224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e72daf18cb8cbdbb2bbbf3491494658a885304fd81d3d2609dc918d91194b7b`  
		Last Modified: Sat, 19 Oct 2024 05:27:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceedd423d59cc486bc9dad535449a46c29156d686af65ead0760ca9fc5c027c`  
		Last Modified: Sat, 19 Oct 2024 05:27:13 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6e6d870fbc507d1254451b1441ebf21ed20b89bb5323c1a8bb0c261e8ddd9a`  
		Last Modified: Sat, 19 Oct 2024 07:28:45 GMT  
		Size: 4.3 KB (4334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00a4bbf063ebaa7759afa010ed7820c830b24ebf737a97d37f58f0f368d66c4`  
		Last Modified: Sat, 19 Oct 2024 07:28:45 GMT  
		Size: 3.5 MB (3468656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b975950f0a86699392fa44a0e7cd7f5eacdca52900e36de62359e57e35964a`  
		Last Modified: Sat, 19 Oct 2024 07:28:46 GMT  
		Size: 29.9 MB (29932426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf115eed26da86bc4a0e7c888f6f8b6335e2b06c5283ecabc586ae0d057577f`  
		Last Modified: Sat, 19 Oct 2024 07:28:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8` - unknown; unknown

```console
$ docker pull groovy@sha256:c2f699e16571f37312a6f0043e8c4e82a358b4c2ddc6d4d30850710784b411fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beca9153aa0cc9a7be39fea8bc04c336edbb8e65c2784c7076a53f79c65ce483`

```dockerfile
```

-	Layers:
	-	`sha256:9a6de6b9a275154c507b58d702122bba8483dfaa202b6db44d871f5bde180ff2`  
		Last Modified: Sat, 19 Oct 2024 07:28:45 GMT  
		Size: 4.0 MB (4010739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef3095429f0f936742e4b3a49c6d6a6761ab5c6764d79d345af27e38dd5b60a`  
		Last Modified: Sat, 19 Oct 2024 07:28:45 GMT  
		Size: 25.1 KB (25100 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8` - linux; ppc64le

```console
$ docker pull groovy@sha256:b9201ef62b6692aa531b45e6f52b4d6d0c422dc8a86d37c7115bc18db7bcc3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184518712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd5e6cfd0b59d9969d343701a1e4f6bf45ba13693229571e788f0ce829b4b8a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Sep 2024 16:23:25 GMT
CMD ["groovysh"]
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 30 Sep 2024 16:23:25 GMT
WORKDIR /home/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_VERSION=4.0.23
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
USER 1000:1000
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334ceb702fdfcb85bc9cfaab00b3806cae756a959247b670cefbabf87a47b2b6`  
		Last Modified: Tue, 17 Sep 2024 01:05:47 GMT  
		Size: 101.1 MB (101079847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd32a1efeedd13b4fd46b3be8b973aefa290a0b75368f31a31fedaffe3672f8`  
		Last Modified: Tue, 17 Sep 2024 01:05:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746fb58333d3760a3857439edea9f2a6bb4e48a6a73ce68ebf98f1dd16365cd9`  
		Last Modified: Tue, 17 Sep 2024 01:05:37 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e530fb7d22db1cd15b79cf8373a2f9681d780c1a07b90723afbae725febd41a4`  
		Last Modified: Tue, 17 Sep 2024 03:36:21 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd3771edd27c9a5d03d8041c0639894c7ae4fd180d78e558fe738865a3dbf13`  
		Last Modified: Tue, 17 Sep 2024 03:36:22 GMT  
		Size: 4.2 MB (4199262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca955d54910b30e7e3a2a416ffe53ef9db841efda880c273f1926e012857dd2`  
		Last Modified: Tue, 01 Oct 2024 01:03:19 GMT  
		Size: 29.9 MB (29932423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b538894a62b19c62b196bc07d9bd988b8c3884c847f89fe6e91f1692bd370b23`  
		Last Modified: Tue, 01 Oct 2024 01:03:18 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8` - unknown; unknown

```console
$ docker pull groovy@sha256:2d94ee32bc578bbbb49ea10bd733010ba5af39d1dd2e356021e1cc0999852564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c430f8fd4b57ae42ef3493f9b62d509e1610b65041ef34cd5dcee01a735897`

```dockerfile
```

-	Layers:
	-	`sha256:16a0c1af59bb90c3d90e74f0decfd85e6518fe4875b34f3087ca223d527cb0a2`  
		Last Modified: Tue, 01 Oct 2024 01:03:18 GMT  
		Size: 4.0 MB (3981861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdbc5af2d1418a73a6ff3734bfaefa37eb36bafdcb8a15a926eae2e722386f4f`  
		Last Modified: Tue, 01 Oct 2024 01:03:18 GMT  
		Size: 25.0 KB (24959 bytes)  
		MIME: application/vnd.in-toto+json
