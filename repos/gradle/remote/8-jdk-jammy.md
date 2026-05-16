## `gradle:8-jdk-jammy`

```console
$ docker pull gradle@sha256:86d445fba87bc2fb8b141081e0051c6db2b3f54b08dcb6a9d84746b0808d33c0
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

### `gradle:8-jdk-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:d08048769d3e748fe279695ab50fc48d61bf8b8f6a1c4b8e9312e2e14ff649e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.5 MB (397538156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fe23aa993d063a20bcc8de1696450f5176d751377ff15314d948b77492f952`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:15:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:15:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:15:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:15:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:15:59 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:16:07 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:43:49 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:43:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:43:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:43:49 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:43:49 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:44:00 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:44:00 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 15 May 2026 21:44:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 15 May 2026 21:44:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:44:03 GMT
USER gradle
# Fri, 15 May 2026 21:44:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:44:03 GMT
USER root
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac0cedbe7243c29e62f2edc257a1b63f1b14230678962e5eaa67199274ff4bc`  
		Last Modified: Fri, 15 May 2026 21:16:25 GMT  
		Size: 20.7 MB (20696796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6525f2e444f155b1052b82e6b57e2c0fd233969b0a16f8e9844714f79c640b64`  
		Last Modified: Fri, 15 May 2026 21:16:28 GMT  
		Size: 158.2 MB (158171523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ffccb56d90e1b9f8366c7b0436c5e01955654355fed3f2cb3a72d476fe59a`  
		Last Modified: Fri, 15 May 2026 21:16:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b8728c87d0a3b82e6130f362030fc722aac7906e1fe98855888dcc8d06d6d1`  
		Last Modified: Fri, 15 May 2026 21:16:24 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88c9fa145b27ac8d53c09bbe674805d0e88168260b9405274feeb9fa5735182`  
		Last Modified: Fri, 15 May 2026 21:44:22 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98ba5a6e5c9c3926c597b1e22cbcad8e94bed50a78797a52b2b78e5347aa36`  
		Last Modified: Fri, 15 May 2026 21:44:25 GMT  
		Size: 50.8 MB (50802941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c452090283a7f1a02b9662657a08c1a5b4966cf0689bc6ecf09fd4bffe6b1f`  
		Last Modified: Fri, 15 May 2026 21:44:27 GMT  
		Size: 138.1 MB (138068533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c44a429431ee28b0d2733f5bf20e31103591611aa756af00c129a47a56fb5ec`  
		Last Modified: Fri, 15 May 2026 21:44:22 GMT  
		Size: 54.9 KB (54893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:6a02b38f8472898bc998106108526ae941f0a60d75b925d6ecade04e437fb7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7891258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d169369000e074f84d4e60a94c89281f38bdad7318715cb13e4e478d3890381b`

```dockerfile
```

-	Layers:
	-	`sha256:a07cb72e15b3234fe287687ed3be3a9c035a502d86a5ba7b42b90ef13805c121`  
		Last Modified: Fri, 15 May 2026 21:44:23 GMT  
		Size: 7.9 MB (7866248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:106a65e7e7a3e730d920f434b3c6cf2458abbec6fc7db5509ecefe0c7320f438`  
		Last Modified: Fri, 15 May 2026 21:44:22 GMT  
		Size: 25.0 KB (25010 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f0254b90b69f0d15963d3ea4c75a3737cb2ceb9fc90bea98ff5f63bca1a583f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.7 MB (394692737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e9a9bbb8ef02317b6c6d364201e761e978f3dea8d4e9ddd74a3e1f0c68ed0a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:16:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:16:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:16:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:16:27 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:16:36 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:44:04 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:44:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:44:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:44:04 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:44:04 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:44:23 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:44:23 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 15 May 2026 21:44:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 15 May 2026 21:44:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:44:26 GMT
USER gradle
# Fri, 15 May 2026 21:44:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:44:26 GMT
USER root
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d852f6dfaad8a40cfaf273f633be26f9a5b8f11e61a91f52b4dfbaccc76b03`  
		Last Modified: Fri, 15 May 2026 21:16:54 GMT  
		Size: 22.1 MB (22110098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b837f585294a258d69b2bb758d9e5316397fb520239e8d38510198ad590a31`  
		Last Modified: Fri, 15 May 2026 21:16:57 GMT  
		Size: 156.5 MB (156473207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0884f5611bcde615b81d8325cb0901219ade1e174f147b636d7414626b5dbff`  
		Last Modified: Fri, 15 May 2026 21:16:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf605f7226c61411efd4513da5e0de7a725ebfb0196db3e5a4bc226e51eca5b9`  
		Last Modified: Fri, 15 May 2026 21:16:53 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cd59e412bdd3c219b64b0dd4f773be345a1631b7b82f59c12aa3b23a930c39`  
		Last Modified: Fri, 15 May 2026 21:44:45 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c172f71bcf0bb0c6f3d98d713611ab63ba64966b87887c49f53fa7a9231042`  
		Last Modified: Fri, 15 May 2026 21:44:47 GMT  
		Size: 50.4 MB (50367953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc2b67ae13ce757fc6a45b154dbfc9639fc011f19667235d4fa352c1f522d13`  
		Last Modified: Fri, 15 May 2026 21:44:49 GMT  
		Size: 138.1 MB (138068536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ece2ad4816a4bc9de999cc8667448e3a18ef22bfcfcd58d4d40f342a10e77`  
		Last Modified: Fri, 15 May 2026 21:44:45 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:992822da2ee7b53bf6866cbd2b1175dbf6f651e903dad128ea8d25f6160915aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7993155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b465892a20613313e9f4720f57b272cc8da5e6d6ce8b79ba210961bd0d33ea4`

```dockerfile
```

-	Layers:
	-	`sha256:e58ad06a1b0bc54dbea7d283e0dcf2419e7ea9abe30d313e28c4995a5e87a0d8`  
		Last Modified: Fri, 15 May 2026 21:44:46 GMT  
		Size: 8.0 MB (7967935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d5cb1766d4dc8b118e787c38e819eeb0cba90ba1fc17b3300cab45bf269a7f`  
		Last Modified: Fri, 15 May 2026 21:44:45 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:db8168ddc6b4862dd68d2a660ef5b6065d18b5fd518582198cdff50f4affb253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.5 MB (408476332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7b0a21e3e7aa62e40d1e0ae010b21af1c6b7a9f23d40fac6c156f56082ceb5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:12:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:12:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:12:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:12:31 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:12:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:12:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:12:59 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:55:25 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:55:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:55:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:55:25 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:55:26 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:56:09 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:56:09 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 15 May 2026 21:56:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 15 May 2026 21:57:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:57:28 GMT
USER gradle
# Fri, 15 May 2026 21:57:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:57:30 GMT
USER root
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ba0627ad64b0a6b1ebf88e18bcc537d7ccaf8ddfb659f50480d115f4660520`  
		Last Modified: Fri, 15 May 2026 21:13:21 GMT  
		Size: 22.6 MB (22589674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702738293916273b91529175215f49625037bc3b44904ef262ce275bd11af5c`  
		Last Modified: Fri, 15 May 2026 21:13:37 GMT  
		Size: 158.3 MB (158345595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6904e6c39634fd6c9f2c2d969ec931cd48321b0f92f325e115123c57b40df6`  
		Last Modified: Fri, 15 May 2026 21:13:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92c36188549b1808c4059d067b329e99a24ea6b0dae89afec63536dc23a8ee6`  
		Last Modified: Fri, 15 May 2026 21:13:33 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672bcb790dc95bcf5ca5e204e1c0a2216203161b806806e44bbe2969014e6c5e`  
		Last Modified: Fri, 15 May 2026 21:56:57 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8c87d40dde67d8ac31dabb8d3b72c8c2a8d30cf39fc5bc1793002ae5f52a88`  
		Last Modified: Fri, 15 May 2026 21:57:00 GMT  
		Size: 54.8 MB (54783997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74158bd6e3dc7eb359c4917bc20775ccf4800708da1493c5e1a37f4e56e58e`  
		Last Modified: Fri, 15 May 2026 21:58:09 GMT  
		Size: 138.1 MB (138068550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770037f680645a470357042c8fa351e3c0c52dbed2c7a74d50cb47d1dec4055`  
		Last Modified: Fri, 15 May 2026 21:58:05 GMT  
		Size: 35.0 KB (35010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:553784b841368041be636b4c39c644d83377fbb75d3f1f15c80eaf2c198f8701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7922220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e743b9c4769012fef8130971cab7deffd2f264c258f7713700a26e4c9e35687`

```dockerfile
```

-	Layers:
	-	`sha256:389168aa72868e76564860a4ba59e99609f69c5e70ed9b9159b4f5c62ad3a809`  
		Last Modified: Fri, 15 May 2026 21:58:05 GMT  
		Size: 7.9 MB (7897128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f504fe2b32fa035787409fdc4cdc6bc2415308191a46d1f31eedc45d6d9e94f`  
		Last Modified: Fri, 15 May 2026 21:58:05 GMT  
		Size: 25.1 KB (25092 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:107aca7c327e279e745ecbb99971959e77dcaa5d0b3afec0afa9ce4b5aedc0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.6 MB (384612607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ccc111e80ccb15b128ebc684e377b788c3c109532bd1f4f96e948fe27480a8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:14:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:14:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:14:45 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:14:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:14:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:14:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:14:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:14:57 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:41:11 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:41:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:41:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:41:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:41:11 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:41:28 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:41:28 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 15 May 2026 21:41:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 15 May 2026 21:41:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:41:32 GMT
USER gradle
# Fri, 15 May 2026 21:41:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:41:32 GMT
USER root
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc011ea20f5533ff592eac2ed518b149dea0f11700e76aab9c45da02157551`  
		Last Modified: Fri, 15 May 2026 21:15:37 GMT  
		Size: 20.4 MB (20419204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d193b91e22f6d1d4fe6ec1bcb1aa930251596b1f1632089a2fdf2872019ebd`  
		Last Modified: Fri, 15 May 2026 21:15:40 GMT  
		Size: 147.4 MB (147398675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf6c8b9a3e0104a5814f417d75320324610a7f2012b304342a549e6a23523c2`  
		Last Modified: Fri, 15 May 2026 21:15:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb5d0d7cbcadf01b0b13fa7805e7f9852101821994e87d95c3a4105dd65b9fa`  
		Last Modified: Fri, 15 May 2026 21:15:36 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26981112ff435556470c8c4e4d72e536dd0b20dbd00aa0427685ec4b0ba8d2e`  
		Last Modified: Fri, 15 May 2026 21:42:04 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668673bb61eba680d41c718139497ddbde51626e2d1b8f42729ee9240c508f15`  
		Last Modified: Fri, 15 May 2026 21:42:08 GMT  
		Size: 50.5 MB (50482106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052884ec4f73625a37a1a485126a939e69aef68946f0be46ddf4a5ab82ed5d82`  
		Last Modified: Fri, 15 May 2026 21:42:07 GMT  
		Size: 138.1 MB (138068536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b8881efca2ab86fed9b1c244980a7e9b009824ee85346e101dc1651d103f61`  
		Last Modified: Fri, 15 May 2026 21:42:04 GMT  
		Size: 35.0 KB (34995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:8b6c6511f6f63381789c501e947e62bcb67fc209740be181356402932230fe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7814940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373a6f46172f0edefcda1f54f00f556db4b9981933d731d247c0214e5c41886b`

```dockerfile
```

-	Layers:
	-	`sha256:de78f72ef2398f5289eaaf1de36dcdaa4f8a9ad79477a0618980cd637d9a6990`  
		Last Modified: Fri, 15 May 2026 21:42:04 GMT  
		Size: 7.8 MB (7789928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f876ca0bb0c63e0d34074c0bbbb0c6fbb405a8035062462b98512f2c5681cf`  
		Last Modified: Fri, 15 May 2026 21:42:04 GMT  
		Size: 25.0 KB (25012 bytes)  
		MIME: application/vnd.in-toto+json
