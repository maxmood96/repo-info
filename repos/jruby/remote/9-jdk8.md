## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:61761eb003932133e841ed250e0916dfbaec34365b443006a51a683937b34926
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:9-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:75cd75cae54c392cb0b429a4a2af4dac2706c6da378ccaebaa7e2cc39fd85dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189085337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc99b862ecbca02bcb5b2489bcb4a01ad31e3897b103ebeb5d713339d0cda751`
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
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 02 Jul 2024 17:37:28 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jul 2024 17:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 17:37:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b774bb3b629182074f56c4fd66bcbe6c07f5e0078a79dc1520e6715111a73e0`  
		Last Modified: Wed, 02 Oct 2024 02:20:32 GMT  
		Size: 16.9 MB (16934012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcfdc2e6cd95129b7c303e478b6aa1e5a821d4ca25a07e155766a61c052101e`  
		Last Modified: Wed, 02 Oct 2024 02:20:38 GMT  
		Size: 103.6 MB (103616439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8c65217c75fe0f01024023748acffa174da1ae08416fda739efa124ec766e6`  
		Last Modified: Wed, 02 Oct 2024 02:20:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f3afb445a6b2ca770250fad69d6e9e6862dda9b969404f4a3b740d4e41e26e`  
		Last Modified: Wed, 02 Oct 2024 02:20:29 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477bf75aaccf2887febf23f433aa890c0de34476be6b7a93c730335e4b1ae80`  
		Last Modified: Wed, 02 Oct 2024 03:56:25 GMT  
		Size: 6.8 MB (6836848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994abce827a729f17423b97ffde4604b9eb18a49c66ab982197c3f2f6287c1b7`  
		Last Modified: Wed, 02 Oct 2024 03:56:26 GMT  
		Size: 31.9 MB (31864107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1778c577790e8f8285187711021587391fa125a892199f3cf2bc1a8ba1ed7ded`  
		Last Modified: Wed, 02 Oct 2024 03:56:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9091ed3a82e3f6304c15b3ce21154c42d78a8d357da8b3ab5113e32328cc054`  
		Last Modified: Wed, 02 Oct 2024 03:56:26 GMT  
		Size: 1.2 MB (1247447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d741a608c1933b5b5956e4398497cf8b4ff2f9b2f15bb11d08fd8c4b1320f9`  
		Last Modified: Wed, 02 Oct 2024 03:56:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk8` - unknown; unknown

```console
$ docker pull jruby@sha256:3fd4fbb68ca2648807606ac381ccd2c7d52d4ee08a658294c9551e063f447588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5102522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57c29252e57e93d53189f77ce1c68d1a0e13507a4cc2d716478b7f354ce6117`

```dockerfile
```

-	Layers:
	-	`sha256:882ff088ab2cdbc806a17bbf2b6ed3a654832e7b6da7a3a83ffd84360a00e0c9`  
		Last Modified: Wed, 02 Oct 2024 03:56:25 GMT  
		Size: 5.1 MB (5082265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4578647eeb0eb049a2e7a1d9690af27fc2e50bd8714a1e54ece743f202f791`  
		Last Modified: Wed, 02 Oct 2024 03:56:25 GMT  
		Size: 20.3 KB (20257 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:9-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:fb93a13b461b6411ab276c76f6f662e87610b3bc06088922f9fe13c4deff636a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185607654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1feb076c0df896b98c65b4f74d615daebf2f025579b86e8178b1272b7bc9bb09`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 02 Jul 2024 17:37:28 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jul 2024 17:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 17:37:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 17:37:28 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 02 Jul 2024 17:37:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1b8e9d0187151e1b4345bdaf25ba92b670bd974da9864e3889cb52bdff5910`  
		Last Modified: Thu, 25 Jul 2024 17:42:58 GMT  
		Size: 102.7 MB (102733753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5785d0ccf0f58401695a0c391cc5ee84d47ab7447c9f77649b8778d1efb12fd0`  
		Last Modified: Thu, 25 Jul 2024 17:42:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2659ed92871ab0fc4c48ebbb22c8e5ed16c8a53f1deb0d5d13b426098055d3`  
		Last Modified: Fri, 23 Aug 2024 19:42:30 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ffc465e0e8695a6f18912a5e669b27eded1da5d8902c9a989b859b280f0398`  
		Last Modified: Fri, 23 Aug 2024 22:46:31 GMT  
		Size: 5.8 MB (5793450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7dbaec6c3ec6fb018a1f6b09e2a9a387ee7f78d12686043c99cc91b06c651`  
		Last Modified: Fri, 23 Aug 2024 22:46:31 GMT  
		Size: 31.9 MB (31864318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b73b6628adb9fe36ddc84ca3d8823de31399a05aafa2e315e023f8edac230`  
		Last Modified: Fri, 23 Aug 2024 22:46:30 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0925281147a13603839469e89a734359c93ff710d730b53dcdf41853235e0a3`  
		Last Modified: Fri, 23 Aug 2024 22:46:31 GMT  
		Size: 1.2 MB (1231308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b050a6433cb91aaf3746d12d3fec413863b8daf10669486cde81bcf3e55cf9b9`  
		Last Modified: Fri, 23 Aug 2024 22:46:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:9-jdk8` - unknown; unknown

```console
$ docker pull jruby@sha256:e4031fe0a70f5d0bac111ee91d07e863ce4b016f91d5836023542ef1b87db2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4823483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0945349a430a688477a49ed387f799e7cdddef0143ad204422eaf2eac564930f`

```dockerfile
```

-	Layers:
	-	`sha256:089c38cc1182127fc65e1e393ff8d071d8eba303a5b74e8883160ef22d830b45`  
		Last Modified: Fri, 23 Aug 2024 22:46:31 GMT  
		Size: 4.8 MB (4802867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcaa5595059b3ce85358fd215e8e92b43a896b5bb4cd60065dfbf31607ff8bcc`  
		Last Modified: Fri, 23 Aug 2024 22:46:30 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json
