## `eclipse-temurin:11-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:111abcfdf6bf9dbfabe46b58b1a256068b4b634737df20debab569638cc9890a
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

### `eclipse-temurin:11-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:63388a8b68bc827ccd4e81f4b68455080f6633db82538fac8495ceee87a4f6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212716537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60317737061b99255eb5cbbcd815d29d0c7352d1e8adfa2472f99773b0475492`
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
# Thu, 05 Feb 2026 22:15:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:15:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:15:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:15:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:15:50 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:15:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:15:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d399ecdb500e67ab2aceb1aaf84a0f8dba3bbddf55acc1bc6afaf15e0c5605`  
		Last Modified: Thu, 05 Feb 2026 22:16:15 GMT  
		Size: 30.4 MB (30394940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7196d500a546076b20397be4c7c18b62e3777c1cebaa183851d0a090d6c4cc3`  
		Last Modified: Thu, 05 Feb 2026 22:16:17 GMT  
		Size: 142.3 MB (142263284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ab3e2b97e910e6bd0641b3300abd05b3ba729a14025ae6ea936a9a92e5da03`  
		Last Modified: Thu, 05 Feb 2026 22:16:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e907ac62616d876a70f69b6056ccea65b99aaec92d94de513bf1bacbaf8dffe`  
		Last Modified: Thu, 05 Feb 2026 22:16:10 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5f8888dfa0b80d43c2d5c048b8656c788537254ad18c08c3db9ae27a58f1adfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244528ab2aec891567a55e6141b63c6f07ef03def4c324d103c6c97571c4171f`

```dockerfile
```

-	Layers:
	-	`sha256:7b286b7a3b153e53786c25edce119065f98ce41a35779aedd7d212c71b0ae700`  
		Last Modified: Thu, 05 Feb 2026 22:16:14 GMT  
		Size: 2.5 MB (2519672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef932a3720b48566916dfd6d2c0cf0e59a8b32f12bf1b9a28824eebf12a1000c`  
		Last Modified: Thu, 05 Feb 2026 22:16:14 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:730532badcce0c9b70f755fcdec48ec114e7b5ebcf8ea1d753a0cbcd3447ea72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (208008076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e556862e4e58ea22961f0ace2c8ccc84a06528096594d6c91e657abca038a7`
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
# Thu, 05 Feb 2026 22:13:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:13:45 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:15:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:15:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7cd8d2b1f49bcef55b9896e6394b936b78704449a78f01b43bfdf2d814cc9`  
		Last Modified: Thu, 05 Feb 2026 22:14:03 GMT  
		Size: 30.8 MB (30830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9761f2065346cb1c63b496cbdc9a470a0dc00dc8ef9ec4327503241fcc5874ab`  
		Last Modified: Thu, 05 Feb 2026 22:15:27 GMT  
		Size: 139.0 MB (138959733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654516c18d0ec836dc1d72a30f0a724b2b1156e071f6d9eedf3394f0f156f5a4`  
		Last Modified: Thu, 05 Feb 2026 22:15:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b3727dc6a3c953ce857dff1c8919e970379a2a1726ac87bd286a44c032ab64`  
		Last Modified: Thu, 05 Feb 2026 22:15:24 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:06b531458a0855daaf2d0d2b43b77534fcd5c58f8239810ebbbd845ae8ff61c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bb13aeffa51c11f19c7dd3084e5f7dc0bfcc1c5b00e0168c74b609506c46f1`

```dockerfile
```

-	Layers:
	-	`sha256:e800789dd6bc86de55df1e6573a12b267c52fa6c0f9a9a5446fb015f58444e1e`  
		Last Modified: Thu, 05 Feb 2026 22:15:24 GMT  
		Size: 2.5 MB (2519660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe8d636df91af519c7a1175131cd01cbbf49141a496ba7eda3fa0469ea79c51e`  
		Last Modified: Thu, 05 Feb 2026 22:15:24 GMT  
		Size: 21.3 KB (21260 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e6257c0bb1391d70c8b84d8d119ae91993cd8d41f758767ba9e3dc157fa9c870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206839049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03aa1a5d447409ff23dfd04bd0d17d85fe9e88902f4c3d6c83d5e347a2b91ed3`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:19:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:19:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:47 GMT
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
	-	`sha256:bff18c37568ce9885d588b9081a3a8d338a2767979381ae50e386ec667476c05`  
		Last Modified: Thu, 05 Feb 2026 22:20:24 GMT  
		Size: 129.5 MB (129499185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f951dbe571e37d8943b81dff4fc33c3f1a5d0db34e1bf5c0d90bf1eb34d3d4e5`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9af3a15c5a709c86e5f2ea899d294620ef318ccfdfd4dc9afda9cf1ad8b9f42`  
		Last Modified: Thu, 05 Feb 2026 22:20:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2a991bd51de943f4ab6e01ac683c572c3f8ba6e366d67187ffe446d5065772c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c5585d8218bd0a11200b56201e531c9bbbfe25499fcb4256d81ce1d422a6cd`

```dockerfile
```

-	Layers:
	-	`sha256:1951328377a83413ed294df74ad829a608515d2d9115181d677c3d28be5c96d7`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 2.5 MB (2517149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4ed79a26ddce8c0cc155d5be27503798dcf4ac2d7d48583f29fc9085e0fd95c`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 21.2 KB (21179 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:8af3a019e86f249efcb34a4c6994d29f0a2b9dfcaba07d46b595033bac58a99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191516937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a98f5e89d9c4170b07478664dd3e97c2859d5ee6901b767461a12d7ccb11e4`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:14:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:14:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:14:50 GMT
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
	-	`sha256:47eb0d01190f0aec96341b39e0746b1c5e8f96dd7fe2eccacfa54ad16cf49fc6`  
		Last Modified: Thu, 05 Feb 2026 22:15:28 GMT  
		Size: 123.0 MB (122972661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8006203217bf89d99c4f2f69f885b04cc36fa0b4773fa2077851b07f8ae2312`  
		Last Modified: Thu, 05 Feb 2026 22:15:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bf7c318cbf510b16ff95aa6bc2538dbf70adc1b130c753f5ef88ee4670c7f0`  
		Last Modified: Thu, 05 Feb 2026 22:15:25 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fa0f1142150256d63b62bf06ebe2f6afd86bbcb0ab828cc63406e1c14ce5236d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6c6e3ce8668bc1b2dd5f61e72f3fcd8cad30d9949e4fbe3b4d5afb18aa7e73`

```dockerfile
```

-	Layers:
	-	`sha256:0ec9203e3e1a55d46ce6ab4e3bd3fcfd436163f7cca34521d4f20e2c30aa7e83`  
		Last Modified: Thu, 05 Feb 2026 22:15:25 GMT  
		Size: 2.5 MB (2507068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0287715d75e9a7448bd90c53d03fd201c1d85d33309fe7d0564a48ec0ebe07f2`  
		Last Modified: Thu, 05 Feb 2026 22:15:25 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json
