## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:629d9c2cd98528fa11b4fc2c8abc575657263ad7ae2c54e92a3d8ea4e6423998
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:9-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:4ec4dd41294f634395a9a9ebf39c986b6c7a75995f500931cc683906e597adfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191357996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42dd48e1fc4ac631d450c8c4fb283aa2dc6b2f8d82fed47a6be24ec7cf509204`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Jul 2024 17:37:28 GMT
ARG RELEASE
# Tue, 02 Jul 2024 17:37:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Jul 2024 17:37:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Jul 2024 17:37:28 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 02 Jul 2024 17:37:28 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 02 Jul 2024 17:37:28 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jul 2024 17:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 17:37:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jul 2024 17:37:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JRUBY_VERSION=9.4.8.0
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JRUBY_SHA256=347b6692bd9c91c480a45af25ce88d77be8b6e4ac4a77bc94870f2c5b54bc929
# Tue, 02 Jul 2024 17:37:28 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 17:37:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 02 Jul 2024 17:37:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 02 Jul 2024 17:37:28 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 17:37:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
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
		Last Modified: Thu, 24 Oct 2024 00:57:04 GMT  
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
	-	`sha256:e8ff8ab7ad7c9397bdc3e39336c91feba5e6cb597b786ba1a13e634d1134a715`  
		Last Modified: Thu, 24 Oct 2024 01:54:29 GMT  
		Size: 6.8 MB (6842051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca354c0df7b76e1e211eb22e9bcd3853b8a0b735c620a076794765212414048c`  
		Last Modified: Thu, 24 Oct 2024 01:54:29 GMT  
		Size: 31.9 MB (31864535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dbbc923fbf23f33299ecb38aad980c886859718ccc44c2a5405818a92ff8b`  
		Last Modified: Thu, 24 Oct 2024 01:54:28 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e7761ce9679a9d385a062e57a98bad80c0a66d97a96d1beedbfad9ecb68693`  
		Last Modified: Thu, 24 Oct 2024 01:54:29 GMT  
		Size: 1.2 MB (1248182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40eabc55eb71250d91460c0b6544d07065d8e3bb9bce4b4b6552a06f562dba21`  
		Last Modified: Thu, 24 Oct 2024 01:54:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk8` - unknown; unknown

```console
$ docker pull jruby@sha256:ca9c1fcf741fb6ccb0e0ebc97d293dda4a057ebbe5deaf3ffbe100d54529da1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec16781a96d73e17b1bcc1c24d54cc7bc4291cc3549b097946cecccad7d72d7`

```dockerfile
```

-	Layers:
	-	`sha256:9fde76e81947eb1d007aa31e08ad05b985ecacdb7aa58d615fb49c8e23ac689e`  
		Last Modified: Thu, 24 Oct 2024 01:54:28 GMT  
		Size: 5.3 MB (5254904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71012b31f4cd1c4349d003e0a57503a1dc25b96fc1ce70d2f333fbbc73c3806`  
		Last Modified: Thu, 24 Oct 2024 01:54:28 GMT  
		Size: 20.3 KB (20281 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:9-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:07fb06816f5584ae52bab9b21257d822cca69ea6334faae525e5bcc33b8443a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187735711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cafcc868a7f0ab196b20caf9a94bd16ba985978229b4a898bfcd736bf9e4e77`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 Jul 2024 17:37:28 GMT
ARG RELEASE
# Tue, 02 Jul 2024 17:37:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Jul 2024 17:37:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Jul 2024 17:37:28 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 02 Jul 2024 17:37:28 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 02 Jul 2024 17:37:28 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jul 2024 17:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 17:37:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jul 2024 17:37:28 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JRUBY_VERSION=9.4.8.0
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JRUBY_SHA256=347b6692bd9c91c480a45af25ce88d77be8b6e4ac4a77bc94870f2c5b54bc929
# Tue, 02 Jul 2024 17:37:28 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 17:37:28 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 02 Jul 2024 17:37:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 02 Jul 2024 17:37:28 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 17:37:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
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
		Last Modified: Thu, 24 Oct 2024 03:17:55 GMT  
		Size: 5.8 MB (5805494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8887a61a444e6bae820b95c427856a003b50c38aed6d5ec8c0bd3aee1f192781`  
		Last Modified: Thu, 24 Oct 2024 03:17:56 GMT  
		Size: 31.9 MB (31864532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b20448c5e472061adede14592dd7efcc78fb9ef02615c99f774a1d3394883e`  
		Last Modified: Thu, 24 Oct 2024 03:17:55 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132e16c754fcba37870e7ca29bd388ea819b70363668682cd9911279837c4826`  
		Last Modified: Thu, 24 Oct 2024 03:17:55 GMT  
		Size: 1.2 MB (1248171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04330dc0af0eef42b426afb196670e46f61999e40366d76aa2d96c53b3392571`  
		Last Modified: Thu, 24 Oct 2024 03:17:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk8` - unknown; unknown

```console
$ docker pull jruby@sha256:b02e0ff66afc44b8015e19c7356ded844dbb281268a9e0ad67e20151fabfacb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab25146e00ae00c3771f50bea76e625a9ba644d38a250ac5bac0f7a3494d710`

```dockerfile
```

-	Layers:
	-	`sha256:c28a82d0d578fcf0ca3f98945310d544d3dd8f202ebf36fa8df3ac693686b84d`  
		Last Modified: Thu, 24 Oct 2024 03:17:55 GMT  
		Size: 5.2 MB (5227831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a07674713de199d75e47027350be4122f49ec1cd996c40ec4d61facb8ec66420`  
		Last Modified: Thu, 24 Oct 2024 03:17:55 GMT  
		Size: 20.5 KB (20493 bytes)  
		MIME: application/vnd.in-toto+json
