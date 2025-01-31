## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:eaa0ba43cf22adb7f0a6ebb0d27b01e1c2bd9c82620aced508c80b6280b20557
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:9e7d5a355bcc6cec24c88256f1b16bdee9d95ce00d2c18a30828e7756855f680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142975214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a8b72cb9c47a3a70618050404e75bb6fa2519aee4ebd536142e7899ac89d0a`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:736914ed604909486ca1980aa7b186717adddcfe25f28e3666e4c1e5946430fa`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 20.3 MB (20251205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6a6fc29da83ffbb26cbf026cc38b929d37f46d627da4435bfbb490407da1a`  
		Last Modified: Fri, 31 Jan 2025 01:29:41 GMT  
		Size: 54.7 MB (54722218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea49627b2936faf3b2b48d821266f89e3471ce8dbeee974c18bfb09103361cbf`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f80771ae776ef9edec8befd7b8a77e535f88b02dd8c9c2b1b99ff58001a3ac3`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e811406e236edbdccbb59dc39b7dd0d8176706f721862d373a5b7a8a91b84411`  
		Last Modified: Fri, 31 Jan 2025 02:15:35 GMT  
		Size: 6.8 MB (6837820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f447aa1e09ec5f5de13255e7e012ffedeff8023abf5a4aab35922b62aaeffb1f`  
		Last Modified: Fri, 31 Jan 2025 02:15:35 GMT  
		Size: 32.4 MB (32369667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be96871cf844354798a6a0fdbdbfab30c1c6a19456e56dec3562a04a1ec5bdb`  
		Last Modified: Fri, 31 Jan 2025 02:15:35 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547578f80a0f9b72a6e863db16319a3c2b18b07aa21c199ae21a85dbc04b1445`  
		Last Modified: Fri, 31 Jan 2025 02:15:35 GMT  
		Size: 1.3 MB (1280466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7efaba3315a97baf27c7cd5c32e4a4d2da10848a25dac3de190ff13f04460f`  
		Last Modified: Fri, 31 Jan 2025 02:15:35 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:2525a75286ea396dea2375d1d951f647a5bf0a208b7f0d3142b1f52a7c790713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635ac4504850a7d36ee14677bc2f0df061884aa49a64d8ce8edf71983a6162d5`

```dockerfile
```

-	Layers:
	-	`sha256:31ccb01baafdd3a5a8e186610618388c798cf6753fac14275a06898064e315a7`  
		Last Modified: Fri, 31 Jan 2025 02:15:35 GMT  
		Size: 5.2 MB (5249816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c6c324b6921409ec316fbf8ed569f32beefc83c8bcc6a0f0d580071ae55b24`  
		Last Modified: Fri, 31 Jan 2025 02:15:34 GMT  
		Size: 20.3 KB (20286 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:bb727d15d74fb90aaa57448dfa572023dbbae594714ffd0499e8068b5a29de10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139350130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0dc3deec362026d599e71c8230010305fb44e85cc63b904b3bb6317e103307`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 29 Jan 2025 18:45:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:7232184dfd406ed5b54e851a280bd7323b4701402a9406613f30c349c9bd4067`  
		Last Modified: Fri, 31 Jan 2025 01:31:05 GMT  
		Size: 53.8 MB (53827736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e7a9d07a5550096d72bd6f01a2e7ac4d6573d0271dfef0d0eb4c25347615f`  
		Last Modified: Fri, 31 Jan 2025 01:31:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fadb503713a054d231da462f0785d432bd94db269c05d507788edfb27bdf64`  
		Last Modified: Fri, 31 Jan 2025 01:31:04 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c4ef1791b675e51365125a2ac585b468878681a2898c1ab43dff2dfa9b2278`  
		Last Modified: Fri, 31 Jan 2025 03:18:09 GMT  
		Size: 5.8 MB (5800989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16263fc340568cfc9683722190ac997d7166ed7257fbbf63e4424a3629d6263e`  
		Last Modified: Fri, 31 Jan 2025 03:18:09 GMT  
		Size: 32.4 MB (32369706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f86f640521f361ba9c45e27be95e1f5707491de8f684502a65f1c27a1e01c`  
		Last Modified: Fri, 31 Jan 2025 03:18:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a64f9f37eaa87a95b5b4a34b4a9942263c07ba2695daa90624ebe6294c03c4d`  
		Last Modified: Fri, 31 Jan 2025 03:18:09 GMT  
		Size: 1.3 MB (1280467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57cda7efe7afb645f15011dac1545334ea4ed6aae6fc38d3a954afaf531f916`  
		Last Modified: Fri, 31 Jan 2025 03:18:09 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:1b2a2f516e0ff98a78e233badbb3b77143b06aeb9e55311b5472a07ca5cad412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88eb3faffdcd6218fe73feb510e81c67ffe725c03bb6580ac953f25ddf5aa823`

```dockerfile
```

-	Layers:
	-	`sha256:828e465f7c13570584f4a167398f7ccb032f25788b40aa2f72ea5b167761b9b7`  
		Last Modified: Fri, 31 Jan 2025 03:18:08 GMT  
		Size: 5.2 MB (5224655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d7ef1844856cbab6e60e0f0616818cdb99aac4f001314951def9e70a14c1d4`  
		Last Modified: Fri, 31 Jan 2025 03:18:08 GMT  
		Size: 20.5 KB (20499 bytes)  
		MIME: application/vnd.in-toto+json
