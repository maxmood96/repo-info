## `gradle:corretto-al2023`

```console
$ docker pull gradle@sha256:3df6aacb712cf7d16cf7b07b21d063535caf775d0e8d8934fe80bff616919d5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:d8584aaf5f1e0798952251849cfc77494c97be44f9a161f73b4304465f3dbe58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.2 MB (432229680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7657fcfad3896d6fe46caa460cc187e6402ae747ba3ed126d2c537249c6bf0a`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04edc0838079d95fa589db479f4ba34a53a5a0224ab75dfa1524aae563c976e1`  
		Last Modified: Thu, 27 Feb 2025 21:08:31 GMT  
		Size: 169.8 MB (169769979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074d06e9b7ed81d184a46ee45f3e476b61188c66b0fc9dbb8013a63712bd85a`  
		Last Modified: Wed, 05 Mar 2025 22:31:56 GMT  
		Size: 72.3 MB (72263205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2c027203bd21686cecf25ad806e9bc61edd9468147f45b932b281a8cc460ba`  
		Last Modified: Wed, 05 Mar 2025 22:31:55 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130a62c6c6c4528db0f9f5eafa3aefad95548302a81b4a5a2dc31e26886f35a`  
		Last Modified: Wed, 05 Mar 2025 22:31:57 GMT  
		Size: 137.0 MB (136988182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0d5f798b5b0b0c080fb93cd90abaaac1138d515ea024bac3edc43502301afc`  
		Last Modified: Wed, 05 Mar 2025 22:31:55 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:aae8a70cd56c0ec5179c2e3e8cb574b8f894e1b912f9f7e986cc4d11ce626f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10762642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953d15db70c7d4f4c75ad61535aac367418538efb1d9b8bd13da8ffa017027ad`

```dockerfile
```

-	Layers:
	-	`sha256:9aafe3c47717cd5d814bba77d95977a6f66a20c7885fa3fb901fe428333508e6`  
		Last Modified: Wed, 05 Mar 2025 22:31:56 GMT  
		Size: 10.7 MB (10742794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9353351bc4abf64b766462645a738790e5a75e9e05efb74f2cdd17d14588134`  
		Last Modified: Wed, 05 Mar 2025 22:31:55 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1fe3b62c90627ef08d5510e23b14d533e97076616aaf9230cfd1899ff677adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.3 MB (429313963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6ba6c349f5042890dab9ac225f20d3fe53fa24adbc3ceed3902ea49c27fe8`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d295914b7779ce95c689cad1e7e96b527a1e5e033a9ef7df7271bfc18128b223`  
		Last Modified: Fri, 14 Mar 2025 00:17:29 GMT  
		Size: 168.1 MB (168075877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a58d661b2f50d4afe429ff327b23082118df56a661e0a770bf2d2bbb7dfd18`  
		Last Modified: Fri, 14 Mar 2025 05:40:07 GMT  
		Size: 71.9 MB (71942719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3105d6db03902aed814478a77bc559f37da7a05ad5545cf9cf5812e78dc4b4cd`  
		Last Modified: Fri, 14 Mar 2025 05:40:04 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48352108f996c5b4e6049c08ffafcbf18b5c88d8981d1588b26894b89cb079dc`  
		Last Modified: Fri, 14 Mar 2025 05:40:08 GMT  
		Size: 137.0 MB (136988179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e5a4391f4b36a4f6a871b17a3038736db399b99d2c809825744c1a46543c78`  
		Last Modified: Fri, 14 Mar 2025 05:40:05 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:9d756b615e2a04dffd90b496c569e17b2e33415414f18eb4bcb2ad292fa20d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10763234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95fdfed0be76597e330e2086a92831007b0d0d327b51a3837269847e4fecbeb`

```dockerfile
```

-	Layers:
	-	`sha256:a1fe4f5de31e36a287cd6bbf6f7ed9e8f2fb1610c9752d58a91e5d8aade90ed9`  
		Last Modified: Fri, 14 Mar 2025 05:40:05 GMT  
		Size: 10.7 MB (10742494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe38aff0f6a2d46fbc84ac501d1d944a6065bec1abde8064b7af02045b010946`  
		Last Modified: Fri, 14 Mar 2025 05:40:05 GMT  
		Size: 20.7 KB (20740 bytes)  
		MIME: application/vnd.in-toto+json
