## `clojure:temurin-17-tools-deps-1.12.4.1618-jammy`

```console
$ docker pull clojure@sha256:65917b23b8f37cb0c411e40f3d1b50a68147b7e317063ec7310adc691259b3d2
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:1a449be86947de8c457483225e8af9300b113d7a821c8e154dacba29a14103ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (246992827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8593d8277c6255f98bad4d9d2dd3582671e9b71f4c91ab05add76261f0c2b08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Wed, 15 Apr 2026 20:33:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:51 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:59 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:03:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:03:44 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 15 Apr 2026 22:04:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8d29a7fb5a5eff078d445b26c980850504fe70e1e71a16a3f29389b428fff0`  
		Last Modified: Wed, 15 Apr 2026 20:34:17 GMT  
		Size: 20.7 MB (20694048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c04484493efcfd7e51bf5a2b0fd48785467c07b702d13ff31d875e655c93d90`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 145.6 MB (145633380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4feccd4212dbc0638aabfe5cb211a26d315fca393ed3cd14a94594119d3e9e45`  
		Last Modified: Wed, 15 Apr 2026 20:34:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a096113c0f3bf06f9458c8fe46dee585723223fc2327bbd8733e2db148e3fcf9`  
		Last Modified: Wed, 15 Apr 2026 20:34:15 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c13d5c70cbb4b82a429dd8256946ab06899ac02bc2d7e47837ccdbdd94bb346`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 50.9 MB (50925417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc8e9bac8dcc5f7effc68c245d0fc325b5f6cebd8c7142d84fe5e0646019b84`  
		Last Modified: Wed, 15 Apr 2026 22:04:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e535f2c18724ea0ee8fec65ba8988c73cd82c87d01964da4c0603e1ab6cd22ec`  
		Last Modified: Wed, 15 Apr 2026 22:04:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:1ea17142bf1c7a61c0996775be536069491fda1cbea59912fb99127ae8cfeeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6478740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f05002ff6d26746ecb12594f45ac5dd1db04c9ec77bea056f28341df8be7351`

```dockerfile
```

-	Layers:
	-	`sha256:c9ecf721ca915f8e6130acdfd63c1fa67ce2976b8700f45529093152b19d2bd7`  
		Last Modified: Wed, 15 Apr 2026 22:04:43 GMT  
		Size: 6.5 MB (6463196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52121947b14255b1a380feaf0ffb194f6a832ff043f5869049339533c2422d17`  
		Last Modified: Wed, 15 Apr 2026 22:04:43 GMT  
		Size: 15.5 KB (15544 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6c94be27ede32f84045328be6ae354ca3c21212b4d37108478e2fee32ec1ba93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245066736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fc2b2486f3db75241846825fbe5da14e303775d8b4bfcf98a1b7d2beb451eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Wed, 01 Apr 2026 20:10:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:26 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 01 Apr 2026 20:10:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:10:34 GMT
CMD ["jshell"]
# Wed, 01 Apr 2026 21:16:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 01 Apr 2026 21:16:13 GMT
WORKDIR /tmp
# Wed, 01 Apr 2026 21:16:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 01 Apr 2026 21:16:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 01 Apr 2026 21:16:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 01 Apr 2026 21:16:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Apr 2026 21:16:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119042784698de060c0d5cc43d352706b7ee7e7a1276c76d57d0f280fe621741`  
		Last Modified: Wed, 01 Apr 2026 20:10:53 GMT  
		Size: 22.1 MB (22109330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eda5106889bca626cb0a4406b593fe860a42f419755ae0d5bc92752d9ffaab0`  
		Last Modified: Wed, 01 Apr 2026 20:10:55 GMT  
		Size: 144.4 MB (144443995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1c8668b97df5516e8bce2046cd3988472171b6edcd2e98e18016a717ea362e`  
		Last Modified: Wed, 01 Apr 2026 20:10:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d8677eb5e96b7bbb642774c817d55735e672ee5a4b53ad578fb5e78804d507`  
		Last Modified: Wed, 01 Apr 2026 20:10:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d64275796dae9b715f60731e7754c09ae459f3dfac938778cec8ecc619ff46f`  
		Last Modified: Wed, 01 Apr 2026 21:16:46 GMT  
		Size: 50.9 MB (50902982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df857925ec65412c2135b187dce86fcd08daf0da8b7db65a458877c31c5f12c2`  
		Last Modified: Wed, 01 Apr 2026 21:16:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ea5bf6c0e81090956650fb3ed4c2ec771abc1fd00bc70ef87303b09b8ea790`  
		Last Modified: Wed, 01 Apr 2026 21:16:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:a5daf1a8ff60c5a6b1b5d5975a1c15463b3838e37d2f362b6051a1d9a1060ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6580400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d48d38518732416a53e59833474c9dece31ef484bbb9dbaaec6d3c317571b79`

```dockerfile
```

-	Layers:
	-	`sha256:129db1cfaa9d7298866971dba74e62e1617d440dc498ced1d1f0dfdb2f8a9fe7`  
		Last Modified: Wed, 01 Apr 2026 21:16:45 GMT  
		Size: 6.6 MB (6564764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158686c882076c0111461fca404281fbd54277f16023747c3a3550bf6c339acd`  
		Last Modified: Wed, 01 Apr 2026 21:16:45 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:2676f6a1e2e7334316315627c09cd9c131881b5a2c65c1031aa026a433fc31a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257547659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a8a5e23a704690dbe8ac5247b55066d506b1d6c2210201697230bcb2026b4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:24:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:24:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:24:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 01 Apr 2026 20:24:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:24:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:24:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:24:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:24:33 GMT
CMD ["jshell"]
# Wed, 01 Apr 2026 21:41:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 01 Apr 2026 21:41:35 GMT
WORKDIR /tmp
# Wed, 01 Apr 2026 21:42:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 01 Apr 2026 21:42:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 01 Apr 2026 21:42:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 01 Apr 2026 21:42:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Apr 2026 21:42:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee56463cac9b6c164d466e594277a3aebd5896511c18c0de5feeb9f0a3ca1b5d`  
		Last Modified: Wed, 01 Apr 2026 20:25:12 GMT  
		Size: 22.6 MB (22583606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0d773ae2febcb020ba41a123cc834eaa333f69e357f2c457332a3af1dfd0c6`  
		Last Modified: Wed, 01 Apr 2026 20:25:15 GMT  
		Size: 145.4 MB (145442058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fc03ee16a3108ce7840a0a4035d81e1fdbce975a00c29a606092644b283171`  
		Last Modified: Wed, 01 Apr 2026 20:25:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca20ae339b86668462293b58df1fbb18dd24745165bc00b5eb7d5743b95a5c9`  
		Last Modified: Wed, 01 Apr 2026 20:25:11 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79f903a3e19faa1e4efe22b786df529b18110905a6023b7f98cd2c881afb74a`  
		Last Modified: Wed, 01 Apr 2026 21:43:34 GMT  
		Size: 54.9 MB (54868848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0391f7fc7b124418d621b36b5e13a7c4c30bbbf22ac4c2a18934f061cf4c552f`  
		Last Modified: Wed, 01 Apr 2026 21:43:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cda9fafa4494dbba815173d796283fd51d9eda76060d2670e09a4772a6ec1`  
		Last Modified: Wed, 01 Apr 2026 21:43:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:54a483f54b751f394220f634881c92f955b4eefbdea4b44df8d0b506279e5506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6509391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb53fe906518da693086e553209e85ad64e6463dbd2613ce2f2626b26d60a4b`

```dockerfile
```

-	Layers:
	-	`sha256:72d9d773f06206d750aabd64bafaa67349cf6195f874d113f95eb355eafe71b5`  
		Last Modified: Wed, 01 Apr 2026 21:43:30 GMT  
		Size: 6.5 MB (6493809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a84cb09075d5712409582699cfa32dca3ca10de81a16e1689a2709ac8e8c13d`  
		Last Modified: Wed, 01 Apr 2026 21:43:29 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-jammy` - linux; s390x

```console
$ docker pull clojure@sha256:424b3dc28e7b5ea5cff2ad5f7ae194e6aeb17d4f736c47e55e285b82ecd76e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235169596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0900802264037185d25a82e95538590e53e8fb4ccf81b2fccea7fe0c25530447`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:11:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:11:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:11:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:11:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:11:51 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 01 Apr 2026 20:11:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:11:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:11:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:11:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:11:59 GMT
CMD ["jshell"]
# Wed, 01 Apr 2026 22:29:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 01 Apr 2026 22:29:49 GMT
WORKDIR /tmp
# Wed, 01 Apr 2026 22:34:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 01 Apr 2026 22:34:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 01 Apr 2026 22:34:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 01 Apr 2026 22:34:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Apr 2026 22:34:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0779b8d04f311a67531b6a69256f026efbec47dc4f4ac6b0b0d3dbc132915c70`  
		Last Modified: Wed, 01 Apr 2026 20:12:27 GMT  
		Size: 20.4 MB (20416503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24fda9bb65c675749cdfdb498a0496d7b41d161ac9542f4e3307d5555fb9524`  
		Last Modified: Wed, 01 Apr 2026 20:12:29 GMT  
		Size: 135.6 MB (135631181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9895206c2c294ed0356be2dd779b34dfe983833be5d9254a2237423632017e68`  
		Last Modified: Wed, 01 Apr 2026 20:12:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737ee381d9370487617eafb4788c4ccd2934f81f15d1878a231031c8a2c58f2b`  
		Last Modified: Wed, 01 Apr 2026 20:12:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b962628941035b61a8d5dd08d7fa4da4cec83c9612604541e49937a288768e8`  
		Last Modified: Wed, 01 Apr 2026 22:36:21 GMT  
		Size: 50.9 MB (50915698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39962fb93edd662ab21ddee608d21ce81e2b7f4e790a8eee755011a9665dcf1e`  
		Last Modified: Wed, 01 Apr 2026 22:36:13 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667d6e118287dac6e776ae04657d81c61ad075b6d55d7334caf6d02de94a1863`  
		Last Modified: Wed, 01 Apr 2026 22:36:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:e7b08e4ac27108f8e93309919a6f2a08fbe9ad53531128eaab8aa080f37439ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6402467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b08f63b0c19ce6e5574ae260957624ef346cb40147c9a5cd047eefcafecf9`

```dockerfile
```

-	Layers:
	-	`sha256:30390345d4d5203b472f0257d70a632a027202debd909190a47bfc8d7e9e076d`  
		Last Modified: Wed, 01 Apr 2026 22:36:15 GMT  
		Size: 6.4 MB (6386923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4679855b03e78b2a9c29e683ed8b78b2ee24d288511fda097e8d7b87751816c`  
		Last Modified: Wed, 01 Apr 2026 22:36:08 GMT  
		Size: 15.5 KB (15544 bytes)  
		MIME: application/vnd.in-toto+json
