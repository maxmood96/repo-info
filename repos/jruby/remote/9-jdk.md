## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:07b8ead7c7286cb908c24a076192738587b99086f410e617125cb75b45665263
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:b82d16fc56142b76ccef8e8a0c09f92d723f0618c57bf41e647c18a7e71686a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139610220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e1a253131e52559fa8f2d48caa8f56d5c1e8caa34abf4deb924196132ce1c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 28 Aug 2025 20:58:57 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
ENV JRUBY_VERSION=9.4.14.0
# Thu, 28 Aug 2025 20:58:57 GMT
ENV JRUBY_SHA256=7ea2be8d0c5989714c795b4544492bf9941c9576e7a78f593a19c85567bc0452
# Thu, 28 Aug 2025 20:58:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 20:58:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Aug 2025 20:58:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Aug 2025 20:58:57 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 20:58:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a709a4c5dc147d0dac56b479fe04718d888d000dd1c42feba248e3d60b39b4`  
		Last Modified: Mon, 01 Sep 2025 23:08:39 GMT  
		Size: 16.2 MB (16150649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95c312878d8a9651cb2180bc59a7b370eeaba6bf39b256bf52ddd1e564dcedb`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 54.7 MB (54739755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bfa90526ba5336f8931786935649c2c330e55139d7a8bdb561b53e61921c83`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cf2fabc85e131f5fb6ebb551a8acf47df0ec4e256b11b16a91c86ed67ac4b1`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5caa5972ef5f9e69ce1ee5dcb677d8a6543154475f592d488e84d4dcaeb824`  
		Last Modified: Tue, 02 Sep 2025 01:46:45 GMT  
		Size: 5.6 MB (5590657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52868976681e6c2672b99ed7386e942bf2dba6522a5411d5e2f6a50cb9daaabb`  
		Last Modified: Tue, 02 Sep 2025 01:46:49 GMT  
		Size: 32.3 MB (32293872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d4b26b409634b3426e4b10b671f8f33a0df97b4030ff96e459767a55b1e311`  
		Last Modified: Tue, 02 Sep 2025 01:36:57 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59eb228c734eaf4a17140c600914d3423d2cb201c5b0b6229940bcfee3e63f5`  
		Last Modified: Tue, 02 Sep 2025 01:46:45 GMT  
		Size: 1.3 MB (1295575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7ce70eecc3dc167352d15ecf9ffa309c844758ceed47be04bcc75c5aff2032`  
		Last Modified: Tue, 02 Sep 2025 01:36:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:bf774c2b5914547708871c7dd91f187e144d335742f0d940a9fb116ee2ee779b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5517525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7143d3b40d10860a9b2cf18ff1e63a8ca9e7c9ea6d7cb78017e8eadea48f5038`

```dockerfile
```

-	Layers:
	-	`sha256:98e0797ce754f2ebd63bcc69ba97f077e1ef0056c0b43b4052a8396232393a72`  
		Last Modified: Tue, 02 Sep 2025 04:00:46 GMT  
		Size: 5.5 MB (5497238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb580831dff854f3aea66c28c86a6e0611f301d5514773a07e93dbb71ea47feb`  
		Last Modified: Tue, 02 Sep 2025 04:00:47 GMT  
		Size: 20.3 KB (20287 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:024b287f65dcc051cb333718321563164a9aafce2ac10c13337dc34506e522db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135301939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498ab00cdd9d78843db19e5966f924f84b0578be029e5af12812535da6961814`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 28 Aug 2025 20:58:57 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
ENV JRUBY_VERSION=9.4.14.0
# Thu, 28 Aug 2025 20:58:57 GMT
ENV JRUBY_SHA256=7ea2be8d0c5989714c795b4544492bf9941c9576e7a78f593a19c85567bc0452
# Thu, 28 Aug 2025 20:58:57 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 20:58:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Aug 2025 20:58:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Aug 2025 20:58:57 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 20:58:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Thu, 28 Aug 2025 20:58:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e940b12283a67ff1c771864e58b58f224257969d16e19a179b3f8289c4d4dfcb`  
		Last Modified: Tue, 12 Aug 2025 18:31:10 GMT  
		Size: 53.8 MB (53839507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30fdff5a53ba3d2e43df30b5277041df566c24f5be4476b4e386dad68d69e`  
		Last Modified: Tue, 12 Aug 2025 18:31:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0ff686944578d38ac0413872ba73e79256657b51fdd048ef40b36aa1225695`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef02b9c5b4cdcd86e5968e74bd1ff73ea9f6c011ff87386496fb5c4c691accf`  
		Last Modified: Thu, 28 Aug 2025 23:34:31 GMT  
		Size: 4.4 MB (4447392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74580245a86be29c5f241adab391f5df25522b4317f85b12d665ae8b3bb94e3`  
		Last Modified: Thu, 28 Aug 2025 23:34:34 GMT  
		Size: 32.3 MB (32293676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4a23682ebcece9dd654f94b8fc2705d71d3f52587786e24b3d49ace450056`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6167fde3b44bae9ba8d6bf39b827bfe7d33c7e3731770868801b79bb2a700ad7`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 1.3 MB (1295601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ef8d919a95779ec93b7fa705db4a82e7cf0ae467477b9ccaab92162da71124`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:b4b932660785454324732420c59260dd5da4036717d72d1390ce0a6f900a954f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5489897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379a18e0ca632decc500648efcdad8c7efbb7a3e54a2e9cf3a0acfbaeeeba11d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c1fa1910237b0bb8c290450886e925e94199c4a0cb279132de59aca77bb91`  
		Last Modified: Fri, 29 Aug 2025 01:00:32 GMT  
		Size: 5.5 MB (5469399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775629a14b298fa4573aa55c2ad4425c79dfca5cb9e4a4e5a90194c755daac45`  
		Last Modified: Fri, 29 Aug 2025 01:00:33 GMT  
		Size: 20.5 KB (20498 bytes)  
		MIME: application/vnd.in-toto+json
