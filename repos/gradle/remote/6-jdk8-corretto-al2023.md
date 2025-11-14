## `gradle:6-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:718fa958ebf1a3f0ed4b0b85327e47d862e6981c251e3e2ddf6a073320c0791f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:b4b4c407ae8203e6226ec134afe1ff0ded472a3a80e901ec8c6d1de3a62b4a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.3 MB (558337253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e782e38bd9191affeecc8df9b5ce9e28d9b39ce8acb6a6a6577c5b07d115610`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:27 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:15:27 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 14 Nov 2025 03:14:53 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:14:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:14:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:14:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:14:53 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:14:53 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:14:53 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 14 Nov 2025 03:14:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 14 Nov 2025 03:14:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:14:55 GMT
USER gradle
# Fri, 14 Nov 2025 03:14:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:14:56 GMT
USER root
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809baed2d1217d8172c8deeb035a0df5a2b40b71b3dab00a99d667761351faed`  
		Last Modified: Fri, 14 Nov 2025 03:14:19 GMT  
		Size: 330.9 MB (330851031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102d8098af09a8ad2a0794ff207181db9ca14feaad77eae64a7006b3148c110f`  
		Last Modified: Fri, 14 Nov 2025 03:15:50 GMT  
		Size: 65.4 MB (65379597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb76d7ea123338f2dab60829e7e818e252c2d4f6fb5e489f8bf6fc428f0988ec`  
		Last Modified: Fri, 14 Nov 2025 03:15:42 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6a50dff3c568205c5aee1dfb5006e57fedff46ac72b7cf463d0cdbb7ab686c`  
		Last Modified: Fri, 14 Nov 2025 03:15:51 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc409468b00ad3cc88a0365c58cb24c8894245a92f1d6d7600608a9a94ef4fb`  
		Last Modified: Fri, 14 Nov 2025 03:15:42 GMT  
		Size: 431.3 KB (431271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:094888a5f7a43c83a217a97112bfcff42e0b2268dfca09e2946bf5d62ff5669c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18066807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46faefc2c747a6c0c17857ef9c319bb54500b5c9a90d825724525f4c7c2cee1f`

```dockerfile
```

-	Layers:
	-	`sha256:cf1ad33a5542fc3311fbfa81850e9e527b7734535addde41dc6e25185592feda`  
		Last Modified: Fri, 14 Nov 2025 06:17:46 GMT  
		Size: 18.0 MB (18045942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbabcbd3879c3fac780cd38567dad827b9bd2cac1d827abc4ecb9f2f25353ed`  
		Last Modified: Fri, 14 Nov 2025 06:17:47 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b98b65718c6eb1f9bb7877431e68c158e531c8e3c5976b710aae669dca569ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364456633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59de3fd985a52049de76775109181d0eafda6d56ad45281793115a103d55f436`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:14:27 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:14:27 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:14:27 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:14:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 14 Nov 2025 03:15:32 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:15:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:15:32 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:15:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:15:32 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:15:32 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:15:32 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 14 Nov 2025 03:15:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 14 Nov 2025 03:15:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:15:35 GMT
USER gradle
# Fri, 14 Nov 2025 03:15:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:15:35 GMT
USER root
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417b09cc61bce7063ee22fdbfec9440fa59193c657107416fc150a8b9c769d68`  
		Last Modified: Fri, 14 Nov 2025 02:15:22 GMT  
		Size: 117.9 MB (117933801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db138dd61ceccfbb43da5cc2112894057fdd60b5c244e2f791bbfffc132da3e`  
		Last Modified: Fri, 14 Nov 2025 03:16:21 GMT  
		Size: 85.5 MB (85522807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fa9ce170bf49d61a6fa7ac2e8572d58fecf133e063e5563d183648cb17591a`  
		Last Modified: Fri, 14 Nov 2025 03:16:12 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cf0d3f28b6fe6f36636f481e2b6b01c9013079e0890db8a0bdfddf81eb0a3b`  
		Last Modified: Fri, 14 Nov 2025 03:16:24 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b59aa1a0b8de1efac70c9ba56ddd4c4057d4abb8e82b99e8e292037979dc87`  
		Last Modified: Fri, 14 Nov 2025 03:16:12 GMT  
		Size: 425.0 KB (425024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:37b51b9f0f291bb2e220bcdc03761de782bd8857a223d65209e0d2fcd99de081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11631146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3c047e45f1fd01767c6582f8fc417a4b08f7336eab1ab54a2b6018bd701781`

```dockerfile
```

-	Layers:
	-	`sha256:e34c1aad2da757320b7214ecef501a8e17337b234ceadc7be9220ebaa9bfb196`  
		Last Modified: Fri, 14 Nov 2025 06:18:03 GMT  
		Size: 11.6 MB (11610108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6c05fa2938a82729a0f6e8786b6c6e5fd19d03683c9642b26e41ab1d1400ea`  
		Last Modified: Fri, 14 Nov 2025 06:18:04 GMT  
		Size: 21.0 KB (21038 bytes)  
		MIME: application/vnd.in-toto+json
