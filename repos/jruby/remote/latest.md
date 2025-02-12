## `jruby:latest`

```console
$ docker pull jruby@sha256:48acfee5159ef231ce5ec78f5838ed2c7f5777a92afd85c59b3cb3dc27086d9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:latest` - linux; amd64

```console
$ docker pull jruby@sha256:572a19e6d4b169e57a18038e5a2c51206794f21e9bc75f226f88a38384c2c92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135735946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b80830a53d4e68a3e042556a0283b9b81b33d14a593c30f8c994f49c076485c`
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
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:31 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
ENV JRUBY_VERSION=9.4.12.0
# Tue, 11 Feb 2025 20:06:31 GMT
ENV JRUBY_SHA256=05c5d203d6990c92671cc42f57d2fa1c1083bbfd16fa7023dc5848cdb8f0aa2e
# Tue, 11 Feb 2025 20:06:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 20:06:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Feb 2025 20:06:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Feb 2025 20:06:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 20:06:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
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
	-	`sha256:9a91294d1c6d69149ce980161b58b735ba16922f0e1f5d5afb96909152c03fe0`  
		Last Modified: Tue, 11 Feb 2025 22:27:50 GMT  
		Size: 12.4 MB (12439102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d04c4b0ef17d9de173f634e646a198e85bd7e84c8a7c9313f2e48cdbd6f7265`  
		Last Modified: Tue, 11 Feb 2025 22:27:50 GMT  
		Size: 32.4 MB (32371863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e105e3b89d20cb71204db7cbcf95a13bd0490362f6791c71314df5aa6bb7f7`  
		Last Modified: Tue, 11 Feb 2025 22:27:49 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e9f82343e27179638397b248d8170ab691c1ae09625ad83af407279af9ef6f`  
		Last Modified: Tue, 11 Feb 2025 22:27:49 GMT  
		Size: 1.3 MB (1280481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bd861379593fb7bf48bfd53369e2b1855a3f7023ad784f681a5162051cb1cb`  
		Last Modified: Tue, 11 Feb 2025 22:27:50 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:latest` - unknown; unknown

```console
$ docker pull jruby@sha256:94a4b2af6f3d4d70a984ed5227def4d202b9727c2e7bec7fcdeadf12c6f9b3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505f5b1a981c7e3150dd57672acf1db849592ebca3481f60a9bdf5213a5f50a7`

```dockerfile
```

-	Layers:
	-	`sha256:7fb3e15ad43d3c593b1b8ed620c5a520f69f81cae614a19ffb5c1e0169de41c3`  
		Last Modified: Tue, 11 Feb 2025 22:27:49 GMT  
		Size: 5.1 MB (5076212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130df02033a0ee047fd2c104d9a2c0b806f901cdea615c910e90a78d0e548f90`  
		Last Modified: Tue, 11 Feb 2025 22:27:49 GMT  
		Size: 21.2 KB (21170 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:latest` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:554702c69ab8bcc76bffbf547117552bdc75c32f9e0b13cc17a9d5fa2fa15d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131094788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de1b8b907da4dcca120d7a052189a1fa6fdfccc8e7155b1211681a4e1bc889e`
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
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:31 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
ENV JRUBY_VERSION=9.4.12.0
# Tue, 11 Feb 2025 20:06:31 GMT
ENV JRUBY_SHA256=05c5d203d6990c92671cc42f57d2fa1c1083bbfd16fa7023dc5848cdb8f0aa2e
# Tue, 11 Feb 2025 20:06:31 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 20:06:31 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Feb 2025 20:06:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Feb 2025 20:06:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 20:06:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Tue, 11 Feb 2025 20:06:31 GMT
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
	-	`sha256:217057814dde8fb5cef41aac51f75d3836182f444b61bcb8ac40fa45b058aece`  
		Last Modified: Tue, 11 Feb 2025 22:27:35 GMT  
		Size: 10.5 MB (10491313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74c3e4791661ebd20aed5157712e378c463e2a89921cad25f0a43c78da16f5b`  
		Last Modified: Tue, 11 Feb 2025 22:27:36 GMT  
		Size: 32.4 MB (32371884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3b3ed4bc50ad95e13eb0d8317f4e20734d1eaf65577bbc45370528a4a7f14b`  
		Last Modified: Tue, 11 Feb 2025 22:27:34 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff28bba406f5dd977765a03dbb86860bba56b48fe53830d11d964f605b6ae0bc`  
		Last Modified: Tue, 11 Feb 2025 22:27:35 GMT  
		Size: 1.3 MB (1280518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b099ae2dafd2d068f799ed0dfa8c3538a77d1318e5fe3e4071b160c257fb6`  
		Last Modified: Tue, 11 Feb 2025 22:27:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:latest` - unknown; unknown

```console
$ docker pull jruby@sha256:6c55b60e4a5e623ad6cf7b9b156115477fa01873aa1ce8a0af935533212c8065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5072497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704bcc502aa74318ae05652e123b7170aacc196e658f7a622bae0f37e0c44c62`

```dockerfile
```

-	Layers:
	-	`sha256:b77df1163019ff6bcb2047b5025eac8a0473268eb1890d11a4879ee343f8d9fe`  
		Last Modified: Tue, 11 Feb 2025 22:27:35 GMT  
		Size: 5.1 MB (5051079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad2b33fb41936b75ce2fa32f45d7ab7f32db3839ff30713fa4e54537824544d9`  
		Last Modified: Tue, 11 Feb 2025 22:27:34 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.in-toto+json
