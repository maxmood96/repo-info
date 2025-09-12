## `gradle:6-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:21e191fe0ba368bae97f43e621ac0d3eb73297a206ecd95c22babb99d2552cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:ce5d7048c8c669fe3f8746cd0635caec42282cfb7345a8830cd9d630fd65bf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 MB (401633482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97170a9a88ce6f0b77a2fc564cfc64359441a31917f0dfc8bb26ae87c338d2d4`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Jun 2025 18:02:05 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:02:05 GMT
ARG version=11.0.28.6-1
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV LANG=C.UTF-8
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f8145f80f6a9693df4d2f42ea579d9b299c3223cd58a6b1c3ba0ca3078d209`  
		Last Modified: Fri, 12 Sep 2025 02:10:10 GMT  
		Size: 154.1 MB (154069919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29558e336ad9b89caba4358d070a42c45421cb4d1e9f6b62c1bbbf2fa67aae36`  
		Last Modified: Fri, 12 Sep 2025 05:19:57 GMT  
		Size: 85.6 MB (85558270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd410c2ede3c9a2570c087027458e50c78156e2d481cad9f87c7a6d897f46056`  
		Last Modified: Fri, 12 Sep 2025 02:11:28 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aecd1b4e60130b290e04d7d573d9c06988978a19533983bc79ecffaf83d9de1`  
		Last Modified: Fri, 12 Sep 2025 02:11:43 GMT  
		Size: 107.7 MB (107696631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aece90c4dc0e68a37d5127d1eeae53157d4c1d055609d0d491b86eb354d7f385`  
		Last Modified: Fri, 12 Sep 2025 02:11:29 GMT  
		Size: 431.3 KB (431277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:3087e30d223fda096adf1ae8753aaf66486ca67c47ff701e7cb3da1c43f5a42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11250643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b42b50e96b4ac0f6673f190055b88b89afd92f720ee9e89784568d139888de`

```dockerfile
```

-	Layers:
	-	`sha256:b0fdafc362ff3c5341f67d47f8bea09170248caed071753c8b50efde5e945141`  
		Last Modified: Fri, 12 Sep 2025 05:17:33 GMT  
		Size: 11.2 MB (11229728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d97482dd578faf8d3cd476f17b671067b454ba45747eb0bdb92e501fee567bae`  
		Last Modified: Fri, 12 Sep 2025 05:17:34 GMT  
		Size: 20.9 KB (20915 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6a7f5ec47eabe44793a76723bacaf392f39e116789a88e3fd840e720c51a2d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.6 MB (398558592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b48ad50ea3537b4a885240bfa7d91b2e9b3c22aba8762150c682c6c2fb83e22`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Jun 2025 18:02:05 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:02:05 GMT
ARG version=11.0.28.6-1
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV LANG=C.UTF-8
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:a2133584a03a0323a461f4ba1900a168268d3305d6206a4e0a210c92b146e94a`  
		Last Modified: Wed, 10 Sep 2025 02:34:05 GMT  
		Size: 52.8 MB (52775111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc19c2d90ec6d5e3f5ebd13458d8ebe5156a4231d95218255092f24a430fcde2`  
		Last Modified: Fri, 12 Sep 2025 02:11:21 GMT  
		Size: 152.6 MB (152577313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2c129cec140f3c771dce6b6d82161e9916ed383adf808c4509f8ae97f4a917`  
		Last Modified: Fri, 12 Sep 2025 02:13:40 GMT  
		Size: 85.1 MB (85082813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb84d70dbb232f297a20baf84127331a3728d4a35bf15f9bf3d0f345ad57381`  
		Last Modified: Fri, 12 Sep 2025 02:13:33 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c875a633bf8e461c1d739ffd8bb25db02121a897ead97f5f72d875e0280fe3b`  
		Last Modified: Fri, 12 Sep 2025 05:17:45 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366221be0a986965adf6d79164d7efe23556da7651581fd51ecc1c8c24bf79c2`  
		Last Modified: Fri, 12 Sep 2025 02:13:33 GMT  
		Size: 425.0 KB (425011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:2231b37e7fa9d89c6ef015e842a7cbb9247a30261502a8f65d85a6619c8d6c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11250634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9524eb05941eab232776805329bdb8b9b2a3b6f2611ca51405500e38019e2eb`

```dockerfile
```

-	Layers:
	-	`sha256:e4cbcced1f542cbf3df9702281f18219829d0f2b06b644ea2dcee31bda913632`  
		Last Modified: Fri, 12 Sep 2025 05:17:42 GMT  
		Size: 11.2 MB (11229547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f244051a5e19e1dc0418a4d5b515fb5e52d942a98132be479f4b0b1175883c`  
		Last Modified: Fri, 12 Sep 2025 05:17:43 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json
