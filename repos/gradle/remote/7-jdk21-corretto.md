## `gradle:7-jdk21-corretto`

```console
$ docker pull gradle@sha256:f6fedfac45e70c47dc085d648585dbef51bfb8e93e5d87d47210eb65e34d769a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:f6133f027995213a1fc34f4cee428bb7620443802d8586f7636816beb4dd4535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.8 MB (417803623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47846692eed85a1520ba60605d4a0edc8f1a72546abcd85cc32215052fae0748`
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
# Tue, 18 Feb 2025 21:10:40 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:40 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 18 Feb 2025 21:10:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER root
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Fri, 07 Feb 2025 02:42:44 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8588faad644cf783ecb619f9dbb7aa8d78b7fa9c77501b94711a7bba97d2df88`  
		Last Modified: Mon, 10 Feb 2025 23:22:22 GMT  
		Size: 169.8 MB (169753173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d30f4ae3d0a5b51b2bbc18e16150d0f2facc687782c3a920b8807cc73188d0`  
		Last Modified: Wed, 19 Feb 2025 21:30:59 GMT  
		Size: 72.1 MB (72112751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546612dbdfc639ae8c6c677a5045400c5475cdb9e0f8bb99d3a731a1ab5539c2`  
		Last Modified: Wed, 19 Feb 2025 21:30:38 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc10087be4ff41c809bd02da5e3c89c9205238504b3eea7f5e07869bbde2cf8`  
		Last Modified: Thu, 20 Feb 2025 01:23:08 GMT  
		Size: 122.7 MB (122730526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50618739ad23775e52bd5ff90d414dda046ca9392d5b7bac9c9af9bbecfa14be`  
		Last Modified: Wed, 19 Feb 2025 21:30:39 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0e18d60d35a2222841ae336b94323f28b123a2faa68835582b3afacbe44ac339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10671003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bb92e0c485ec0267dcdc6f1209212212e239cc615e49f86e9c495cd5e86256`

```dockerfile
```

-	Layers:
	-	`sha256:a464d3fa4b80a0169b7981f15d212ad1da193d82dfc308e1200db4fe3a730a51`  
		Last Modified: Thu, 20 Feb 2025 00:29:59 GMT  
		Size: 10.7 MB (10651751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c55970f6f284c7b4b07fb9a796b7de2ec572bb7e0755c5b4efff9f9b2dbe4a`  
		Last Modified: Thu, 20 Feb 2025 00:29:59 GMT  
		Size: 19.3 KB (19252 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5a2e1f487e35c3c06fc22f4fc3b81926acf9dc860fefb5e7d5831d1f8913871a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414912714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f73540aef8a89d24ab3d9ac594b10804a6250e87db8db002ed897a2a27237e1`
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
# Tue, 18 Feb 2025 21:10:40 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:40 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 18 Feb 2025 21:10:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER root
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Fri, 07 Feb 2025 02:45:10 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7feeff8a60e4d7d7ae6e10d0a1d0796d8d07a16ed9dad63f734432e89c68d9ce`  
		Last Modified: Mon, 10 Feb 2025 23:34:26 GMT  
		Size: 168.1 MB (168063141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06945ff65c7d307d6862379032fb6b532eb9fe1e7bd7ae6a7e178447a49ed27`  
		Last Modified: Tue, 11 Feb 2025 09:10:06 GMT  
		Size: 71.8 MB (71786881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4883efbf3f642122c0880695c27a5b92dd31a0c46bbc6dc26da6623eb88f442`  
		Last Modified: Wed, 12 Feb 2025 00:50:38 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8464d096aa20c14974ccc0c7c78e93f343227fa3f409821d7b9c87c6f6e99d4d`  
		Last Modified: Thu, 20 Feb 2025 01:24:11 GMT  
		Size: 122.7 MB (122730528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7200d604cae2db8c1023b9dc8a2a3b01580b1403d35927e133d5984fa06b1541`  
		Last Modified: Wed, 19 Feb 2025 21:40:30 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:cc0b38c03c3f19ff4d407e02fc7de559235b343695c0d46c0faa60eb4f5aaa24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10670155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9432b8259028fdbc17ab4f2fd99a4421feba1ef4bb10ad1fa749d3d13da685`

```dockerfile
```

-	Layers:
	-	`sha256:ab625e197ebe55e13fcb641012234014f4a29b372146b637823cabd1b331b065`  
		Last Modified: Thu, 20 Feb 2025 00:30:04 GMT  
		Size: 10.7 MB (10650729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9c6dd57043452a01c888345b1e86bc9e40fdc9fd15f107f1236c2ab3d41fbd`  
		Last Modified: Thu, 20 Feb 2025 00:30:05 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.in-toto+json
