## `eclipse-temurin:21-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:78240d10c28c82896e4613020838ac9c11b3e54c841f06748acc9a8c514f2bea
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

### `eclipse-temurin:21-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:83360bcbf036323866516280d36356b5cd4554f82a5a09a7dcd079b1a605d1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229921008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6fbcf240a9babd70706544735ab20aa9616696ba3efb92825505ec452d2540`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:53:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:53:01 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:53:01 GMT
ENV container oci
# Thu, 19 Mar 2026 04:53:01 GMT
COPY dir:af440ed069b945cf125ef868e769f70d1b1e33071b111d96c1e9a1ffc5f76e4e in /      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:53:01 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:6585c86973269b2041af40b485e0e6f045b49959f72c04fee4a05795e2e5a97c in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:53:02 GMT
COPY file:6585c86973269b2041af40b485e0e6f045b49959f72c04fee4a05795e2e5a97c in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:53:02 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:52:47Z" "org.opencontainers.image.created"="2026-03-19T04:52:47Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:52:47Z
# Fri, 20 Mar 2026 00:16:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:16:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:16:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:16:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:16:48 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 20 Mar 2026 00:17:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:17:30 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:17:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:17:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:17:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f862e22eed3c55bcf45baceaa7dd39dbd424275e0f2d3130583784c94e488dfd`  
		Last Modified: Thu, 19 Mar 2026 06:14:45 GMT  
		Size: 34.6 MB (34610902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc4c023340201067f35068ba6e3598759d43c5f098949fa0053d75a2afdb654`  
		Last Modified: Fri, 20 Mar 2026 00:17:14 GMT  
		Size: 37.4 MB (37446661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8fea63c675e3bfc8b45927785ec5e448410f25f602408e30985ad73655577`  
		Last Modified: Fri, 20 Mar 2026 00:17:51 GMT  
		Size: 157.9 MB (157861027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f91afd45a1f10802f41f006cee5fab858f9c605f88e4883806699f3f7f505`  
		Last Modified: Fri, 20 Mar 2026 00:17:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bed630ae90f921879bad72b9898b99baddf38c98fd3fa433f2f6fa265a87e5`  
		Last Modified: Fri, 20 Mar 2026 00:17:45 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6311469828c51f80ed4653441b8cc4f1081ae1ba2020bc917e8d7e4ff23e559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077be3bab1c488ef98cf41272f927f67a57f567412122b1d72f20882cacee28d`

```dockerfile
```

-	Layers:
	-	`sha256:4a13386f44247da822ea35db9783c88f318d81db4c39cf4baa26f1ec78514f6d`  
		Last Modified: Fri, 20 Mar 2026 00:17:47 GMT  
		Size: 3.8 MB (3791625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eadc81bb592c0ceb82311fa219627d48e5fa1988789f6d5c625b65aa5420cc24`  
		Last Modified: Fri, 20 Mar 2026 00:17:46 GMT  
		Size: 21.3 KB (21315 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6493e631809c5cb6cd0ef7ca833415cee48d8d79f6c9b9e9ba0f090007a4c2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226205110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146358f8486e56672382c4db84f3449bd4c7126905d6a0c805bafc911439b7f3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:55:27 GMT
ENV container oci
# Thu, 19 Mar 2026 04:55:27 GMT
COPY dir:ddf23ac9073f2f0aebc549dd652158e51758019b3f147b69bcf85b8c51fd9394 in /      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:55:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:3038f4da402f5d3deadca7034502c693a744bf96305b10c79908db4a59bf74a2 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:3038f4da402f5d3deadca7034502c693a744bf96305b10c79908db4a59bf74a2 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:55:28 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:55:11Z" "org.opencontainers.image.created"="2026-03-19T04:55:11Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:55:11Z
# Fri, 20 Mar 2026 00:15:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:15:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:15:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:15:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:15:31 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 20 Mar 2026 00:15:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:15:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:15:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:15:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:15:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32559d11b9ee98b34627afd92e663006f6191d5024358c48c175361f14b3bf84`  
		Last Modified: Thu, 19 Mar 2026 06:26:47 GMT  
		Size: 32.7 MB (32683055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5769b95a0b3f02f2c1ed3ff6444e1b03be4eaeab9817cfe4d7cf1ac5d08a9d5`  
		Last Modified: Fri, 20 Mar 2026 00:15:59 GMT  
		Size: 37.4 MB (37383434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb80cc19b252b83a7282a2dbd70837c18461c232b77b1cf5ce99e35cd00eb26`  
		Last Modified: Fri, 20 Mar 2026 00:16:02 GMT  
		Size: 156.1 MB (156136204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b21374d6b93be8efc7635c699bbf20a11550e836da4edb229890a5ca50705f`  
		Last Modified: Fri, 20 Mar 2026 00:15:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c44a9600d14b841200cdaaa154e441ea9da78a33087b8453485d47bf9567589`  
		Last Modified: Fri, 20 Mar 2026 00:15:48 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:26653c805a52693d3627edaa146a281898649478b3224cf8214ccdbdd877b3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7618fbf210f3604e067c26a9a676e0495c36d39734a45055c74e96abdb32951`

```dockerfile
```

-	Layers:
	-	`sha256:7fcd05f0092fdb118de7447b044c603414de88bb54e6598d861d85527afcf5df`  
		Last Modified: Fri, 20 Mar 2026 00:15:58 GMT  
		Size: 3.8 MB (3791051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba11d306da920e59e027fc20c1d066718db4913e8a57d5275ccc63a3d9ce1cc`  
		Last Modified: Fri, 20 Mar 2026 00:15:58 GMT  
		Size: 21.4 KB (21431 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5edc914fd1981f3c4fc901cba323cf67d9969931aeb0821767ec5686bf1e4ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235916110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce98f9c4a225023e6244743e30f5e69662b082728d9a2aa8b0d4444c916abd2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:54:26 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:54:26 GMT
ENV container oci
# Thu, 19 Mar 2026 04:54:27 GMT
COPY dir:02874e9a4cbd11d21ae5a0b0d5ceabca448e8e4b7d87ed83fe20e3fe3891053a in /      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:54:27 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:cd93def3bf43c5dabe55bff87f8d330823b7a378238d571cd76fa53ae8fb0d3c in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:54:27 GMT
COPY file:cd93def3bf43c5dabe55bff87f8d330823b7a378238d571cd76fa53ae8fb0d3c in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:54:28 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:54:15Z" "org.opencontainers.image.created"="2026-03-19T04:54:15Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:54:15Z
# Fri, 20 Mar 2026 00:02:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:02:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:02:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:02:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:02:04 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 20 Mar 2026 00:08:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:08:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:08:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:08:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:08:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d4c7683a582dd524d9a529f07d62fb8d8a6768403c45eb8da73d739aaacbbd8e`  
		Last Modified: Thu, 19 Mar 2026 06:27:21 GMT  
		Size: 38.7 MB (38730914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cb46297f5b33cc4db0990c621afa3066c8a88767766b1d83c47221837e903b`  
		Last Modified: Fri, 20 Mar 2026 00:02:45 GMT  
		Size: 39.2 MB (39201421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9fefb0d426d6338c70dae80ed5d8eb420bc37e54f20cd2feccd999da6aa05`  
		Last Modified: Fri, 20 Mar 2026 00:08:48 GMT  
		Size: 158.0 MB (157981356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184165d2408dd696a3cba5af6fed25dee1ee67c405d39ca30a06031ed66d4ee2`  
		Last Modified: Fri, 20 Mar 2026 00:08:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d40c5adacc6d592cf6c32e9a40e92c68886ff7607ba48af1247a25fb98419b2`  
		Last Modified: Fri, 20 Mar 2026 00:08:44 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:11ea6d74c08e4796db1bfcb9cd86fd9817d30075163f32f9a6d097b53639429e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded04af47a5d1ec174361a06e2add37b270ce093c51cfef8fd678e7ef3728d3c`

```dockerfile
```

-	Layers:
	-	`sha256:3560b3f323f6d11b29d694c2bd6c78d2468b313eeba213bd453ae38bac0a928c`  
		Last Modified: Fri, 20 Mar 2026 00:08:44 GMT  
		Size: 3.8 MB (3778457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd5d4bfdf4778fa7c6952b772ca1c6765be8039466192385c7ccaf2639a96c3`  
		Last Modified: Fri, 20 Mar 2026 00:08:44 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:49226b861140efc740b5a8416298c83da7b4966b86e2b46719f6f927153236b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219323447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe479c4fc12ef6aeb1100c73de8b3e162c07ff958f448c33e2d23cc31cc3a5d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 05:27:33 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 05:27:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 05:27:34 GMT
ENV container oci
# Thu, 19 Mar 2026 05:27:34 GMT
COPY dir:f746ef018dd3f7fba95b363c4653a5edbac791b1963bab35d68387e37854182c in /      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 05:27:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:ccda15be012570b9ee4c334e02edf875ddce34b3e788c2b4b2da3a4753faf610 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 05:27:34 GMT
COPY file:ccda15be012570b9ee4c334e02edf875ddce34b3e788c2b4b2da3a4753faf610 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 05:27:35 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T05:26:51Z" "org.opencontainers.image.created"="2026-03-19T05:26:51Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T05:26:51Z
# Fri, 20 Mar 2026 00:01:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:01:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:01:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:01:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:01:45 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 20 Mar 2026 00:03:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:03:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:03:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:03:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:03:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63c8858510565f2c5ca6837c562373228e6bd18c78642693e77e10422f59c586`  
		Last Modified: Thu, 19 Mar 2026 06:26:56 GMT  
		Size: 34.4 MB (34389317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52932ad68498d79edf7e415e512c223a0be61689d7a86e4d8782695524e4ae0`  
		Last Modified: Fri, 20 Mar 2026 00:02:12 GMT  
		Size: 37.8 MB (37826887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10924a94234801c1732f51e9f63b3095d3974bfeb0b6f64448cf1e0198f79e76`  
		Last Modified: Fri, 20 Mar 2026 00:03:56 GMT  
		Size: 147.1 MB (147104826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daf0b2a70699bca98a962771e00acde513f7caf44ea23fe0eb433116b37aff3`  
		Last Modified: Fri, 20 Mar 2026 00:03:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9c24e7a7bdbfccf54466a2b91eff0de37e7bc798f5e7d718d23f8756bc9429`  
		Last Modified: Fri, 20 Mar 2026 00:03:53 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:681d7fd506a72aafdab0f3b784e898a6e1cb9c00debd5c4bc8ea2bc6f7da86c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3798531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5546c4f8ac71e8547d288cb6a2b88b5bfa3f5a27d3c05f93091253ebd071f8`

```dockerfile
```

-	Layers:
	-	`sha256:30514b1677bd05ff86100cfa7eff3ef5e0a2420326909d04d20b2c2b5a14f7a4`  
		Last Modified: Fri, 20 Mar 2026 00:03:53 GMT  
		Size: 3.8 MB (3777215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae6d05d8855413adc4a944fbbb58e7326fe7d2e7f18bfabbd1cdccb90a96a2c`  
		Last Modified: Fri, 20 Mar 2026 00:03:53 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
