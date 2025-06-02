## `gradle:jdk24-corretto`

```console
$ docker pull gradle@sha256:cd908014dca464a4efe88f9e5011453f629a4b2753769c9e7125671e86c0a90b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk24-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:1d95e48c8479264b5d815eed4465de837b9a7382eb027232029116d9432990f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.9 MB (461910246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61441faeeba7c06b93dc84373d29cbb68ccbbe2050f69f1fc59e6e82dd97aaf`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 29 May 2025 19:22:22 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:22:22 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_VERSION=8.14.1
# Thu, 29 May 2025 19:22:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER gradle
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER root
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Wed, 14 May 2025 01:42:44 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62dbbf3c08e9d1517a47b48f3a2d5a2957390e20d36f17ce3f450b6179adbac`  
		Last Modified: Mon, 19 May 2025 23:37:20 GMT  
		Size: 187.2 MB (187184906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7188304d421d700e2868ba90c58c75576b4fe4ed513d671d85b765e924ef2119`  
		Last Modified: Mon, 02 Jun 2025 16:48:46 GMT  
		Size: 83.7 MB (83658481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543106f7c61de5544b6473a9ca0d02db7bb8ea9ed0569363f9a56e95069696ab`  
		Last Modified: Mon, 02 Jun 2025 16:48:45 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b962f58657c65e811edef6759635cb192973940c572ca11c3f9fb35fcfa2625`  
		Last Modified: Mon, 02 Jun 2025 16:48:47 GMT  
		Size: 137.4 MB (137395576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baabcd1527eacf94894775acbddd630cdf0baa05ff0dafdc8569fa2f0d7ddfe`  
		Last Modified: Mon, 02 Jun 2025 16:48:45 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:efeb1b4bf3baa49a5b8593e7bfce62d4fc92394fbd55c30807cf52ce99a80dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11304189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca492c513c940bcd9021b59336bfb7e5a3effdcb0f91076f623258d1a6745e92`

```dockerfile
```

-	Layers:
	-	`sha256:64cdcfdde5a5a848bbae74b384a26bb129262eea2c9888ee546c4c3b168a12e4`  
		Last Modified: Mon, 02 Jun 2025 16:48:45 GMT  
		Size: 11.3 MB (11282607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07d5fff2811b256b3d27c80fddeb66ee6124359799b9ad3fef3cedf750a232e7`  
		Last Modified: Mon, 02 Jun 2025 16:48:45 GMT  
		Size: 21.6 KB (21582 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:edf363a07c7fba3e6b4c86f3260881040152a5f1c7703e33def70095f8ca12da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.5 MB (458484607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053bbdc6270276e6079fd6776c1034c8ebb9d292f3bc485f1a2e90ce8085d097`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 29 May 2025 19:22:22 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:22:22 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_VERSION=8.14.1
# Thu, 29 May 2025 19:22:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER gradle
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER root
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Wed, 14 May 2025 01:42:43 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606c71bde4a7d05e0626f9b64fb3e0bc776c63157501c509a656a16ad481691`  
		Last Modified: Tue, 20 May 2025 00:04:05 GMT  
		Size: 185.2 MB (185232892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b930de29459826d11666af4e4c3e37faf95cc3a27ac035a5ab3b5669f3cb4702`  
		Last Modified: Mon, 02 Jun 2025 17:18:27 GMT  
		Size: 83.2 MB (83229193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3246d2bb3ade0125f375e3fe09ce63011e48f397ead0f4526b5fe2b8c8afb0c4`  
		Last Modified: Mon, 02 Jun 2025 17:18:25 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ebbe70d99dc0af96b1b4a240e0ee19971d002fb0d7ad16abc72c38b55240e9`  
		Last Modified: Mon, 02 Jun 2025 17:18:29 GMT  
		Size: 137.4 MB (137395580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fd59e6b9c8b862be0263836aa55bf11fa6eb062daec2d35e9704b1b35ea774`  
		Last Modified: Mon, 02 Jun 2025 17:18:25 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e21263b96485fe4baa7dc1e48c612ddc802b84c56ba143a9fe9b2866a2356ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11303399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acee7d2ee12d0e90e7c2709dd63daab5101091272c05c2443f5d7dd04baaa14`

```dockerfile
```

-	Layers:
	-	`sha256:541dbcead8c5963c52c23dfa5714bb17b83b7115736d7904754b9705a97f981f`  
		Last Modified: Mon, 02 Jun 2025 17:18:26 GMT  
		Size: 11.3 MB (11281620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcea036fc7fa66e76c08349e5f0674e82d0cb17638bc3265f83f8ef34c055060`  
		Last Modified: Mon, 02 Jun 2025 17:18:25 GMT  
		Size: 21.8 KB (21779 bytes)  
		MIME: application/vnd.in-toto+json
