## `eclipse-temurin:23-jre`

```console
$ docker pull eclipse-temurin@sha256:7597763da2056f96505fa3a899c1b9206c117540b0dffe94976569dfda4d5c44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
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
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:23-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:dae8f3deeb48ba738c6ee0067db4b49a09683e613c63a235e34bf6b65efdc746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98052187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d42e3fc236522766e05485c4a8e5de18045169547774cdf52eb92d55dc7188`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1a16c654e67a72dadfa632969a457404ad1cc30c6375857fdcb393e0592ce3ba';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='b2a8a287ebd2d2a1d5d32eb6b79768cf2b5e02f1b4d6d4791297feb8636b9e2f';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='a21355923fdcdcc49fcf6359f2763f49f001bd4caeb970f7313f18aeaa61b588';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='c2c8f8add6af6518cfc565ec0a7410e031301b91f2d8bd594303d7f04680da4e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='0b34d3e945e3e3e25313e0dbad7dfdba1b6c31f2d87e4b0d943581acbcf4fbb2';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a09517e7e3917c1032b417f82525f0831635c6409d3c26fb5711ac48196c79`  
		Last Modified: Tue, 04 Feb 2025 07:35:15 GMT  
		Size: 15.3 MB (15329373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9576a438ad7ba74346eb2b52f3c182cb2b119d67bed47fc73de346df27326b5d`  
		Last Modified: Tue, 04 Feb 2025 07:50:52 GMT  
		Size: 53.0 MB (52966209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc2c47ad38e7d67bad4ca57f090f0adfae22cedec3680888f5bd18a6f2b7634`  
		Last Modified: Tue, 04 Feb 2025 07:49:54 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6a6c325b1ca5d6d0d4b426358d7695914db53286c7639a92c8ed036182c47df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950988adb34a050e7d8cc03169826dbc0f24a6c869cd874c522a13ad351107a2`

```dockerfile
```

-	Layers:
	-	`sha256:b45d5e5530d5213a6beb21b1e27334edbc0c9875e4d044784e3d96af1c229737`  
		Last Modified: Tue, 04 Feb 2025 04:41:12 GMT  
		Size: 3.1 MB (3062384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4a092865b19c366a6d7aef20ecf8aae1720ee8da4bfb42f1c0a2a5c063d0d1`  
		Last Modified: Fri, 07 Feb 2025 19:03:40 GMT  
		Size: 22.9 KB (22913 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8106312283677b1f5a6ae3517ed3971402795e16760b34223ca11175e7a741a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96238864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e21d3d799171fa194bb4de5d8c8087f04457ae08e74b0cd9c3c52f18399b89`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1a16c654e67a72dadfa632969a457404ad1cc30c6375857fdcb393e0592ce3ba';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='b2a8a287ebd2d2a1d5d32eb6b79768cf2b5e02f1b4d6d4791297feb8636b9e2f';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='a21355923fdcdcc49fcf6359f2763f49f001bd4caeb970f7313f18aeaa61b588';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='c2c8f8add6af6518cfc565ec0a7410e031301b91f2d8bd594303d7f04680da4e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='0b34d3e945e3e3e25313e0dbad7dfdba1b6c31f2d87e4b0d943581acbcf4fbb2';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c1ccc74d495ffee1d088a99f1c96cfc84fe3bd2364face0055ec84e68d005e`  
		Last Modified: Tue, 04 Feb 2025 20:33:37 GMT  
		Size: 15.3 MB (15323625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4906befdd2056fd131b53d8805108880d3bd1bfee2f48d892cb30dc408d702`  
		Last Modified: Tue, 04 Feb 2025 19:41:37 GMT  
		Size: 52.0 MB (52019327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d4e431c4643fc52d3dff8bbdc4238c3fd0db5294ffc05c36095d14fceed3ab`  
		Last Modified: Tue, 04 Feb 2025 20:33:31 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e67d6d0656aa8ed22d6aed7be6278ea753ff77b1abd84f3dd4f78a171ee3f2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecadf64ecaae29913ced1ce99fc609dc968fccae39abcf649d4c2acefaae6206`

```dockerfile
```

-	Layers:
	-	`sha256:dfecb63ea7bd07d2530d46d683da7fb9b53578576ada6b0e8c0efb544ac5c44a`  
		Last Modified: Tue, 04 Feb 2025 09:27:24 GMT  
		Size: 3.1 MB (3062224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bbe642aedf61b86ba8aa37d39e4350a12ad7f116f6e496e292558e3df40cbaf`  
		Last Modified: Fri, 07 Feb 2025 19:03:49 GMT  
		Size: 23.0 KB (23047 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f9b5e563851cf42dfb6a267d595017f0b42e95b09dc9027fc35a64485489376e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104020486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db688203da3e2404f61014a27ad27e18e946790026d2607436588e6977f95109`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1a16c654e67a72dadfa632969a457404ad1cc30c6375857fdcb393e0592ce3ba';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='b2a8a287ebd2d2a1d5d32eb6b79768cf2b5e02f1b4d6d4791297feb8636b9e2f';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='a21355923fdcdcc49fcf6359f2763f49f001bd4caeb970f7313f18aeaa61b588';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='c2c8f8add6af6518cfc565ec0a7410e031301b91f2d8bd594303d7f04680da4e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='0b34d3e945e3e3e25313e0dbad7dfdba1b6c31f2d87e4b0d943581acbcf4fbb2';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e466bbaab5f7701cf968c729e620418f61a018b51d10ad23b3e95b8ada4a2490`  
		Last Modified: Tue, 04 Feb 2025 07:51:54 GMT  
		Size: 16.8 MB (16779285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8acb8eb6c80d7d9bf199aa4af622199cad1a691eca27e74ffd83a530579237`  
		Last Modified: Wed, 05 Feb 2025 09:49:54 GMT  
		Size: 52.8 MB (52849062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5224c10493f5dfdee3f7804928d025296b04f54c3d499b30eb1207fdb68234`  
		Last Modified: Wed, 05 Feb 2025 09:49:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:612b205289e566ea0ad79d2c67fedba6777a53253ac4292bd4542ba05ccd1970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0a04bd354b99fa93d38788e364a3a21629e88c4b463576c0e677741e5e338f`

```dockerfile
```

-	Layers:
	-	`sha256:bb978c8ef5fc2a0e1c550c0fa8c7ac84ba628fc8326170f08f2c8bb8f4a207ac`  
		Last Modified: Tue, 04 Feb 2025 07:51:53 GMT  
		Size: 3.1 MB (3065621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e7492fdd6e7eec11ecface52c38b9760a8d694d035a56b20113451d059004f`  
		Last Modified: Fri, 07 Feb 2025 19:03:59 GMT  
		Size: 23.0 KB (22961 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:4c11f698d63cfd8fdcde0246222546eb4e7d8310eabbf5d7a0210499f57acabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97740723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f25ba59c15cd873c0084a79fd26510aba453310a06020f3f621ccce7228735`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:46:38 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:46:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:47:10 GMT
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Mon, 27 Jan 2025 04:47:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1a16c654e67a72dadfa632969a457404ad1cc30c6375857fdcb393e0592ce3ba';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='b2a8a287ebd2d2a1d5d32eb6b79768cf2b5e02f1b4d6d4791297feb8636b9e2f';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='a21355923fdcdcc49fcf6359f2763f49f001bd4caeb970f7313f18aeaa61b588';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='c2c8f8add6af6518cfc565ec0a7410e031301b91f2d8bd594303d7f04680da4e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='0b34d3e945e3e3e25313e0dbad7dfdba1b6c31f2d87e4b0d943581acbcf4fbb2';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Tue, 04 Feb 2025 07:00:41 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab8c9919375adf91e031abe2b6fec76f63a29ac570cf850ac27cd9af673c6f`  
		Last Modified: Tue, 04 Feb 2025 05:24:02 GMT  
		Size: 16.1 MB (16098065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5beadcb9c7be23fe11db274f3e831b3aecf6ba3ab8cd33cc17eb3f94959d767`  
		Last Modified: Wed, 05 Feb 2025 09:49:55 GMT  
		Size: 50.7 MB (50656433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1323944876260b60f009dbffc1ea832bbfd8fc30632cc54de6c80c6459901eee`  
		Last Modified: Fri, 31 Jan 2025 02:18:24 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4d915e13406f95f70c4030591f81c2c52a8381c1ee613b23ab5083a29f018008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3076920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1e6cc12c0cebe580032abb14e7f28f2c1d831eb640522066fe24d15103bf57`

```dockerfile
```

-	Layers:
	-	`sha256:69ec8b5fa66659b6afb161479081dd880f4bb9ace3a5b794d8e0d75bd36404f7`  
		Last Modified: Tue, 04 Feb 2025 05:24:00 GMT  
		Size: 3.1 MB (3053959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b00a9bdce262158a361fd1c0b0a3ff6c83b711bb9c0aa1534de4b9e8ab61c79`  
		Last Modified: Fri, 07 Feb 2025 19:04:09 GMT  
		Size: 23.0 KB (22961 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:4b6c3703f12ebdb8330a435468032d8a29adcbf17239f80fe7ca770499988716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95380024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d287e2d14ad81f8b3af33605b338dbc7eb9f98089d451bfec485f0b57d63ad73`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:15:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:15:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:15:20 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Mon, 27 Jan 2025 04:15:20 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1a16c654e67a72dadfa632969a457404ad1cc30c6375857fdcb393e0592ce3ba';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='b2a8a287ebd2d2a1d5d32eb6b79768cf2b5e02f1b4d6d4791297feb8636b9e2f';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='a21355923fdcdcc49fcf6359f2763f49f001bd4caeb970f7313f18aeaa61b588';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='c2c8f8add6af6518cfc565ec0a7410e031301b91f2d8bd594303d7f04680da4e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='0b34d3e945e3e3e25313e0dbad7dfdba1b6c31f2d87e4b0d943581acbcf4fbb2';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Tue, 04 Feb 2025 08:21:20 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba121be1d103d37674b5a23b0e17431f1c1c16e3c48a83f28f607052a53bd6a`  
		Last Modified: Tue, 04 Feb 2025 07:57:07 GMT  
		Size: 15.9 MB (15883170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a174e4bdd56794658846f595213e5b59c198519cecb8b3eec5f206db780a0c5`  
		Last Modified: Fri, 07 Feb 2025 19:04:16 GMT  
		Size: 49.5 MB (49466976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496f8b1a23100fa91933d57c8532a4525c86573808b28dab82e8af5e406dcf7`  
		Last Modified: Fri, 07 Feb 2025 19:04:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1e58a8f764d19f19877eacde6caec4879b615de516be51191a0fac0b448bee79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3086885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cfdd73fd5aafea2feaadebacd676d6498a05ba4f447e387014dd931452ba0b`

```dockerfile
```

-	Layers:
	-	`sha256:e62e87572e4c90f9f89c0cf5980b7de4166efea36eec9a10334e9941ce4f1830`  
		Last Modified: Wed, 05 Feb 2025 09:49:54 GMT  
		Size: 3.1 MB (3063973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d838164a9a9919f9c3c9ac4c2be0df923a1cc0c5447a88c1e792019db5293eff`  
		Last Modified: Tue, 04 Feb 2025 07:57:06 GMT  
		Size: 22.9 KB (22912 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:1d5b3d38fd32389f18d68c265385c5ba28f7290eba0e38ddf96d62b2b323a359
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2584500660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e68ba5dced4d4d62da444a5583c186d3218fd8b4a0a38d8f87c4ca4b89ba43`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 01:35:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:35:13 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:35:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:35:38 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4feda805cc910b20ad35875f9c399f5e411b198d10001e2933e4411c0c5c5ef`  
		Last Modified: Fri, 31 Jan 2025 01:35:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea937d872eb81b11103320fa34507a345f81b6e8a240cd938a60951a0e695aa`  
		Last Modified: Fri, 31 Jan 2025 01:35:40 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb37ab49d6f95950941963cda5bcd58d2e96858e311c498d93f995d443b67ed`  
		Last Modified: Fri, 31 Jan 2025 01:35:48 GMT  
		Size: 83.8 MB (83826556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd5589b0894a703c313129106b22f6f9001eb64e7323e6428a70d6cb44a55b2`  
		Last Modified: Fri, 31 Jan 2025 01:35:40 GMT  
		Size: 393.9 KB (393936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:9973814cce470eeae450d7a8493fea1dd4ac554aef0731e015ac9c97a3ad7cb8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346514748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e86a436ea68829845137d7f2798686396620a7293eb86a8b28bda928a5607a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 01:30:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:31 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:31:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:32:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 21:54:27 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02c54efdb6c7c8d372ff2c5e4b8cd49253a1aece02ebaa0d7c860f95baf793b`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb2921b8a7cb101c5da9e2a545f9a29f05fba5908c68fe5e47f26b0bcc05f90`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1324988da678383e030f5f916d35020f87f2c9c58a540f1fc1f0371c012a250`  
		Last Modified: Fri, 31 Jan 2025 01:32:13 GMT  
		Size: 83.8 MB (83799630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a67400351edadf6fad844da0dd811e4e2731a4d603bc512a23d270108c7acbe`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 327.3 KB (327290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:3be34c964b4142bad6d7989a2031bbd59b93dd26184cab3128adf0640129e15d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2209879561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b6a54120085002fb0834bf894b90a3efb8326be0a759ead54e17ea562c115d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:30:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:31 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:31:43 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07ddf8b8d004692261d0ab769a31176abd22b5203cee44317328f9113a99e486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:31:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 20:54:32 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220ecb0bb24b174b973fb5007cddcd591f2e577157e0146f2aac383e77952592`  
		Last Modified: Fri, 31 Jan 2025 01:31:56 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b5e3ce265816a3760eb5fcca2e29db5fb4093aadd07425cddd990923f3a88`  
		Last Modified: Fri, 31 Jan 2025 01:31:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd04f2d57b3eb8f451a2ce046693d32328d7b59361714f3550d2ee141f51454`  
		Last Modified: Fri, 31 Jan 2025 01:32:02 GMT  
		Size: 83.8 MB (83797056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dc0a95911cdb36c2a6c3283e614420e41365ed7ece6cb610b3f26a451b6d6c`  
		Last Modified: Fri, 31 Jan 2025 01:31:57 GMT  
		Size: 3.9 MB (3867729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
