## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:7acee67c370a0fd0865424b9e2c779e88519f45aa807fd44ce0ae2ae9d420337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:7fc5fc585bc97c82812c3cc63181a5432f6b9f2971f646119b51492e162726c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191458253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e315ae43d50f10bd78e479391bfb9db25479338c57891a4fbafa6a1ce782a0`
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
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 04 Nov 2024 22:12:50 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
ENV JRUBY_VERSION=9.4.9.0
# Mon, 04 Nov 2024 22:12:50 GMT
ENV JRUBY_SHA256=8d64736e66a3c0e1e1ea813b6317219c5d43769e5d06a4417311e2baa8b40ef7
# Mon, 04 Nov 2024 22:12:50 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 22:12:50 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Nov 2024 22:12:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Nov 2024 22:12:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 22:12:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c9980332f7322e535750a2e2683b1ba80418f1b363808c04de3372d7925a18`  
		Last Modified: Thu, 24 Oct 2024 00:57:02 GMT  
		Size: 20.3 MB (20256458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bea8b50cebf78e368754be683c90523bf40ebbf5dec5c4e8b78b7847ce25835`  
		Size: 103.6 MB (103632934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5501e974c1c6bea8706311b47725b152e02c08eed3ad261c03cacadbf0a0721a`  
		Last Modified: Thu, 24 Oct 2024 00:57:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4542904de5b1699510187d785cdf2ff22b77c8fea420357f73c566f7caebdd24`  
		Last Modified: Thu, 24 Oct 2024 00:57:01 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559fde0d72b97502a7a940c45d2cb2b817b08e260c6d6090f173ffca5eaadb95`  
		Last Modified: Mon, 04 Nov 2024 23:07:12 GMT  
		Size: 6.9 MB (6855430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62779a9f1a60d90b5303b1f219497e93675323dc48f15b8ac19cb48134214b7d`  
		Last Modified: Mon, 04 Nov 2024 23:07:13 GMT  
		Size: 31.9 MB (31927516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6919fb56c8e4a63bbf130b5377c6e2bda120fa3f36a8cf90c7eb460dab311112`  
		Last Modified: Mon, 04 Nov 2024 23:07:12 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb26732a6e29ae21638dbcbdd45976f17f8a40717c34fa4f0154c0ffbb34b10`  
		Last Modified: Mon, 04 Nov 2024 23:07:12 GMT  
		Size: 1.3 MB (1272079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc81ce1f589a9b01e24542becb371ed746845e733083ee79c038a5b07ff7b8f`  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:a7b7b5a67935452218fe3af72ca2f83270dd1aa674f6a8ea1ce7bd04e7545039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da9b83d79e948385cca6105c069e78ed31ee07270ba111d3c42b0bc305ac332`

```dockerfile
```

-	Layers:
	-	`sha256:35f846bf55fdddeaeeef1d0275a8482f529dbebbc39d1cc65b2dd8208f0d3e0a`  
		Last Modified: Mon, 04 Nov 2024 23:07:12 GMT  
		Size: 5.3 MB (5257400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60c52b2f0937c723a8b79bf05f096579eda5a44c5a38282fe7c249f3686fbba9`  
		Last Modified: Mon, 04 Nov 2024 23:07:11 GMT  
		Size: 20.3 KB (20281 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:e6736477144d955ef3fbbe2e82a83f0825c25c591f57d252724b09170a9c10e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187822665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79120d4c9c2e609f5505854ce6ffd6ffeda232be0d10c7edff040b3963704f4`
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
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 04 Nov 2024 22:12:50 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
ENV JRUBY_VERSION=9.4.9.0
# Mon, 04 Nov 2024 22:12:50 GMT
ENV JRUBY_SHA256=8d64736e66a3c0e1e1ea813b6317219c5d43769e5d06a4417311e2baa8b40ef7
# Mon, 04 Nov 2024 22:12:50 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 22:12:50 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Nov 2024 22:12:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Nov 2024 22:12:50 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 22:12:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Mon, 04 Nov 2024 22:12:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7944fa14982850a5d6fef396e75bb75cff1a66cd0eb74db10ed75ba31d11c024`  
		Last Modified: Thu, 24 Oct 2024 00:56:58 GMT  
		Size: 20.1 MB (20093942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab479ff4fa9a437cf1c7d951a56a838896da906af63fccbd9a368b74bdae31`  
		Last Modified: Thu, 24 Oct 2024 00:56:59 GMT  
		Size: 102.7 MB (102746969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83210471bf69c505ebd872a23cd75436eb31188b51e3aca2e42a2fa66fba31c0`  
		Last Modified: Thu, 24 Oct 2024 00:56:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29010567a099048d56cd79fe6a4013e1e91bbc31b0752c3bb6c5ecae1a90bcfa`  
		Last Modified: Thu, 24 Oct 2024 00:56:57 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0fd00613e2f866e1f22140c5697f90d436e7daa86dd96e1415ec59bac7efb`  
		Size: 5.8 MB (5805494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fea4798130ea09278b74b6417db803fb2f337bdcef22d7a0055c42c3a82f266`  
		Last Modified: Mon, 04 Nov 2024 23:37:36 GMT  
		Size: 31.9 MB (31927591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48938267fde6a4b89cfe9fe7b0c0828b62a0c8ffe60693ba3f72abbaaee94e77`  
		Last Modified: Mon, 04 Nov 2024 23:37:34 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db357ffad08412da1dc30d391217a05ba8b3133d12a73d2e395cf71acfe6e18e`  
		Last Modified: Mon, 04 Nov 2024 23:37:35 GMT  
		Size: 1.3 MB (1272065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236b447860812ecc2d780f8466b3ad905ac7081cbf87528ee590da77afed9ef`  
		Last Modified: Mon, 04 Nov 2024 23:37:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:c3a9f4a8b5af1d0ce196d141152d63304b6b024ad9c7d7e68678f714c43faab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c77b4dd5333f1f68aa007a7fa2c5617651dc4f9bddc2f0e1836f470fef8f8ec`

```dockerfile
```

-	Layers:
	-	`sha256:87e187fcee44189472777da0c94a495d2f57001fbf855ff4affb305c73a34d3b`  
		Last Modified: Mon, 04 Nov 2024 23:37:35 GMT  
		Size: 5.2 MB (5230327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1472ff4bad61b9b877ef85d1efdba30196e893941988c9f608283a2aa44b3aaf`  
		Last Modified: Mon, 04 Nov 2024 23:37:34 GMT  
		Size: 20.5 KB (20493 bytes)  
		MIME: application/vnd.in-toto+json
