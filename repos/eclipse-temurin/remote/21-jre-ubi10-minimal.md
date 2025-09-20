## `eclipse-temurin:21-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:ff2324550b0344c3d62296d10789bab1dcdb5a6fdc7da60fb79330f5f9933029
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

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b29a520f23e891ac0f4be9fb8fdb48c19fa570eea219e83671f727732970c4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141476965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad04ef0071994c4d6d577b38447582174b9a02f52a98978d16cad0b85410e5b0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:803739b98e03bf68bf6a38a8f6483d10fe821f02411e40ca88b9cb4b28dd4154 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:2c9300aa2a82321bdb1295eb5cf59270c200f77d73b01c9b866932f5e4bf93c1 in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:2c9300aa2a82321bdb1295eb5cf59270c200f77d73b01c9b866932f5e4bf93c1 in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:66650c37460078d8c2d0cd24db860f6161318b74f8ec36e265e5dfc8b2c68b38 in /root/buildinfo/labels.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="006ec712cf2384ae208886f1374479d6db3cf3ef" "org.opencontainers.image.revision"="006ec712cf2384ae208886f1374479d6db3cf3ef" "build-date"="2025-09-18T08:57:28Z" "release"="1758185635"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c7c1af01dcba6b2246e3016b8a9343366229fe2c0139e83fe302779c89327e03`  
		Last Modified: Thu, 18 Sep 2025 18:15:04 GMT  
		Size: 33.4 MB (33421910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841d23301283eafa15c6f4be76a9e75821a877a079e99d9bb8b5ce9d36be7c5a`  
		Last Modified: Fri, 19 Sep 2025 20:44:22 GMT  
		Size: 55.1 MB (55087840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6130c9eda7a782c42f0a35a9c91657cb460b7286a77326e1dfeb197a022fac49`  
		Last Modified: Fri, 19 Sep 2025 20:45:11 GMT  
		Size: 53.0 MB (52964797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c58b8af750a6f585cae96ec83fe0c8c6edbb91d14a4ed394fb7d7882cde142`  
		Last Modified: Fri, 19 Sep 2025 20:45:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70cddb0f34b7d8b4795f1b62129919dac62de60fd6fd55f43d0f203c54a000`  
		Last Modified: Fri, 19 Sep 2025 20:45:00 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ed364ca5f6f8c0c4ebb5afd2d7878b56f2a7d9001ade7c6d13ad201c2941fe22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1195faaf1de04e3a10e2866680aba8f70bfaab9357eac2935ef07b092bbcf2`

```dockerfile
```

-	Layers:
	-	`sha256:e2d1a220ed044c1f327e040df94decfc2e0140461eadabff625fd5474f396413`  
		Last Modified: Sat, 20 Sep 2025 00:16:03 GMT  
		Size: 5.6 MB (5591972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73abc39a33a871ac10ccb913b484543ff0d88d77a9154c46dbcd1f30e441e98`  
		Last Modified: Sat, 20 Sep 2025 00:16:04 GMT  
		Size: 20.4 KB (20373 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6ccc85bee7c8015becd2f6dfbdfe87d5b879e840cb8ce9fc9ca357d9826b1df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138568769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c0137696a188ad076821e17e033d4c19aae49919153514a693480d1e2f84e4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:33992e65f9cf921a4a25b5fc80aabaf97b1bcbc7a300c349ab96d3b192356905 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:d6bed8458a41401e1eb450fa7dee5de0cfd1eb9af941fb4d4091d55094ec9222 in /root/buildinfo/labels.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="006ec712cf2384ae208886f1374479d6db3cf3ef" "org.opencontainers.image.revision"="006ec712cf2384ae208886f1374479d6db3cf3ef" "build-date"="2025-09-18T09:02:08Z" "release"="1758185635"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a7185aa967c4147e64b2e1acf0e7c0053597895038769c26379a2e4b5bbbbc17`  
		Last Modified: Thu, 18 Sep 2025 18:15:06 GMT  
		Size: 31.6 MB (31559410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be73ef13b8794f9c91c9f96773279e6c8b971db35bb7fd3c7015139db88591c`  
		Last Modified: Fri, 19 Sep 2025 20:45:02 GMT  
		Size: 54.9 MB (54863402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739342d6d65eab2238c5219b21aaf34f8e4a58b1cbadd0561feda3a80a256198`  
		Last Modified: Fri, 19 Sep 2025 20:44:58 GMT  
		Size: 52.1 MB (52143540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bea35b02f54ebd56be42f72f534036e8f6d47ee7ad80ec6d71e5d4060079ef2`  
		Last Modified: Fri, 19 Sep 2025 20:44:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05ae6b152a53df0f3a40eed87088fa6d39110e8b73653d016858c7f116af25d`  
		Last Modified: Fri, 19 Sep 2025 20:44:51 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9f496a5354fc00db0956092dda922f5bf2b5747187dac488fd9248699ced90cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b26d6faa40e781297f41a7a5ebc9653293f96e59a7e29f1642daa975c410b`

```dockerfile
```

-	Layers:
	-	`sha256:4d27485be3be5bb550637ef8bb80bfbfbb6e765d72e6491f840c0786cbc0bc3d`  
		Last Modified: Sat, 20 Sep 2025 00:16:09 GMT  
		Size: 5.6 MB (5591450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63de2ba6b45939bf2e32276f5337c196cf3a90aa72cee568dd1ba21a102d3282`  
		Last Modified: Sat, 20 Sep 2025 00:16:10 GMT  
		Size: 20.5 KB (20477 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:3b9860a174b2f75664b9ccc8e4db7c15a0ba75d44a58d2c3e7c674e7e1d50ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146862165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07eb81c15ecbf6e642b56cc901255a0c9dd9e71e547cea6d702fe7489bf86447`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:a9eec0dbfd64b4e3799eacf95d2a455550044cefbdae6843b3a86713e7aa8a30 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:c1a94e993cf7eb52a4e10bcb4b214f43512d41819a7bbe81e1a8e1ffd179babe in /root/buildinfo/labels.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="006ec712cf2384ae208886f1374479d6db3cf3ef" "org.opencontainers.image.revision"="006ec712cf2384ae208886f1374479d6db3cf3ef" "build-date"="2025-09-18T08:59:19Z" "release"="1758185635"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5ed0c627d2764f746fe46dd17129e3a0ea21b975c8032517caa92f755bca083b`  
		Last Modified: Thu, 18 Sep 2025 18:14:55 GMT  
		Size: 36.8 MB (36783077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc85e798b4af5ee8a38ad1cd1661824c5cd485095c534ba4b2a107f85ef94b22`  
		Last Modified: Sat, 20 Sep 2025 00:49:07 GMT  
		Size: 57.1 MB (57089564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4037b0e715fba5323f88047c52542d45fb318574329ac358daffce1a275167d2`  
		Last Modified: Sat, 20 Sep 2025 01:03:52 GMT  
		Size: 53.0 MB (52987106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f432e712f68dae6d2155aa1afe8f8225eab32f85d3082558e72aec7c3029d89d`  
		Last Modified: Sat, 20 Sep 2025 01:03:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c14435e55886f72718c2ae7bc164360b32fb1f53a1b3239533127715d43c7b`  
		Last Modified: Sat, 20 Sep 2025 01:03:50 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0aba4af3f6a0f5be6ae067417d00336524e746e455b9c9a2d4aec9e69af7373f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5601440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eb15bc11e2d21efb2b9a91d038d08bda9608bdb37e1236e8365e1ae3bde2d2`

```dockerfile
```

-	Layers:
	-	`sha256:c2317c0826e8cc7e7cda67e59b34f8f72b872c2fd6ac836a3ddc1ef71487ab2f`  
		Last Modified: Sat, 20 Sep 2025 03:15:02 GMT  
		Size: 5.6 MB (5581037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4becc0195db2c271f46028f1b1afe2a1a53e17ea4f80172fb100366452645a00`  
		Last Modified: Sat, 20 Sep 2025 03:15:03 GMT  
		Size: 20.4 KB (20403 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:014f69569ebf9b9c054cb1beb25fcc73987409a45d1298cd5abcba856fb1dfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138604035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d0904d0482471d6483cbf80d0d9b0e3cced7ab040087a31eb13dcccdd46499`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:a44f607975ffdfe1d1e6fbbd7c788fb60e0798aaa1ee5af9d8224939a997f5ca in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:e5a38773908c2b8bea3ed4c99da19aeb90b951ddd5134f07d9b370f1d1a9ed8f in /root/buildinfo/labels.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="006ec712cf2384ae208886f1374479d6db3cf3ef" "org.opencontainers.image.revision"="006ec712cf2384ae208886f1374479d6db3cf3ef" "build-date"="2025-09-18T09:12:17Z" "release"="1758185635"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:30f7339d64a9a25df6fdea38f8c5f6a45428f9e53b3c84fd4ec4476e63892d49`  
		Last Modified: Thu, 18 Sep 2025 18:15:07 GMT  
		Size: 33.4 MB (33412886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d042ada3a5cec9fd3884dbeeba937048c4e0c0c456c62660c0afff1681d438a8`  
		Last Modified: Fri, 19 Sep 2025 21:47:17 GMT  
		Size: 55.7 MB (55686358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0c5729853870b72e43410bcca3a2f194984237fe84c30456d7169527d9abd4`  
		Last Modified: Fri, 19 Sep 2025 21:58:56 GMT  
		Size: 49.5 MB (49502375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95df1e28cc7232ba8403e5f1b4d0d237d2571efd189af9badb06d6e7fde583`  
		Last Modified: Fri, 19 Sep 2025 21:58:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9f1059da9fdf2dd2f194d07322030c51897269b80fcbde8abf52f46d56bf33`  
		Last Modified: Fri, 19 Sep 2025 21:58:54 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7dcb30c806584c90a150e118f1386e6055c8801871e453101ed4b0994767fe9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0008ed2d6ae7608f601d19e1f29c684d08b6253bc2140aeeeb4fa1130cd296`

```dockerfile
```

-	Layers:
	-	`sha256:9fe08461c14582dfe5d24fd4c8e5c0d3224afdcb82e066b3ba27b47fa5fbd99d`  
		Last Modified: Sat, 20 Sep 2025 00:16:19 GMT  
		Size: 5.6 MB (5581898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136a5fa28a8aecd88e65edad4bac617184d4f89abeca517c7db22bcc4030aeba`  
		Last Modified: Sat, 20 Sep 2025 00:16:20 GMT  
		Size: 20.4 KB (20373 bytes)  
		MIME: application/vnd.in-toto+json
