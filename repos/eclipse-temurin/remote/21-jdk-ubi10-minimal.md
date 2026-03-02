## `eclipse-temurin:21-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:921593b4bd806663951440ce35077f3c554d390816a22b8065113bb5be34f66f
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

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:34ec1a5b90dec06623a1508dadaded89ede63279dbbc2baab0c7a9d4c59df66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229903569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2845bae8f4d6df2272be607727608059085b31939d9a1da07ff14605e591547`
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
# Mon, 02 Mar 2026 22:05:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:05:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:05:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:05:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:05:09 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 02 Mar 2026 22:06:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:06:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:06:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:06:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:06:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4377b1aab54b81e1e3b39331172fb1424f433cdfe28e8bf6f9cd313a971d0d61`  
		Last Modified: Mon, 02 Mar 2026 10:45:10 GMT  
		Size: 34.6 MB (34610905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f276e3eb8f3d45a8ee4d3cba66d483e300e92657d38599052823f1d516f222e4`  
		Last Modified: Mon, 02 Mar 2026 22:05:28 GMT  
		Size: 37.4 MB (37429238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827ae1c10d500c64ac3da3752a9c470834c288c91c501d0926ce0cb02ac7ec81`  
		Last Modified: Mon, 02 Mar 2026 22:06:23 GMT  
		Size: 157.9 MB (157861009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296754410aaa11c057c63cad164af72631744ba68e29655a87520b1afdc7dc0a`  
		Last Modified: Mon, 02 Mar 2026 22:06:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2e04ad7dc6c76f98b7341f04a39698dc2721d4349090216cb5b9dd10a3bd0f`  
		Last Modified: Mon, 02 Mar 2026 22:06:20 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4c6f3f257e08ee512e42cb00c17aeaa53f2e69960d38fcf2bb60f138a58edcc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bbaa40adf8cca5dae8605d161586b37e43f6260e972ac3e82408c37ac9ef1d`

```dockerfile
```

-	Layers:
	-	`sha256:87f2b7abd81498f363211d9dc40e7faee9b46e7106ed1873771f68f38f7a6bdb`  
		Last Modified: Mon, 02 Mar 2026 22:06:20 GMT  
		Size: 3.8 MB (3791619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:131176939901db1ee3db60be1a665c40406af984b227ec924ecd65282d82f9d6`  
		Last Modified: Mon, 02 Mar 2026 22:06:20 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:88b098038a2923ef9853b13357a4e14dd69d4eae0c2a5b89fab5c80a97cbe9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226196102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d663591ab9f2adacbfd7ec2331161493bbff91d1abf2b40b38f8e33f488cae91`
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
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 02 Mar 2026 22:09:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:09:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:09:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:09:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:09:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ab71f30be3b758ee5a6fbf5d72df781f51e8cf5753ddf02671b2d7e13e4932fb`  
		Last Modified: Mon, 02 Mar 2026 11:28:23 GMT  
		Size: 32.7 MB (32683006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3889f3884aa943c26e1c1b3de15da7a5aebe5f569d872cc163230b47be37b7`  
		Last Modified: Mon, 02 Mar 2026 22:08:32 GMT  
		Size: 37.4 MB (37374475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8424ff744137f0d69dadc7dc6e139833c657583ecdbf1354a5437fab16096336`  
		Last Modified: Mon, 02 Mar 2026 22:09:28 GMT  
		Size: 156.1 MB (156136202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07deadb2ca749914d5586c21915b7a392533d88f4682722819df7ef3397b28b7`  
		Last Modified: Mon, 02 Mar 2026 22:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f137add0773cd301526b67b6d55f23bfe29b02feab165412ca6e9472f5715e61`  
		Last Modified: Mon, 02 Mar 2026 22:09:26 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ce0fee69ce98b997a31d8f4f99f8ddfb604c0dda9782f253192e5bf8e91fc725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5eee9bc11fc498fc07ee7f5ddbac9e28c601367023a5e171a62af4f4ea513`

```dockerfile
```

-	Layers:
	-	`sha256:930070ebbad75e2aede287f082a72e5331038353847ed6c0ee133ef950e78005`  
		Last Modified: Mon, 02 Mar 2026 22:09:25 GMT  
		Size: 3.8 MB (3791045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa972ef555e27d63678c9eee39646d32c580dfcd0ae5a90d818a81b0d3b798a7`  
		Last Modified: Mon, 02 Mar 2026 22:09:25 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:bdb981a998c5bfe817f68855d7e4163f45bce296dc32ab899b8c5b20d177e81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235898064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af25bcc281475b8c152d2b3436ef5aa35288fac192a19a19e00800bf0a487571`
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
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 02 Mar 2026 22:14:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:14:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:14:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:14:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:14:15 GMT
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
	-	`sha256:e6db1b50cb23cc81782f1e68ab4925664465988bacdf8e99354a09bb48837ef7`  
		Last Modified: Mon, 02 Mar 2026 22:15:03 GMT  
		Size: 158.0 MB (157981336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36798030e22ecd09ea3913a7627d209fd31e011fb52f14b3be6b066935518e08`  
		Last Modified: Mon, 02 Mar 2026 22:14:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04d48866363f99add341fb489417035c913c593acc5778e3309b47b7c14dd1b`  
		Last Modified: Mon, 02 Mar 2026 22:14:54 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6360107358bf6b030e1235ed11fa959c4128dc3cad9bff2ece7d0f764f5d8e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173e87b846e28cb351ac18eee09c054b37173c10816592fe03a3b489a7ebdb6d`

```dockerfile
```

-	Layers:
	-	`sha256:3dd23cf234622e6a5b756a6d36af8dc1af9e23942b4394ba06a778ed383ce67b`  
		Last Modified: Mon, 02 Mar 2026 22:14:54 GMT  
		Size: 3.8 MB (3778451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3005fde9a10e781957e3609de12a563d29fbcef78750420bf6938d9bb09cb2ed`  
		Last Modified: Mon, 02 Mar 2026 22:14:54 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:1890650f1a48451c0333738d49588e129a36f80722b5e691a568676cd6ccdda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219307611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5ff41f19013999df9bb5a1fc960dfbeeca4846e9c62738c1f59a6a9a70667d`
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
# Mon, 02 Mar 2026 22:06:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:06:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:06:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:06:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:06:18 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 02 Mar 2026 22:07:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:07:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:07:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:07:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:07:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:994f616032f72d0ca9e8101a9d46009ec833cad6f73762dc4e8b95e1492b92d5`  
		Last Modified: Mon, 02 Mar 2026 12:12:14 GMT  
		Size: 34.4 MB (34388694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c78511c21b0da95cf534d58ef20e248f21114652f106ce5c6bb3ffc8ab5984`  
		Last Modified: Mon, 02 Mar 2026 22:06:47 GMT  
		Size: 37.8 MB (37811658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb2d4393f4df92f14abc524b6797c475180fed63a66411f1adab6c12f2bcaa`  
		Last Modified: Mon, 02 Mar 2026 22:07:46 GMT  
		Size: 147.1 MB (147104839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b54a98b13be16e8bed5f89516dc85c63527b6529936688193bd1358e4ceef6`  
		Last Modified: Mon, 02 Mar 2026 22:07:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18092f97af5473d1416973de0781898566995dce2350bcf7f415f3d47ffe242b`  
		Last Modified: Mon, 02 Mar 2026 22:07:43 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:88768dc75e02ea6e84cf12498ec3cd98ed993f9a24dcc502f770062f9487ac3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3798525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002d7a75db762b5b62fab872b9a3a9281c78e90b8a813114d3e97d2687361247`

```dockerfile
```

-	Layers:
	-	`sha256:99d1ccf21cbd0ece72caa4ddb03e54053efbe2b61354d6b1bf0ebd2e4f0f6b7e`  
		Last Modified: Mon, 02 Mar 2026 22:07:43 GMT  
		Size: 3.8 MB (3777209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb1eafb87ffeac76074f5102045fc55eddefec8d397d367f8ff189fa4a49a54`  
		Last Modified: Mon, 02 Mar 2026 22:07:43 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
