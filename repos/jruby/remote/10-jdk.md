## `jruby:10-jdk`

```console
$ docker pull jruby@sha256:d95c2daf584dd894369f72efe10cd1cde4de50b60c56948a4fc4d1fd015db96c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jruby:10-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:dcd283a104a722340e7ae75a132d6ef0e963d85e4b09ad642b01073b2d78a30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277628542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ccf1e83e5c823fac1d72e341d6ea18a30fa7d9aa0e4df73eab258faa47f872`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:07 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='ac411d52862fe8a4a48a6c3546bebced8f4879cd728746fc4ee4b06151aa9f8b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:20:14 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 17:49:06 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 17:49:07 GMT
ENV JRUBY_VERSION=10.0.3.0
# Thu, 05 Feb 2026 17:49:07 GMT
ENV JRUBY_SHA256=0edb5b02c3f482205d1cf8358f38e31d9e4c6d93a210039224750c72501e4717
# Thu, 05 Feb 2026 17:49:07 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Thu, 05 Feb 2026 17:49:07 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:49:07 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc # buildkit
# Thu, 05 Feb 2026 17:49:13 GMT
RUN gem install net-telnet xmlrpc # buildkit
# Thu, 05 Feb 2026 17:49:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 05 Feb 2026 17:49:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 05 Feb 2026 17:49:13 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:49:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Thu, 05 Feb 2026 17:49:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220e5f46c2556ad3d4e13b9f9820a6a493d998f1bc423515840a27d7a4f41ffe`  
		Last Modified: Thu, 15 Jan 2026 22:20:30 GMT  
		Size: 23.0 MB (22961225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3307ab29355ce71f400857b35cca7442414151b6d8d767171d67282f986ad07`  
		Last Modified: Thu, 15 Jan 2026 22:20:33 GMT  
		Size: 157.8 MB (157839172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ebe7eabaf26192ec8e30edade0a6df98ef2590420dfb0ef843456388a54147`  
		Last Modified: Thu, 15 Jan 2026 22:20:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8fd45c97cdc03c294a3813fd5dbdfccd2e3609de14ffa984b6f160afbb7edf`  
		Last Modified: Thu, 15 Jan 2026 22:20:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b269d06eef45c61f31fad920e5c395a008f2d00af2b5d749e7c6bd0b199530ea`  
		Last Modified: Thu, 05 Feb 2026 17:49:27 GMT  
		Size: 18.7 MB (18653984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04aa52682b89b586f60278ee124a5172526e9ce98e3e46ee3a98c43b183c0a0`  
		Last Modified: Thu, 05 Feb 2026 17:49:27 GMT  
		Size: 36.1 MB (36121148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da9abb8ca1c6ce437857c4373599934fb9384c62053ed08903544dd56856575`  
		Last Modified: Thu, 05 Feb 2026 17:49:26 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ac7e92972d48334b12cff062a52b036f1373effaa94e88ed67d8985dc7d307`  
		Last Modified: Thu, 05 Feb 2026 17:49:27 GMT  
		Size: 12.3 MB (12324223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a1d6efbb133307cd0e26e4c8c111fade3c48f4028f20bfd3637b7f8b57d00b`  
		Last Modified: Thu, 05 Feb 2026 17:49:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:10-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:51e7d6fc0cea7ecced50fa5c5dc9d662b34ed0b449560892dc4edf296421b961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4944760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb70ccd57701380963a2ed3f24dcec3e92af18c24df017d9d69bf0c6282ddcdb`

```dockerfile
```

-	Layers:
	-	`sha256:0008a10d630a65c6c31e66bcf442834ec1a811a88ba7c7de45f9e025d86ad714`  
		Last Modified: Thu, 05 Feb 2026 17:49:26 GMT  
		Size: 4.9 MB (4924414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5ab4b29702de0dcf39b0f133775d173a3d0646cc2d8ea02962a0bed7611813a`  
		Last Modified: Thu, 05 Feb 2026 17:49:26 GMT  
		Size: 20.3 KB (20346 bytes)  
		MIME: application/vnd.in-toto+json

### `jruby:10-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:c79666101a294e7423b72fead858b34b04d0c062a2bde12f80387dead2ee8f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274945940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e20e269ee139b985c5a71fbe0a5be0b76ce6d0a4a39ecf7544f3812660200c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:39 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='ac411d52862fe8a4a48a6c3546bebced8f4879cd728746fc4ee4b06151aa9f8b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:20:47 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 17:50:05 GMT
RUN apt-get update && apt-get install -y libc6-dev make --no-install-recommends && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 17:50:06 GMT
ENV JRUBY_VERSION=10.0.3.0
# Thu, 05 Feb 2026 17:50:06 GMT
ENV JRUBY_SHA256=0edb5b02c3f482205d1cf8358f38e31d9e4c6d93a210039224750c72501e4717
# Thu, 05 Feb 2026 17:50:06 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1 # buildkit
# Thu, 05 Feb 2026 17:50:06 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:50:06 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc # buildkit
# Thu, 05 Feb 2026 17:50:13 GMT
RUN gem install net-telnet xmlrpc # buildkit
# Thu, 05 Feb 2026 17:50:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 05 Feb 2026 17:50:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 05 Feb 2026 17:50:13 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:50:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME" # buildkit
# Thu, 05 Feb 2026 17:50:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733d8aa488b55ac09113fb6923a025dd6c789770c55b738387a34a5cad1bf82e`  
		Last Modified: Thu, 15 Jan 2026 22:21:04 GMT  
		Size: 24.2 MB (24166529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2014bd5938928d55149f3bd12aafc9edd2b2564be58b1b8f4741a761c254d773`  
		Last Modified: Thu, 15 Jan 2026 22:21:07 GMT  
		Size: 156.1 MB (156108045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205e43b16a07ab88cb31484712b906ca3fe032a61a21b18c69765799353c4b3`  
		Last Modified: Thu, 15 Jan 2026 22:21:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313b0162d5f630b291fc13a699023e777b0b5a20343c7c6b72c776d70a0b9ee9`  
		Last Modified: Thu, 15 Jan 2026 22:21:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8c9b7324cd303f97bedf5a0bdf7f9555e10d2dc9a60e5ade93ca4ba17037ec`  
		Last Modified: Thu, 05 Feb 2026 17:50:28 GMT  
		Size: 17.3 MB (17325787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdf9fc8fafdd8fcea5bb29b0a4345f723f1a43759348ddda052840260e1f7bd`  
		Last Modified: Thu, 05 Feb 2026 17:50:29 GMT  
		Size: 36.1 MB (36120450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b6e2c2da874d0474e063b61e776c3b28bd1160e20e118cd84e2be4997ea733`  
		Last Modified: Thu, 05 Feb 2026 17:50:27 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95aede09c2783c7b443a6c1f04d27c21c807d461448aeabc57aa2651beb467f`  
		Last Modified: Thu, 05 Feb 2026 17:50:28 GMT  
		Size: 12.4 MB (12358522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56638378e6f733c36a8f9ecf28e543afce812a363a4af2f983e34ade19a960cf`  
		Last Modified: Thu, 05 Feb 2026 17:50:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jruby:10-jdk` - unknown; unknown

```console
$ docker pull jruby@sha256:6cfdd4b6aa893e9ebe40779dfff289dc443d89abb830a465ca109defdc3faedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12190a1c4ba0f02f4e4332e501c09b6cc6ef507207a6fd5c0fa0a0ae4b448196`

```dockerfile
```

-	Layers:
	-	`sha256:647f7799f72fa45e5f1418e168349ebf233daaad92a21652867ac466fb2d060e`  
		Last Modified: Thu, 05 Feb 2026 17:50:27 GMT  
		Size: 5.0 MB (5028506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c7466bc2c8b6fc06b1b4bac4be40f154765c2a5548ab4091ebf97d6a86b59d`  
		Last Modified: Thu, 05 Feb 2026 17:50:27 GMT  
		Size: 20.6 KB (20558 bytes)  
		MIME: application/vnd.in-toto+json
