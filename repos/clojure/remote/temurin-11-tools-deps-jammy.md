## `clojure:temurin-11-tools-deps-jammy`

```console
$ docker pull clojure@sha256:4a80307ed3d659072de5901def378f46d88f66806cd47ce0fadea2b1ec62ed74
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

### `clojure:temurin-11-tools-deps-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:9c852fb6345d642bcc2cfefaf5594517eb456902f4c896d6161c33d32c8b762b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239649868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e924ae49ca7479907114807c7cdd4a64bec97e3c2b622cf7748079dd199894`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:15:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:15:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:15:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:15:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:15:39 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Fri, 15 May 2026 21:15:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:15:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:15:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:15:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:15:48 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:45:35 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:35 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 04 Jun 2026 17:45:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d630b784a3d3c9e89518a3acf4feed5d7c54447839cc18c301cb7ee245ea2b18`  
		Last Modified: Fri, 15 May 2026 21:16:05 GMT  
		Size: 16.2 MB (16152906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660cc62ff9718679c89d9b11fa428f76c19a80043d5e4a52642a19024c1dbd03`  
		Last Modified: Fri, 15 May 2026 21:16:08 GMT  
		Size: 145.9 MB (145894804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f18ccba1d1821eced1a7f822772a225b57df5bead923ad01f1c37e1ebe0bd63`  
		Last Modified: Fri, 15 May 2026 21:16:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc4e063649e4b9bb51446107f7bd0b01455593ee345f7fc125f78260e914a4c`  
		Last Modified: Fri, 15 May 2026 21:16:04 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198a9ec7663af790206ad4bc4c2dc300dc6a84a7ab0a202e2334af1b2fabbe6`  
		Last Modified: Thu, 04 Jun 2026 17:46:03 GMT  
		Size: 47.9 MB (47862385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfb5040da03a207864b41d2abff0784d76ecb29e5eb5b5187aef414f7f6bfe0`  
		Last Modified: Thu, 04 Jun 2026 17:46:02 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:356f483b9d22f16cdd7237b63e3d46ad5f65bf557255445572113076b5b8de98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c278ef018bf1abeb8b249221cc06f92846ba50a9f2bc9b357fb89795549a4fd`

```dockerfile
```

-	Layers:
	-	`sha256:e0e5ac6913dcfcbd137a1d10424fb56e39cfc8a223fe70d06d48e4ce75e0d39b`  
		Last Modified: Thu, 04 Jun 2026 17:46:02 GMT  
		Size: 6.3 MB (6320788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a148451545bf29f112fd1983febf6eae56e6028615cc88e40aa2404164c76772`  
		Last Modified: Thu, 04 Jun 2026 17:46:02 GMT  
		Size: 13.5 KB (13508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab27378791f16fed7eb47883200d226444c2ec29e5d0ba04dfbc4842ccc71efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234112367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690d741908c5a6107f80dbc0616864f44ddd6a591cd5a62168e1aea6965d28e3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:15:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:15:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:15:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:15:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:15:53 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Fri, 15 May 2026 21:16:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:16:01 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:44:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:44:50 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 04 Jun 2026 17:45:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c0ae0ac078a442fed4e0a97dd8c4968165e92052e49fcae3c3f233abbd0eca`  
		Last Modified: Fri, 15 May 2026 21:16:18 GMT  
		Size: 16.1 MB (16076234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364c6c40357b481b1b26c6c11720de3dd72a3bbad7f499971f103efc79addf83`  
		Last Modified: Fri, 15 May 2026 21:16:21 GMT  
		Size: 142.6 MB (142588521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bc326dfe4ea11f21f0f0bb4f6a5686fdd140b95fe1125f158abb88239deb77`  
		Last Modified: Fri, 15 May 2026 21:16:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb50d9aa1fdda8a54b2787672840c41a0cc1165e14d3f515c888e3cde82ffb`  
		Last Modified: Fri, 15 May 2026 21:16:09 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa75a270a7f84817500fb365b0a18ffab50478ec68cca565230af7b28bb0c8b2`  
		Last Modified: Thu, 04 Jun 2026 17:45:19 GMT  
		Size: 47.8 MB (47837903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaeb4d055620f8b2a41d242570843695172adeac2b4bfdd4f657a9312d69acb`  
		Last Modified: Thu, 04 Jun 2026 17:45:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:ae703602a791cccb30b734edb4cfb2899a30635a2df3de7b4c8ba07f4d7f6f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab27d3f55ecf3e6a8ca8e9ba79f7048f03a56639565d847d5511e35874ce191a`

```dockerfile
```

-	Layers:
	-	`sha256:98ef0f026df5af49af8679386f9f7ff033660d4c95229de28dd37291f524c2c4`  
		Last Modified: Thu, 04 Jun 2026 17:45:17 GMT  
		Size: 6.3 MB (6327172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22dadbf69d4b15b285d54ec54cf53c96bc1f118b0691e4e60422c6cac4d895e4`  
		Last Modified: Thu, 04 Jun 2026 17:45:17 GMT  
		Size: 13.6 KB (13600 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:7df9f73e65180a3f24ee22f5571a77325649f4a4a9ee58c91d91a00f1978b705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237208604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffedc6fc866407dc238962b6d68d5cae64cc07399c2bc85cc8b8e5cdc40a6e1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:10:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:10:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:10:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:10:20 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Fri, 15 May 2026 21:11:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:11:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:11:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:11:16 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:48:52 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:48:52 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:49:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 04 Jun 2026 17:49:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:49:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74563760a17437dfb610242b605ae18edc6feef6143f0f512cfd8f6e66afb898`  
		Last Modified: Fri, 15 May 2026 21:10:51 GMT  
		Size: 17.6 MB (17625928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b621f40887b3b7f679f0045e8efd6608dce4b71d6f4a5a3365298cdaa4850835`  
		Last Modified: Fri, 15 May 2026 21:11:49 GMT  
		Size: 133.1 MB (133123367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf13ce02d18691272e15a971dd1a78e8c684c9bce92bebe750435e81e2d9fec6`  
		Last Modified: Fri, 15 May 2026 21:11:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75555ec41b0bb7fa0548e73a9eac0d5136fe7088c82b25a62a4599ab80f89744`  
		Last Modified: Fri, 15 May 2026 21:11:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81cb3759df99704010b0148e8d1f5bcfe5e8dfacd47e452611c9d952f7540d8`  
		Last Modified: Thu, 04 Jun 2026 17:50:00 GMT  
		Size: 51.8 MB (51809499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972583b5a15cf547706cf5005371a4dd9d9cc03fbdfedc91650708a2cb442819`  
		Last Modified: Thu, 04 Jun 2026 17:49:58 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:6de13dcd5cf287f5c31dc881ddf43059b8b8a4d57c4e25c04fadbc8b32d57cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6338942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a75714046c5f135f67e2033b5e2712ed4e45fd75b2a2cbd4f5345e92569341`

```dockerfile
```

-	Layers:
	-	`sha256:3ac631120faf98331e11d6c357bcd37cf75a9ac0496c606f34eceaff5ac83ec1`  
		Last Modified: Thu, 04 Jun 2026 17:49:59 GMT  
		Size: 6.3 MB (6325396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f95a493ca27f5c4076820d6bc2fff82bc41af9912775204cd17e47fbace1cdd`  
		Last Modified: Thu, 04 Jun 2026 17:49:58 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-jammy` - linux; s390x

```console
$ docker pull clojure@sha256:27b273e3cfa89c45aaec1d0470eab8036d9a2ef35c4a6da5b1076eccc284f2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218871082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab7a64c0f359c7294dea0fab0a4d97d16beb62556225e4fdbb7f45291cbc838`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:12:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:12:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:12:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:12:14 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Fri, 15 May 2026 21:12:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:12:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:12:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:12:32 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:40:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:05 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 04 Jun 2026 17:40:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:40:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cb997e338ec619cbc0e124d371f4da963043155539b97992361ce020bfd40`  
		Last Modified: Fri, 15 May 2026 21:13:18 GMT  
		Size: 16.2 MB (16151221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f06449f41a26d9d99a3f46291d4bb9093885440ad621b6d9f7c154680ebd81b`  
		Last Modified: Fri, 15 May 2026 21:13:27 GMT  
		Size: 126.7 MB (126662685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4acec68e3e02bb7dcb8a25b9ec886efb000abce2ae691c218f56888b029563`  
		Last Modified: Fri, 15 May 2026 21:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463625b62adea2aaf5460220acec27c97ea373f1fcd073e668dfed2dbe8005cf`  
		Last Modified: Fri, 15 May 2026 21:13:16 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9a313613c94cb6f7fd5a33dfd13ac38d8554b51d2c64ed0aa9a38d2549903d`  
		Last Modified: Thu, 04 Jun 2026 17:40:45 GMT  
		Size: 47.9 MB (47851781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fab0fde16b584dfeba60b87bdad5ef0a6659046ca61cc56460b0bd40fe66e90`  
		Last Modified: Thu, 04 Jun 2026 17:40:45 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:fd848e9dd0b09a9df01ddb41b37ff5a0c75eb3b2af8d9b91e78f33e0d7969721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3ffbacc79d65603c693f4dc78180c45ff4053f098145309dd608e6987a6d64`

```dockerfile
```

-	Layers:
	-	`sha256:fe2363eadf8d2ae250ca5b8a9f6465aa98c88a14a559274ad8ddde92240868b4`  
		Last Modified: Thu, 04 Jun 2026 17:40:45 GMT  
		Size: 6.3 MB (6316715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2a3605f2353853d29b9b7bf92f5016e5f49a8ac14896cd045ce6f857a5e2938`  
		Last Modified: Thu, 04 Jun 2026 17:40:44 GMT  
		Size: 13.5 KB (13508 bytes)  
		MIME: application/vnd.in-toto+json
