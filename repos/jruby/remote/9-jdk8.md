## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:539c6a1fe0f6fd60ce6f5b414f777b9b80d666ef906b439f9a1eee11e86221e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:9-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:6f0036f3830a4c87d3f6d622f9841ac70e27910fa3ad95e24498c9c9db7ecb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140240442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfab3615061978312678f9bee184ce2cd856de1ec92466721001e388a1af0f29`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:09:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:09:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:09:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:09:45 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:09:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:09:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:09:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:09:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:08:06 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:08:07 GMT
ENV JRUBY_VERSION=9.4.14.0
# Wed, 01 Apr 2026 21:08:07 GMT
ENV JRUBY_SHA256=7ea2be8d0c5989714c795b4544492bf9941c9576e7a78f593a19c85567bc0452
# Wed, 01 Apr 2026 21:08:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Wed, 01 Apr 2026 21:08:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:08:07 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Wed, 01 Apr 2026 21:08:12 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Wed, 01 Apr 2026 21:08:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 01 Apr 2026 21:08:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 01 Apr 2026 21:08:12 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:08:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Wed, 01 Apr 2026 21:08:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8499d88555db34ced0d9fb448fe2757038134d3dc92b148d3294903ee80ccedd`  
		Last Modified: Wed, 01 Apr 2026 20:10:02 GMT  
		Size: 16.1 MB (16149341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f81662495fd8eb3bf0d73e8a9ca270e94c676be7b77189158c47670dcb9c00`  
		Last Modified: Wed, 01 Apr 2026 20:10:03 GMT  
		Size: 55.2 MB (55172983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1264b7f728fb3ca363a22fb104cc2ff53cf7875a92304d376f3d68bf4eb0845c`  
		Last Modified: Wed, 01 Apr 2026 20:10:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a75f3861b4d2848014118e5406a557171cb25de18141f3a33e516f6d8699e47`  
		Last Modified: Wed, 01 Apr 2026 20:10:01 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9680f13f1db33a68f221e8c608fa579219069d943a67461355c168edde68ae`  
		Last Modified: Wed, 01 Apr 2026 21:08:22 GMT  
		Size: 5.6 MB (5589386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cb69ba82cf0252109e79b24a346c5bb0f15b851dca6968f35b7ab1c34d7235`  
		Last Modified: Wed, 01 Apr 2026 21:08:23 GMT  
		Size: 32.3 MB (32293846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b839ea06932a97e64a8af265c29ba42740c1f2aebdfa01b303b0721749cb7c7`  
		Last Modified: Wed, 01 Apr 2026 21:08:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742fc6a6a56c799e858a73fea54a78516f11cbd9dca1bc1ea629755d514068a0`  
		Last Modified: Wed, 01 Apr 2026 21:08:22 GMT  
		Size: 1.3 MB (1295697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087a730a44b7fae603e4711f0c1b7335eec88601e583fd743c01f1ab3e2fe6f3`  
		Last Modified: Wed, 01 Apr 2026 21:08:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk8` - unknown; unknown

```console
$ docker pull jruby@sha256:7945ca47b9ef4c85990f46c5d72a6c840c2614bc42ac83409d94e553db3ed1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5518123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd98efe84cbc7885a9b719b10102f36d15bcd08f35d84054f5dad79d325786e`

```dockerfile
```

-	Layers:
	-	`sha256:aea4a24bb369a3b6a0c9926e63e852b72a9a3dd44e31a65241a10ec6fedcc0f1`  
		Last Modified: Wed, 01 Apr 2026 21:08:22 GMT  
		Size: 5.5 MB (5497881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdabafe1836b22da594fa0bb3c997812231543d86520d18f4b0333fab9d39fa0`  
		Last Modified: Wed, 01 Apr 2026 21:08:22 GMT  
		Size: 20.2 KB (20242 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:9-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:632534b157f8c52b6123173af380dcb728b61ce57816c1c591074205feace260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135989553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0da353d5f48a6d1e5e0f26e13234a68950e02f72762fcfc8a111dfe2848307`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:09:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:09:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:09:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:09:44 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:09:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:09:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:09:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:09:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:08:20 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:08:21 GMT
ENV JRUBY_VERSION=9.4.14.0
# Wed, 01 Apr 2026 21:08:21 GMT
ENV JRUBY_SHA256=7ea2be8d0c5989714c795b4544492bf9941c9576e7a78f593a19c85567bc0452
# Wed, 01 Apr 2026 21:08:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Wed, 01 Apr 2026 21:08:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:08:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc # buildkit
# Wed, 01 Apr 2026 21:08:28 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Wed, 01 Apr 2026 21:08:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 01 Apr 2026 21:08:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 01 Apr 2026 21:08:28 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:08:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Wed, 01 Apr 2026 21:08:28 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d202f2689bfc1f8be0c2401b89369902c9e75737b17229b3ecfec10f5dfb7d`  
		Last Modified: Wed, 01 Apr 2026 20:10:03 GMT  
		Size: 16.1 MB (16073500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0df55b8dc8fd6c1a2bb709ef0c3fb4b8a51c9ad12bfc3422466bf2442d88ce`  
		Last Modified: Wed, 01 Apr 2026 20:10:04 GMT  
		Size: 54.3 MB (54261194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2473e4004616f2603862c97fbf7815aeffde716a1630655438fc6a270188891`  
		Last Modified: Wed, 01 Apr 2026 20:10:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2df5f701b2421adc136c63973b745c2c2641d29a9c6414c56d12c1aa068f2b`  
		Last Modified: Wed, 01 Apr 2026 20:10:02 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc71a9b193594a4ba59319e1dfbb091fdfacdbac7f125e029f8f0f5a553009dc`  
		Last Modified: Wed, 01 Apr 2026 21:08:39 GMT  
		Size: 4.5 MB (4455644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f14e1bcaa1885a1c664e308cb8a8bf7d07732fa4e30c7d6bb668dd32dc3cca7`  
		Last Modified: Wed, 01 Apr 2026 21:08:40 GMT  
		Size: 32.3 MB (32293788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17236aa00faeefaae201daf9507b6b17a820c8eb298be1f5686f8a759634608a`  
		Last Modified: Wed, 01 Apr 2026 21:08:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9ccaf4944970986a89e9c0b75a0ca9b339289e867929d6ffa53fccc14773f`  
		Last Modified: Wed, 01 Apr 2026 21:08:40 GMT  
		Size: 1.3 MB (1295710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57191cbad71d80dd9dd561cefc25b86ef1d425142853292f85c6bfc5f5819035`  
		Last Modified: Wed, 01 Apr 2026 21:08:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk8` - unknown; unknown

```console
$ docker pull jruby@sha256:50cf689c6254b18f5c888ef0c044c388318d72294eac020e911959f9552e1e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5490515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61b28d7bfca6657489b915d4ada279998bdfc519c5fa0e3931b94c7a77a695`

```dockerfile
```

-	Layers:
	-	`sha256:a8167696d24b3889e5d2f467c30ba350660a8cbec0d83f71e4e4df39ce84622c`  
		Last Modified: Wed, 01 Apr 2026 21:08:39 GMT  
		Size: 5.5 MB (5470060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c976bb6f5f8470500cd892b5acfa444e5a61a3c7d704ff6de1ca702ff6b162b6`  
		Last Modified: Wed, 01 Apr 2026 21:08:39 GMT  
		Size: 20.5 KB (20455 bytes)  
		MIME: application/vnd.in-toto+json
