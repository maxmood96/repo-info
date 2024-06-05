## `clojure:temurin-22-jammy`

```console
$ docker pull clojure@sha256:0c96da0e9820063acf670754e5956bd2be19652b7c32d234e3bd7942d40b8215
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:dc29f00ee9d6ec045b095553c1807234ade370f311a1b6931e99322659f177be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256123999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c86a60104a9e84341e8a66044797574e70687c6642780588e93af3f49265e57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ARG RELEASE
# Tue, 28 May 2024 15:17:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 May 2024 15:17:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 May 2024 15:17:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 28 May 2024 15:17:11 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e054688d33d41005bf114d52de305d98787a5ce7be2a08ab0722f9464685f`  
		Last Modified: Wed, 05 Jun 2024 05:02:16 GMT  
		Size: 16.3 MB (16338122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df2b221df5b07a4c404a2df3b87c2f6286810bb38950288097a111d5158afbf`  
		Last Modified: Wed, 05 Jun 2024 05:02:26 GMT  
		Size: 156.7 MB (156718220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f348f1f8dedbe421fc6144be550fff2a4404c00fe5785dfa6981f81826e1a7c8`  
		Last Modified: Wed, 05 Jun 2024 05:02:14 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711d4222a20af5cb309b47f0255be9df2e2a66a188796386223466d4e0585ea1`  
		Last Modified: Wed, 05 Jun 2024 05:02:14 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e4a6fe1cc9c89eb94e56cd0f02d4ab21d15f8aa7a7c49514dd0f2a7cf020c4`  
		Last Modified: Wed, 05 Jun 2024 06:12:45 GMT  
		Size: 52.6 MB (52626447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5a0dc7255a54c207fddfb5d9a2c872acc070dabd3d0f304bfa9edf4b92267e`  
		Last Modified: Wed, 05 Jun 2024 06:12:43 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea48279b04ab192a9f684bb9130426cd92e1c8c1e9a63f48783a6db4deb7547`  
		Last Modified: Wed, 05 Jun 2024 06:12:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:87bb7b9cfdc4406407195cca428353021b9b1b13f738e794603abf8bd86beb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5902736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87e87bff12ff61a0843ad480d6cbbc7137a2c18a10e3c713c7bc854fc6c7947`

```dockerfile
```

-	Layers:
	-	`sha256:9ca46d5b900223f06183dd2e3bc8cc06b293a7f8365205d0c27b5cef528b6a8e`  
		Last Modified: Wed, 05 Jun 2024 06:12:44 GMT  
		Size: 5.9 MB (5887260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f1051df488918fc7b56039adad7e2c24fc9f74a933248dba8c9b96c1a67b5c0`  
		Last Modified: Wed, 05 Jun 2024 06:12:43 GMT  
		Size: 15.5 KB (15476 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5d7753749bd05a819263388585bae1e40ac464c3527468937eddf221dc64e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253510642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb05d9699be6e22db87c3c9e655ad4dca98bd4126a6b28ce1506cb850b020d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ARG RELEASE
# Tue, 28 May 2024 15:17:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 May 2024 15:17:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 May 2024 15:17:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890080877365c3306b8b11b415e298a3f94de3a3cac174b27903d05a99169317`  
		Last Modified: Wed, 05 Jun 2024 04:58:36 GMT  
		Size: 17.8 MB (17754166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97acb13211adcb33c9c3ca02d53363187e401145f9f585896acbd49a77cdb7e4`  
		Last Modified: Wed, 05 Jun 2024 04:58:44 GMT  
		Size: 154.7 MB (154738632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88cc32d15cb3bc0b7ce0a6ad99502ccd26604d43b2a9748877887d5c190683`  
		Last Modified: Wed, 05 Jun 2024 04:58:33 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016aa22f40a6185d6a60d03b34b8644ac1e05558c4348a04964ffc7b254ba934`  
		Last Modified: Wed, 05 Jun 2024 04:58:34 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a7f70cd187b5641096e39291185c6a0ec0c94cf3b361de7aebe9beccbf2cce`  
		Last Modified: Wed, 05 Jun 2024 14:27:53 GMT  
		Size: 52.6 MB (52613611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce2c08f200f1c6c655ac3a15479159be0627c99e8127134cfe98e5e61a0abb`  
		Last Modified: Wed, 05 Jun 2024 14:27:51 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f0a212994cbf9f5e472233c03ad3e142107b4e1fc7d9229e462fc28f7d353f`  
		Last Modified: Wed, 05 Jun 2024 14:27:51 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:2ea3f9cce82488677cfbdff53e5b8102dc91ed8476e78081aff90efd32324a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6005354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04948d4e728f8f447bed3d5c697f72dfbb25376919caef064df3e6632b7e50f`

```dockerfile
```

-	Layers:
	-	`sha256:acf80ed377a5525147c50f3205b3f01e18ad0d97b7ef72ee89d825a1e2e560be`  
		Last Modified: Wed, 05 Jun 2024 14:27:51 GMT  
		Size: 6.0 MB (5989573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4bb63ed2fd9d1c4c85fa3574d8caaca184c43d844e5a18bcd42a50f255abdd`  
		Last Modified: Wed, 05 Jun 2024 14:27:51 GMT  
		Size: 15.8 KB (15781 bytes)  
		MIME: application/vnd.in-toto+json
