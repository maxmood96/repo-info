## `eclipse-temurin:23-jre`

```console
$ docker pull eclipse-temurin@sha256:d26950918386388a3c33e8272bb26e116bbe9b325c1239228e176617ab861e9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:23-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b140a0b441726be4e9318659a559ae9a82f8edf344de11e90a13536d538d2cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94540687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f1d224c30e2c878fb7d2b5dd01db1e3f66db6152230f21a976bf16472921a5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 19:12:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 19:12:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='ca32d942ef5357fb948604cd8aea5c597130cf7fdf6ddee267b4aa99406ee471';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b88b3151a58399fc22740c16d54e54cdc855c980d9db58a7741efe9149aa150`  
		Last Modified: Sat, 19 Oct 2024 02:08:22 GMT  
		Size: 11.8 MB (11842962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d0d27eb5d647431d54ad64c05725d6000bfc5732d85bafd0316891ba126b03`  
		Last Modified: Sat, 19 Oct 2024 02:08:23 GMT  
		Size: 52.9 MB (52945220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0adefe70c53091970acf37b6e538382947f824d320b0fb6017e77c696bdbe5b3`  
		Last Modified: Sat, 19 Oct 2024 02:08:21 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ecaa81d48ceb8c90ebc9a1f2933ea61a84f775aafc6afc043c87dad68c3555a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2950728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078d2e19988857821478a153f2cc93f9fe40ce53e5d253206931cd1ea45ff8c8`

```dockerfile
```

-	Layers:
	-	`sha256:47b98a44b28db8d2fbbd8caa196b6e8cb1d0aa1085e4a89a0810062c233ba0db`  
		Last Modified: Sat, 19 Oct 2024 02:08:21 GMT  
		Size: 2.9 MB (2929228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615a33fcb9b87bdb2348c241291e835aed46fffc1ecfcb41a95dcc79f0a092a7`  
		Last Modified: Sat, 19 Oct 2024 02:08:21 GMT  
		Size: 21.5 KB (21500 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a14b56f2915925553e0f6b7435c8359a7c1ca6795673462f27c250e2337ab311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92688113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8041fc86a799f02d82005d93cb918e071ed5005c1736bec153316f5f677b5fbc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 19:12:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 19:12:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='ca32d942ef5357fb948604cd8aea5c597130cf7fdf6ddee267b4aa99406ee471';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266d0a2f4031d8e2494780b70e1bf1ff8425fabed67fb328882af0366cb67f63`  
		Last Modified: Sat, 19 Oct 2024 05:43:16 GMT  
		Size: 11.8 MB (11834917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36c153d55b033a09bcd68edff7c7fd11c894e91f1e579c5111492f9a950e282`  
		Last Modified: Sat, 19 Oct 2024 05:43:18 GMT  
		Size: 52.0 MB (51965210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6193d1acd11b782e53ba6deb47ecfeda26a9c685ee2f787b9e7c8a6d4df8d2`  
		Last Modified: Sat, 19 Oct 2024 05:43:16 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:53ff2efad96191d59eef0552278992c84966d2955db002b195113427bd6a7dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2950692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52479545bc35b2dc08a5761ed93619c054e0c91e3ba68625867d8bdc272ea185`

```dockerfile
```

-	Layers:
	-	`sha256:9b98f1d238b842462ba1731510e3fe7969069162b57ef25770a4ff268faeafa0`  
		Last Modified: Sat, 19 Oct 2024 05:43:16 GMT  
		Size: 2.9 MB (2929058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9089ab48c771e94292e88468ee09911b921f2c44da5e43ccf7b741bfd8b50c19`  
		Last Modified: Sat, 19 Oct 2024 05:43:16 GMT  
		Size: 21.6 KB (21634 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:c03bda97dbe4fee832c360348395d11a9d91174aff1ea628bebe8e24d50c6c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99702029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c102bde3eafe537abdd8a7d5479e5b9dc5a89011cfda8a7e8be65c053c740da5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 19:12:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 19:12:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='ca32d942ef5357fb948604cd8aea5c597130cf7fdf6ddee267b4aa99406ee471';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097ea9eee70e511fa34689d3447a4c58b503a388b0f6ad14fe53e355232f001b`  
		Last Modified: Sat, 19 Oct 2024 04:43:30 GMT  
		Size: 12.5 MB (12490457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c86bb85f9f4484bdf36f9811f5480cecd61fe3c7330620e7d894f64f8a968`  
		Last Modified: Sat, 19 Oct 2024 04:43:31 GMT  
		Size: 52.8 MB (52820462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146e056786da348f111e14f39c3effe47e5104cb63f6c84a43b3a3928333dcaf`  
		Last Modified: Sat, 19 Oct 2024 04:43:29 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9f93477f472166e225f95ccf79dba7d806ce0a77a1af8275b37b7a979ef21f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2953958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1665bbf9fa7d223e50b574e14eda2bc286eb7410f285f37dcd4e56d28c326ad5`

```dockerfile
```

-	Layers:
	-	`sha256:cb375e7971e97bcb42477aa2c9129496b02c96ec3596342e29c276115d47e4f5`  
		Last Modified: Sat, 19 Oct 2024 04:43:30 GMT  
		Size: 2.9 MB (2932410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe23a541a3c2406e5751025745e4514b11dda16b74b4ee0c7391db3478d48950`  
		Last Modified: Sat, 19 Oct 2024 04:43:29 GMT  
		Size: 21.5 KB (21548 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:66237f7472e36f18833bb33cd2c82dc4e6c244474a9560f0852334fedca169de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92946651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80b98ba17c715063c3fc1015932358ecfa6b9cc8a47ef8654ece0dcfa17a215`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 19:12:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 19:12:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='ca32d942ef5357fb948604cd8aea5c597130cf7fdf6ddee267b4aa99406ee471';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33789cdea11e58629344c39aa1ded6609d0599f48ff592bc2c5be08909bcf75f`  
		Last Modified: Sat, 19 Oct 2024 04:57:18 GMT  
		Size: 11.9 MB (11947026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df68cfa0e72fe70d04b609498c28427a5bab75f24dbe394c5acc09ca6222824a`  
		Last Modified: Sat, 19 Oct 2024 04:57:23 GMT  
		Size: 50.0 MB (50045897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ddc514b29672cb25bc08fd2f23d6f6583976762d9a9738f6370f00df361a11`  
		Last Modified: Sat, 19 Oct 2024 04:57:16 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e26ec88af368324581e01b3e5d033b763911de5d50ae46774759541f3f1b123e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2942352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d70ccf5a287af1910538e769dc1f02d3ba0b3bfffc97381bb7772db216dad0`

```dockerfile
```

-	Layers:
	-	`sha256:0d587b3fdc741af94dd91237b1f20ff8e50cabe623428d2371fa64542347f305`  
		Last Modified: Sat, 19 Oct 2024 04:57:16 GMT  
		Size: 2.9 MB (2920804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f597a07cff9ba440b538b5ebe23cf301a6ce2067681feb1cf4e633683efbc5`  
		Last Modified: Sat, 19 Oct 2024 04:57:16 GMT  
		Size: 21.5 KB (21548 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:985852a2645fbb7ff8d43f1afbd8caa750e6b745c3be221c5f4d56bfed478aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91617885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4009e860cee84094b0e6368ff1b1b77c7f51627759ca765049f0e24cb1309f97`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 19:12:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 19:12:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 19:12:13 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Sep 2024 19:12:13 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='ca32d942ef5357fb948604cd8aea5c597130cf7fdf6ddee267b4aa99406ee471';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc6016d016ce7af3e96255481b213ce31662b9ad9b6ea1501d09576f5ebf2a`  
		Last Modified: Sat, 19 Oct 2024 04:13:02 GMT  
		Size: 12.2 MB (12156640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715ec6eef1368e3e75f5ee1df586063adbe16044f76aae14c4e97dbc1e176664`  
		Last Modified: Sat, 19 Oct 2024 04:13:02 GMT  
		Size: 49.4 MB (49439490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8918f98296a1b67fc9e4fe454f14bcc3e10e77c72c00d2e4889662f186319d8d`  
		Last Modified: Sat, 19 Oct 2024 04:13:02 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:58c0a83b82393020abd5595a8cd31fa462e1e7b20015f4cc9a7e00f57bedca74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2952328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d9c24dc5cbe59b4e07902564a6eeb39fd07806e73bcd1b4a48dafa65fc0b67`

```dockerfile
```

-	Layers:
	-	`sha256:1a8b9d1e509f4eb368bb53b79180f7ae6088b8e05b036ce3cfe34c7a6a0277f5`  
		Last Modified: Sat, 19 Oct 2024 04:13:02 GMT  
		Size: 2.9 MB (2930828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a33c3431956acd9ee81b678811651e3dab24ee5abd59579eb415dbff7ad52d42`  
		Last Modified: Sat, 19 Oct 2024 04:13:01 GMT  
		Size: 21.5 KB (21500 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:d0c8ffb74f4a5ae6526fafd8d2ab5113dc7c214aa687bf76a20a8f950f751fd9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884035752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89217c3304ea352b54f5520037532946ddee16ed438323384d169acf34d005eb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Sat, 19 Oct 2024 01:04:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 01:04:36 GMT
ENV JAVA_VERSION=jdk-23+37
# Sat, 19 Oct 2024 01:05:09 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 01:05:16 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9617b4646fbaf0d19397e9a7a82133da2492b30fc974c7b73f6e0a62050e238`  
		Last Modified: Sat, 19 Oct 2024 01:05:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4f61e3548694fb16d3af79a621cdb0e4c9d463aec57ff22d6f67ce514f13d8`  
		Last Modified: Sat, 19 Oct 2024 01:05:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9862aa55a35e9826f90a6cb0f65f7b46b3abdedd8cb69efb19f84f36863974ca`  
		Last Modified: Sat, 19 Oct 2024 01:05:25 GMT  
		Size: 84.3 MB (84329858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953d49d780958f85ceb2bb663a4a0ed228a060c39770e6238eacada5ae364bdd`  
		Last Modified: Sat, 19 Oct 2024 01:05:18 GMT  
		Size: 361.8 KB (361769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:8d69f4aa1eacbc2b8998c074f2edb67f269f249fc0273050c1c19da32a509a61
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1990022081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5d1a95370b1880d3407b479f8a5cf67dafbc620ca5380b8e164373634ba827`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 19 Oct 2024 00:57:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:57:48 GMT
ENV JAVA_VERSION=jdk-23+37
# Sat, 19 Oct 2024 00:59:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 00:59:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ff74a4b599dc3232757a51eea50c8706c4b17250a8b5736af26630bb98a0c5`  
		Last Modified: Sat, 19 Oct 2024 00:59:46 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5323352f9c2995ffcbedde7785a0afbc4a7df400505ce9bda9ea49a321638616`  
		Last Modified: Sat, 19 Oct 2024 00:59:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8632167b64008202e7b912a81dae13e74907f8d5ad9f7ccd753563f1c9fff134`  
		Last Modified: Sat, 19 Oct 2024 00:59:53 GMT  
		Size: 84.4 MB (84351426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b561f729028e2ba80746196d33c0f387be2a3bbaa78a53cb44b6fe5df277d6`  
		Last Modified: Sat, 19 Oct 2024 00:59:47 GMT  
		Size: 3.8 MB (3842807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
