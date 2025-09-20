## `eclipse-temurin:8u462-b08-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:cb329f2dbe3160b60b8fc8e99032e668517706dbd775443135a3966232c6a6ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u462-b08-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:753c5a85b8c801cbc79152182432e47950f5921e70d02bcf6b4df21f4bc437b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130385525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1647d94f13563dd2b6bd1104a8e449c6083bdcd01d80472a5a2a94366a29f9`
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:c7ecf0d56143142b40d3f1e14c72b8cb06da50ff81efa4f3d15776f5c1861319`  
		Last Modified: Fri, 19 Sep 2025 21:17:24 GMT  
		Size: 55.1 MB (55088149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d7f318841892204834162aacbf0b5f2fe2542e0dba3aa678b441d99ea2b11f`  
		Last Modified: Fri, 19 Sep 2025 20:44:13 GMT  
		Size: 41.9 MB (41873047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ea9916001928cc3ea8f5d6f25fdfb4a0ceab5ebccf26292a8bdbd00853884`  
		Last Modified: Fri, 19 Sep 2025 21:17:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e5fbf69a88745bab07dbf60cca9752562f10efd3d170d4b176a71c51179ea9`  
		Last Modified: Fri, 19 Sep 2025 21:17:18 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b2a7fdaa2d39ecfea329cbf4b5924306aa4089ee6548121ce378e1a12f7fb90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21bd4c3ab2660930017614c8b93691ee42e39bc8d7e4de3a668d8f19fbdf60d`

```dockerfile
```

-	Layers:
	-	`sha256:2cd76a74a04a5da5f92326628033ba49ab03d6bb8b8f6360d3d20e18f4115402`  
		Last Modified: Sat, 20 Sep 2025 00:18:50 GMT  
		Size: 5.6 MB (5619587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122ef9f511fe9359f1d48af16c481def68d39394bbb1d6baaf49b0c0488a37d8`  
		Last Modified: Sat, 20 Sep 2025 00:18:51 GMT  
		Size: 19.6 KB (19554 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u462-b08-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c136be58e2578bb6a06a2efa211b8c25e9d871a463875efcdd2f253cb6babc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127302916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4beb3d3107242b7bc5b5f12b8dbaa74152648d23592e041084d2c367bb1abeae`
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:e9e32b01371e043cffdef929b0ab679fec51d7b61308b54d74e56ebc3adbdf2d`  
		Last Modified: Fri, 19 Sep 2025 20:44:55 GMT  
		Size: 54.9 MB (54863280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05adb6e754c5ff7c456cccafcb467d6740b7645452705031994ba96f05e68b26`  
		Last Modified: Fri, 19 Sep 2025 21:16:16 GMT  
		Size: 40.9 MB (40877807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd2fa08b20cff1d1eb2dc77c483637d4779d968ae68c12d66eeeb0dd505bb83`  
		Last Modified: Fri, 19 Sep 2025 21:16:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da4e2d089a3b246129872309220aee975b052be110c0fc12b36a6dddec7fe8d`  
		Last Modified: Fri, 19 Sep 2025 20:44:04 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:09d4498923f80a7f4394f61bdbc71fa19d21e5fe6984105c728ea80b2917eadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793881105c3cad26e1b98ab9780e0402eb8b10d20aba18530610c1e8a8ffe5a6`

```dockerfile
```

-	Layers:
	-	`sha256:36de9ed98db28e0aa273396a2c95904fbc556a1365393560df2b5cdc022e0589`  
		Last Modified: Sat, 20 Sep 2025 00:18:57 GMT  
		Size: 5.6 MB (5619755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb60f5804672bfdd3834d2741f2266b3cc4d6ea8e4f2f2170274276387935724`  
		Last Modified: Sat, 20 Sep 2025 00:18:58 GMT  
		Size: 19.7 KB (19658 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u462-b08-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f8b9334f6015c81d5dd571e3542ac5d77fed72ced25576791088b5e0c4d0b5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135130209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfeb060ecfc11e62121071349115fafe669e04503551e924a7ab5d87252f7b0`
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:f0d10e6f7f92f050033897220b2e758786010ba0e78f782567ddc6db7df7be10`  
		Last Modified: Sat, 20 Sep 2025 00:51:54 GMT  
		Size: 41.3 MB (41255149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6e3ec00f574462c25983d8f7b121eb053209de96c5b6e73efb2f06aa3074e4`  
		Last Modified: Sat, 20 Sep 2025 00:51:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e599083a2234aa0fc5097e5af391c6f04747e775cd7e384654bc12107165edf3`  
		Last Modified: Sat, 20 Sep 2025 00:51:49 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0831b8a0685f295375ebb53fc7b061de8f679d3515c0f6740d00ef48a644b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcbafbd9cfc00481fba09018113d6d85552aef4869a035162bcb0446ac63329`

```dockerfile
```

-	Layers:
	-	`sha256:b1a39b2ad9be9a31291eba9f45a51f9054bc005a0f9bce22646c5325cbfb1275`  
		Last Modified: Sat, 20 Sep 2025 03:17:13 GMT  
		Size: 5.6 MB (5609342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31e4ad7d9df95a419d3c2f0511dd37d5541f9485f205aad54ebd79d9633cf7e7`  
		Last Modified: Sat, 20 Sep 2025 03:17:14 GMT  
		Size: 19.6 KB (19583 bytes)  
		MIME: application/vnd.in-toto+json
