## `jruby:latest`

```console
$ docker pull jruby@sha256:7f024543ef1a0ff6983b4b459e5ed4d8880b0c152b3d4a707933d2b56b301218
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:latest` - linux; amd64

```console
$ docker pull jruby@sha256:1554ae0f2a6b80fb90f476c204d039e2406ba1c5b33b7a22a916bae057845860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130132563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf252e2d92eecc524824b4eb72cbebd894d7a73204f8d852eb8a139f00130d7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 29 Jan 2025 18:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 18:45:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 18:45:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Jan 2025 18:45:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 29 Jan 2025 18:45:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Jan 2025 18:45:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENV JRUBY_VERSION=9.4.11.0
# Wed, 29 Jan 2025 18:45:12 GMT
ENV JRUBY_SHA256=cf4067bdc3a6ab518c786588e2486adc047b9cea0b96a43218b03ac651d26e11
# Wed, 29 Jan 2025 18:45:12 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 18:45:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 29 Jan 2025 18:45:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 29 Jan 2025 18:45:12 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 18:45:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58623e1650ebe4dbc9a54be169a098c559ca74062678f7305c1b29bc01c14ee2`  
		Last Modified: Fri, 31 Jan 2025 01:29:41 GMT  
		Size: 20.3 MB (20251206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538260ff9dfb998d33d883205b277cf302568a2ec180a3ca9339a7c1d060f332`  
		Last Modified: Fri, 31 Jan 2025 01:29:41 GMT  
		Size: 41.9 MB (41879483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ba2f973c3fac81aa9dbe4d14b2224f613adb1d5a317fdcf46567d1657a394b`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec21a3487de493e79717b1f5f20d7e07ce22d0bea68828000a9221b3affa81f`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d93879ef0ab2157249327f744ebd79f559482d71346f21bc749d7062ee50f`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 6.8 MB (6837900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4716820b282910c3157e57c038a617e5cdf860ae347aef38502386987e5d712`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 32.4 MB (32369664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828c853c6b545d884db5f156fd1a498eaf5a9eaa43812c14eb62677b62871c77`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc03f9e7efcab0c6519115116cf7db6e9f88b7e739a97af6b05aaeba8c8db81`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 1.3 MB (1280501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5cc04ca66503bff0e4e457ea1cbd51686425f9658aa15251a184d9b522decd`  
		Last Modified: Fri, 31 Jan 2025 02:12:00 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:latest` - unknown; unknown

```console
$ docker pull jruby@sha256:183fc20333988bda9692efffaa75a81b214e3fbc25bb2181498fbc1353c228b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5096209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce05bfe70aa69db4bd5386d4649f7aae5731d80091e94d2c57f5d960fb1fb54`

```dockerfile
```

-	Layers:
	-	`sha256:0c7f3d36104193ae05418817da25afc57da085999e8c6d69f149a3738adfd44b`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 5.1 MB (5075044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df52c527c3fc1fe14417bb52d884db381cd693794b4b13dfe660b972c125e6e`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 21.2 KB (21165 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:latest` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:7ca18cf9b1d640fd3d5542652f0602e7f86995676ae1295ee6d758838338647c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126402252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbd4ad9ed0247252de840fb271de16d63526fd82c8eafd3b3c477729115fafa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 29 Jan 2025 18:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 18:45:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 18:45:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Jan 2025 18:45:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 29 Jan 2025 18:45:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Jan 2025 18:45:12 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENV JRUBY_VERSION=9.4.11.0
# Wed, 29 Jan 2025 18:45:12 GMT
ENV JRUBY_SHA256=cf4067bdc3a6ab518c786588e2486adc047b9cea0b96a43218b03ac651d26e11
# Wed, 29 Jan 2025 18:45:12 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 18:45:12 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 29 Jan 2025 18:45:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 29 Jan 2025 18:45:12 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 18:45:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec110cdef34c6829c2f088dd32067784ed2dd806d4657a74f60a167560815080`  
		Last Modified: Fri, 31 Jan 2025 01:33:08 GMT  
		Size: 40.9 MB (40879861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f74fd78af2433d1304ba76f2dc5fe0aeaa7e26b77e8deeacc09b3729f3d709`  
		Last Modified: Fri, 31 Jan 2025 01:33:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4a0076d0f6e9da1387fe0c1bde2ecd400d764f61a18f1f37618d6de067b88`  
		Last Modified: Fri, 31 Jan 2025 01:33:07 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e4d2dc9b8fedaac8ca2d52987a659815f4bf0bb20e7a6799be81d2814ee78c`  
		Last Modified: Fri, 31 Jan 2025 03:17:28 GMT  
		Size: 5.8 MB (5800968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c934a12134bdb10e3e3b1192d310a300c3568da1dc8ba8c4ed40ce968a730150`  
		Last Modified: Fri, 31 Jan 2025 03:17:34 GMT  
		Size: 32.4 MB (32369717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf3172abc1e3a91e1633a9eeddd19154ad391e1cf5412cf479a240790e26c2`  
		Last Modified: Fri, 31 Jan 2025 03:17:28 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae19ec9875c163f5415d9ae7c03c354cadb90f5e314d5fb8c82e197beb632f3d`  
		Last Modified: Fri, 31 Jan 2025 03:17:28 GMT  
		Size: 1.3 MB (1280497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aea344d9b966d0502259b24ed4c9fd26523ca356f0f1d8aae4bb0b8c2318b2`  
		Last Modified: Fri, 31 Jan 2025 03:17:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:latest` - unknown; unknown

```console
$ docker pull jruby@sha256:96d5493c2be7cbb78c940f5f23a76ab0752cad137a02d8bc590eef6f48a5a3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a87b10977ad6ad10516c0cab1918049057bc9bc025fc29714a810ec0348d92`

```dockerfile
```

-	Layers:
	-	`sha256:0d101775c31dd02d13c0a72632bb14d982f0b434c0e9056571891654cee9ce63`  
		Last Modified: Fri, 31 Jan 2025 03:17:28 GMT  
		Size: 5.0 MB (5049911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a61980aab137bf490123d10136b00f044908a9445f1ff2fc62501cfbef8ff539`  
		Last Modified: Fri, 31 Jan 2025 03:17:27 GMT  
		Size: 21.4 KB (21413 bytes)  
		MIME: application/vnd.in-toto+json
