## `maven:3-eclipse-temurin-21-noble`

```console
$ docker pull maven@sha256:470cfb0e5509ef3ca31e584e3a344426277ac9d193cbb414f415b18ce9e45eb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `maven:3-eclipse-temurin-21-noble` - linux; amd64

```console
$ docker pull maven@sha256:52086eca98284e21d8b42fc2ee860b2eb2e7a7544f1e99007d32577d0570113a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242308469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba2db0f483eeecdc229b289c8fa83db1b5cb274b4d465ed88c528acaabff1ce`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:23 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='ac411d52862fe8a4a48a6c3546bebced8f4879cd728746fc4ee4b06151aa9f8b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:30 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:30 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 19:21:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:21:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:21:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:21:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:21:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:21:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:21:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:21:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:21:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:21:34 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:21:34 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:21:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:21:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694a65171100ee0c49ca2bfcd177a374e7701e81b7762cdef53296a32b081aca`  
		Last Modified: Sat, 08 Nov 2025 17:59:57 GMT  
		Size: 23.0 MB (22959360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86722725fc802c9f5e6c7d2ba7430cbc2dde48879e7b42e30391e13e0986445c`  
		Last Modified: Sat, 08 Nov 2025 18:21:13 GMT  
		Size: 157.8 MB (157839157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab1e4ba0698d1bad926f5cc45c22f9aea73fedb038821fe611974f75c19e53`  
		Last Modified: Sat, 08 Nov 2025 17:59:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e433affea882468548913a1ed9ca35215c03bc1ffe961651008d6b9516708861`  
		Last Modified: Sat, 08 Nov 2025 17:59:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93c967762b3948e38f22eb4ed2b17c665e3d933a60e69835f6f45abb40edb3f`  
		Last Modified: Sat, 08 Nov 2025 19:21:55 GMT  
		Size: 22.5 MB (22540738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47f14a5b0181a805300e271f2e61d49482f3826caaccce44cbb980509be945a`  
		Last Modified: Sat, 08 Nov 2025 19:21:53 GMT  
		Size: 9.2 MB (9242592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7341c7293ad8950c7aea265017e59e7e3019aa9eff593cdcc636c13150980d31`  
		Last Modified: Sat, 08 Nov 2025 19:21:52 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c5fdcd99ffb46954f568108dd1f27c62889b4243712853609c2e7d9c124516`  
		Last Modified: Sat, 08 Nov 2025 19:21:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:04a3b598a4a489fe6898621674af4b303b5002084f5a155a4e1b23136dc7efbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5068530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3402326e7ed01dd478fad7b413e62ced3145f999dd268fad70a81c2df3749d32`

```dockerfile
```

-	Layers:
	-	`sha256:beba789c96beb4ba4d099eefb41ddc8f36e8204079566809fdecfc3a465e6aa4`  
		Last Modified: Sat, 08 Nov 2025 21:31:32 GMT  
		Size: 5.0 MB (5047843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c4259825c256a340bb3fa18eb32a346c95f0d395da5591e7e529b3ae1c714f8`  
		Last Modified: Sat, 08 Nov 2025 21:31:32 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4fa118eab204b1f1a44d122e0c491c5c5421c0375220ceefac69f3e1ee3a6156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240992065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6544919ff643ee49dd0dc249036ed65c55c5491ed5ed092a8e866db318c3ed92`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='ac411d52862fe8a4a48a6c3546bebced8f4879cd728746fc4ee4b06151aa9f8b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:01 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 19:21:00 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:21:01 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:21:01 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:21:01 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:21:01 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:21:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:21:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:21:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:01 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:21:01 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:21:01 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:21:01 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:21:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:21:01 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:01 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ba84db114d2bfc0a4a102c125874dc12f7a222737d3e9a9ee1028cb47ceba0`  
		Last Modified: Sat, 08 Nov 2025 17:59:32 GMT  
		Size: 24.2 MB (24167209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fd2fc60408d4b3df93299f9fefd76774c68bec9ac39acc1f2027cb737cb69`  
		Last Modified: Sat, 08 Nov 2025 18:20:53 GMT  
		Size: 156.1 MB (156108118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf87fe5ffec6a85a87f12689543eabd99b9a8f09452cf21ea8fcc5f4e4ec76d`  
		Last Modified: Sat, 08 Nov 2025 17:59:30 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed95a64b4c74b52b7cab3eae09f733fad5164629a2638b4dc39a5dcf13f6859b`  
		Last Modified: Sat, 08 Nov 2025 17:59:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8accf96cd78abe17fa543e03c4a96c626ac8ff5c78a3a2dc843f8df1efaea789`  
		Last Modified: Sat, 08 Nov 2025 19:21:24 GMT  
		Size: 22.6 MB (22608977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b213120e740c0fba98699868c7c721384bea70c3125c425f457b2b93237583`  
		Last Modified: Sat, 08 Nov 2025 19:21:22 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9237c8ad16bfbba52bd32db400540486ced674e3a961ada73257b952923e401a`  
		Last Modified: Sat, 08 Nov 2025 19:21:21 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df848aab33e40a20e47d1f4c5f412707eec223daf9b64fdf57a8e8d27e10fcda`  
		Last Modified: Sat, 08 Nov 2025 19:21:21 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:32370348070dca04d483485601a822c303a37b8c22a5d1307e7741049cc1484e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e28e88dc2663301e49690fd67902cc98448049753fde7a83647e14425aa09f4`

```dockerfile
```

-	Layers:
	-	`sha256:ffa2977926d6ab433eaaa8882af349cb622b9086580798a66ef627e776e333d0`  
		Last Modified: Sat, 08 Nov 2025 21:31:37 GMT  
		Size: 5.2 MB (5185440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6777aec6c9d1129bb9824534ac710a341c31239aced75f1201f2bdfb07c77518`  
		Last Modified: Sat, 08 Nov 2025 21:31:38 GMT  
		Size: 20.9 KB (20857 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:4ae6211fed9db7673622d16d7347c9188593e5e5a419c9f93a232df52c3bacbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252209852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134dd28bb1e9ac5880fc693eaaa9f648f853fdaae27b7ad0e7dcc603b7722d7c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40485ed64a16d829ecdf6f09ebfcef0f10e3da8b5606ce65ebf8149476226327`  
		Last Modified: Thu, 09 Oct 2025 21:15:18 GMT  
		Size: 24.1 MB (24101794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497a01c732b97de848fefecb9dedb2cd3abb8e9f81190fcc77deecc795ead4ff`  
		Last Modified: Fri, 10 Oct 2025 00:55:43 GMT  
		Size: 158.0 MB (157969903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02133995d6ec0b4f8e30473d9010f45d6c8df9f3bce90beb8c8987a550ea6cf8`  
		Last Modified: Thu, 09 Oct 2025 21:18:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52a8523cffdbe17ffcaec81e72a1bba38f8478da6edd3dbb5d115c7b7ae3cfd`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60d472c0803a8e249510e0846360e515c93fd04599b75de2ff842a7c183d2b`  
		Last Modified: Fri, 10 Oct 2025 09:27:06 GMT  
		Size: 26.6 MB (26588563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddae5ffedccd24bc93ffeb6d2b82047ceb5822c4dc6bcbd14140e54ad703647c`  
		Last Modified: Fri, 10 Oct 2025 09:27:02 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeb7d9ebc17ff9531ac3efceda889eb9a11532f632d2a0c458a335cd89582f9`  
		Last Modified: Fri, 10 Oct 2025 09:27:01 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858cae0491924be952ad2f121e26a3981d9ca7d6f10952018675ea25f64dd43e`  
		Last Modified: Fri, 10 Oct 2025 09:27:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:4ce457e44fb3a27d71cf5d02818bf9b0e4a75d12b9004236c2e8a87a2d841464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a87c30858da793d0a1663f12d7137acffe19cdc7177ef3f587acbab39e2a78`

```dockerfile
```

-	Layers:
	-	`sha256:82591f23b89cbaee8c2c515ee6c6c43b77b2ea6a9f1e5f8c1403df8863c55eb5`  
		Last Modified: Fri, 10 Oct 2025 11:28:05 GMT  
		Size: 5.1 MB (5098416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d6638f27e399fb0ca55d2cdf9b78130e28bee9cbf66ce7a3329acd2ae0f4360`  
		Last Modified: Fri, 10 Oct 2025 11:28:06 GMT  
		Size: 20.8 KB (20796 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-noble` - linux; riscv64

```console
$ docker pull maven@sha256:11b8f01bb212e6817ee3c0ad25f5acda41d97a3568d48797a543da37f2e0ffcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244942603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7877b7bca3dfea7077917aaf3b8d44089ec46bcf6d93834860de8545e272a4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ab17616cf4e436097dac72b5902ca2cd73114fe92dc0252d55ec741bd29f55`  
		Last Modified: Wed, 15 Oct 2025 06:43:49 GMT  
		Size: 20.1 MB (20143051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09c06e929ffe38330e2162b92ad66b68f18cbe17706bc66f7a51af75b8bc59d`  
		Last Modified: Wed, 15 Oct 2025 07:09:32 GMT  
		Size: 153.6 MB (153602054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397340d741a5f810322965ea1e03ae1cfa785e6a6ec1c07babbcd766f9ef9bca`  
		Last Modified: Wed, 15 Oct 2025 06:54:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e5514eed33119a8aa22d285b463c6ffa2eda242011b1b5404506a04064ef89`  
		Last Modified: Wed, 15 Oct 2025 06:54:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283955ef3142b97affdb158b72f7442313f98ee6b2bce839720fee36d19c8b56`  
		Last Modified: Thu, 16 Oct 2025 12:10:33 GMT  
		Size: 31.0 MB (31000059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3643b7091d41c2523e2b6cd8fcb59b7b2f42d0e8dd603790c6d6a7727b422c9d`  
		Last Modified: Thu, 16 Oct 2025 12:10:28 GMT  
		Size: 9.2 MB (9242578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72624215dcad4c2261fd065f7e4483179d39d1af8ef65d14e61cb7e5853f989f`  
		Last Modified: Thu, 16 Oct 2025 12:10:27 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52f1762d07118c79de2b448acc6b51f6c01e1651239376607f7aa82f897e8d4`  
		Last Modified: Thu, 16 Oct 2025 12:10:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:18d4898777cb608c85df176f755d31215d8d134079cb42de30f1ca3906f711b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5609a8ce1544563d5cd91bfb935b8083a99e4892634f900b9c820e8b249aee`

```dockerfile
```

-	Layers:
	-	`sha256:d6a03b1f043544e4fcbba99801df29558942dd0644aaaed975b9879e8628ecb6`  
		Last Modified: Thu, 16 Oct 2025 14:28:04 GMT  
		Size: 5.2 MB (5151481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05cc11b9ab50d926ed52d36efec4a40af8ca85a38669ffded20ef3569a8e7d37`  
		Last Modified: Thu, 16 Oct 2025 14:28:05 GMT  
		Size: 20.8 KB (20797 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-noble` - linux; s390x

```console
$ docker pull maven@sha256:cc720097ccaff533f487d0197c0a2a2d87dfb9bcf34fe3a2b07906f16fd9057a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (232029554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63622de872aee17bd6b7f9e4dcf47cc07e9f9d2c9daeaec644ab9292209df5ca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:05 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:07 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 01 Oct 2025 13:02:07 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:01:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:01:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:01:40 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:08:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='ac411d52862fe8a4a48a6c3546bebced8f4879cd728746fc4ee4b06151aa9f8b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:08:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:08:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:08:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:08:35 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 21:05:04 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 21:05:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 21:05:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 21:05:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 21:05:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 21:05:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 21:05:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 21:05:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 21:05:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 21:05:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 21:05:05 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 21:05:05 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 21:05:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 21:05:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 21:05:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cfa5332fec2dcb147043885d5f4d85503b0e5f3e3b8897a9485fc9daa1b15c`  
		Last Modified: Sat, 08 Nov 2025 18:02:23 GMT  
		Size: 22.1 MB (22130373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d9aa2e8cdf6cfacefdba1eb03ebedfc0dd1ea11af5d8704e36d4a5d3e1beb1`  
		Last Modified: Sat, 08 Nov 2025 22:31:12 GMT  
		Size: 147.1 MB (147080656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221d423b3ad73114e619dafc7dcb9eaa8b4d21953dc756b8dc61ecb0229db80c`  
		Last Modified: Sat, 08 Nov 2025 18:09:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64233e11824d9524e6a9d9e1ae4de84a6c63690d47b2d32c169954bfe4efd701`  
		Last Modified: Sat, 08 Nov 2025 18:09:09 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65684a6e0f6b7178e7f3083ceec5bf45ba1b5f3f1ddcd7be74898a3dbf068428`  
		Last Modified: Sat, 08 Nov 2025 21:05:33 GMT  
		Size: 23.7 MB (23666321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5a57e673cee76a3cd864442df58ac5fa01353050504ede279d2786ed4658b7`  
		Last Modified: Sat, 08 Nov 2025 21:05:33 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc7e3412045c40e18b99a46f7889dbd75667be1dd826e925fb9d49810200d3`  
		Last Modified: Sat, 08 Nov 2025 21:05:31 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346ee04460acd878e212c5b3aff5c14d0b3816b73a73b300850fbe52eefe37f4`  
		Last Modified: Sat, 08 Nov 2025 21:05:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:bc11ad35f808a799d0063c7232419eb22d631e5a90606fd551a3b7423e882a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b5785f2af9c05549f3f96568a40ac0c94ef297211dbb1fcb6061de46f36fc3`

```dockerfile
```

-	Layers:
	-	`sha256:89791a7e9808c9b15c2153f146c01df9812b1a0c58c35d26f7af65aa2f97159e`  
		Last Modified: Sat, 08 Nov 2025 21:31:52 GMT  
		Size: 5.0 MB (4993245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e83ffa5f6e6c0b3d33ac66aaaa9c8a9ca4d23126f8bfb81fc8db7be7dd195d`  
		Last Modified: Sat, 08 Nov 2025 21:31:53 GMT  
		Size: 20.7 KB (20688 bytes)  
		MIME: application/vnd.in-toto+json
