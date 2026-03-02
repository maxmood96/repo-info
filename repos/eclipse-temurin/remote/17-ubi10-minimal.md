## `eclipse-temurin:17-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:fcdfc9291cb6297fb9a5381c52c8d73b9593598391c12165e9e97ba5dca366f6
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

### `eclipse-temurin:17-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1d9789b1182a048e968c7174adfc8f0d13ef4a6f66d7f8295fc17d1495353a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217679676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6c43b7b51aed27c2c2784f0a4800a6b6d9c4826cfe30ea35e2f42b5199b254`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 08:55:55 GMT
ENV container oci
# Mon, 02 Mar 2026 08:55:55 GMT
COPY dir:bc9a8a44e634605c4ff89328666c26f0c256afabea6c375c1017a88a80500ea2 in /      
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 08:55:55 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 08:55:56 GMT
COPY file:c0327936eac36593f0ab8d7da594e1a816cbe84da917c4d0a34bfcc7a914e024 in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:55:56 GMT
COPY file:c0327936eac36593f0ab8d7da594e1a816cbe84da917c4d0a34bfcc7a914e024 in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:55:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T08:55:38Z" "org.opencontainers.image.created"="2026-03-02T08:55:38Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T08:55:38Z
# Mon, 02 Mar 2026 22:05:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:05:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:05:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:05:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:05:12 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 02 Mar 2026 22:05:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:05:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:05:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:05:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:05:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4377b1aab54b81e1e3b39331172fb1424f433cdfe28e8bf6f9cd313a971d0d61`  
		Last Modified: Mon, 02 Mar 2026 10:45:10 GMT  
		Size: 34.6 MB (34610905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ccd897668e75fe4ef478ad40e40cf6065c2c61c6a932e4a705ef55a6a0f3e1`  
		Last Modified: Mon, 02 Mar 2026 22:05:29 GMT  
		Size: 37.4 MB (37429200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7008af90d16656daaae9d6441fd6337e5164c234cea09866748364319c0a3e8e`  
		Last Modified: Mon, 02 Mar 2026 22:06:02 GMT  
		Size: 145.6 MB (145637153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c854b10808489946f3e09b2c73202d3d5803a4b6143f6722047b77a2fbf28a82`  
		Last Modified: Mon, 02 Mar 2026 22:05:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd1038b292cbbba2ed0e2b05b56547a65ed368d80626613640785cda045cbf0`  
		Last Modified: Mon, 02 Mar 2026 22:05:49 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:352465732436814c9c5ed8b39ad244e74943ba4d49759242b35896ed0e0bf434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e50f5337b6b119d9f2067f2f34f938ba08a73c5f8b926ad67a7fc8ab9120fbf`

```dockerfile
```

-	Layers:
	-	`sha256:9843a442fdb3e4f00c251bbe66a9b738a0c0880864d11c0008cdadbf944868d3`  
		Last Modified: Mon, 02 Mar 2026 22:05:58 GMT  
		Size: 3.8 MB (3789767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:350632a899b4f22efbaa64367728de27126178df1b05702f113c4456a0b8004a`  
		Last Modified: Mon, 02 Mar 2026 22:05:58 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:70483a55c459f2f71ea79f8d585cc191d5fcfa44be0ca7a0a666fc630b11dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214506515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f35a284e804cb2c6e66eb7db38f0a4130ab154bd06e56874bb3e1217acfb35`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 08:58:05 GMT
ENV container oci
# Mon, 02 Mar 2026 08:58:06 GMT
COPY dir:c8a0e6b85769dc5b1153f2d95c0dab0c21c76be6878d56a453a175f235aec4f0 in /      
# Mon, 02 Mar 2026 08:58:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 08:58:06 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:09f44631adf2e487fe312f2a1e81a1022d21dd1ab82974e6dcdb1c9761ad2ce6 in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:09f44631adf2e487fe312f2a1e81a1022d21dd1ab82974e6dcdb1c9761ad2ce6 in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:58:07 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T08:57:50Z" "org.opencontainers.image.created"="2026-03-02T08:57:50Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T08:57:50Z
# Mon, 02 Mar 2026 22:08:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:08:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:08:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:08:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:08:14 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 02 Mar 2026 22:08:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:08:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:08:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:08:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:08:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ab71f30be3b758ee5a6fbf5d72df781f51e8cf5753ddf02671b2d7e13e4932fb`  
		Last Modified: Mon, 02 Mar 2026 11:28:23 GMT  
		Size: 32.7 MB (32683006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0a4bc094691173901df638d572125ecb683695471edf39a9b5416a19f8f4e3`  
		Last Modified: Mon, 02 Mar 2026 22:08:34 GMT  
		Size: 37.4 MB (37374516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c672743d1bafe173afb79800de562fcc65817097a2e295d8079248bd8ebcf954`  
		Last Modified: Mon, 02 Mar 2026 22:09:08 GMT  
		Size: 144.4 MB (144446572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b0f21f5f307d93b22538eb7b84167ac3d31792270ec5d8bd9147db02f66d3`  
		Last Modified: Mon, 02 Mar 2026 22:09:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afc1202c7efb2a6c6fb38522e16bc67da2f576923cf83c958790bee20ad76a9`  
		Last Modified: Mon, 02 Mar 2026 22:09:05 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b5a6c76840fad87ff741b7f706ab255dac703feaf007286792c96b850921f8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f209c6d6b17beaa3ab3fc17843e3f783ad366189ecf96f37ed9c473674b36ca1`

```dockerfile
```

-	Layers:
	-	`sha256:159f34383c9c2ba0755d6cac188ff37f5e0fb13344d4ce46d1dad9302614fb23`  
		Last Modified: Mon, 02 Mar 2026 22:09:05 GMT  
		Size: 3.8 MB (3789193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:924eadecf15c3bcd9835dec3e5e5a7d6251cbbc8d6ea605b7e6c38a0771add82`  
		Last Modified: Mon, 02 Mar 2026 22:09:05 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:3ed567da08c2f484f8be9e24a5744285101041f0b5c43c59cfb1a2c8be8c7d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223376725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb97428ab47cd0006842e2dd8418111c6bb7b66c6b9afdce8fa7a4b048c1f7b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 09:04:59 GMT
ENV container oci
# Mon, 02 Mar 2026 09:05:00 GMT
COPY dir:e20d8c9b5112eae2ec3cf27567703617b532b3d50e37e22798356175a81af012 in /      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 09:05:00 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:f249adc52ffecf442b4262c353b6483cbd86a0119b4a0d56c2ae3482dda5e6dd in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:f249adc52ffecf442b4262c353b6483cbd86a0119b4a0d56c2ae3482dda5e6dd in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:05:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T09:04:48Z" "org.opencontainers.image.created"="2026-03-02T09:04:48Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T09:04:48Z
# Mon, 02 Mar 2026 22:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:11:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:11:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:11:17 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 02 Mar 2026 22:13:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:13:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:13:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:13:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:13:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:52175d44fca07e14e1039fd9cb5b5c7a4f5a641951f3018cac642ab2b0d7aa2d`  
		Last Modified: Mon, 02 Mar 2026 12:12:22 GMT  
		Size: 38.7 MB (38730989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df108a302998b0b0c1beb639de829388ba26f170d0578e18c4fcfeb7e8204b`  
		Last Modified: Mon, 02 Mar 2026 22:11:53 GMT  
		Size: 39.2 MB (39183318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42fa175f5e6802105d47005805e1ac220dfd774e4dafa7f44f45c6014e08664`  
		Last Modified: Mon, 02 Mar 2026 22:13:55 GMT  
		Size: 145.5 MB (145459998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce493049948b805673f720ab225cc536b7f9a68456d6dcc2b7973c4da9acc95c`  
		Last Modified: Mon, 02 Mar 2026 22:13:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738de3841936aef877836c1fee68c93bbdbf6ed76c977de0815e40b8e0edee5`  
		Last Modified: Mon, 02 Mar 2026 22:13:52 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c1afc60689b3d970bb231d6dc7d5bf5dcd3f013d5323cf542d6670ecd7e8b320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3797951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07f750d6c20a7dca19f9499cbbba3d21f193cfd754a54dcb8d814675b0772ac`

```dockerfile
```

-	Layers:
	-	`sha256:15f6ea7bc2ed5384e30b91cee5da66fdef82e1cd6d9f9a4a537c88446f44e4a9`  
		Last Modified: Mon, 02 Mar 2026 22:13:52 GMT  
		Size: 3.8 MB (3776599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6584f3e7d1a68a2f817c2512761cd304f99f529b5bc3b18435f40cb3c48a98b0`  
		Last Modified: Mon, 02 Mar 2026 22:13:52 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:eb9730f93aa7c3baa3592273a4e8a83a8fe7c877085e814187a01a1b19f97df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207831929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e312af91ad34f9ff4d7c1531e83c0c6de81e4c28f8728e69d0fb5ff0825902`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 09:51:06 GMT
ENV container oci
# Mon, 02 Mar 2026 09:51:07 GMT
COPY dir:5dd35d5c1dec7b82721f4ea46a7d4cf99ee4456a5024db00ef7a4185cd459224 in /      
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 09:51:07 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:3bfe8a93182a824c0d137026e37cb062ae718ca91203068e33c3ca4c98e5db8a in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:3bfe8a93182a824c0d137026e37cb062ae718ca91203068e33c3ca4c98e5db8a in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:51:07 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T09:50:54Z" "org.opencontainers.image.created"="2026-03-02T09:50:54Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T09:50:54Z
# Mon, 02 Mar 2026 22:06:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:06:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:06:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:06:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:06:24 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 02 Mar 2026 22:06:43 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:06:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:06:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:06:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:06:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:994f616032f72d0ca9e8101a9d46009ec833cad6f73762dc4e8b95e1492b92d5`  
		Last Modified: Mon, 02 Mar 2026 12:12:14 GMT  
		Size: 34.4 MB (34388694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3078602b97a878a102573fd6c6801179bcd5d66bbf8d0248fc7c82789e08a531`  
		Last Modified: Mon, 02 Mar 2026 22:06:48 GMT  
		Size: 37.8 MB (37811662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac7d298466ce3fb76022444ca6885bf3cdcaa66425f7d85755191821b51d5e9`  
		Last Modified: Mon, 02 Mar 2026 22:07:15 GMT  
		Size: 135.6 MB (135629152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0320c18887ca2c551592c03447cb2e3187c6150b0e7572971edd9d24c92d272`  
		Last Modified: Mon, 02 Mar 2026 22:07:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdbd145a9493be2158cf7da282b798b09f0d6a8a949b1c6eae38be3543d8d77`  
		Last Modified: Mon, 02 Mar 2026 22:07:10 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c381285400454d8d19686f6e06791f5370ff566197a62231961a09f820483e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799996091143112c3f76358f61dc65d94e348a29b0a40178ecd3635fdcfb6d48`

```dockerfile
```

-	Layers:
	-	`sha256:ef8f19970d483879a7f05872e1c152f647017a97109e0285fe39282948093425`  
		Last Modified: Mon, 02 Mar 2026 22:07:11 GMT  
		Size: 3.8 MB (3775357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a4392fce4cc0d2cfc4c88b043c2e7f0542d1dee473cf8f08626d0e79ab42fd`  
		Last Modified: Mon, 02 Mar 2026 22:07:10 GMT  
		Size: 21.3 KB (21315 bytes)  
		MIME: application/vnd.in-toto+json
