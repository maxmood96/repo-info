## `jruby:10-jdk`

```console
$ docker pull jruby@sha256:f93e34ed8add6148ac31a72a3106d048bd72cdb755f098bcae8ca816ce497e96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:10-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:5e9dc3aed1f5f58629ce4678daa3a017e217c7ad1dd8ebbc539d11f49fb05181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (263982480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e233fdc698a06b688ec3b10e32f49bc56689333a15ad024e6259a07c4b8a29`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

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
# Sat, 08 Nov 2025 18:28:48 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:28:49 GMT
ENV JRUBY_VERSION=10.0.2.0
# Sat, 08 Nov 2025 18:28:49 GMT
ENV JRUBY_SHA256=b8a026f38aa98461a04ed0aa0b20891ce257ecbe53e124719ce9ee5b804525f1
# Sat, 08 Nov 2025 18:28:49 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Sat, 08 Nov 2025 18:28:49 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:28:49 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc # buildkit
# Sat, 08 Nov 2025 18:28:56 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Sat, 08 Nov 2025 18:28:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 08 Nov 2025 18:28:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 08 Nov 2025 18:28:56 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:28:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Sat, 08 Nov 2025 18:28:56 GMT
CMD ["irb"]
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
	-	`sha256:0f6eccf5320b61a2a8269589345ad01ad5dbc129614245d49feb6386f98968de`  
		Last Modified: Sat, 08 Nov 2025 18:30:54 GMT  
		Size: 6.0 MB (6020422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a91d979b6021f47fbb8076fe6e687411029436aaa26f8bf9592291f436dae7`  
		Last Modified: Sat, 08 Nov 2025 20:18:24 GMT  
		Size: 33.9 MB (33918537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e4f5f328dfa9634d72afaa1f8994579c4b8c2a2438b4b32fe8d2ee86826d4c`  
		Last Modified: Sat, 08 Nov 2025 20:18:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b3efcdc58a28c3a6bd43d3ae55762aa7a2b42d4c33f292f47cafdef10336f8`  
		Last Modified: Sat, 08 Nov 2025 20:18:22 GMT  
		Size: 13.5 MB (13519081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2040ddc1e7261f2291fb5e44924bc6a76c83d63ddd87762031020c3ce28b867`  
		Last Modified: Sat, 08 Nov 2025 20:18:21 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:10-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:424eb6aa75981c04523f3ebafb262b1534b9d1a0787acc7f47af0bcfd24c9109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f9d324074284d42ba1fe0aa55be72117ef2644e9eb4506c3425571cccdc5ac`

```dockerfile
```

-	Layers:
	-	`sha256:0fa22bbeaef8e413e1314a80515ba16486b853446d1f493946ce0184f469bad3`  
		Last Modified: Sat, 08 Nov 2025 22:59:23 GMT  
		Size: 4.9 MB (4925542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bac92ad0c953caa95032afffade1b3cee9dc1ca501e203696eafa04c5c492644`  
		Last Modified: Sat, 08 Nov 2025 22:59:23 GMT  
		Size: 20.4 KB (20370 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:10-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:3f0c0bcb94be52c83ea5eb813822904d2bc684a6bb4de5fd4a367b9673cb50ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261589287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b1801056e017e6dc50510fbc3bc790e4f9b0dfaed1bd812cd1a41732416537`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

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
# Sat, 08 Nov 2025 18:27:39 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:27:40 GMT
ENV JRUBY_VERSION=10.0.2.0
# Sat, 08 Nov 2025 18:27:40 GMT
ENV JRUBY_SHA256=b8a026f38aa98461a04ed0aa0b20891ce257ecbe53e124719ce9ee5b804525f1
# Sat, 08 Nov 2025 18:27:40 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Sat, 08 Nov 2025 18:27:40 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:27:40 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc # buildkit
# Sat, 08 Nov 2025 18:27:49 GMT
RUN gem install bundler rake net-telnet xmlrpc # buildkit
# Sat, 08 Nov 2025 18:27:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 08 Nov 2025 18:27:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 08 Nov 2025 18:27:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:27:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Sat, 08 Nov 2025 18:27:49 GMT
CMD ["irb"]
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
	-	`sha256:cedf397ef47d0c0db2d839a07f638bd53a6fed2957fdcf90742420fdbf7ef396`  
		Last Modified: Sat, 08 Nov 2025 18:28:09 GMT  
		Size: 4.9 MB (4931795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9e0e01bbcc6b1766da6c58ae070f977f5bae2d8f6d3b9ec9ef6e1d1ea3a5d0`  
		Last Modified: Sat, 08 Nov 2025 18:28:19 GMT  
		Size: 33.9 MB (33918535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581fe04490fd109a2d0b1829cf7025345202f156cfd42d634d0c080a1da410e`  
		Last Modified: Sat, 08 Nov 2025 18:28:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516ca6d350e567f22baa9293b60e5e16d12a8508327cec745f48b35ea21f47cb`  
		Last Modified: Sat, 08 Nov 2025 18:28:10 GMT  
		Size: 13.6 MB (13599138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175128802ca30b96b9e74343328e63831eeba6d4d2ac78aa4ea45a296399395`  
		Last Modified: Sat, 08 Nov 2025 18:28:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:10-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:723ac1a7378533f9c0dc2d7183ffa27d8bfa2be712fc824468cf4a6360234c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5050216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4308753aa4c97cb2497a8296984836e22e8debd58a8de2121d148baacbb738`

```dockerfile
```

-	Layers:
	-	`sha256:3a9139afeb6d49cefec710782e1c4cea8dfcf900c4867824892981f11e96164b`  
		Last Modified: Sat, 08 Nov 2025 19:59:27 GMT  
		Size: 5.0 MB (5029634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd3f4b5743fc827faf2fdcfff0b7d845086ba500db7d47f52cb7d661b48ae09`  
		Last Modified: Sat, 08 Nov 2025 19:59:27 GMT  
		Size: 20.6 KB (20582 bytes)  
		MIME: application/vnd.in-toto+json
