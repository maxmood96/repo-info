## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:93cbc34ce8082bb8ced16628f9c06245ca2e6fb484ba3d9d1392e7b0999695f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:a9ed6ff3df59e073b6e358b6a2be5755a20642ab2accffad215ed700c1ee8280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148614805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341e3ec6cbce9a9ebb0d282b4ef0ea31dba5885b0d8218f566515c611dc65f76`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Jun 2025 19:07:04 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
ENV JRUBY_VERSION=9.4.13.0
# Tue, 10 Jun 2025 19:07:04 GMT
ENV JRUBY_SHA256=226d9c3a2e332f8f249838f96c20e87e0df2b9a464a11477b47be6dafb66412c
# Tue, 10 Jun 2025 19:07:04 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 19:07:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 10 Jun 2025 19:07:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 10 Jun 2025 19:07:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 19:07:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20980e7d78f727e72412bce891dc672054ede0e7266aa671206c81efba9e2c2`  
		Last Modified: Thu, 08 May 2025 17:14:38 GMT  
		Size: 20.3 MB (20260437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778ef8878677f723d33d7e7a3a6921f72123b78dd518f1202d8f5bfd7dd6e8c`  
		Last Modified: Thu, 08 May 2025 17:14:41 GMT  
		Size: 54.7 MB (54721859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbc5a2fd6ab8c3df0b9b9e316280ada9c3cfbfade63bf4bf37fc926033a0362`  
		Last Modified: Thu, 08 May 2025 17:14:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Thu, 08 May 2025 17:14:37 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51824c40ae602dbc8acf66b952fb4ce461fddac1e80345a8bad7c719d52cc572`  
		Last Modified: Tue, 10 Jun 2025 22:38:37 GMT  
		Size: 12.4 MB (12422509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e62e0ee87ff8c69d6c4fbd93b54da1ff69104b491ecfe1afb645ca62873d95d`  
		Last Modified: Tue, 10 Jun 2025 22:38:45 GMT  
		Size: 32.4 MB (32401251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c478f0089f18bf63b602adf04623162902ea86cdd86436222f131455448fe0a4`  
		Last Modified: Tue, 10 Jun 2025 21:09:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2185a5e3d6f3c7ff909ff0e5a2300999f56929e2b13fee122a0690d64416068`  
		Last Modified: Tue, 10 Jun 2025 21:16:04 GMT  
		Size: 1.3 MB (1295582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfd4e9d917fc570601a27dbed97b9d41cfda5b15facf0b57a23547b94e48d06`  
		Last Modified: Tue, 10 Jun 2025 21:16:23 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:0bc3ab654878880033e93120adcd16064df24202857eb9505650ce60049f0659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f11a11d3285f271832c7bd80389b78b83394dce12a26dd9418d845fad60bdbc`

```dockerfile
```

-	Layers:
	-	`sha256:54ab3dad8c973ca7b1c2cd8740ab8252e4e880d09bc30e70fe95d5b7bb4802b8`  
		Last Modified: Tue, 10 Jun 2025 21:59:41 GMT  
		Size: 5.4 MB (5435043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbe014560ed1232e13432cb0eadf33f6b738b7a0ab7ec4ac327eeb5310766bb`  
		Last Modified: Tue, 10 Jun 2025 21:59:42 GMT  
		Size: 20.3 KB (20292 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:aa60c855bb813b064844b1d6d265cfb1c6bd0f209c225e05562e2997d3df947b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144077629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e2388e9104795d70d47c34d72d48d60196f637d6b43f4b9bfec4f0ec628044`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Jun 2025 19:07:04 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
ENV JRUBY_VERSION=9.4.13.0
# Tue, 10 Jun 2025 19:07:04 GMT
ENV JRUBY_SHA256=226d9c3a2e332f8f249838f96c20e87e0df2b9a464a11477b47be6dafb66412c
# Tue, 10 Jun 2025 19:07:04 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 19:07:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 10 Jun 2025 19:07:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 10 Jun 2025 19:07:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 19:07:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Tue, 10 Jun 2025 19:07:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c00c0b5c103330a238db0e07c88322ec3b801e044907a6ee5bf54251f50252`  
		Last Modified: Thu, 08 May 2025 17:16:38 GMT  
		Size: 53.8 MB (53834692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6602bf4e0b42d138670f1641a397f020adb9041bace6008882cc98ad0595ea8`  
		Last Modified: Thu, 08 May 2025 17:16:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4675a7cf7687748bf9b99626829b1724a4c405d81d66ddb19b67b51cc2d34c`  
		Last Modified: Thu, 08 May 2025 17:16:44 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d7c6780204a2ffbc34da3112996c57d68c2830e56ef9ba65b636b5d0a85018`  
		Last Modified: Mon, 09 Jun 2025 09:21:26 GMT  
		Size: 10.5 MB (10472672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cb749f1b269873a77e49df0d5d88c2e95365207ae32d0ad79c7440db23927`  
		Last Modified: Tue, 10 Jun 2025 21:09:05 GMT  
		Size: 32.4 MB (32401288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c478f0089f18bf63b602adf04623162902ea86cdd86436222f131455448fe0a4`  
		Last Modified: Tue, 10 Jun 2025 21:09:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f27a460b19cb5b896921b64ff1a5c26381577c073f1bd31ce27f78a22252d5a`  
		Last Modified: Tue, 10 Jun 2025 21:09:03 GMT  
		Size: 1.3 MB (1295565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8249768e95ab21b550a54653c90a5effa5d9284952fecf5644ae84cb1397b8`  
		Last Modified: Tue, 10 Jun 2025 21:09:03 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:8562a4481516f8dbf4cee55ed74b73a46874fb0cd1907ab6e7e397462f9fc10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5428510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b0c3646ef9783c21fb4e8ee9fe1cfc563e5896131eb9364e9904210268dd34`

```dockerfile
```

-	Layers:
	-	`sha256:0eef1e32e296a7795bef305cc35547c5e978104884a038814994d98293873b5b`  
		Last Modified: Tue, 10 Jun 2025 21:59:47 GMT  
		Size: 5.4 MB (5408006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5b11042a090b7f2ae1b961b3272c20ee22702a76752259a84253dd3aee77e31`  
		Last Modified: Tue, 10 Jun 2025 21:59:48 GMT  
		Size: 20.5 KB (20504 bytes)  
		MIME: application/vnd.in-toto+json
