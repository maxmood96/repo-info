## `gradle:jdk26-corretto-al2023`

```console
$ docker pull gradle@sha256:1c09813d20c8ff1e175272e37560e3f6de17d85c28b9e96ab3fbc9f31a7f3e1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk26-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:ff2952574f3fb75130c5084ec9abd10e456ce8c28e2143a4129d59c55aabc3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.0 MB (471963613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f0aff116fe4255df248c09cd38befdaf0fc0e7f756bec43f19cc98593f2178`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:15:26 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 22:15:26 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:15:26 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:15:26 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:15:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Fri, 10 Apr 2026 16:55:39 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 16:55:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 16:55:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 10 Apr 2026 16:55:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 10 Apr 2026 16:55:39 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 16:55:39 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 16:55:39 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 16:55:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 16:55:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 16:55:42 GMT
USER gradle
# Fri, 10 Apr 2026 16:55:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 16:55:42 GMT
USER root
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9e4b80620d99ad8c8758cc56db4e4e815d82e7ec126a917e0f4a8abe16ad13`  
		Last Modified: Fri, 03 Apr 2026 22:15:52 GMT  
		Size: 193.5 MB (193452417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961043f7d91dd056d0d42ab9ba919841b87516a32a236d6f08f0b8fa7d699e77`  
		Last Modified: Fri, 10 Apr 2026 16:56:16 GMT  
		Size: 86.1 MB (86104278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182d3225cbc30642fcda3612e994f9cbcd5ac49803fa3308eca61b73c5514b29`  
		Last Modified: Fri, 10 Apr 2026 16:56:09 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60e5fd23f574b68f642ee6cb1a1db85aaafb90f3e5ea99cddafbcf8164ee73e`  
		Last Modified: Fri, 10 Apr 2026 16:56:18 GMT  
		Size: 137.8 MB (137808329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f219daa73dfa3cbf1567b1c352932e439af1839cf9e644911f118a1a6f2f6722`  
		Last Modified: Fri, 10 Apr 2026 16:56:09 GMT  
		Size: 25.6 KB (25607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:c8a338bbcae97b1f6ad1eddaf9579924a50fa71a4e0caac07fb2fe4840d82bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11366789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf53d9de3eeb9a4cdb662cf47b6e49146b4b2f94df72a52cab44d6047ddc40f`

```dockerfile
```

-	Layers:
	-	`sha256:b1205b4b80e103c5663b21fd392e7ee804605f8f7f2684e905e41c7ac2b01eb8`  
		Last Modified: Fri, 10 Apr 2026 16:56:10 GMT  
		Size: 11.3 MB (11345138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184cc289982de03f62a04526a8cde31de4007a9146ba0fae49c715da0b2698d7`  
		Last Modified: Fri, 10 Apr 2026 16:56:09 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a4a0eb64a36ff9d3012bbc1ad0fda335bde455d1b6588ef93622b12c6a84a776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.2 MB (468155826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28639a0ecd51cd79f14c29a8d0fc38ea63b0934fc7437af8ec295ee84f3259f7`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:45 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 22:14:45 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:45 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:45 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Fri, 10 Apr 2026 16:57:06 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 16:57:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 16:57:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 10 Apr 2026 16:57:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 10 Apr 2026 16:57:07 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 16:57:07 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 16:57:07 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 16:57:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 16:57:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 16:57:09 GMT
USER gradle
# Fri, 10 Apr 2026 16:57:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 16:57:10 GMT
USER root
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc73e75f6054bfd006658c319ccb8f00d291a0d86167595d67b7799d3d93696`  
		Last Modified: Fri, 03 Apr 2026 22:15:13 GMT  
		Size: 191.3 MB (191273065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8db98821a3ff8e6678b14fad7c7327096059c4b5f236f48db93c7aa973c916e`  
		Last Modified: Fri, 10 Apr 2026 16:57:42 GMT  
		Size: 85.6 MB (85600586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4d0346f3d0be8dcdee7b5dfdaf74c534d4c151c97347ca10f8e9194e1c5ff1`  
		Last Modified: Fri, 10 Apr 2026 16:57:38 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bf4053f33e6ab64575fd0fcbdcb4612984fceb6f6a5d99377f8b18ddde2d32`  
		Last Modified: Fri, 10 Apr 2026 16:57:44 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aa18333efb7f45d6fdf133f4717a5d611abcc96239e6390c523898dfeaade6`  
		Last Modified: Fri, 10 Apr 2026 16:57:38 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:6991c017ebcbff53ed993cd275530e39409580258a8100cdfd693165560fa68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11365994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becc409aa1efe79d5352a850f93dd055e102d288e825afd1447d15f542f3112a`

```dockerfile
```

-	Layers:
	-	`sha256:bef3de45803390d6352c2fc1575f62518fe5824aa1aa4378080e303844556b28`  
		Last Modified: Fri, 10 Apr 2026 16:57:39 GMT  
		Size: 11.3 MB (11344147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a31a9a17f776286c8098dbe42d69c89cbb4dbab73fd247b787281d35ec4dca`  
		Last Modified: Fri, 10 Apr 2026 16:57:38 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json
