## `eclipse-temurin:26_35-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:3f44cc0e35a6dc392ebdce7ce953973abd7af64b25c13e3e63d626aa25516078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:26_35-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:cb058195328395a94430bfea8d0bfde44eabcc31af48400aac683d035d07634c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105599715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47b9b9e2f505927a442f74f2ab756d06164810cb63ac3abc58aa16c077b787e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:35:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:35:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:35:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:35:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:35:07 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:35:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        arm64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64el)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:35:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f867c36849cd1cc4145ee69309c24455c4a1abdbe6410e643187ba6ebe481d`  
		Last Modified: Wed, 15 Apr 2026 20:35:41 GMT  
		Size: 11.4 MB (11406128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd11919a60b3cdcee3d3c9f5bfc22049bf443a6cd2ecba9ad9171a53349df561`  
		Last Modified: Wed, 15 Apr 2026 20:35:43 GMT  
		Size: 64.5 MB (64454778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd437048fc064058b0a42b33bf2de1aef3eda351f28595f03f9b1922b15d28b5`  
		Last Modified: Wed, 15 Apr 2026 20:35:41 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ff673a44946c3e27922a27966e43646c4281d2fd09051ca0e4754ae3f9e7f2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5122022f1331adaaaf9123210b5a0d804697c48aab6d80806305f31847deb1`

```dockerfile
```

-	Layers:
	-	`sha256:f33bbac54b8b080faafa01919e3c22bc9179b8ef84b015cf0ef0868d645e08be`  
		Last Modified: Wed, 15 Apr 2026 20:35:41 GMT  
		Size: 3.6 MB (3645814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3edb89c931223183687ebddaf4105d2653cf08f96813d5a83c4258c9ecc8a208`  
		Last Modified: Wed, 15 Apr 2026 20:35:41 GMT  
		Size: 22.2 KB (22165 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5fcba4c3f0ea0c426cb4b176fc4de11aacf8bf570deb2ca79c508271635a1419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102294089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8682a43e97123c26c96622cb9b2f0039df8299ed6ba78d8b757c0f2e6d168e2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:35:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:35:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:35:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:35:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:35:18 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:35:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        arm64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64el)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:35:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e9cec5f605dca337e7774e91e665f3604f2dce07d1633f381545b0e66e1604`  
		Last Modified: Wed, 15 Apr 2026 20:35:54 GMT  
		Size: 11.4 MB (11354823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e02942ce34f024ab9075416a620c71d970c02b1d95865590f791409fc6a0c0f`  
		Last Modified: Wed, 15 Apr 2026 20:35:55 GMT  
		Size: 63.3 MB (63330407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedabaad65383637077b671c502b4e228ef13a160b145a74978539362d82f523`  
		Last Modified: Wed, 15 Apr 2026 20:35:53 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3db238da646acb03e71ac397dd5ff7a8c702e50f9388cc5ecfc83529c209e10b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01bc29010eaf782030b3bba95e7c76f6cbda7054c3f61049b851e08b96f8ada`

```dockerfile
```

-	Layers:
	-	`sha256:a5dba94012e21d82f6e74731ba01683ea105b02d92a199bd9cfb093c73e12109`  
		Last Modified: Wed, 15 Apr 2026 20:35:53 GMT  
		Size: 3.6 MB (3645452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5dea0b4e2bcb6d3b1d3432b3bfef21e7b02c03731f8e36c362e102b93ce994`  
		Last Modified: Wed, 15 Apr 2026 20:35:53 GMT  
		Size: 22.3 KB (22275 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:ff11a7e89915121f1112bdf3b95e0dbf6c093b3125990d2bf2b7290aa35e7d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110358995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b281ded67985336ea47c2bb6b03e51082c36764ec128dc109829b118c5d91480`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:25:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:25:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:25:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:25:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:25:30 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 21:29:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        arm64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64el)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:29:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:29:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:29:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909d898f2bdb14a5db55f323742311c05dc5d65a3445032fd1682cb00c00674a`  
		Last Modified: Wed, 15 Apr 2026 21:26:41 GMT  
		Size: 11.9 MB (11894606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7e758ac8e629acecf4b827308acead32c469c8a780374316a80e06c4d13c47`  
		Last Modified: Wed, 15 Apr 2026 21:30:27 GMT  
		Size: 63.8 MB (63813678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9293ca0c4195f0bf733b0e20b73cede3f5ae3d52d5d2c1f11bbb106be4c765e`  
		Last Modified: Wed, 15 Apr 2026 21:30:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9310a0bf2cc857e6cb808a050e147cf76a033eeaf8eb440232d02d4154d19ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7a22484c509bf31407d607a52e5cc11a9c387f2666276b4d6accddf04ccdbd`

```dockerfile
```

-	Layers:
	-	`sha256:f4a810e46126789583006bed065418c6e102de5a107767426a43c3c2042e5794`  
		Last Modified: Wed, 15 Apr 2026 21:30:25 GMT  
		Size: 3.6 MB (3649139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca3aa09fe9798f242bb68e2f10d2dc96a6edce181ff3281de715df1ba59c6d9`  
		Last Modified: Wed, 15 Apr 2026 21:30:24 GMT  
		Size: 22.2 KB (22201 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-jammy` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:34140314d4cd06e0973c0810089e5f827faa27f361f0b1b89c6db88a36c8b62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101873267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52885b59199ab19158497c508fe8279f993c723b8b6edb4e50aa6c19ea04afa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:47:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:47:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:47:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:47:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:47:10 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        arm64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64el)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:48:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:48:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f19aa0d0411a5c0643187a344eee948bcd0bb6b44180ff22d32df9e8c9c1738`  
		Last Modified: Wed, 15 Apr 2026 20:47:46 GMT  
		Size: 11.5 MB (11499282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f2b9cd0b6d22a2f770286aea7074bf17de65db9c2451673f72d921feb8a525`  
		Last Modified: Wed, 15 Apr 2026 20:48:44 GMT  
		Size: 62.2 MB (62169371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b797aa1e19f1304772c8248ff599dc55afe866f6b08f2e1a42dc20bd8d02e2a`  
		Last Modified: Wed, 15 Apr 2026 20:48:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bb559a254279b41666481eda4c3444fbc746ded99a1979d9fa74571cb1132a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973abbc600aa9e3d7f89bc73e3fc42a3bd1c798a046217d3a825da05cab0548d`

```dockerfile
```

-	Layers:
	-	`sha256:1c0c0aa6a6645774b8d956b3b6dc2c687cf5bbb2c4b639591365f974f45aa424`  
		Last Modified: Wed, 15 Apr 2026 20:48:42 GMT  
		Size: 3.6 MB (3646800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d3a2671787432ef1c04e78dccb6387b07dd5e6e2deb167287daeb0703a49b`  
		Last Modified: Wed, 15 Apr 2026 20:48:42 GMT  
		Size: 22.2 KB (22165 bytes)  
		MIME: application/vnd.in-toto+json
