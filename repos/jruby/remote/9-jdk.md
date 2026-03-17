## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:50b45fde8d0274607fc341821a0d69634e8bb0acd907e5a24107fca10b0c1ddd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:945b9fbf5e11324762c044f68ceec6d104d7d7aefae2338fea13f07ee8f97970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140048300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d884c0d34cab0de56485c0450ad1b9c7170bee53cc853f9852781fb779737f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:21:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:21:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:21:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:21:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:21:58 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Mar 2026 01:22:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Mar 2026 01:22:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:22:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:22:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:37:54 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:37:54 GMT
ENV JRUBY_VERSION=9.4.14.0
# Tue, 17 Mar 2026 02:37:54 GMT
ENV JRUBY_SHA256=7ea2be8d0c5989714c795b4544492bf9941c9576e7a78f593a19c85567bc0452
# Tue, 17 Mar 2026 02:37:54 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Tue, 17 Mar 2026 02:37:54 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:37:54 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Tue, 17 Mar 2026 02:37:59 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Tue, 17 Mar 2026 02:37:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 02:37:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 02:37:59 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:38:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 02:38:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393028e021f4abfeac64f5baffd8d8eccd40415155bbc59b900622b73f3ec405`  
		Last Modified: Tue, 17 Mar 2026 01:22:13 GMT  
		Size: 16.1 MB (16149245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561a695d28ffec6a01e4b866a09299e6b1eb4fe442ac3eeaa8fc32ed86cad32b`  
		Last Modified: Tue, 17 Mar 2026 01:22:14 GMT  
		Size: 55.2 MB (55172932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176369b6cce001f7e34c8f795b9cefbfdf3e8b27f126ffbfbd4367d75f2a999f`  
		Last Modified: Tue, 17 Mar 2026 01:22:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0edb850b2281e2d7eb56e8fb962ab7990903d0b1d39b4573d45f1794e38f573`  
		Last Modified: Tue, 17 Mar 2026 01:22:12 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70de2038482dfbe1218adb02a9101cf189ffdeb0a4092c254dcae0ed673df2c`  
		Last Modified: Tue, 17 Mar 2026 02:38:14 GMT  
		Size: 5.6 MB (5595323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2370bef0db9272cdd155fc5fe3a2a4be8eeadda09465bad47060aff9f360156f`  
		Last Modified: Tue, 17 Mar 2026 02:38:19 GMT  
		Size: 32.3 MB (32293823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90658cfe5df6e516fc7631ed1534bf23c859b58aff660683b8e4cc3eb88ec71`  
		Last Modified: Tue, 17 Mar 2026 02:38:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49662f090364569c9f2669df35c8bce24c25a57605ab99ba2298c5eca8e3b724`  
		Last Modified: Tue, 17 Mar 2026 02:38:11 GMT  
		Size: 1.3 MB (1295682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c5663cf1508eb88d15a4c25d5e1db7900d8731af5b881cac6b489cdc039d2`  
		Last Modified: Tue, 17 Mar 2026 02:38:14 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:988a5637bf7b22b82b7ce1b8bb215d6634173298e2ebd88125fd70e7cede74c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5518125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e3fc660a582e79f580d190420b8d2bcc906bc8ccb666e7f1b3842521209621`

```dockerfile
```

-	Layers:
	-	`sha256:e6b8889f8a1ab0120f42751518ce0cbebb54c8a5340d8fbf0c49c67e582391e1`  
		Last Modified: Tue, 17 Mar 2026 02:38:13 GMT  
		Size: 5.5 MB (5497881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7bb9b28e5afcc800706337646265a627ac7f4792c87a2c0e6c2e53e50e6b077`  
		Last Modified: Tue, 17 Mar 2026 02:38:10 GMT  
		Size: 20.2 KB (20244 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:cca79ae10625a0e1f09c2b454201ec1f75f1ab1344aa791884ab3d07fb182fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135776373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f701acdf2cde18e3498acd93baa45c0564a60a482045311cb08ec01523072fda`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:00 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Mar 2026 01:23:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Mar 2026 01:23:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:42:03 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:42:04 GMT
ENV JRUBY_VERSION=9.4.14.0
# Tue, 17 Mar 2026 02:42:04 GMT
ENV JRUBY_SHA256=7ea2be8d0c5989714c795b4544492bf9941c9576e7a78f593a19c85567bc0452
# Tue, 17 Mar 2026 02:42:04 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Tue, 17 Mar 2026 02:42:04 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:42:04 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Tue, 17 Mar 2026 02:42:12 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Tue, 17 Mar 2026 02:42:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 02:42:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 02:42:12 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:42:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 02:42:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9760802dfd0cb54abb91f0a7edff239728c4ae9fb364b171184c3c341f45817b`  
		Last Modified: Tue, 17 Mar 2026 01:23:18 GMT  
		Size: 16.1 MB (16073512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9cecfa663aeefa1f74e82234125d8362682783d2dd3ef50561ea6f7924c307`  
		Last Modified: Tue, 17 Mar 2026 01:23:19 GMT  
		Size: 54.3 MB (54261202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5de71062001c71d8526cc55d837526d7baf759722846d8ac468f6f6a3637e4`  
		Last Modified: Tue, 17 Mar 2026 01:23:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb12bad2bd3abcb2ec314de334056db3257220a0b067d6c6bf772b3f607b00a7`  
		Last Modified: Tue, 17 Mar 2026 01:23:17 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbce7f53e40196fe7ce7fd1bf1e8c813cd0476ccc16665c44e13b0b040187972`  
		Last Modified: Tue, 17 Mar 2026 02:42:24 GMT  
		Size: 4.5 MB (4460286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518ca5da33e6047996d8e1b000c13ed9ee58f01f80a58b75ed1bd43d476d048f`  
		Last Modified: Tue, 17 Mar 2026 02:42:24 GMT  
		Size: 32.3 MB (32293854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113ce30228306caa5ac1c962abe8d4001215151f60def414def62e4137fa4ad1`  
		Last Modified: Tue, 17 Mar 2026 02:42:23 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84569576bbc94b6178ed0d8b7b17b5ab50fc9a8ae16c1d80e60c9d36fdb5953e`  
		Last Modified: Tue, 17 Mar 2026 02:42:24 GMT  
		Size: 1.3 MB (1295718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596bd436884947eb7301c7c6ee8ac91938779e4ce576221501ba2c5fb33df1ad`  
		Last Modified: Tue, 17 Mar 2026 02:42:25 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:52505855a79b306e658cdcaf329a044fae7343e5ce1722f84b5b10c09f090755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5490516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b523f370da2b85c32155467f4453c536221f5ca81bc6a9ec2ee9f8d022a6acdd`

```dockerfile
```

-	Layers:
	-	`sha256:9e1cd764cf45547fe8ea7bb82f4857cc8f48d3fb2c5b4c45749795d37809ab0d`  
		Last Modified: Tue, 17 Mar 2026 02:42:24 GMT  
		Size: 5.5 MB (5470060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb69b42bdf3ac095a200a0070da0e8b3486756dbe0037ca952eff23cdf298c0`  
		Last Modified: Tue, 17 Mar 2026 02:42:23 GMT  
		Size: 20.5 KB (20456 bytes)  
		MIME: application/vnd.in-toto+json
