## `eclipse-temurin:17-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:9b915f8a003f0cd07b0da48a2787b5294b02708d1be0cd545efae39caaa475f1
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

### `eclipse-temurin:17-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9a58242a4a1f6683f35b8d9a8b5334e51dc03f5443a497dfb708f1d02ae1c9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216090446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ce869a64982852ee254053d0e14ae02bc3a297f2d8010f73f963058fe4d9c9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 22:16:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:16:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:16:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:16:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:16:50 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:17:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:17:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:17:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:17:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:17:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f83e2f5284b78ba5ad73f3fcfd6d268625a7f5e1ed1836bbc1a8d7df433a17`  
		Last Modified: Thu, 05 Feb 2026 22:17:06 GMT  
		Size: 30.4 MB (30395011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc0a4f9d704d855f7c0b4e961498aa0d7421b71dd269a0a13de30a7ce2ef16a`  
		Last Modified: Thu, 05 Feb 2026 22:18:10 GMT  
		Size: 145.6 MB (145637123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cb0a4e1e49fe8df66514caced73e7cd67782f4aad9c2954269d24185711a8b`  
		Last Modified: Thu, 05 Feb 2026 22:18:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1678fce80630f8cdf6fed1940527ec5bf8c9b6d425393148319dab324528cde`  
		Last Modified: Thu, 05 Feb 2026 22:18:07 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f7d91b944dc5be07d28be31c8d228453e740fc03c5fa6731c8c4bab02b134100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2521299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12971b2eb01247fe6c6d84fd3a901bd084aa5e57a2ce2bdc655919cb0fc128de`

```dockerfile
```

-	Layers:
	-	`sha256:3e8d1a5958f4edfd5a51ab815474d508ba453c47510b25e5f3ec0e7efe187132`  
		Last Modified: Thu, 05 Feb 2026 22:18:07 GMT  
		Size: 2.5 MB (2500156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0852981b4157218a532ca7a8681cac2cc0107a09f1fedfbef290adccd682cfb3`  
		Last Modified: Thu, 05 Feb 2026 22:18:07 GMT  
		Size: 21.1 KB (21143 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e919b7f6957f349ff63be15067aa764414380c35999b2c4fbd72255f82336806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213494911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5426dcad166046be3aa2964b8bc387ec8b2c42860c0430bd87e69c9f4a7b87e7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 22:14:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:14:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:14:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:14:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:14:17 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:16:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:16:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:16:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:16:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:16:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af106f73fff8b8cbc7a98f00d7cd18f3401d2d8c3d8f0c83e70aff6da28d245b`  
		Last Modified: Thu, 05 Feb 2026 22:14:32 GMT  
		Size: 30.8 MB (30830071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d913377b1392bff281cda5a3707562a135077c7c1eeb26f59cc3c9572751b09a`  
		Last Modified: Thu, 05 Feb 2026 22:17:05 GMT  
		Size: 144.4 MB (144446599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48452c05d2446d8ef5e22274cee6806a7d4db4ad7a605d7cb6e116f7597cb7ee`  
		Last Modified: Thu, 05 Feb 2026 22:17:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60b98b5d1c7bb8e14dc6c80d54e15f829ce0c22633d591f7e7ef96e87acad4`  
		Last Modified: Thu, 05 Feb 2026 22:17:01 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c19b27f27f4408b26e2f3ee204e235ec96bda15f182bf5a3b8ee68d26b862a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2520783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9eecb72e6c080d4e278c90096fd846d169f36210e8a008a0304712041befb98`

```dockerfile
```

-	Layers:
	-	`sha256:1840d00bd680cdf553a7bc0d9492cc87fcc4c72b78d135ba76a2f598295db742`  
		Last Modified: Thu, 05 Feb 2026 22:17:01 GMT  
		Size: 2.5 MB (2499526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4832ef8efc9865fb1f6de8994ada787c3f4aa14ee35a0936811916834435787`  
		Last Modified: Thu, 05 Feb 2026 22:17:01 GMT  
		Size: 21.3 KB (21257 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:400b22275174a63d685020396df9474a8db0e19e06b02866a3eb083677a371d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.8 MB (222799807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6042c2daabab367eaceba16c97800b6918065f6b78b5d572580a53238b59a7f6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 05:19:59 GMT
ENV container oci
# Thu, 05 Feb 2026 05:20:00 GMT
COPY dir:88b5851a77c5a8923c1135eccf97b07bb1b1d533881d05c9e3cd86d6a7a70b84 in /      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 05:20:00 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:2deeab01ced2f311ec55a8229431b4137952c26bddd647f35c23005dfebf307c in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:2deeab01ced2f311ec55a8229431b4137952c26bddd647f35c23005dfebf307c in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:20:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T05:19:48Z" "org.opencontainers.image.created"="2026-02-05T05:19:48Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T05:19:48Z
# Thu, 05 Feb 2026 19:47:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 19:47:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:47:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 19:47:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:47:50 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:24:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:24:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:24:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:24:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:24:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4626d1a4e0f331b320f43bc1ebbec9d324207923aa2afcf48e14cccec11d1caf`  
		Last Modified: Thu, 05 Feb 2026 06:10:00 GMT  
		Size: 44.5 MB (44461525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8721df182f63163a820ae421087a60cd6792f46abb4eee0680081557ec55653e`  
		Last Modified: Thu, 05 Feb 2026 19:48:35 GMT  
		Size: 32.9 MB (32875919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a8059a2f2218a9c66f8e4f7d843aa597a3f0bc0057a7a94962bb2c88c50f3d`  
		Last Modified: Thu, 05 Feb 2026 22:25:06 GMT  
		Size: 145.5 MB (145459943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdf74f5e1379df43bd7a6c14bf759e646678ef8fbf0a4389ef96cabf72b9ec3`  
		Last Modified: Thu, 05 Feb 2026 22:25:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1e79e4e61ad1cf0c448e5e64538757ecb43aacb355df0ce3f6365bf819125f`  
		Last Modified: Thu, 05 Feb 2026 22:25:03 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1c8fd0d92f52596a2312baf790d6736b9e19081cae397d96a8be8aa84b6a728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2519428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5626e3875f3957e437a28dc725d5dc474ff7ee8db723fdd6085cf3a01278cf`

```dockerfile
```

-	Layers:
	-	`sha256:648e34cbf77beb0b0f3715d1993589b26c4520a07fe4f5e9e00aea5b65ec55e3`  
		Last Modified: Thu, 05 Feb 2026 22:25:03 GMT  
		Size: 2.5 MB (2498248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c3904f4815461f10a7915846b6f0d5df338301f953b88b09b665870fdc421bd`  
		Last Modified: Thu, 05 Feb 2026 22:25:02 GMT  
		Size: 21.2 KB (21180 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:06df30469abd15276328a673e48128349deed06c2e6a2dfafe62fbd75cd5f30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204173386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef4944f2ff4ed119bfe447f2773c7e83e522a9876d9689a1c4d376c1f214e06`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 05:17:51 GMT
ENV container oci
# Thu, 05 Feb 2026 05:17:52 GMT
COPY dir:0e0d0f454e08e5032aa10e9d7ae13a0cb2cd8a11785e0b58e1a01538558ce0cb in /      
# Thu, 05 Feb 2026 05:17:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 05:17:52 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 05:17:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 05:17:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 05:17:53 GMT
COPY file:748632c315c26c838fdb41aeb4c8e2a22097da0af431c7843ae16d688e0efb29 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:17:53 GMT
COPY file:748632c315c26c838fdb41aeb4c8e2a22097da0af431c7843ae16d688e0efb29 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:17:53 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T05:16:21Z" "org.opencontainers.image.created"="2026-02-05T05:16:21Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T05:16:21Z
# Thu, 05 Feb 2026 19:47:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 19:47:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:47:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 19:47:36 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:47:36 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:18:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:18:30 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:18:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:18:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:18:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f61ab8e0b1fdec6911789bb1a925a7d3cc972464edb07d7ced8c2dff439f9138`  
		Last Modified: Thu, 05 Feb 2026 06:09:54 GMT  
		Size: 38.1 MB (38123371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c353f4c5b4419cc991f4c1d5b64c9fce0e8c324b802cb20167ec931e0841f324`  
		Last Modified: Thu, 05 Feb 2026 19:48:05 GMT  
		Size: 30.4 MB (30418483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031aa2fa3ad8e7a3450e9c4c94bafe670fc7e2d1b4c1b29c21c23b75f4241da7`  
		Last Modified: Thu, 05 Feb 2026 22:19:11 GMT  
		Size: 135.6 MB (135629109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3401eeb0c76f84da969af7b0ac9f6f924de78ee9ff784ae09300da3612ebd3d2`  
		Last Modified: Thu, 05 Feb 2026 22:19:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc9dd6bf12b04afc87307e40ffae92f0157d584f2c63b3715d571a54ed5b7a`  
		Last Modified: Thu, 05 Feb 2026 22:19:07 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:582c9762ca8ef6632888104676b9de9d654009b1dec4fa5835eeb620600541f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107c4090c35e6205c182484725e0ee905ae2d47b3015823873924fafe1d794cd`

```dockerfile
```

-	Layers:
	-	`sha256:1db6f0b0b6862bd58b9564bbcd88a06bb5f211d13d1d033ed5278d085327577a`  
		Last Modified: Thu, 05 Feb 2026 22:19:08 GMT  
		Size: 2.5 MB (2487548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7aa7ec07f5c6033eedbedf50d93761a8cc9cd034b78630e22e68213da45a800`  
		Last Modified: Thu, 05 Feb 2026 22:19:07 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json
