## `clojure:temurin-17-tools-deps-jammy`

```console
$ docker pull clojure@sha256:cbf54cf1690de7b4831421284f50e762cbfb4ab80b7109d8ede1b777edaaaf44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:583fd97a0e0b9ac1faa0a8c283689646ad09865068fb6e286a430be09fdd9213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247930611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6ef203c027ff60663ca5b4e7ef86ee0de73eee39542b23c95dfbda2e950757`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
ARG RELEASE
# Wed, 26 Mar 2025 16:17:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 26 Mar 2025 16:17:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 26 Mar 2025 16:17:22 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 26 Mar 2025 16:17:22 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["/bin/bash"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7575fa115e62f663c8e530c448272a4f4dde81c6f5744b8ba99d3dbfa5671d2`  
		Last Modified: Wed, 23 Apr 2025 16:32:06 GMT  
		Size: 20.7 MB (20693830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5c220288dea1cf3e5d90e266c084b0c2e42da563ec1b8953b5142be498ff2b`  
		Last Modified: Wed, 23 Apr 2025 16:32:08 GMT  
		Size: 144.6 MB (144646773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7164c6fee456ad2ff449de6a87782c809fca0c9e2e7d1e73b141c603dcd8f00`  
		Last Modified: Wed, 23 Apr 2025 16:32:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0137fea4bef4dc4ff919d973a8ae36f29edacba15f7b5129ebe177983d665fe0`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc66d50adbe06dc54c1133184f09494fb244b64faa859e8282a5664879f64d`  
		Last Modified: Wed, 23 Apr 2025 17:16:08 GMT  
		Size: 53.1 MB (53054153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b183bd286016a669fe07af91a7789cebb140ce6e8bcb06e21c5777e26b33cd`  
		Last Modified: Wed, 23 Apr 2025 17:16:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83cf0b6bc1b840b247ba222a1dc8d2f8409a7a601ddec0073e94a34eeed5b06`  
		Last Modified: Wed, 23 Apr 2025 17:16:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:696cbdf18e6fe3122a483808fe2d8f463a9788176d1c4b04a94fe7582208b605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6233531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51515791a192881c7b39c8dd638b5017c90b00807bfa4cba44a06c8022e41d32`

```dockerfile
```

-	Layers:
	-	`sha256:5f690e8e7ed1e910841333c1a5104b1e8aa8548947fd87f0d2d053a462f8d08b`  
		Last Modified: Wed, 23 Apr 2025 17:16:06 GMT  
		Size: 6.2 MB (6217260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17b47cfc346d953bad8d8b0e02790717ba27af6285f29b9e56d370cbc8f0949`  
		Last Modified: Wed, 23 Apr 2025 17:16:06 GMT  
		Size: 16.3 KB (16271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31d7abcfaab36e0eedf61bef37ff5cb2e4c54e2f2cfdd871a29e55ef2195ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245895570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1d69849f7cec79fb322c642563574e92379a9ba7eaa5a8e6b634d1f7792679`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
ARG RELEASE
# Wed, 26 Mar 2025 16:17:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 26 Mar 2025 16:17:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 26 Mar 2025 16:17:22 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 26 Mar 2025 16:17:22 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["/bin/bash"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b14141c255ebde08ea2dc9ff81289f3fcec02625983b6981b076ad4ae3927b`  
		Last Modified: Wed, 09 Apr 2025 07:04:42 GMT  
		Size: 22.1 MB (22069470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966800e8635a1ca13ef064688a406dd4d9e1586b47b05ec84a24e3c6b2ae6808`  
		Last Modified: Wed, 23 Apr 2025 16:36:18 GMT  
		Size: 143.5 MB (143512496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eca0d1f21e46c96a0458e71c91a601408e944bbf262536a187f6e4e82cc0024`  
		Last Modified: Wed, 23 Apr 2025 16:36:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fbd5441388ada2bd61d783b3f56b9ea0a6c5656aa9386551d64fcc39d53f90`  
		Last Modified: Wed, 23 Apr 2025 16:36:15 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c622799afeb4548ac8f1e87663edb208ef831800d88a71adf39649d7fea60087`  
		Last Modified: Wed, 23 Apr 2025 19:52:46 GMT  
		Size: 53.0 MB (52955887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de86d2d55227d259ab94a36d1e22a5a1da574e04fb1e2dac649d9bd2c84c87f0`  
		Last Modified: Wed, 23 Apr 2025 19:52:44 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d50cb3acac4e2994cc7dfe83554f9da4f95f3edf72591058bb17dee4b9399c`  
		Last Modified: Wed, 23 Apr 2025 19:52:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:ae3aac06a85b84d94f2822eaf86c918584cc410f60f0afa817b2dd8a04ec8248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6335238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ac3301a2f9c251c9b4709f1c2b1d089c50256791866ac330451ef750729a52`

```dockerfile
```

-	Layers:
	-	`sha256:eff3dd07568f7ebbfc0e139186c2938ba3bd09223fd264c81893c4c90b78cf09`  
		Last Modified: Wed, 23 Apr 2025 19:52:44 GMT  
		Size: 6.3 MB (6318851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7bdf0e86e7727c769a06b53520645ca1c05e065ba9e3caace62ccdc6dc40a0`  
		Last Modified: Wed, 23 Apr 2025 19:52:43 GMT  
		Size: 16.4 KB (16387 bytes)  
		MIME: application/vnd.in-toto+json
